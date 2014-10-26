title: 02-XML
description: emchateau, ENC 27-30 octobre 2014
theme: themes/remark-dark-em.css
name: inverse
layout: true
class: inverse

---

name: index
class: center middle

# 01 – eXtensible Markup Language
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

name: introduction
class: center middle

# Introduction sur .red[XML]

???

On vient de voir qu'un balisage descriptif permettait de **se concentrer sur le contenu du texte plutôt que sur la présentation physique finale du document**.

Dans une démarche qui privilégie avant tout l’édition du texte, il convient en premier lieu de **rendre la structure du texte explicite, c’est-à-dire de clarifier à la fois les relations hiérarchiques et séquentielles**. La présence du balisage détermine par la suite la possibilité de traiter les éléments pour une transformation.

Le métalangage informatique XML (Extensible Markup Language) permet le développement de vocabulaires descriptifs de balisages interopérables spécifiques à certains domaines.

- cf. Bray, Tim, Paoli, Jean, Sperberg-McQueen, C. Michael, Maler, Eve, et Yergeau, François, [Extensible Markup Language (XML) 1.0](http://www.w3.org/TR/REC-xml/), Recommandation du W3C, 2008.

## Un modèle de contenu arborescent

Son **modèle de contenu arborescent** est précisément conforme au modèle OHCO.

S’il offre une grammaire lisible par la machine, il ne présente pas une réelle sémantique et ne peut donc à lui seul spécifier formellement une sémantique.

XML propose simplement **une solution rigoureuse, compréhensible par les machines, pour définir un langage de balisage descriptif**.

## Une large utilisation dans le domaine culturel

La plupart des contenus des bibliothèques numériques aujourd’hui mis à disposition sur le web sont encodés en utilisant un balisage XML. « La large adoption de vocabulaires XML spécialisés comme la TEI rendent disponible une importante information sémantique, mais seulement sous la forme d’une documentation en prose et de pratiques partagées. »[1]

[1] Coombs, James H, Renear, Allen H, et DeRose, Steven J. ["Markup Systems and the Future of Scholarly Text Processing."](http://xml.coverpages.org/coombs.html) Communications of the ACM 30, no. 11 (1987): 933-947.

---

layout: false

.left-column[

## .red[Historique]

## Caractéristique

## Extensible

]

.right-column[

# e.red[X]tensible .red[M]arkup .red[L]anguage

### basé sur SGML

### Première version du langage 1998

### version 1.1

]

--

.left-column[

## extensible

## ctrl

]

???

Dans son Référentiel général  d’interopérabilité publié en 2009, la Direction générale de la modernisation de l’État recommande l’utilisation des technologies XML (Extensible Markup Language) à des fins d’interopérabilité et de pérennisation de l’information.

- cf. Ministre du Budget, des Comptes publics, [Référentiel Général d'Interopérabilité (RGI)](http://references.modernisation.gouv.fr/rgi-interoperabilite), 2009.

---

# Exemple de document XML

```xml
<?xml version="1.0"?>
<doc xmlns="http://example.org/​namespace">
  <p n="1">This is a paragraph.</p>
  <p n="2">This paragraph mentions <placeName>Bristol</placeName>.</p>
</doc>
```

???
Un document XML prend toujours la forme suivante.

Un document XML consiste en une séquence de caractères lisibles par l'homme. C'est **un simple fichier texte** qui ne contient pas de code additionnel ou de données binaires.

Seulement, vous pouvez constater que ce document comporte certaines séquences de caractères régulières (ici mises en valeur par la coloration).

La première ligne de ce documents s'appelle le **prologue**. C'est une instruction qui permet d'indiquer qu'il s'agit d'un document XML et la version du langage. On peut également préciser l'encodage des caractères.

---

# Exemple de document XML

```xml
<?xml version="1.0" encoding="UTF-8"?>
<doc xmlns="http://example.org/​namespace">
  <p n="1">This is a paragraph.</p>
  <p n="2">This paragraph mentions <placeName>Bristol</placeName>.</p>
</doc>
```

???

## Encodage

Ici on utilise **l'encodage de caractère UTF-8** (pour Universal Character Set) qui permet de représenter la pluspart des caractères du « répertoire universel de caractères codés » initialement développé par l'ISO (ISO/CEI 10646), aujourd'hui entièrement compatible avec le standard **Unicode**.

Le répertoire Unicode peut contenir plus d’un million de caractères.

cf. https://fr.wikipedia.org/wiki/UTF-8

cf. Jukka Korpela. "Guide to the Unicode standard" http://www.cs.tut.fi/~jkorpela/unicode/guide.html


## Composition

Les caractères `<` et `>` sont utiliser pour marquer le début et la fin de **balises** à l'intérieur de ce flux textuel. Ces éléments possèdent un nom.

Vous remarquez que ces balises, ou markup, ou encore étiquettes, sont appariées. À chaque **balise ouvrante** correspond une **balise fermante** qui se distingue en débutant par la séquence `</`.

Le document comporte également des *attributs*. Ce sont des **paires nom-valeurs** qui se rattachent aux éléments.

--

### Les séquences `<`, `>` et `</` délimitent les balises

### Les paires nom-valeur des attributs ont la forme `nom='valeur'` équivalente à `nom="valeur"`

---

# Dénomination


---

# Document bien formé

---

# Validation
