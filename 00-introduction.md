# Introduction

<h2>De l'importance de la gestion des données de la recherche</h2>

La gestion rigoureuse et cohérente des données de la recherche constitue aujourd’hui un enjeu de taille pour la production de nouvelles connaissances scientifiques. Guidés par le « [Plan National pour la Science Ouverte](https://www.ouvrirlascience.fr/plan-national-pour-la-science-ouverte/) », les différents organismes de recherche et les Instituts du CNRS s’emparent de ces questions primordiales aux côtés des acteurs de la Science Ouverte pour participer à la réflexion et à la mise à dispositions des outils, méthodes et infrastructures répondant aux besoins des communautés scientifiques en matière de gestion et de partage des données scientifiques. 

Améliorer les pratiques de gestion des données de la science devient nécessaire pour garantir l’intégrité scientifique et la traçabilité de la recherche produite, mais aussi pour rendre accessible, partager, permettre la réutilisation ou la reproductibilité des données produites et financées sur des fonds publics.

Gérer les données de la recherche est un processus difficile qui suppose un travail long et coûteux, des moyens techniques et humains parfois importants et qui comprend plusieurs étapes avant d’aboutir à la publication et l’archivage de données fiables, de qualité, respectueuses du droit des personnes et de la législation en vigueur.

```{sidebar} <span style="font-weight: normal; font-size: 14px;">Cycle de vie des données de la recherche établi par l'Atelier Données</span>
<font size=2>Etapes pour une gestion FAIR des données d'un projet de recherche.</font>
```
```{image} images/donnees.png
:width: 350px
```
Pour formaliser les différentes étapes de gestion des données nous nous sommes servis du "[cycle de vie des données](https://www.cnrs.fr/mi/IMG/png/donnees.png)". Il s’agit d’un cercle vertueux qu'on peut faire correspondre aux différentes phases d’un projet scientifique.

<h2>L'apport des réseaux métiers du CNRS</h2>

Dans leurs différentes pratiques, les réseaux métiers du CNRS, regroupés au sein de la [MITI](https://miti.cnrs.fr) (Mission pour les Initiatives Transverses Interdisciplinaires) et des Instituts du CNRS sont en première ligne pour participer à ce mouvement d’ouverture et de partage des données. Les personnels des organismes de recherche qui les constituent, œuvrent pour mettre en place de bonnes pratiques de gestion et participent également au processus de production des données scientifiques aux côtés des équipes de recherche. C’est aussi dans ce cadre qu’ils interviennent en appui et soutien à la recherche scientifique.

C'est précisément ce travail de soutien que nous nous proposons de rendre compte dans ce document qui, à travers de nombreux séminaires communications et formations, vise à fournir les meilleures pratiques du moment en matière de gestion des données, et peut ainsi s'apparenter à un "guide de bonnes pratiques".  

Certes de nombreux guides existent déjà dans le domaine, mais l'originalité de ce document réside dans son application aux données de la recherche sous l'angle de différents métiers de la recherche. Il fournit donc un point de vue transversal intéressant et traduit les efforts et le soutien mis en place par les personnels d’appui à la recherche au sein des réseaux, dans la gestion et la valorisation des données scientifiques.

<h2>Objectifs du guide</h2>

Ce guide est la production de l'"[Atelier Données](https://mi-gt-donnees.pages.math.unistra.fr/site/index.html)" du groupe de travail Données inter-réseaux. Il s’agit d'un groupe de travail composé de plusieurs réseaux métiers de la MITI ([Calcul](https://calcul.math.cnrs.fr/), [Devlog](http://devlog.cnrs.fr/), [QeR](http://qualite-en-recherche.cnrs.fr/), [Rbdd](http://rbdd.cnrs.fr/), [Renatis](http://renatis.cnrs.fr/), [Resinfo](https://resinfo.org/), [Medici](http://medici.in2p3.fr/)), du [réseau SIST](http://sist.cnrs.fr), regroupant les gestionnaires de données environnementales, et labellisé par l'Institut INSU , de l'INIST, et de la Direction de l’Information Scientifique et Technique du CNRS (DIST-CNRS). [Les activités de cet Atelier](https://sist19.sciencesconf.org/data/pages/diapo_GT_donnees_sist19_v2.pdf) de la MITI ont été présentées lors du séminaire SIST 2019.

Ce guide fait suite à un premier travail plus synthétique réalisé en 2017 qui visait à établir [une cartographie de l’action des réseaux en matière de gestion des données de la recherche](https://mi-gt-donnees.pages.math.unistra.fr/site/download/GTInterreseaux-CartoSyntheseV6-optimise.pdf). Ce travail rendait compte dans ses grandes lignes, des usages et des questionnements des réseaux sur la gestion des données, tout en apportant une vision des métiers transversale sur le sujet et les problématiques attenantes. 

Il nous est apparu opportun d'aller plus loin et de détailler plus précisément les apports de nos réseaux métiers, compte tenu :      
  - des nombreuses actions de formation ou de sensibilisation mises en place,    
  - des compétences et expertises développées prenant appui sur des pratiques standardisées qui font leurs preuves sur le terrain,    
  - de la diffusion de recommandations et de solutions techniques et organisationnelles au sein des communautés grâce à la veille technologique et juridique réalisée très régulièrement.

Dans ce document, nous avons donc voulu témoigner des travaux qui rendent compte des processus de gestion des données de la recherche, réalisés au sein de nos réseaux métiers,  tout en guidant le lecteur vers d'autres ressources pédagogiques lui permettant d’approfondir le sujet. Ce guide fera des renvois systématiques vers des ateliers, séminaires, formations organisés par les réseaux pour rendre compte et approfondir ces bonnes pratiques.

Ce guide est donc un document un peu hybride proche du vadémécum, composé d’un inventaire d’actions de formations (conférences, séminaires, présentations), d’un répertoire de liens, de recommandations professionnelles, complétées de définitions utiles, pour approfondir le sujet de la gestion des données dans les réseaux métiers.

## Sommaire 

Ce Guide abordera l'ensemble des phases et actions nécessaires pour une gestion FAIR des données :
- les 2 premières phases "{ref}`imaginer` et {ref}`concevoir-planifier`", sont des étapes préparatoires d'un projet, où l'on se préoccupe d'avoir toutes les informations nécessaires (formations, infrastructures), réfléchi au de plan de gestion de données, préparé les organes de stockage, et mis en place les outils de gestion de projet. cette partie doit aider le lecteur qui veut améliorer sa gestion des données, à se poser les bonnes questions et à savoir puiser les infos/réponses dans des ressources.
- les phases 3 et 4 "{ref}`collecter` et {ref}`traiter`" sont les phases de collecte et de traitement des données. On s'attache à bien associer des métadonnées sur les données collectées. On insiste sur l'importance des standards et normes dans les protocoles et les formats de données pour assurer l'interopérabilité et la réutilisabilité des données. On commence à se préoccuper du stockage et de la sauvegarde des données, et à les déposer sur des plateformes de gestion de données locales.
- la phase 5 "{ref}`analyser`" est une phase d'analyse dans laquelle on s'occupe de définir et mettre en place des chaines logicielles avec des méthodes et des outils d'analyse des données
- la phase 6 "{ref}`archiver`" rend compte de l'importance de préserver et archiver les données sur le long terme. On s'attarde a bien définir les termes, réfléchir aux données pertinentes à préserver et voir quelles solutions s'offrent à nous.
- la phase 7 "{ref}`publier`" est la phase finale permettant de diffuser les données correctement de manière interopérable à travers des catalogues de données, des thesaurus de mots clés fournissant une interopérabilité sémantique, des identifiants pérennes et des entrepôts de données, des datapaper.

Pour terminer, ce guide s’adresse ainsi à toute personne désireuse de se former à la gestion des données de la recherche et son objectif est d'aider le lecteur à analyser son besoin et trouver des solutions adaptées, voire se rapprocher des réseaux métiers qui les ont exprimées. Il est destiné à être évolutif et s'enrichira au fil du temps par les pratiques des réseaux métiers. 

Le lecteur est appelé à contribuer en faisant remonter ses modifications et références manquantes dans les sections "commentaires" prévues à cet effet dans chaque chapitre.