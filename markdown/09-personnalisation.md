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


Afin de produire une modélisation de ce type, et éventuellement le manuel d’encodage qui l’accompagne, il est nécessaire de bien comprendre sa source. Aussi ne faut-il pas envisager l’encodage comme une fin en soi, mais plutôt comme un moyen de travailler et d’étudier le matériau textuel. La définition du modèle s’opère au moyen d’aller-retour continus avec les sources textuelles que l’on souhaite traiter.

La définition du schéma s’opère au moyen d’aller-retour continus avec les sources textuelles que l’on souhaite traiter.

- On effectue généralement d’abord une **première modélisation à partir d’un échantillon jugé représentatif** du corpus.

- Enfin, lors du passage à l’échelle, il est parfois nécessaire de **corriger quelques choix s’avérant inappropriés ou bien encore de renforcer le contrôle** par l’intermédiaire du schéma.

- Le processus d’élaboration du modèle est donc **un processus incrémentiel**, et le schéma n’est pas d’emblée figé dans le marbre.

---

name: odd
template: inverse
class: center middle

# .red[2.] Le Langage ODD

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

## Organisation de la TEI (rappel)

- 22 Modules

- [Classes de modèle](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/REF-CLASSES-MODEL.html)

- [Classes d'attribut](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/REF-CLASSES-ATTS.html)

???

L’architecture de la TEI permet de construire un schéma en combinant comme de besoin des déclarations d’éléments et d’attributs.

Chaque élément est documenté par un élément de spécification adéquat et dispose d’un identifiant unique dans le système.

Pour plus de facilité, ces spécifications sont groupées dans des modules distincts qui peuvent être combinés entre eux. Chaque module détermine un certain nombre d’éléments spécifiques qui peuvent également renseigner des classes particulières. Toutes les classes sont disponibles globalement, indépendamment des modules dans lesquelles elles sont déclarées.

Lorsque c’est possible, les modèles de contenus sont définis en termes de classes (classes), les modules peuvent également déclarer certains motifs particuliers (patterns).

## Les modules de la TEI

Dans l’infrastructure de la TEI, les éléments de la TEI sont organisés au sein de différents modules qui les regroupent par type d’utilisation.


## Système de classes

Outre ces vingt-deux modules, les cinq cent quarante-trois éléments de la TEI et leurs attributs sont également organisés en classes de modèle (model class) et classes d’attribut (attribute class) afin de faciliter leur modification.

Les éléments d’une même classe peuvent apparaître au même endroit dans un modèle de contenu, il s’agit alors d’une classe de modèle, ou partager un ensemble d’attributs, il s’agit alors d’une classe d’attributs.

Dans les deux cas, on dit qu’un élément hérite des propriétés des classes auxquelles il appartient. Les classes (et donc les éléments qui sont membres de ces classes) peuvent également hériter des propriétés d’autres classes.

-	[liste les classes de modèles](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/REF-CLASSES-MODEL.html)

-	[liste les classes d’attribut](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/REF-CLASSES-ATTS.html)


---

name: application
template: inverse
class: center middle

# .red[3.] Génération d'un Schéma XML ou RelaxNG

---

.left[.footnote[[revenir au début](#index)]]

---
