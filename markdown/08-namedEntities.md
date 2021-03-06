title: 08-namedEntities
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

class: center middle

# 08-Entités nommées
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

layout: false
.left-column[
  ## Introduction
]

.right-column[
# le module namesdates

]

???

Ces dernières années, dans le cadre de la P5, un important travail a été mené sur la représentation des lieux et des personnes qui peut particulièrement intéresser les historiens.

Parallèlement à cet effort de modélisation, un travail en cours sur le mapping de ce modèle de contenu avec CIDOC-CRM au sein d'un [groupe d'intérêt spécial (SIG) consacré aux ontologies](http://www.tei-c.org/SIG/Ontologies/).

[Pour ce qui concerne l'histoire de l'art, il faut également noté un autre groupe de travail sur la définition d'un élément `object`].

---

name: sommaire
template: inverse

.left-column[
##  .red[Sommaire]
]

.right-column[
# Entités nommées

## 1. Les entitées nommées

## 2. Les formes du nom

## 3. Le modèle de contenu (states, events)
]

---

# Entités nommées définition

### unités lexicales sélectionnées pour leur intérêt sémantique

- noms de lieux

- noms de personnes

- objets, etc.


???

Les entités nommées sont des unités lexicales sélectionnées pour leur intérêt sémantique : noms de lieux, de personnes, des objets etc.

LB: La TEI se positionne avec Frege dans la grande discussion philosophique autour de la théorie de référence: elle cherche à encoder ce qu'il appelle das bedeutung (signification)

---

## Pourquoi s'en occuper ?

### Construction d'index

### Constitution de bases de données

### exposition dans le LOD

???

- Utiliser les textes comme une base de données

- Mise en relation des textes entre eux

- Traitement type TAL, cartographie, index (facile avec XSLT)

- Suivi de tendance, veille Optimisation de recherche et moteur de recherche sémantique Production de savoir par inférence (classification de documents par exemple)

en perspective : le web sémantique

---

# Ce que propose la TEI pour les entités-nommées

## Balisage générique

Pour signaler la présence des noms propres ou de références nominales dans un texte

### `name` nom quelconque

### `rs` chaîne de référence

## Balisage plus spécifique

### `persName` nom de personne

### `orgName` nom de personne

### `placeName` nom de lieu

---

# La classe modele.nameLike

Regroupe les éléments qui se rapportent tous à un nom de personne ou de lieu

### agents (`name`, `orgName`, `persName`)

### lieux (`place`, `country`, `district`...)

Chacun avec des propriétés de nommage, des traits, des états, des événements, des relations.

???

L'élément person peut être instancié à l'intérieur d'un élément <persList> pour créer par exemple un fichier d'autorité dans un projet.

Classe modele.namelike (comme un nom) regroupe des éléments qui se rapportent tous à un nom de personne ou de lieu. Les éléments appartenant à cette classe y figurent. Voit qu’une superclasse qui est composée de plusieurs classes dans lesquelles des éléments comme persname, name, etc.
Comme il s’agit d’une classe, tous les éléments qui appartiennent à cette classe ont certaines propriétés.

---

# Les formes du nom


## exemple de personne

- La forme du nom peut être fournie au moyen de l'élément `persName`

- L'élément est répétable

```xml
<person xml:id="ArnMag">
 <persName xml:lang="is">Árni Magnússon</persName>
 <persName xml:lang="da">Arne Magnusson</persName>
 <persName xml:lang="la">Arnas Magnæus</persName>
</person>
```

```xml
<orgName type="voluntary"
 ref="tag:projectname.org,2012:PAS1">Pennsyla. Abolition Society</orgName>
```

???

L'association avec la classe `person` est basée sur la hiérarchie de l'élément XML (inclusion). L'association est implicite.

Pour indiquer plusieurs formes du nom distinctes, cet élément est répétable. Agrégation : une instance de la classe <person> possède une ou plusieurs instances (ou "composants") de la classe cible, ici `persName`

p. e. pour les formes langagières, la forme du nom autorisée, etc.
ici c'est la conjonction de l'élément et de l'attribut @full qui permet de typer la forme du nom.


Par exemple contraindre la fourniture d'une forme autorisée du nom, d'une langue, etc.
Ou au contraire autoriser son absence.

---

# Composantes du nom

- `forename` prénom

- `surname` nom  de famille

- `nameLink`, `roleName`, `genName`

`@full`	indique si le nom est donné dans une forme normalisée

`@sort`	spécifie l'ordre des composantes du nom entre elles

```xml
<persName ref="tag:projectname.org,2012:pn9">
   <forename sort="2">Sergei</forename>
   <forename sort="3" type="patronym">Mikhailovic</forename>
   <surname sort="1">Uspensky</surname>
</persName>
```

???

De même, il peut y avoir plusieurs manières de traiter les composantes du nom :
`forename`, `surname`, etc.

nom propre, prénon, particules, titres, etc.


`model.persNamePart` groupe les éléments qui font partie d'un nom de personne.
Comporte un certain nombre d'éléments qui permettent à l'encodeur de fournir une sous-structure détaillée pour la désignation des noms propres.

`addName`	(additional name) contains an additional name component, such as a nickname, epithet, or alias, or any other descriptive phrase used within a personal name.
`forename`	contains a forename, given or baptismal name.
`genName`	(generational name component) contains a name component used to distinguish otherwise similar names on the basis of the relative ages or generations of the persons named.
`nameLink`	(name link) contains a connecting phrase or link used within a name but not regarded as part of it, such as van der or of.
`roleName`	contains a name component which indicates that the referent has a particular role or position in society, such as an official title or rank.
surname	contains a family (inherited) name, as opposed to a given, baptismal, or nick name.
`surname` contains a family (inherited) name, as opposed to a given, baptismal, or nick name.


`att.personal` (attributes for components of names usually, but not necessarily, personal names) common attributes for those elements which form part of a name usually, but not necessarily, a personal name.

`roleName` qui peut par exemple être typé : Nobiliaire, honorifique, grade, épithète
```xml
<persName ref="tag:projectname.org,2012:DUDO1">
   <roleName type="honorific" full="abb">Mme</roleName>
   <nameLink>de la</nameLink>
   <surname>Rochefoucault</surname>
</persName>
```

---

# Liens vers des données d'autorité

### `@key` pour fournir une référence externe

### `@ref` pour une référence au moyen d'une URI

On privéligiera dans des notices d'autorité, une approche qui s'appuie sur un élément introduit récemment dans le modèle de contenu de `person`, `org` et `place`

### `idno`

???

### Liens vers des données d'autorité

att.canonical` provides attributes which can be used to associate a representation such as a name or title with canonical information about the object being named or referenced.

@key	provides an externally-defined means of identifying the entity (or entities) being named, using a coded value of some kind.
@ref	(reference) provides an explicit means of locating a full definition for the entity being named by means of one or more URIs.


`att.naming` provides attributes common to elements which refer to named persons, places, organizations etc.

@role	may be used to specify further information about the entity referenced by this name in the form of a set of whitespace-separated values, for example the occupation of a person, or the status of a place.
@nymRef	(reference to the canonical name) provides a means of locating the canonical form (nym) of the names associated with the object named by the element bearing it.


`att.responsibility` provides attributes indicating who is responsible for something asserted by the markup and the degree of certainty associated with it.

@resp	(responsible party) indicates the agency responsible for the intervention or interpretation, for example an editor or transcriber.
@cert	(certainty) signifies the degree of certainty associated with the intervention or interpretation.

---

# Le modèle conceptuel

### .red[traits] des caractéristiques ou des traits

### .red[states] des caractéristiques ou des états qui se maintiennent seulement pendant une durée définie

### .red[events] des événements qui peuvent conduire à un changement d'état

???

Le périmètres des caractéristiques pouvant affecter une entité nommée est très vaste.

La TEI fournit trois éléments génériques, et quelques-uns plus spécifiques. Elle indentifie trois classes principales d'information :

### traits

- des caractéristiques ou des traits qui en gros ne changement pas avec le temps

### des états

- des caractéristiques ou des états qui se maintiennent seulement pendant une durée définie


### des événements

- des événements ou des incidents qui peuvent conduire à un changement d'état ou, moins fréquemment, à un changement de trait



### Éléments biographiques et prosopographiques

Ce module fournit également des éléments pour la représentation d'information à caractère biographique, historique ou proposographique sur la personne, les lieux, ou l'organisation à laquelle un nom fait référence.

--> production de fichier d'autorité ou collection d'information bio

Là encore, TEI propose une stratégie flexible où l'encodeur peut puiser selon  selon l'approche adaptée à ses besoins.

Principes des base
Les informations concernant les personnes, les lieux, et les organisations sont coprennent une série d'assertions relatives :

- à des caractéristiques ou _traits (traits)_, qui en général ne changent pas au cours du temps

- à des caractéristiques ou _états (states)_ qui sont seulement vrai une période de temps donnée

- des _événements (events)_ ou incidents qui peuvent conduire à un changement d'état ou moins fréquemment de trait.


#### Traits

Traits, typiquement indépendants du vouloir de la personne, ou de ses actions. Peuvent être d'ordre physiques, sexe, couleur des yeux, ou culturels, ethniques, croyance...

```xml
<trait type="ethnicity" key="alb">
 <label>Ethnicity</label>
 <desc>Ethnic Albanian.</desc>
</trait>
```

#### États

Les états incluent par exemple le statut marital, le lieu de résidence et la position ou l'occupation.
Durée définie, c'est-à-dire un début et une fin.

<state type="office" from="1777-04-07"
 to="1780-07-12">


---

# Événements

### `birth`

### `death`

### `event`

### `listeEvent`

???

```xml
<person xml:id="WM">
 <event type="marriage" when="1859-04-26">
  <label>Marriage</label>
  <desc>
   <name type="person" ref="#WM">William Morris</name> and <name type="person"
    ref="http://en.wikipedia.org/wiki/Jane_Burden">Jane Burden</name> were
     married at <name type="place">St Michael's Church, Ship Street, Oxford</name> on
  <date when="1859-04-26">26 April 1859</date>. The wedding was
     conducted by Morris's friend <name type="person" ref="#RWD">R. W.
       Dixon</name> with <name type="person" ref="#CBF">Charles
       Faulkner</name> as
     the best man. The bride was given away by her father,
  <name type="person" ref="#RB">Robert Burden</name>.
     According to the account that <name type="person"
    ref="http://en.wikipedia.org/wiki/Edward_Burne-Jones">Burne-Jones</name>
     gave <name type="person" ref="#JWM">Mackail</name>
   <quote>M. said to Dixon beforehand <said>Mind
         you don't call her Mary</said> but he did</quote>. The entry in the
     Register reads: <quote>William Morris, 25, Bachelor Gentleman, 13
       George Street, son of William Morris decd. Gentleman. Jane Burden,
       minor, spinster, 65 Holywell Street, d. of Robert Burden,
       Groom.</quote> The witnesses were Jane's parents and Faulkner. None of
     Morris's family attended the ceremony. Morris presented Jane with a
     plain gold ring bearing the London hallmark for 1858. She gave her
     husband a double-handled antique silver cup.</desc>
  <bibl>J. W. Mackail, <title>The Life of William Morris</title>, 1899.</bibl>
 </event>
</person>
```

Contiennent des données relatives à n'imposte quelle événement significatif associé à une personne, un lieu ou une organisation.
@where pour indiquer le lieu en pointant vers un élément <place>

listEvent pour structurer


The model.persStateLike class contains elements describing physical or socially-constructed characteristics, traits, or states of a person. Members of the class comprise the following specific elements:
faith specifies the faith, religion, or belief set of a person.
langKnowledge (language knowledge) summarizes the state of a person's linguistic knowledge, either as prose or by a list of langKnown elements.
nationality contains an informal description of a person's present or past nationality or citizenship.
sex specifies the sex of a person.
age specifies the age of a person.
socecStatus (socio-economic status) contains an informal description of a person's perceived social or economic status.
persName (personal name) contains a proper noun or proper-noun phrase referring to a person, possibly including one or more of the person's forenames, surnames, honorifics, added names, etc.
occupation contains an informal description of a person's trade, profession or occupation.
residence describes a person's present or past places of residence.
affiliation contains an informal description of a person's present or past affiliation with some organization, for example an employer or sponsor.
education contains a description of the educational experience of a person.
floruit contains information about a person's period of activity.
state contains a description of some status or quality attributed to a person, place, or organization often at some specific time or for a specific date range.
trait contains a description of some status or quality attributed to a person, place, or organization typically, but not necessarily, independent of the volition or action of the holder and usually not at some specific time or for a specific date range.


Person

att.responsibility provides attributes indicating who is responsible for something asserted by the markup and the degree of certainty associated with it.
@cert	(certainty) signifies the degree of certainty associated with the intervention or interpretation.
@resp	(responsible party) indicates the agency responsible for the intervention or interpretation, for example an editor or transcriber.

att.editLike provides attributes describing the nature of an encoded scholarly intervention or interpretation of any kind.
@evidence	indicates the nature of the evidence supporting the reliability or accuracy of the intervention or interpretation. Suggested values include: 1] internal; 2] external; 3] conjecture

att.source provides attributes for pointing to the source of a bibliographic reference.
@source	provides a pointer to the bibliographical source from which a quotation or citation is drawn.

---

# Relations

`listRelation` fournit des informations sur les relations identifiées parmi les personnes, les lieux et les organisations, soit informellement en prose, soit exprimées formellement sous forme de liens de relation.

```xml
<listRelation>
 <relation name="parent" active="#P1 #P2"
  passive="#P3 #P4"/>
 <relation name="spouse" mutual="#P1 #P2"/>
 <relation type="social" name="employer"
  active="#P1" passive="#P3 #P4"/>
</listRelation>
```

---

template: inverse
class: center middle

# à [demain](09-personnalisation.html)

.left[.footnote[[revenir au début](#index)]]
