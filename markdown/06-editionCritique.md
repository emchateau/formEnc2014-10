title: 06-editionCritique
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

class: center middle

# 06-Édition critique
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

layout: false
.left-column[
  ## Introduction
]

.right-column[
# Édition critique

]

---

name: sommaire
template: inverse

.left-column[
##  .red[Sommaire]
]

.right-column[
# Édition critique

## 1. [L'inscription du texte sur le support](#inscription)

## 2. [Les corrections éditoriales](#corrections)

## 3. [Les variantes](#variantes)

]

---

name: inscription
template: inverse
class: center middle

# L'.red[inscription du texte] sur le support

---

## Ajouts et surplus


### .red[<add>] texte ajouté

```xml
<add place="above">nous</add>
```

### .red[<del>] texte supprimé

```xml
<del rend="overstrike">claustra</add>
```

### .red[<subst>] substitutions (génétique)

```xml
<subst>
  <del>claustra</del>
  <add place="margin">fenêtre</add>
</subst>
```

---

# Prise en charge des lacunes

### .red[<gap>] passage ne pouvant pas être restitué pour des raisons matérielles

```xml
<gap reason="illegible" agent="ink-blot" />
```

### .red[<unclear>] passage en partie illisbile

```xml
<unclear agent="ink-blot" cert="low" resp="#EC" />
```

### .red[<suplied>] passage en partie illisbile

```xml
<supplied reason="hole" source="#autreEd">les</supplied>

???

Ne pas confondre gap et space qui sert à désigner un espace blanc jugé significatif

```
xml<space quantity="1" unit="cm">
```

---

name: corrections
template: inverse
class: center middle

# Les .red[corrections éditoriales]

---

# Passages fautifs

### .red[<sic>] passage fautif, ou segment syntaxiquement incorrect

### .red[<corr>] correction de l'éditeur

### .red[<abbr>] abréviation

### Utilisation de .red[<choice>]

```xml
<choice>
  <abbr>M<hi rend="superscript">r</hi></abbr>
  <expan>Monsieur</abbr>
</choice>
```

???

Même utilisation de choice possible pour les segments syntaxiquement incorrects.

```xml
<choice>
  <sic>charbone</sic>
  <corr>charbon</corr>
</choice>
```

Partout, utilisation des attributs @cert, @resp et @source qui peuvent s'avérer utile.

---

name: variantes
template: inverse
class: center middle

# Les .red[variantes] et les .red[mains]

---

# Description des mains

### .red[@hand]

### .red[handDesc] et ses sous-éléments dans le header

```xml
<handDesc>
  <handNote xml:id="c2Hand1" scope="major">à l’encre noire</handNote>
  <handNote xml:id="c2Hand2" scope="minor">au crayon</handNote>
</handDesc>
```

???

handNote est répétable et peut contenir une localisation avec locus.

---

# Les variantes

# Trois approches pour l'alignement

Les Guidelines proposent trois approches pour aligner des passages textuels lorsque l’on établit une édition critique :

- la **méthode de localisation référencée**,	où les entrées d’apparat critique sont liées aux blocs de texte identifiés qui contiennent les lemmes respectifs

- la **méthode d’attachement à double point**,	où les entrées d’apparat critique sont liées à des ponts de départ et de fin identifiées dans un texte

- la **méthode de segmentation parallèle**,	où les entrées d’apparat critique son encodées au moyen d’une transcription du texte connu invariable et de tous les témoins.


???

Les Guidelines proposent trois approches pour aligner des passages textuels lorsque l’on établit une édition critique :

- la **méthode de localisation référencée**,	où les entrées d’apparat critique sont liées aux blocs de texte identifiés qui contiennent les lemmes respectifs

- la **méthode d’attachement à double point**,	où les entrées d’apparat critique sont liées à des ponts de départ et de fin identifiées dans un texte

- la **méthode de segmentation parallèle**,	où les entrées d’apparat critique son encodées au moyen d’une transcription du texte connu invariable et de tous les témoins.

La méthode par segmentation parallèle est le plus couramment utilisée lors de l’encodage de sources en XML-TEI pour comparer des témoins. Cette méthode correspond également à une méthode de travail pour l’établissement du texte.

---

# Segmentation parallèle

### .red[<app>] entrée d'apparat critique

### .red[<lem>] lemme ou leçon retenue du texte

### .red[<rdg>] variante (lecture)

```xml
<app>
  <lem>remener</lem>
  <rdg wit="#l-1-C #l-1-D #l-1-E #l-1-F">remettre</rdg>
  <rdg wit="#l-#-a">conduire dehors</rdg>
</app>
```

---

# Variantes

### .red[<rdgGrp>] pour regrouper plusieurs variantes ayant un lien entre elles

### .red[@type] pour catégoriser la variante

### .red[@cause] pour expliciter la cause de la variante

---

# Tableau de tradition

```xml
<listWit>
  <witness xml:id="A">
    <msDesc>
      <msIdentifier>
        <country>France</country>
        <settlement>Paris</settlement>
        <repository>Archives nationales</repository>
        <collection>Monuments ecclésiastiques</collection
        <idno>S 2364 n° 5</idno>
      </msIdentifier>
    </msDesc>
  </witness>
  <witness xml:id="B">
    <msDesc>
      <msIdentifier>
        <country>France</country>
        <settlement>Paris</settlement>
        <repository>Archives nationales</repository>
        <collection>Monuments ecclésiastiques</collection>
        <idno>LL1157 p. 383b-384b, n° XXXVI</idno>
        <msName>Cartulaire blanc de l’abbaye de Saint-Denis, tome I</msName>
      </msIdentifier>
      <msContents>
        <msItem>
          <rubric xml:lang="lat" >De dimidio arpento vinee nobis vendito a Petro de Cellario <num value="36">XXXVI</num></rubric>
        </msItem>
      </msContents>
    </msDesc>
  </witness>
</listWit>
```

---

# Localisation référencée

```xml
<div type="alignmentText" xml:id="cAlignmentText">
 <linkGrp>
<!-- Front -->
  <link target="#c1Front #c2Front"/>
  <link target="#c1FrontFr #c2FrontFr02"/>
  <link target="#c1FrontFr01 #c2FrontFr01"/>
  <link
    target="#c1FrontFr01.p001 #c2FrontFr01.p001"/>
<!-- ... -->
 </linkGrp>
</div>
```

---

template: inverse
class: center middle

# Gérer des [structures complexes](07-teiCorpus.html)

.left[.footnote[[revenir au début](#index)]]
