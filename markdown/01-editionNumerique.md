title: 01-editionNumerique
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

name: index
class: center middle

# 01-Un rapide panorama de l'édition critique avec TEI
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
# L'édition critique numérique

## 1. Caractéristiques attendues d'une édition critique

## 2. La prise en charge numérique de l'édition critique

## 3. Le potentiel des éditions numériques
]

---

# Comment rendre compte de la .red[source primaire]

## - Objectivité / parti-pris

## - Édition de sources primaires

## - Matérialité de l'édition

---

#Critères de scientificité

## fiable

## consistante

## justification des partis pris

---

# Un investissement important

## Méthode de travail adaptée (temps long, travail en équipe)

## Interopérabilité

## Pérennité

---

# Peut-on .red[(sérieusement)] utiliser un traitement de texte ?

## S'intéresser au contenu plutôt qu'à la forme

## L'expressivité

---

# Exemples

elec

hyperdonnat

Les liens

- sandrart.net

- vangoghletters.org

---

Ce que l'on peut attendre d'une édition critique numérique

Documentation de l'édition

Contrôle de la production

Perennité et interopérabilité

---

# Encodage descriptif / encodage présentationnel


???

Parce qu’il détermine tous les traitements informatiques qu’il est possible d’effectuer sur le texte, le balisage a historiquement constitué une question fondamentale dans l’histoire de l’informatique. Depuis l’article séminal de Coombs et ses collègues, on a pris l’habitude de distinguer plusieurs types de balisages : procédural, présentationnel, ou descriptif.

