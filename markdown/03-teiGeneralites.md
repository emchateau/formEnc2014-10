title: 03-teiGeneralites
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

name: index
class: center middle

# 03-La Text Encoding Initiative comme cadre de travail pour l'édition des textes
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

layout: false

.left-column[

## .red[Introduction]

]

.right-column[

# Pourquoi la Text Encoding Initiative ?

## Considérations guidant les choix

- adaptation aux objectifs scientifiques
- interopérabilité
- pérennisation

## Autres aspects

- [Référentiel Général d'Interopérabilité](http://references.modernisation.gouv.fr/rgi-interoperabilite)
- Large adoption (standard de fait)
]


???


La production d'une édition électronique exige la mobilisation de techniques spécifiques pour l'établissement des textes, l'enregistrement des annotations scientifiques et la publication.

Deux considérations doivent principalement guider les choix en la matière :
- d'une part l'adaptation aux objectifs scientifiques du projet,
- d'autre part l'interopérabilité et la pérennisation.

Sur ces derniers points, le Référentiel général d'interopérabilité publié en 2009 par la Direction générale de la modernisation de l'État recommande l'utilisation des technologies XML (eXtensible Markup Language)

- cf. Ministre du Budget, des Comptes publics, [Référentiel Général d'Interopérabilité (RGI)](http://references.modernisation.gouv.fr/rgi-interoperabilite), 2009.


En outre, le dialecte XML de la Text Encoding Initiative (TEI) s'est très largement imposé ces dernières années comme **standard de fait** dans le domaine de l'édition numérique à caractère scientifique.

Telle que la définie Laurent Romary, la TEI est une « Norme de balisage, de notation et d'échanges de corpus des documents électroniques. Elle s'est élaborée à partir des besoins de structuration, de conceptualisation et de mise en réseau des textes »

Sa large adoption, les possibilités de personnalisation, ainsi que l'expérience acquise en matière de traitement des sources primaires à caractère textuel en histoire ou en littérature ces dernières années permet de juger que son utilisation est le plus souvent tout fait adaptée.

Nous verrons cependant que certains aspects propres à un projet peuvent nécessiter des adaptations dans l'utilisation de ce dialecte, ou qu'il faut parfois conjointement confier à d'autres modèles documentaires la prise en charge de l'enregistrement du travail.

---

layout: false

.left-column[

## .red[Introduction]

]

.right-column[

# La Text Encoding Initiative

### Un effort international pour unifier les pratiques d'encodage de textes dans le domaine académique

### Un vocabulaire XML qui permet de produire des modèles de textes

### Un cadre de travail

### Un ensemble de recommandations ([_Guidelines_](http://www.tei-c.org/Guidelines/))

]

???

La Text Encoding Initiative (TEI) est un effort international pour **unifier les pratiques d’encodage de textes** dans le domaine académique.

Elle fournit **un vocabulaire XML** qui permet de produire des modèles de textes que l’on peut utiliser à différentes fins notamment pour l’édition de sources primaires.

Plus qu’un schéma générique, elle offre en fait **un cadre de travail** qui permet de traiter différents cas de figure.

Ce cadre de travail se compose
- d’un vocabulaire,
- d’une documentation qui en fournit la sémantique en langage naturel,
- et d’un ensemble de recommandations rassemblées sous l’intitulé de Guidelines.

En ce sens, comme le relève Florence Clavaud dans son cours à l'École nationale des chartes, il s’agit plutôt d’une sorte d’« ontologie générique du texte ».

---

name: sommaire
template: inverse

.left-column[
##  .red[Sommaire]
]

.right-column[
# La Text Encoding Initiative comme cadre de travail pour l'édition des textes

## 1. [Historique de la TEI](#part1)

## 2. [Objectifs et principes](#part2)

## 3. [L'infrastructure de la TEI](#part3)
]

---

name: part1
template: inverse
class: center middle

# .red[1.] Historique de la TEI

---

name: historique1

.left-column[
##  .red[historique]
]

.right-column[

# Un projet collectif
- [Association for Computers in the Humanities](http://ach.org)
- [Association for Literary and Linguistic Computing](http://eadh.org)
- [Association for Computational Linguistics](http://www.aclweb.org)

Recherche d'un modèle commun pour encoder & partager des textes

### .red[novembre 1987] – Première réunion au Vassar College à Poughkeepsie

### Création de la Texte Encoding Initiative

### .red[juin 1990] – Premier brouillon (P1)

### .red[mai 1994] – Première publication des __Guidelines__ (P3)

]

???

La Text Encoding Initiative est née d’un constat partagé, au sein d’une communauté de chercheurs déjà engagés dans la production de textes numériques, du manque de solutions pour faciliter l’échange de textes et d’information sur leur travail.


## réunion de Poughkeepsie 1987

En novembre 1987, une première rencontre fut organisée sous l’égide de l’Association for Computers and the Humanities (ACH) au Vassar College à Poughkeepsie avec une trentaine de représentants issus du monde des archives, des centres d’informatique appliquée aux sciences humaines, ou d’organisations professionnelles pour examiner à nouveau la question de la standardisation.

S’accordant tous sur le besoin de pratiques communes, ces participants formulèrent une dizaine de principes directeurs.

- cf. Ide, Nancy M., et Sperberg-McQueen, C. Michael, [« The Text Encoding Initiative: Its History, Goals, and Future Development »](http://www.cs.vassar.edu/~ide/papers/teiHistory.pdf), dans Computers and the Humanities, editor. Nancy M. Ide et Jean Véronis vol. 29, 1995, p. 5-15.

Ceux-ci mettaient notamment l’accent sur la conversion de formats et la nécessité de développer un métalangage pour des schémas d’encodage descriptifs.


## Création de la Text Encoding Initiative

L’ACH, rapidement suivie dans son effort de standardisation par l’Association for Literary and Linguistic Computing et l’Association for Computational Linguistics formèrent ensemble la **Text Encoding Initiative (TEI)** afin de conduire le projet sous une forme internationale et multilingue et **développer des recommandations pour la préparation et l’échange de textes électroniques dans le domaine universitaire**.

Plus de 50 chercheurs contribuent déjà à la TEI P1 (juin 1990)

15 groupes de travail collaborent de 1990-93 à la P2


## 1ères Guidelines 1994

Dès 1994, la TEI publiait une **première version officielle de ses Guidelines for the Encoding and Interchange of Machine-Readable Texts**.

Ce rapport proposait un ensemble de conventions pour l’encodage de différents types de textes pour servir dans le domaine des sciences du langage ou des sciences humaines. Cette première publication constitue un jalon important car jamais auparavant les chercheurs n’avaient été capables de formuler un consensus sur les pratiques d’encodage.

---

name: historique2

.left-column[
##  .red[historique]
### (suite)
]

.right-column[

# Développements du projet

### Création de groupes de travail disciplinaires

### Diffusion du modèle

### .red[janvier 1999] Création d'un [consortium international](http://www.tei-c.org/index.xml)

### .red[juin 2002] Mise à jour pour prendre en compte XML (P4)

### .red[novembre 2007] Version actuelle des [Guidelines](http://www.tei-c.org/Guidelines/P5/) (P5)

]

???

## Développements du projet

Création de groupes de travail par champs disciplinaires. La première version officielle des Guidelines P3, était le travail de 200 personnes.

Diffusion du modèle par l'intermédiaire de séminaires, d'ateliers, qui permettent le recueil des remarques des utilisateurs.

Création d'un consortium international en janvier 1999.

Mise à jour de la P3 pour prendre en compte XML (P4, publiée en juin 2002).

Immédiatement après la publication de cette version 4, début du travail sur la P5, version actuelle du projet publiée en novembre 2007.

P5 qui incluait nombreuses améliorations concernant l'encodage de  charactères, le traitement des parties graphiques, la description des manuscrits, le balisage externe, et la structuration des Guidelines proprement dit.

---

name: impact

.left-column[
##  .red[Impact]
]

.right-column[

## Un projet ancien

- D'abord développé en SGML

- Largement employé

- Souvent la solution la plus adaptée pour les corpus textuels ou les sources primaires

## Impact de la TEI

- Une large reconnaissance internationale

- Conservation à long terme du patrimoine culturel

- Éviter la bibliothèque de Babel numérique

- Projet phare des Humanités numériques

]

???

## Un projet ancien

Comme vous le constatez, la TEI est un projet d'une dizaine d'années plus ancien que le méta-langage XML. Elle fut dans un premier temps développée en SGML, un méta-langage dont XML est une simplification.

La TEI a adopté XML dès la première publication de sa spécification en 1996, certains membres de la TEI avaient en effet participé à son développement.

Par la suite, les Guidelines ont été étayées par l'apport de nombreuses spécialités pour prendre en charge une plus grande diversité de textes.

Malgré l'ancienneté du projet, elle reste l'un des dialectes XML les plus largement employé. On dispose donc de beaucoup de recul sur son utilisation. Dans bien des cas, c'est la solution la plus adéquate pour traiter certaines choses comme le texte ou la production de sources primaires.


## Impact de la TEI

Reconnu internationalement comme un outil d'importance cruciale à la fois pour la conservation à long terme de données électroniques et comme moyen efficace d'utiliser ces données dans de nombreux domaines.

Son schéma d'encodage est particulièrement adopté pour la production d'éditions critiques de textes littéraires ou de sources primaires, de larges corpus linguistiques, ou encore la production de métadonnées détaillées relatives à des collections de textes patrimoniaux de toutes sortes.

- cf. liste (non exaustive) des projets répertoriés http://www.tei-c.org/Activities/Projects/

Adoptée par de nombreuses organisations telles que le National Endowment for the Humanities aux États-Unis, l'Arts and Humanities Research Board au Royaume-Uni, la Modern Language Association, l'Expert Advisory Group for Language Engineering Standards de l'Union européenne et de nombreuses autres organismes à travers le monde qui financent ou promeuvent la production de textes électroniques.

- Succès qui permet d'assurer conservation à long terme de notre patrimoine culturel porté dans un monde en réseau.

- Une solution pour éviter la bibliothèque de Babel numérique

- À tous les égards l'un des projet phares les plus durables dans le domaine des Humanités numériques (Digital Humanities).

---

name: part2
template: inverse
class: center middle

# .red[2.] Objectifs et principes

---

name: principesDirecteurs

.left-column[
##  .red[Principes directeurs]
]

.right-column[

# Faciliter l’échange et l’intégration des travaux des chercheurs

- Concevoir et maintenir **un modèle international générique**, applicable à tous les textes, écrits dans toutes les langues, datant de toutes les périodes

- Guider les utilisateurs non techniciens (**documenter le modèle**)

- Aider les spécialistes et les techniciens en leur offrant un modèle **souple et adaptable**
]

???

## Principes directeurs

Faciliter l’échange et l’intégration des travaux des chercheurs

- Concevoir et maintenir **un modèle international générique**, applicable à tous les textes, écrits dans toutes les langues, datant de toutes les périodes

- Guider les utilisateurs non techniciens (**documenter le modèle**)

- Aider les spécialistes et les techniciens en leur offrant un modèle **souple et adaptable**

---

name: miseEnOeuvre

.left-column[
##  .red[Mise en œuvre]
]

.right-column[

## Publication de recommandations
- simples
- faciles à employer
- compréhensibles

## Généricité

## Modularité et possibilités de personnalisation ou d'extension

## Utilisation des syntaxes et mécanismes XML

]

???

Rapidement **la TEI a privilégié la publication de recommandations** plutôt que celle d’un standard ou d’une norme.

L’objectif était de spécifier des conventions d’encodage simples, faciles à employer, relativement compréhensibles, et qui fournissent d’amples mécanismes d’extension afin de pouvoir répondre à des besoins particuliers.

- Ide, Nancy M., et al., op. cit.

Cette **modularité avec ses possibilités de personnalisation et d’extension** seyait mieux à la recherche.

Néanmoins, la TEI s’est rapidement imposée comme standard de fait pour l’encodage de textes numériques dans le domaine des sciences humaines. Plusieurs raisons expliquent en grande partie cette situation.

- D’une part, la TEI repose sur l’utilisation de syntaxes et de mécanismes XML standardisés par le W3C (World Wide Web Consortium) qui présentent de nombreuses garanties en termes d’interopérabilité et permettent d’utiliser les outils puissants disponibles pour manipuler des arbres XML.

- D’autre part, l’importante généricité de la TEI lui permet de couvrir une grande gamme de besoins. Cela explique en grande partie l’importante pénétration de la TEI dans la communauté scientifique.

Aujourd'hui la TEI cherche à s'abstraire du modèle XML avec la définition d'un langage TEI permettant de spécifier ses propres schémas.

---

name: organisation

.left-column[
##  .red[Organisation]  du Consortium
]

.right-column[

## Le [TEI Council](http://www.tei-c.org/Activities/Council/)

- Formé de 12 personne, chargé de l’élaboration et évolution des Guidelines,

## Le [TEI Board of Directors](http://www.tei-c.org/Board/)

- chargé de la gestion du Consortium (orientations stratégiques, gestion financière, recrutement, etc.)

## Une large communauté d'utilisateurs

- [Workgroups](http://www.tei-c.org/Activities/Workgroups/)

- [SIG Special Interest Groups](http://www.tei-c.org/Activities/SIG/)

- [Liste de diffusion tei-l](https://listserv.brown.edu/tei-l.html)

- [liste de diffusion francophone tei-fr](https://groupes.renater.fr/wiki/tei-fr/)

]

???

La TEI est organisée autour d'un Consortium international et d'une importante communauté d'utilisateurs.

Le Consortium TEI rassemble de nombreuses organisations internationales. Il est actuellement structuré par deux instances.


### Le TEI Council

- Formé de 12 personne

- Chargé de l’élaboration et évolution des Guidelines,


### Le TEI Board of Directors

- chargé de la gestion du Consortium (orientations stratégiques, gestion financière, recrutement, etc.)


### Une large communauté d'utilisateurs

Fondamentale.

Nombreux groupes de travail
- [Workgroups](http://www.tei-c.org/Activities/Workgroups/)
- [SIG Special Interest Groups](http://www.tei-c.org/Activities/SIG/)

Plusieurs listes de diffusion :
- https://listserv.brown.edu/tei-l.html
- https://groupes.renater.fr/wiki/tei-fr/

---

name: organisation2

.left-column[
##  .red[Organisation]  (suite)
]

.right-column[

## Un projet "open source"

- Les Guidelines et l'ensemble du code sont maintenues sur [Sourceforge](http://sourceforge.net/projects/tei/)

- Projet collaboratif appuyé sur un entrepôt Subversion

- Discussion des problèmes rencontrés, suggestions de modifications sur les listes et le gestionnaire de bugs

]

???

# Organisation

Projet distribué sous la forme d'un projet "open source"

- Les Guidelines et l'ensemble du code sont maintenues sur [Sourceforge](http://sourceforge.net/projects/tei/)

- Projet collaboratif appuyé sur un entrepôt Subversion

- Discussion des problèmes rencontrés, suggestions de modifications sur les listes et le gestionnaire de bugs

---

name: part3
template: inverse
class: center middle

# .red[3.] L'infrastructure de la TEI

???

Comme on l'a vu précédemment, la TEI peut donc se concevoir comme un cadre de travail technique, un framework, qui accompagne l’éditeur ou l’encodeur dans la structuration de l’information.

Elle consiste en un ensemble de préconisations qui doivent être adaptées aux spécificités inhérentes à chaque projet éditorial.

- Comme le relève Florence Clavaud, « cette modularité qui garantit la flexibilité du modèle et sa généralité, peut parfois dérouter l’encodeur inexpérimenté ou le confronter à des choix difficiles. » La définition des solutions d’encodage implique d’opérer des choix entre plusieurs solutions admissibles en en saisissant bien tous les tenants et les aboutissants.

- Elle implique un aller-retour continuel entre les sources textuelles à traiter et la documentation de la TEI afin de réévaluer les solutions d’encodage envisagées.

Ce besoin de personnalisation s’explique, d’une part parce que le texte est souvent un objet hétérogène, et d’autre part car l’encodeur ou l’éditeur peut avoir des objectifs différents.

- Dans le cas d’un texte dramatique, il pourra se révéler nécessaire de trouver un moyen pour marquer les locuteurs.

- Les éléments nécessaires pour traiter le discours oral ne seront sans doute pas les mêmes que ceux requis pour le traitement diplomatique.

- On n’abordera pas un ensemble de textes composites ou un corpus de la même manière que des textes isolés.

Ces différents cas de figure expliquent assez bien le besoin de métadonnées spécialisées pour décrire les contenus.


Ce que propose la TEI c’est un ensemble de mécanismes pour les traiter. « Formellement parlant, les Guidelines fournissent à la fois des règles syntactiques sur la manière dont des éléments et des attributs doivent être utilisés dans des documents valides, mais aussi des recommandations sémantiques sur l’interprétation que l’on doit attacher à certaines constructions syntactiques. En ce sens, elle fournissent à la fois une définition de type de document, et une déclaration de type de document. Plus exactement, on peut distinguer le modèle abstrait de la TEI (TEI Abstract Model) qui définit un ensemble de concepts en rapport, et le schéma TEI (TEI schema) qui définit un ensemble de règles et de contraintes syntactiques.  »

- cf. Sperberg-McQueen, C. Michael, Burnard, Lou, et Bauman, Syd, [TEI P5 : Guidelines for Electronic Text Encoding and Interchange](http://www.tei-c.org/Guidelines/P5/), 23.3.

---

name: structure

.left-column[
##  .red[Distinguer]
]

.right-column[

# Modèle abstrait de données

- qui définit un ensemble de concepts et de relations entre ces concepts

- qui permet d'exprimer des définitions formelles (modèles de contenus)

# Implémentations techniques du modèle

- qui définissent l'ensemble des règles et contraintes syntaxiques sous forme de schémas XML ou de DTD

]

???

Pour bien comprendre ce que propose la TEI, il convient de distinguer le modèle abstrait de données, des implémentations techniques du modèle.

# Modèle abstrait de données

- qui définit un ensemble de concepts et de relations entre ces concepts

- qui permet d'exprimer des définitions formelles (modèles de contenus)

# Implémentations techniques du modèle

- qui définissent l'ensemble des règles et contraintes syntaxiques sous forme de schémas XML ou de DTD


Ces deux composantes **forment ensemble les Guidelines**.
Ces Guidelines expriment sous forment littérale ([Donald Knuth](http://www.literateprogramming.com)) le modèle abstrait de données, et propose des implémentations techniques du modèle.

Si la conception de la TEI découle en grande partie des technologies XML, et que son infrastructure repose principalement sur ces technologies, la TEI pourrait tout aussi bien être exprimée par l'intermédiaire d'un autre véhicule si un nouveau formalisme technique devait s'imposer à l'avenir.

---

# Un cadre de travail flexible et modulaire

### [22 modules](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ST.html#STMA)

- Classement des 555 éléments de la TEI par domaines d'application
- Chaque module fait l'objet d'un chapitre de la documentation

### [Classes de modèle](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/REF-CLASSES-MODEL.html)

### [Classes d'attribut](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/REF-CLASSES-ATTS.html)

???

Dès l'origine, la TEI a été conçue pour être employée comme un ensemble de briques permettant de construire des schémas spécifiques pour un projet donné.

L'infrastructure de la Proposition numéro 5 de la TEI (P5) consiste en :

- vingt-deux modules parmi lesquels sont répartis les nombreux éléments de la TEI qui font l'objet d'une importante documentation textuelle

- ils sont formellement classés dans des classes de modèle et d'attributs auxquels on peut faire appel pour spécifier un schéma.

[cf. Personnalisation de la TEI ](09.personnalisation.html)

---

name: modules
# Les 22 [modules](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ST.html#STMA) de la TEI

![module](images/modulesTEI.png)

---

name: modules
# Les 22 [modules](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ST.html#STMA) de la TEI

### Regroupés par domaine d'application, à chaque module correspond un chapitre des [Guidelines](http://www.tei-c.org/Guidelines/)

### Trois modules habituellement requis :

- [core](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/CO.html) éléments disponibles dans tous les documents TEI

- [header](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/HD.html) en-tête TEI

- [textstructure](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/DS.html) structure de text par défault

& [tei](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ST.html) infrastructure TEI

### ex d'autres modules spécialisés

[namesdates](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ND.html) pour les noms et dates, [transcr](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/PH.html) pour la critique textuelle, [msdescription](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/MS.html) pour la description de manuscrits, [figure](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/FT.html) facsimili, ...

???

Les modules constituent avant tout un moyen commode de grouper par domaine d'application les nombreux éléments de la TEI (ils sont actuellement au nombre de 555).

Chaque module fait l'objet d'une description littérale dans un chapitre des Guidelines.

Trois de ces modules sont habituellement requis lors de la production d'un schéma (`core`, `header`, et `textstructure`, on utilise également `tei` pour RelaxNG).


Outre ces trois modules, on fait fréquemment appel aux modules suivants `figures`, `namesdates`, `linking`, `transcr`.

- Le module [namesdates](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ND.html) est particulièrement adapté pour la description des entités historiques de type personnes et lieux.

- Le module [figure](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/FT.html) est utilisé conjointement avec `transcr` pour traiter la description des facsimili.

- [transcr](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/PH.html) est destiné à la transcription de manuscrit

- [msdescription](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/MS.html) sert à la description de manuscrits.

Il est également possible d'utiliser le module `dictionaries` pour le traitement d'un glossaire.

---

name: conclusion
template: inverse
class: center middle


# Conclusion


???

## Avantages

Conçue comme un modèle générique de structuration et de sémantisation des textes, la TEI présente de nombreux avantages. On relève notamment :

- sa modularité et sa flexibilité

- son expressivité (niveau de granularité)

- le fait qu’il s’agit d’un standard reconnu internationalement (interopérabilité, pérennité)

- le fait qu’elle dispose des propriétés intrinsèques au modèle XML : séparation entre le contenu et a présentation, possibilité de générer plusieurs formats de sortie à partir d’une même source, bon candidat pour la pérennisation

- son adaptation à l’édition électronique (croisement de sources, fac simili, hyperliens, etc.)

- les possibilités de modulation de l’affichage et d’accessibilité, ses aspects économiques

Mis à part le fait qu’elle soit rapidement apparue comme un standard de fait pour la publication de textes numériques en sciences humaines, ce sont d’abord ces qualités qui expliquent la large implantation de la TEI dans la communauté scientifique. Elle sert de format à de nombreux projets d’envergure internationale (Blake archive  , Perseus  , Rosetti  , etc.). Plusieurs projets français de grande envergure utilisent également la TEI dans le domaine des sciences historiques (BVH, Élec, le portail Telma, ENS Lyon, Desgodets, ANR Ampère, etc.).


## S'approprier la TEI

La TEI fournit ainsi, à l’aide d’un vocabulaire et d’une infrastructure technique, **un cadre de travail pour la modélisation des textes**. Dans la limite de leur expressivité, de tels modèles peuvent être employés à telles ou telles fins. La volonté de la TEI de couvrir l’ensemble des besoins a pour pendant négatif la nécessité de personnaliser son schéma. Et l’utilisation de la TEI suppose l’apprentissage de son vocabulaire.

Cette difficulté d’accès, ainsi que la nécessité de manier des outils nouveaux, reste un problème qui n’est toujours pas complètement réglé. Cependant, la TEI a largement été adoptée aujourd’hui dans le secteur académique pour la publication de sources primaires ou l’édition numérique. C’est la raison pour laquelle on peut affirmer qu’elle constitue de ce point de vue un standard de fait qui justifie en grande partie son utilisation dans un projet scientifique d’édition.


## Le problème de l'interopérabilité

À de nombreux égards, le large emploi de la TEI est censé répondre à un **désir d’interopérabilité et de pérennisation**. La promesse des standards est de nous rendre la vie plus aisée : TEI, XML, Unicode ont le potentiel de faciliter l’échange et la réutilisation des documents, c’est notamment la raison pour laquelle on y a recours.

Cependant, par sa généricité même, la nature profonde de la TEI qui nécessite d’opérer des choix, ou permet d’être étendue en fonction des besoins, explique en grande partie les difficultés que l’on peut rencontrer lorsqu’il s’agit de rassembler des collections de documents en termes de compatibilité.

Il ne suffit pas que les textes soient tous encodés en TEI pour qu’ils soient véritablement interopérables. Chaque document est représentatif du modèle que se fait l’éditeur du texte. Ainsi, la compatibilité ne peut être atteinte que si plusieurs documents suivent le même ensemble de conventions.

---

name: sourcesBiblio
template: inverse
class: center middle

# Sources et bibliographie

---

name: biblio

# Orientations bibliographiques

- Burnard, Lou. [What is the Text Encoding Initiative](http://books.openedition.org/oep/426), OpenEdition Books, 2014.

- Sperberg-McQueen, C. Michael, Lou Burnard, and Syd Bauman. [TEI P5 : Guidelines for Electronic Text Encoding.](http://www.tei-c.org/Guidelines/P5/) Charlottesville, Virginia: Text Encoding Initiative Consortium, version 2.5.0, 2013.

- Wittern, Christian, Ciula, Arianna, Tuohy, Conal, ["The Making of TEI P5"](http://llc.oxfordjournals.org/content/24/3/281.abstract) Literary and Linguistic Computing 24, no. 3 (2009): 281-296.

- Ide, Nancy M., and C. Michael Sperberg-McQueen. ["The Text Encoding Initiative: Its History, Goals, and Future Development."](http://www.cs.vassar.edu/~ide/papers/teiHistory.pdf) In Computers and the Humanities. Edited by Nancy M. Ide and Jean Véronis. 1995.

- Mylonas, Elli, and Allen Renear. ["The Text Encoding Initiative at 10: Not Just An Interchange Format Anymore – but a New Research Community."](http://link.springer.com/article/10.1023%2FA%3A1001832310939) Computers and the Humanities 33, no. 1-2 (1999): doi:10.1023/A:1001832310939.

---

template: inverse
class: center middle

# La [suite](04-teiMacrostructure.html)

.left[.footnote[[revenir au début](#index)]]
