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

## 1.

## 2.

## 3.
]

---

Les Guidelines proposent trois approches pour aligner des passages textuels lorsque l’on établit une édition critique :

- la **méthode de localisation référencée**,	où les entrées d’apparat critique sont liées aux blocs de texte identifiés qui contiennent les lemmes respectifs

- la **méthode d’attachement à double point**,	où les entrées d’apparat critique sont liées à des ponts de départ et de fin identifiées dans un texte

- la **méthode de segmentation parallèle**,	où les entrées d’apparat critique son encodées au moyen d’une transcription du texte connu invariable et de tous les témoins.

La méthode par segmentation parallèle est le plus couramment utilisée lors de l’encodage de sources en XML-TEI pour comparer des témoins. Cette méthode correspond également à une méthode de travail pour l’établissement du texte.

---

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

???

L’utilisation d’identifiants uniques rassemble plusieurs avantages, ceux-ci permettent d’identifier précisément, à l’exclusion de tout autre, une unité textuelle ou un passage dans l’un des manuscrits. Ils constituent donc une bonne pratique notamment pour la citabilité. Comme on utilise ici l’attribut global de XML @xml:id qui doit nécessairement être unique dans un fichier XML, il y a un contrôle d’unicité (ce contrôle s’applique à l’ensemble du corpus car il est compris dans une arborescence de fichiers XML). Enfin, le fait d’utiliser des identifiants uniques, a surtout l’avantage de permettre de traiter les regroupements de paragraphes, les interversions, les ajouts, indépendamment du manuscrit édité (et donc par la suite éventuellement d’éditer toutes les variantes du texte ou le réemploi des sources XML-TEI dans d’autres projets).

---

name: sourcesBiblio
template: inverse
class: center middle

# Sources et bibliographie

---

name: biblio

# Orientations bibliographiques

- Driscoll. "P5-MS: A General Purpose Tagset for Manuscript Description." Digital Medievalist 1 (2006). http://www.digitalmedievalist.org/journal/2.1/driscoll/ (accessed February 23, 2014).

---

template: inverse
class: center middle

#

.left[.footnote[[revenir au début](#index)]]
