title: 05-teiHeader
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

class: center middle

# 05-Le teiHeader et la description des manuscrits
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---
name: introduction
class: center middle

## Introduction

???

---

name: sommaire
template: inverse

.left-column[
##  .red[Sommaire]
]

.right-column[
# L'entête TEI

## 1. [L'importance des métadonnées](#metadonnees)

## 2. [Les composants du header](#composants)

## 3. La description du [manuscrit](#description)
]

---

name: metadonnees
template: inverse
class: center middle

# L'importances des métadonnées

---

layout: false

# L'importance des métadonnées

### autoportées

### intégration dans des bibliothèques numériques

### choix des modèles descriptifs

???

Un important travail a été mené sur la production des en-têtes TEI et la question des métadonnées. Pour arrêter les choix d’encodages, il convient d'examiner un certain nombre de pratiques documentaires  et de rechercher des guides de bonnes pratiques pour la TEI.

Un travail en cours conduit au sein du consortium cahier destiné à produire un moissonnage des en-têtes TEI en OAI-PMH (Open Archives Initiative Protocol for Metadata Harvesting).

On se dirige donc vers la définition de pratiques commune pour la communauté francophone. Il serait dommage de ne pas s'y conformer.

---

name: composants
template: inverse
class: center middle

# Les composants du teiHeader

---

# Les composants du teiHeader

### `fileDesc` la description de fichier

### 3 éléments facultatifs

- `encodingDesc` description des convention d'encodage

- `profileDesc` information classificatoires

- `revisionDesc` révisions

---

# teiHeader minimal

```xml
<teiHeader>
  <fileDesc>
    <titleStmt>
      <title><!-- titre --></title>
    </titleStmt>
    <publicationSmt>
      <p><!-- mentions de publication --></p>
    </publicationSmt>
    <sourceDesc>
      <p></p>
    </sourceDesc>
  </fileDesc>
</teiHeader>
```

---

# fileDesc

## trois éléments mandataire

- `titleStmt` mentions de titre et de responsabilité

- `publicationStmt` mention de publication (du texte électronique)

- `sourceDesc` renseignements sur la source dont est issu le fichier numérique

## trois éléments facultatifs

- `editionStmt` informations relatives à l'édition

- `extent` taille du fichier

- `seriesStmt` informations relatives à la collection

- `noteStmt` notes fournissant des informations sur le texte

---

# Mentions de titre et de responsabilité  `titleStmt`

```xml
<titleStmt>
 <title xml:lang="fre" type="main">Sauval 1724</title>
 <principal>
   <persName ref="#MCL">
     <forename>Marianne</forename>
     <surname>Cojannot-Le Blanc</surname>
   </persName>
 </principal>
 <funder>
   <orgName>Labex Les Passés dans le Présent</orgName>
   <date from="2013" to="2018">2013-2018</date>
 </funder>
 <respStmt>
   <resp key="mrk">encodage XML-TEI</resp>
   <persName ref="#EC">
     <forename>Emmanuel</forename>
     <surname>Château</surname>
   </persName>
 </respStmt><!-- ... -->
</titleStmt>
```


---

name: description
template: inverse
class: center middle

# La description des manuscrits

---

name: sourcesBiblio
template: inverse
class: center middle

# Sources et bibliographie

---

name: biblio

# Orientations bibliographiques

- Glorieux, Frédéric, et Jolivet, Vincent, [« weboai, Human web interface on OAI repository »](http://weboai.sourceforge.net), SourceForge.

- [DeMArch Description des manuscrits et fonds d'archives modernes et contemporains en bibliothèque](http://www.bnf.fr/fr/professionnels/normes_catalogage/a.ead_demarch.html).

- Hawkins, Kevin, Dalmau, Michelle, et Bauman, Syd, [Best Practices for TEI in Libraries](http://www.tei-c.org/SIG/Libraries/teiinlibraries/main-driver.html).

- Lou Burnard ed., [The ENRICH Schema – A Reference Guide](http://projects.oucs.ox.ac.uk/ENRICH/).

- Driscoll. "P5-MS: A General Purpose Tagset for Manuscript Description." Digital Medievalist 1 (2006). http://www.digitalmedievalist.org/journal/2.1/driscoll/ (accessed February 23, 2014).

---

template: inverse
class: center middle

# Mettre [en pratique](ex03-teiHeader.html)

.left[.footnote[[revenir au début](#index)]]

---
