title: 04-Macrostructure
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

name: index
class: center middle

# 04-Macrostructure
Formation TEI | ENC 27-30 octobre 2014

.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

---

layout: false
.left-column[
  ## Introduction
]

.right-column[
# L'édition critique numérique

- domaine en évolution rapide
- biblio ecdotique traditionnelle
- biblio langue anglaise

Pas de norme ou de référence unique, même si certaines réalisations constituent des références fortes et des standards techniques qui favorisent la convergence.
]

---

name: sommaire
template: inverse

.left-column[
##  .red[Sommaire]
]

.right-column[
# La macrostructure TEI

## 1. [Structure d'un document TEI](#part1)

## 2. [Le teiHeader](#part2)

## 3. [Macrostructure du texte](#part3)
]


---

name: part1
template: inverse
class: center middle

# .red[1.] La macrostructure TEI

---

# Composition d'un fichier TEI

```xml
<TEI xmlns='http://www.tei-c.org/​ns/​1.0'>
  <teiHeader>
    <!-- métadonnées décrivant le texte --> </teiHeader>
  <text>
    <!-- représentation du texte lui-même -->
  </text>
</TEI>
```

???

Tous les documents TEI reçoivent une organisation similaire.
L'élément racine (celui qui contient tous les autres) est un élément `TEI`, celui-ci est placé dans l'espace de nom tei avec l'attribut `xmlns`, ce qui signifie que tous les sous-éléments sont placés dans cet espace de nom par défaut.

Un document TEI se compose d'au moins deux parties :
- `teiHeader` qui accueille les métadonnées décrivant le texte
- `text` qui reçoit la représentation du texte lui-même.

name: part2
template: inverse
class: center middle

# .red[2.] Le teiHeader

---

name: part3
template: inverse
class: center middle

# .red[3.] Macrostructure du texte

---

template: inverse
class: center middle

# Maintenant, passons à [la pratique](ex02-teiMacrostructure.html) !

.left[.footnote[[revenir au début](#index)]]

---
