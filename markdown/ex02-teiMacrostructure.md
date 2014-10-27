title: 01-editionNumerique
description: emchateau, ENC 27-30 octobre 2014
theme: theme/remark-dark.css
name: inverse
layout: true
class: inverse

---

name: index
class: center middle

# ex02-TP macrostructure TEI
Formation TEI | ENC 27-30 octobre 2014


.footnote[[Répertoire GitHub](https://github.com/emchateau/formEnc2014-10) | [Programme](00-programme.html)]

???

## Exercice basé sur plusieurs documents

Nous allons travailler sur plusieurs documents, par là-même ce sera l'occasion de montrer plusieurs problématiques et de montrer que la TEI est suffisamment générique pour s’adapter à plusieurs cas de figure différents.

J’aimerais aussi au terme de ces séances que vous puissiez vous faire une idée sur le fossé qui existe entre ce que l’on peut faire avec un traitement de texte et ce que l’on peut faire avec TEI : vous verrez combien la TEI offre un niveau d’expressivité nettement supérieur.


## Une approche générique de l'édition

Mon discours sera volontairement générique.
Dans le temps qui nous est impartis, on ne pourra évidemment pas aborder tous les aspects de la TEI ou de l'édition critique. Nous nous concentrerons ici sur le cœur de travail de l'ENC, l'édition critique de manuscrits dans le cadre de l'édition de sources primaires.

Les exemples envisagés pourront bien évidemment également s'appliquer aux éditions imprimées, mais par certains aspects les utilisations seront probablement différentes.

Nous ne parlerons ni de l'encodage du discours oral, ni de l'encodage lexicographique ou linguistique.

On ne va pas vraiment non plus se placer du point de vue d'une approche spécifique par exemple, celle de l'édition de roman du XIXe siècle, où l'on conserve plusieurs manuscrits témoignants de plusieurs états du texte, ensuite, les épreuves de l’éditeur, et enfin, une ou plusieurs éditions.

La prise en charge d'un tel cas, réclamerait de prendre en compte le processus de création, et l’ensemble des états des manuscrits.


## L'édition diplômatique

Mais il y aurait encore bien d’autres cas de figure : par exemple les historiens du MA confrontés à des sources primaires, ont souvent des objectifs bien différents. Il s’agit pour eux de rendre accessibles des textes difficiles d’accès ou dispersés, les éditer, puis de les transmettre. Ils seront alors probablement moins confrontés à des problématiques d’états, même si cela n’est pas totalement à exclure.

Il est possible que vous disposiez d’un texte en parchemin, et qu’ensuite le texte ait été copié. Dans les abbaye, etc. ou autres lieux de pouvoirs, on avait pris l’habitude de transcrire dans des registres les originaux de l’ensemble des titres ou des droits d’une entité pour qu’ils soient plus faciles à manipuler. Par ailleurs, parfois eu besoin d’altérer ces documents pour asseoir des droits (falsification). Ensuite toute la tradition érudite qui ont retranscrit ces sources par la suite, souvent d’abord sous forme manuscrite.

En l'absence de sources manuscrites, on sera sans doute confrontés à d’autres problématiques que celle de traduire la tradition du texte. Et je n'évoque même pas les approches linguistiques. Par exemple manière d’utiliser le latin à une époque donnée, etc.


## L'établissement du texte

Typiquement, dans un tel processus, que l’on soit diplômatiste, historien de la littérature (généticien), linguiste, ou autre, **la première étape sera l’établissement du texte**.

- Le trouver, le localiser, le lire, le comprendre.

- Essayer de réunir les différents états s’il y en a.

- S’il y en a, voir quel texte on retient.

Cela dépend des textes dont on dispose. Le plus souvent on gardera l’original, la version dont on est sûr de la provenance, celle qui réunit le plus de marques d’authenticité.


## La transcription

Ensuite on transcrit. La règle de base est d’**être le plus fidèle possible par rapport au manuscrit**. Selon les dates ou les époques pourra adopter des règles différentes. Lorsque l'on s'occupe de documents de l’époque moderne, on corrigera la ponctuation, dans certains cas l’on corrigera même l’orthographe. Tandis que lorsque l'on a affaire à un texte plus ancien on lissera probablement moins le texte.

Mais **transcrire le texte c’est aussi prendre en compte les ratures, les marges, gloses, mots gommés, abréviations** (comment les restituer).

Il s'agit également d’**exprimer la mise en page**. Selon les types de documents ou les dates, on marquera les changements de lignes, les changements de colonnes. Pour les documents plus récents, on se contera le plus souvent de noter les changements de page. L’inscription sur le support est importante pour la compréhension du document. Il est également important de noter si certains caractères sont tracés plus gros que d’autres, s'il y a l'emploi d’autres couleurs, et qu’en faire.

Lorsque l'on est confronté à plusieurs états, on va transcrire tous ces états. Ou dans la tradition française, choisir un texte que l’on appellera l’original et lui rapporter toutes les variantes de la tradition du texte. Par exemple une charte originale avec sceau. Copiée par un moine, on essaye de repérer en quoi cette transcription est différente en rapportant les variantes des états différents au témoin de référence. Ou bien fait différentes transcriptions parallèles.

On va aussi établir l’apparat critique plus généralement : par rapport au témoin de référence noter les éléments de mises en page, ratures, etc. qui vont faire l’objet de notes d’apparat critique.


## L'analyse

Une fois le texte correctement établi, intervient toute une phase d’analyse : ce qu'on peut appeler l’annotation sémantique.

Une fois que l’on a établi le texte, il convient de se donner les moyens de le comprendre. Cela va se traduire par la production de métadonnées.

- Identifie le document, va essayer de déterminer sa date (pas forcément simple). Date qui peut être établie par un règne, une date religieuse dont l’occurrence varie selon les années, etc. Analyser le document, le titrer. Donner un lieu où le texte a été établi.

Ensuite tout un travail d’annotation plus précis, pour essayer dans le cas où ensemble d’annotations liées à un contexte précis, on sera probablement amené à expliquer le contenu du texte par un apparat de notes historiques. Annotations à but explicatif, historique, ou linguistique.

Intervient aussi également l’indexation, dans l’idée où vous intervenez sur la production d’une indexation dans le cas de la production d’un corpus de texte.
Ici tout le travail d’annotation linguistique ou sémantique.

Enfin intervient toute une série d’action de type interprétative. De plus en plus peut être amené dans le contexte du numérique à considérer que malgré le travail mené pour l’annotation sémantique, rien ne remplace la traduction. Alors besoin d’aligner ces traductions. Enfin dans le cadre diplomatique, peut être amenés à analyser le discours. Pour le MA étude du discours diplomatique depuis le 17e siècle. On sait que selon le type d’actes, on a un formulaire : un ensemble d’informations dans le même ordre, ce que l’on vend, ce que l’on donne, qui je suis, quelles sont les clauses, les réserves, etc. Peut être amenés dans certains travaux à vouloir isoler ces différents segments de textes, c’est-à-dire à vouloir faire une analyse interprétative. Peut être amenés à découper le texte autrement si analyse le récit, etc.

Mais dans tous les cas, la première étape consistera à établir le texte. C’est à dire identifier les textes, les transcrire, et au-delà créer tout un apparat qui permettra d’exploiter les textes.

L’informatique aidera à fouiller, chercher, compter les choses. À les structurer. À les présenter, et les publier en ligne.

---

layout: false

# Choisir une édition pour travailler

### [Journal de Delescluze](../exercices/journalPrisonDelescluze/)

### [Journal des travaux de Labrouste](../exercices/journalTravauxLabrouste/)

### [Thalamus](../exercices/thalamusMontpellier/)

???

Ici va travailler sur des exemples. Ne va pas travailler sur l’établissement du texte, ce travail est déjà fait, vous aurez les fichiers Word de transcription. Simplement on reviendra à la source (l’image du manuscrit) pour savoir comment encoder les phénomènes.

3 autres sous-dossiers qui concernent trois manuscrits différents.
Dans ces dossiers, tout le temps des images numériques car on aura toujours besoin des images numériques, ne peut pas se contenter de la transcription (un extrait) en traitement de texte. Un fichier annexe qui donne des informations sur la transcription.

Ce sont des **cas réels**.


## Thalamus

Thalamus : manuscrit conservé AM Montpellier, une production du Consultat médiéval.

Le Consultat de Montpellier a commencé au 14e siècle à rédiger de manière rétrospective, année par année, ce que l’on peut appeler aujourd’hui des chroniques occitanes.

Années par années, relevées la liste des consuls et des officiers désignés et progressivement, ces listes consulaires ont été étoffées par une chronique annuelle des événements étant intervenus dans la ville et plus largement dans la région ou en Europe.

10aine de témoins. Choix d'un ms maître auquel rapporte tous les témoins.
édition fautive de 1840.


## Journal Prison Delescluze

Un document conservé aux archives privées dans le fonds Delescluze. Un ensemble de carnets produits par Louis-Henri Delecluze un opposant politique français 1851.

Emprisonné prison de Belle-ille en mer. Et à la fois pour survivre et passer le temps, carnets. Continué à lire. Moyens continuer acheter de l’encre, du papier, des livres. Tenu sa comptabilité journalière. Rédigé ses pensées philosophiques. Consigné discussions politiques avec autres prisonniers. = journaux intimes.

Début d’édition dans le cadre d’un travail de Master 2 par Nathalia Anachkeva ? 2010. Par la suite Benjamin Danfrey a fait sa thèse d’archiviste paléographe sur ce travail en poursuivant le travail d’édition mais pas en TEI. Travail également sur les textes littéraires de Delecluze. Actuellement en train de préparer l’édition électronique de l’ensemble.


## Journal des Travaux de Labrouste

Transcription et édition scientifique par Marie-Hélène de La Mure, conservateur général au département de la Réserve de la Bibliothèque Sainte-Geneviève, avec le concours, en 2012, de Brunilde Renouf, élève du Master "Technologies numériques appliquées à l'Histoire" de l'École nationale des chartes.

---

# Associer son fichier à un schéma

## XML Schema

```xml
<TEI xmlns="http://www.tei-c.org/ns/1.0"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xsi:schemaLocation="http://www.tei-c.org/ns/1.0  ../schema/TEIschema.xsd">
  <teiHeader></teiHeader>
  <text></text>
</TEI>
```

## RelaxNG

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-model href="../TEIschema.rng"  type="application/xml"
 schematypens="http://relaxng.org/ns/structure/1.0"?>
 <TEI xmlns="http://www.tei-c.org/ns/1.0"
 xmlns:xi="http://www.w3.org/2001/XInclude">
  <teiHeader></teiHeader>
  <text></text>
</TEI>

```

???

Le problème, un manuscrit dont a les images. On a une édition d’une bonne qualité.

Notre but, de passer de ce fichier là à une édition XML-TEI.

Notre but sera aussi de s’affranchir de l’édition word. D’une part, car on aura sans doute envie d’aller plus loin. Mais aussi parceque l’édition word est déjà un peu le résultat du processus que l’on va mener. Va faire comme si partait de rien.
Procéder selon les étapes évoquées tout à l’heure.

1° étape de l’édition du texte

Avant tout, il va falloir créer un fichier XML vide. Et surtout, se donner moyen de ne pas raconter n’importe quoi en TEI, et en conséquence se donner les moyen de rendre votre document valide contre un modèle.

Comme notre but est de définir un modèle. Le but n’est pas d’abord de s’enfermer. TEI un modèle générique dans lequel doit faire un choix. Le but arriver à un modèle un peut plus restrictif.

Mais dans un premier temps lorsque n’a pas encore analysé le texte, partir d’un modèle relativement large et progressivement choisir les fonctions qui nous paraissent appropriées.

Dans un premier temps, choisir un schéma le plus générique possible pour produire la transcription d’un manuscrit.

Pour cela un outil en ligne qui s’appelle Roma. Faire l’exercice pour que vous sachiez dans une situation comparable vous débrouiller avec tout cela.

Choisir :
Pour notre proposition transcr, texcrit, namesdates, analysis, certaintly, et msdesc, et module linking et gaigi.

---

template: inverse
class: center middle

# à [demain](00-programme.html#programmeJour2)

.left[.footnote[[revenir au début](#index)]]