cf. Coombs, James H, Renear, Allen H, et DeRose, Steven J, [« Markup Systems and the Future of Scholarly Text Processing »](http://xml.coverpages.org/coombs.html), Communications of the ACM, n° 11, t. 30, 1987, p.933-947.

La supériorité du balisage descriptif sur les autres types de balisage du texte a clairement été établie depuis quelques années. Un tel balisage présente l’avantage notable d’assurer une meilleure distinction entre le contenu et la forme (et donc de séparer les traitements). Cette distinction garantit une meilleure maintenance du texte encodé et une meilleure portabilité des artefacts numériques.

---

# La production d'un balisage descriptif

Identifier explicitement la structure sémantique sous-jacente d'un document, indépendamment de tout traitement déterminé à l'avance.

### Distinguer à l'intérieur du texte différents objets éditoriaux

### Fournir une information sémantique

### Possibilité de produire des vues distinctes

???

La production d’un **balisage descriptif** consiste à identifier explicitement la structure sémantique sous-jacente d’un document, cela indépendamment de tout traitement déterminé à l’avance.

cf. Renear, Allen, Dubin, David, Sperberg-McQueen, C. Michael, et Huitfeldt, Claus, [« XML semantics and digital libraries »](http://dl.acm.org/citation.cfm?id=827140.827192), Proceedings of the 3rd ACM/IEEE-CS joint conference on Digital libraries, p. 303-305, 2003.

Il s’agit de **distinguer explicitement à l’intérieur du texte différents objets éditoriaux** en les encadrant par des balises dont le nom peut être arbitraire.

Ce faisant l’auteur d’un balisage fournit une **information sémantique** et pragmatique suffisante pour produire des vues alternatives sur le document ou bien une édition basée sur la structure du texte.

---

# Procédure mise en œuvre lors du balisage

###  Reconnaissance des éléments

### Sélection des balises

### Réalisation du balisage, marquage de l'élément

???

Les trois opérations qui interviennent au cours du balisage sont donc les suivantes :

-	la reconnaissance des éléments, reconnaître que l’élément courant est un élément d’un certain type (paragraphe, citation en prose, note de bas de page, etc.)

-	la sélection des balises, déterminer le balisage qui s’applique au type d’élément reconnu

-	la réalisation du balisage, marquage de l’élément

cf. Coombs, James, et al., op. cit.

---

# OHCO, Ordered Hierarchical Content Objects

L'idée d'un balisage descriptif suggère une représentation du texte qui correspond à un modèle d'**éléments contenus hiérarchiquement imbriqués** (OHCO, _Ordered Hierarchical Content Objects, en anglais_).

- structure hiérarchique

- relations linéaires

???

L’idée d’un balisage descriptif qui repose sur le fait de marquer le contenu d’un texte par des éléments suggère une représentation du texte qui correspond à ce qu’on a appelé un modèle d’***éléments contenus hiérarchiquement imbriqués*** (OHCO, Ordered Hierarchical Content Objects, en anglais).

Dans une telle représentation du texte, les éléments contenus (paragraphes, citations, phrases, notes, etc.) sont présentés à l’intérieur d’une structure hiérarchique. La structure du texte est hiérarchique parce qu’ils résident les uns à l’intérieur des autres. Les objets reçoivent donc des relations linéaires.


---

# Avantages sur un balisage présentationnel

### Expressivité

### 1. Processus d'établissement du texte simplifié

### 2. Réduction des problèmes de maintenance

### 3. Meilleure portabilité


???

Contrairement aux apparences, les logiciels de traitement de texte qui mettent en forme les documents ne simplifient pas la production de documents en éliminant le besoin du balisage. D’une certaine manière cela est devenu plus clair aujourd’hui avec l’adoption des formats XML par Microsoft Word et Open Office. Mais, le balisage requis pour ces formats, tout en étant plus consommateur de ressources, n’atteint pas la même expressivité qu’un simple balisage descriptif. Par ailleurs, les dispositifs d’édition fondés sur un balisage descriptif présentent plusieurs avantages sur le balisage fondé sur la présentation comme LaTex :

1. Le **processus d’établissement du texte se trouve simplifié** par la focalisation sur le contenu plutôt que sur le contrôle du programme (dans le cas d’un balisage procédural) ou de la présentation typographique de la copie (comme avec LaTex)

2. Les **questions de maintenance sont réduites** à un nombre limité de problèmes indépendants du fichier proprement dit. L’actualisation des styles et la mise à jour s’en trouvent facilitées sans risque de corruption des documents.

3. Enfin, ils fournissent de meilleurs standards dans le domaine patrimonial et culturel, ou pour l’industrie, du point de vue de la **portabilité**. Ils permettent en effet le partage aisé des fichiers et réduisent, à terme, les coûts de publication.


Autrement dit, le balisage descriptif offre un certain nombre d’avantages pour l’éditeur. Outre qu’il **permet de partager des documents pour collaborer sans se préoccuper d’éventuelles incompatibilités**, il offre un **gain de temps de production et de gestion en permettant la réalisation de plusieurs éditions successives à partir d’un même fichier source, ou de produire plusieurs manifestations (présentations) d’un même fichier**. De surcroît, ce balisage permet le plus souvent la **génération automatique de l’information bibliographique** directement à partir du fichier source (ce qui réduit les erreurs et permet une citation aisée dans les bases bibliographiques) ou d’inclure directement des documents dans des bases de données en ligne pour la publication et la recherche plein-texte.

---

# Conclusion (lessons learned)

Privilégier le marquage sémantique plutôt que présentationnel

Ne pas se contraindre du point de vue logiciel

Profiter pleinement des possibilités offertes par le numérique

Disposer d'un cadre de travail qui contrôle la qualité des documents

???

Même si la mise en place d’un balisage descriptif du texte, implique le déploiement d’une infrastructure technique sans-doute moins confortable pour travailler que l’utilisation de logiciels de traitement de texte, il faut relever qu’il permet de se concentrer sur le contenu du texte plutôt que sur la présentation physique finale du document. Bien entendu, concernant l’édition de manuscrits historiques, ou de sources primaires, il pourra être nécessaire de traiter la matérialité physique du document. Néanmoins c’est avant tout l’édition du texte qui est ici privilégiée. Dans une telle démarche, il convient en premier lieu de rendre la structure du texte explicite, c’est-à-dire de clarifier à la fois les relations hiérarchiques et séquentielles. Et la présence du balisage détermine la possibilité de traiter les éléments pour une transformation.

---

Notes

Liste des figuresIntitulé

---

name: sourcesBiblio
template: inverse
class: center middle

# Sources et bibliographie

---

name: biblio

# Orientations bibliographiques

Burnard, Lou, O'Brien O'Keeffe, Katherine et Unsworth, John. [Electronic Textual Editing. Modern Language Association](http://www.tei-c.org/About/Archive_new/ETE/Preview/index.xml), 2006.

Schillingsburg, Peter L., [From Gutenberg to Google](http://books.google.fr/books/about/From_Gutenberg_to_Google.html?id=rd57F8IjyF0C), 2006.

Coombs, James H, Renear, Allen H, et DeRose, Steven J. ["Markup Systems and the Future of Scholarly Text Processing."](http://xml.coverpages.org/coombs.html) Communications of the ACM 30, no. 11 (1987): 933-947.

Hayles, Katherine. ["Print Is Flat, Code Is Deep: The Importance of Media-Specific Analysis."](http://www.lab404.com/242/hayles_print_is_flat.pdf) Poetics Today 25, no. 1 (2004): 67-90.

Barney, Brett. ["Digital Editing with the TEI Yesterday, Today, and Tomorrow."](http://www.jstor.org/stable/10.2979/textcult.7.1.29) Textual Cultures: Texts, Contexts, Interpretation 7, no. 1 (2012): 29-41.

Boot, Peter. ["Some Digital Editions and Some Remaining Challenges."](http://www.janusdigital.es/articulo.htm?id=7) Janus, Estudios sobre el siglo de oro , no. 1 (2012).

---

# Orientations bibliographiques .inverse[(suite)]

- Guyotjeannin, Olivier, and Olivier Poncet. _[L’édition électronique de sources d’archives médiévales et modernes, Quelques réflexions](https://intranet.enc.sorbonne.fr/files/20100315-Edition-electronique-intro-OGJ-OP.pdf)_. mars, 2010.

- Bourgain, Pascale, and Françoise Vieillard (dir.), _Conseils Pour L'édition Des Textes Médiévaux_. Conseils généraux, Fascicule I. Documents d'archives, Fascicule II. Textes littéraires, Fascicule III. Paris: Comité des travaux historiques et scientifiques / École nationale des chartes, 2001-2002.

- Barbiche, Bernard. _["Conseils Pour L’édition Des Textes De L’époque Moderne (XVIe-XVIIIe Siècle)"](http://theleme.enc.sorbonne.fr/cours/edition_epoque_moderne/edition_des_textes)_. Theleme (Techniques pour l'Historien en Ligne : Études, Manuels, Exercices).

- Christine Nougaret et Elisabeth Parinet (dir.), _Conseils pour l'édition des textes de l'époque moderne_, École nationale des chartes, **à paraître en décembre 2014 (avec un chapitre de Florence Clavaud consacré à l'édition électronique) !!**.

---

template: inverse
class: center middle

# XML, [quésaco](02-xml.html) ?

.left[.footnote[[revenir au début](#index)]]
