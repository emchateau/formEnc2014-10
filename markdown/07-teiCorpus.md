title: 07-teiCorpus
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

class: center middle

# 07-Liens et structures complexes
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

layout: false
.left-column[
  ## Introduction
]

.right-column[
# Corpus TEI

]

???

On l’a vu, la Text Encoding Initiative fournit un grand nombre de balises dans lesquelles il est possible de puiser pour modéliser son texte. Personne ne les utilise toutes dans le cadre d’un même projet. En d’autres termes, on doit construire des représentations du texte source qui reflètent les phénomènes que l’on observe d’un point de vue structurel, sémantique ou linguistique, et que l’on va modéliser d’après la manière dont on espère les exploiter par la suite. À cet égard, la modélisation XML-TEI est une opération intrinsèque au processus éditorial et qui a directement trait au caractère scientifique de l’édition numérique. Puisqu’il s’agit bel et bien de produire un artefact orienté.

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

# Macrostructure

Les manuscrits que nous avions à traiter présentaient généralement une structure textuelle relativement commune qui pouvait facilement être prise en charge à l’aide des éléments structurels offerts par la TEI. Il a systématiquement été établi une division tripartite dans l’édition avec les éléments <front> pour les parties liminaires, <body> pour le corps de texte et <back> pour les paries postérieures. À l’intérieur de ces différentes parties, <titlePage> avec ses sous-composants permettait de prendre en charge les pages de titre, et une combinaison des éléments <div>, <p>, <list> et tous ses composants, ainsi que <seg> a paru adaptée et suffisante pour traiter presque tous les cas de figure. Un système de typage des divisions a toutefois été établi pour préciser cette macrostructure en utilisant l’attribut @type. La liste fermée des types de division doit encore être restreinte par le schéma.

---

# teiCorpus

```xml
<teiCorpus>
  <teiCorpus>
    <TEI>
      <!-- témoin manuscrit -->
    </TEI>
    <TEI>
      <!-- témoin manuscrit -->
    </TEI>
    <TEI>
      <!-- témoin manuscrit -->
    </TEI>
  </teiCorpus>
  <teiCorpus>
    <!-- ... -->
  </teiCorpus>
</teiCorpus>

```

---

# Utilisation de XInclude

```xml
<teiCorpus xmlns="http://www.tei-c.org/ns/1.0"
    xmlns:xi="http://www.w3.org/2001/XInclude">
    <teiHeader>
      <!-- ... -->
    </teiHeader>

    <!-- Inclusion du fichier TEI du manuscrit des Ordres (O) -->
    <xi:include href="o/desgodetsO.tei.xml" parse="xml">
        <xi:fallback>Fichier TEI du manuscrit des Ordres de Desgodets non trouvé</xi:fallback>
    </xi:include>

    <!-- Inclusion du fichier TEI du manuscrit des Commodités (C) -->
    <xi:include href="c/desgodetsC.tei.xml" parse="xml">
        <xi:fallback>Fichier TEI du manuscrit des Commodités de Desgodets non trouvé</xi:fallback>
    </xi:include>
  </teiCorpus>
```

- [XML Inclusions (XInclude) Version 1.0 (Second Edition), W3C Recommendation 15 November 2006](http://www.w3.org/TR/xinclude/).

---

# Utilisation de XInclude

équivaut à :

```xml
<teiCorpus xmlns="http://www.tei-c.org/ns/1.0"
    xmlns:xi="http://www.w3.org/2001/XInclude">
    <teiHeader>
      <!-- ... -->
    </teiHeader>
    <!-- Inclusion du fichier TEI du manuscrit des Ordres (O) -->
    <TEI>
      <!-- contenu du fichier TEI -->
    </TEI>
    <TEI>
      <!-- contenu du fichier TEI -->
    </TEI>
</teiCorpus>

---

template: inverse
class: center middle

#

.left[.footnote[[revenir au début](#index)]]
