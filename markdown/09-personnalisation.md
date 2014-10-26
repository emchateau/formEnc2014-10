title: 09-personnalisation
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

class: center middle

# 09-Personnalisation de la TEI
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

name: introduction
class: center middle

# Introduction

???
La Text Encoding Initiative (TEI) est un projet universitaire international dont l'objectif est de favoriser le partage et l'échange de sources textuelles encodées. Le contexte scientifique du projet explique que la TEI ne constitue pas une norme proprement dit, mais avant tout un cadre de travail personnalisable dans lequel puiser en fonction des besoins propres et particuliers de chaque projet de recherche. La philosophie de la TEI consiste à fournir un vocabulaire nécessaire pour la description des textes sans pour autant dicter précisément ce que ces textes doivent contenir ou pourraient contenir. Ainsi, la TEI spécifie des conventions d'encodage simples, faciles à employer et relativement compréhensibles qui sont accompagnées d'amples mécanismes d'extension afin de pouvoir répondre à des besoins particuliers{Ide 1995}.

À certains égards, on peut dire comme le suggère Florence Clavaud qu'elle propose une sorte « d'ontologie générique du texte » capable de prendre en charge tant l'hétérogénéité des matériaux textuels rencontrés que des points de vue adoptés. Pour autant, celle-ci n'est pas exprimée de manière formelle mais sous forme d'une documentation littéraire inspirée des principes de la programmation littéraire de Donald Knuth.

---

name: sommaire
template: inverse

.left-column[
##  .red[Sommaire]
]

.right-column[
# Personnalisation de la TEI

## 1. [Une logique modulaire](#logiqueModulaire)

## 2. [Le langage ODD](#odd)

## 3. [Génération d'un Schéma XML ou RelaxNG](#application)
]

???

Nous allons maintenant voir comment mettre en œuvre une personnalisation de la TEI en fonction des besoins particuliers d'un projet d'édition.

- revenir sur la logique modulaire de la TEI

- s'arrêter sur le langage ODD

- applications pratiques avec la génération d'un Shéma XML ou RelaxNG pour contrôler la production ou valider des documents

---

name: logiqueModulaire
class: center middle

# .red[1.] Une logique modulaire

---

layout: false
name: systemeModulaire

# Un système modulaire

## Une modélisation s'exprime à l'aide d'un .red[schéma]

## La définition du schéma s'opère au moyen d'.red[aller-retour avec les sources textuelles]

- Première modélisation à partir d’un échantillon représentatif

- Correction ou renforcement du contrôle lors du passage à l'échelle

- Un processus incrémentiel, le schéma n’est pas figé dans le marbre


???

## Un système modulaire

Dès l’origine la TEI a été conçue pour être employée comme un ensemble de briques permettant de construire des schémas spécifiques pour un projet donné.

- Dans cet esprit, la TEI propose un vocabulaire pour décrire les textes sans préjuger de ce que les textes pourraient contenir.

- Aussi est-il important de comprendre que la TEI ne propose pas un schéma global, mais un ensemble de modules parmi lesquels choisir les éléments qui répondent à ses propres besoins en termes de modélisation.


## Une modélisation qui s'exprime à l'aide d'un schéma

**Cette modélisation s’exprime à l’aide d’un schéma** qui est une personnalisation de la TEI. Il s’agit en fait de produire un sous-ensemble de la TEI approprié à son projet. Comme la TEI utilise les technologies XML, il est possible de contrôler la production d’un document dans un éditeur XML ou encore de valider son contenu en l’associant à un schéma qui peut être rédigé dans divers formats (RelaxNG, W3C XML schema, etc.). Un schéma constitue donc à la fois une manière de représenter le modèle de contenu des documents traités et de contrôler leur structure ou leur contenu d’un point de vue technique.


## Une définition qui s'opère au moyen d'aller-retour avec les sources textuelles

La définition du schéma s’opère au moyen d’aller-retour continus avec les sources textuelles que l’on souhaite traiter.

- On effectue généralement d’abord une **première modélisation à partir d’un échantillon jugé représentatif** du corpus.

- Enfin, lors du passage à l’échelle, il est parfois nécessaire de **corriger quelques choix s’avérant inappropriés ou bien encore de renforcer le contrôle** par l’intermédiaire du schéma.

- Le processus d’élaboration du modèle est donc **un processus incrémentiel**, et le schéma n’est pas d’emblée figé dans le marbre.

---

# De quoi a-t-on besoin ?



---

# .red[O]ne .red[D]ocument .red[D]oes it all (.red[ODD])

## C'est précisément l'objet de ODD qui propose un vocabulaire spécialisé pour définir

- des schémas
- des types d'éléments XML
- des macros ou patrons
- des classes d'éléments ou d'attributs
- une manière de faire référence à ces objets

---

.left[.footnote[[revenir au début](#index)]]

---
