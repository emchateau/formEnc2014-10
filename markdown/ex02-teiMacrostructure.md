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

---

layout: false

# Choisir une édition pour travailler

### [Journal de Delescluze](../exercices/journalPrisonDelescluze/)

### [Journal des travaux de Labrouste](../exercices/journalTravauxLabrouste/)

### [Thalamus](../exercices/thalamusMontpellier/)

???

## L'établissement du texte

Typiquement, dans un tel processus, que l’on soit diplômatiste, historien de la littérature (généticien), linguiste, ou autre, **la première étape sera l’établissement du texte**.

- Le trouver, le localiser, le lire, le comprendre.

- Essayer de réunir les différents états s’il y en a.

- S’il y en a, voir quel texte on retient.

Cela dépend des textes dont on dispose. Le plus souvent on gardera l’original, la version dont on est sûr de la provenance, celle qui réunit le plus de marques d’authenticité.


## La transcription

Ensuite on transcrit. La règle de base est d’être le plus fidèle possible par rapport au manuscrit. Selon les dates ou les époques pourra avoir des règles différentes. Si des documents de l’époque moderne, on corrigera la ponctuation, peut-être que l’on corrigera même l’orthographe. Si un texte plus ancien, probablement lissera moins le texte. Mais transcrire le texte c’est aussi prendre en compte les ratures, les marges, gloses, mots gommés, abréviations (comment les restituer). Ensuite toute la manière d’exprimer la mise en page. Selon les types de documents ou les dates, on cherchera à exprimer les changements de lignes, les changements de colonnes. Pour les documents plus récents, souvent se contentera de noter les changements de page. L’inscription sur le support est importante. Important également de voir si certains caractères plus gros que d’autres, si d’autres couleurs, et qu’en faire.
Si plusieurs états, on va transcrire tous ces états. Ou dans la tradition française, choisir un texte que l’on appellera l’original et lui rapporter toutes les variantes de la tradition du texte. Par exemple une charte originale avec sceau. Copiée par un moine, on essaye de repérer en quoi cette transcription est différente en rapportant les variantes des états différents au témoin de référence. Ou bien fait différentes transcriptions parallèles.
On va aussi établir l’apparat critique plus généralement : par rapport au témoin de référence noter les éléments de mises en page, ratures, etc. qui vont faire l’objet de notes d’apparat critique.

---

template: inverse
class: center middle

#

.left[.footnote[[revenir au début](#index)]]
