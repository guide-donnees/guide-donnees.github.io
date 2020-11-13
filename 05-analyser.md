(analyser)=
# Analyser


Derrière le terme "analyser" s'entend l'extraction de l'information des données le plus souvent par l'utilisation de puissance de calcul.
Cela recouvre de nombreux types de techniques (calcul intensif, traitement statistique, machine learning, visualisation ...), et nécessite également des plateformes adaptées.

Cette étape du cycle de vie de nombreuses données impose que ces données soient exploitables, c'est-à-dire bien organisées, dans des formats adaptés à l'analyse envisagée, de façon à pouvoir leur appliquer des traitements automatisés.

Plusieurs évènements récurrents, annuels ou bisannuels, auxquels participent activement les réseaux métiers, comme les 
[JCAD (Journées Calcul et Données)](http://www.france-grilles.fr/category/journees-jcad/), les [JDEV (Journées du DEVeloppement logiciel)](http://devlog.cnrs.fr/manifestations/start) par exemple, intègrent de nombreuses interventions sur ces différentes thématiques, allant de la description des plateformes aux outils disponibles, en passant par l'organisation des développements et la reproductibilité. Ils incluent aussi très souvent des retours d'expérience particulièrement riches.



## Plateformes de traitement de données

De nombreuses ressources sont disponibles, à différentes échelles, pour analyser et traiter des données.
De façon générale, on distingue :

- Les ressources de type calcul intensif ou HPC (High Performance Computing) organisée à l'échelle européenne (EuroHPC ou Tier 0), nationale (GENCI et les centres nationaux ou Tier 1) et régionale (mésocentres ou Tier 2),
- les ressources de type cloud (par exemple le cloud distribué de France Grille France Cloud),
- les ressources de type grille de calcul ou HTC (High Throughput Computing), par exemple l'infrastructure France Grille ou le Centre de Calcul de l'IN2P3.

Elles sont décrites dans une [page spécifique](10-infrastructures.md).

## Outils pour l'analyse des données

Il existe de très nombreux outils permettant d'analyser ses données, allant du langage de programmation au workflow de traitement en passant par les logiciels de visualisation ...

### Langages de programmation

Certains langages de programmation sont plus particulièrement utilisés pour l'analyse de données. En dehors du langage R spécifique aux statistiques et à la science des données, l'écosystème s'enrichit très rapidement :

- Python devient de plus en plus utilisé en science des données. Une [introduction sur le sujet](https://github.com/fran6w/IRMAR/blob/master/IRMAR.pdf) a été réalisée en décembre 2017 par Francis Wolinski (Société Yotta Conseil) dans le cadre d'une journée organisée par le réseau Calcul.

```{admonition} [Présentation et illustration de l’écosystème Python pour la data science](https://github.com/fran6w/IRMAR/blob/master/IRMAR.pdf)
:class: seealso
Francis Wolinski (Société Yotta Conseil) 
Journée Python et Data Science IRMAR Rennes - 2017
```

- Julia est un des langages qui prend de l'importance sur ce sujet. Plusieurs présentations qui lui sont consacrées apportent un éclairage intéressant :
	- Une [journée d'introduction au langage](https://calcul.math.cnrs.fr/2019-01-journee-julia.html) et à son utilisation en traitement de données aborde en particulier [le cadre des algorithmes Map/Reduce](https://calcul.math.cnrs.fr/attachments/spip/Documents/Journees/jan2019/julia_map_reduce.pdf), ainsi que [les performances du langage sous forme de benchmarks](https://plmlab.math.cnrs.fr/fabreges/julia-2019/-/blob/master/bench.pdf) .

Des retours d'expérience illustrent l'utilisation de ces outils :

Concernant les outils python, l'[utilisation de Dask à la place de job array](https://jcad2019.sciencesconf.org/data/20191009_JCAD2019TutoDaskJobArray.pdf) a été présentée lors des JCAD 2019 par Guillaume Eynard-Bontemps, CNES.



### Approches méthodologiques

L'analyse des données ne concerne pas uniquement les modèles statistiques. 
De nombreux domaines appliqués reposent sur l’analyse de données géométriques: médecine, neurosciences, sismique, météorologie, vision par ordinateur, apprentissage statistique. Cette variété d'applications se retrouve dans la forme, la qualité et la sémantique des données ainsi que dans la nature des problèmes mathématiques qu’elles posent. 
Une [école thématique a été consacrée à ce sujet en 2018](https://geomdata.sciencesconf.org/), à destination des non spécialistes.
Elle l'a abordé sous plusieurs angles :

- Analyse topologique de données,
- Anatomie computationnelle,
- Méthode d’évolution de front et fast marching,
- Méthodes variationnelles pour l’imagerie
  

 Outre les présentations, de nombreux TP ont été proposés avec la mise en œuvre pratique des algorithmes, dans le langage Python. 

 Un des enjeux de l'analyse de volumes de données de grandes tailles, multidimensionnelles concerne les méthodes de réduction de la dimension (classiques comme ACP, AFC, MDS, …) ou issues du « machine learning » (kernel PCA, …).
 Cette approche a été abordée lors d'une [école thématique qui a eu lieu en 2017](https://calcul.math.cnrs.fr/2017-09-anf-reduction-dimension.html).
 Cette formation, nécessitant des connaissances de base en calcul matriciel, a permis d'approfondir certaines des techniques matricielles (recherche de valeurs propres, décomposition en valeurs singulières), sur le plan à la fois théorique et pratique.

 On peut trouver un exemple d'[utilisation concrète de ce type de technique](https://jcad2018.sciencesconf.org/data/afranc_jcad_2018_vendredi.pdf) présenté lors des JCAD 2018 par Alain Franc, INRA, appliqué à la biologie.

 De façon un peu générale, toutes ces approches conduisent ou sont la base de certains pans de l'Intelligence Artificielle. De plus en plus d'évènements sont consacrés à ces technologies.

Une [introduction](https://indico.mathrice.fr/event/130/contribution/3/material/slides/0.pdf) sur cette thématique a été réalisée en 2018 dans le cadre des Journées Système du réseau ResInfo.
De même, le réseau SARI grenoblois a organisé une journée sur le sujet, avec une [présentation de Jean-Luc Parouty](https://sari.grenoble-inp.fr/lib/exe/fetch.php?media=theme:ia_deep_learning:ia_deep_learning:ia_machinelearning_pres20190606.pdf) particulièrement didactique.

Compte tenu de l'engouement engendré autour de l'IA, de nombreuses journées et conférences sont organisées sur le sujet. En particulier, il fait l'objet de sessions spéciales lors des Journées Développement (Jdev) de [2020](http://devlog.cnrs.fr/jdev2020/t8) et [2017](http://devlog.cnrs.fr/jdev2017/t7).

### Visualisation des données numériques

Un des outils d'analyse les plus utilisés est la visualisation des données. Cependant cette visualisation peut s'avérer particulièrement délicate dans le cadre de très gros volumes de données, et nécessite de s'appuyer sur des solutions techniques spécifiques.

 Dans le domaine des données numériques, plusieurs bibliothèques sont particulièrement adaptées aux données de grande taille, ainsi qu'à la visualisation in situ, c'est-à-dire en cours de calcul en ce qui concerne les données de simulation : VisIt et ParaView. Plusieurs interventions sur ce sujet ont été réalisées dans le cadre d'une [journée dédiée organisée en 2017 par le réseau Calcul](https://calcul.math.cnrs.fr/2017-12-atelier-visualisation.html) .

 De même, une [action de formation](  https://calcul.math.cnrs.fr/2016-11-anf-visu-data.html) a été complètement consacrée à ce sujet en 2016 par le réseau Calcul. Elle a en particulier abordé les bonnes pratiques concernant la production de données : formats d'archivage, technique d'analyse, cycle de vie ... ainsi que les outils de visualisation avancés (visualisation in situ, temps réel, web).

La visualisation des données est également au coeur des problématiques des utilisateurs du calcul intensif. Le projet européen PRACE sur le calcul intensif propose des formations spécifiques, en particulier sur les outils de la [visualisation scientifique](https://materials.prace-ri.eu/view/divisions/visualisation.html).




## Mettre en place des méthodes d'analyse et des chaînes logicielles
L'analyse des données peut nécessiter la mise en place d'un workflow de traitement utilisant des chaînes logicielles. Il existe des environnements virtuels de recherche (VRE Virtual Research Environment) qui facilitent la mise en place de ces méthodes d'analyse complexes.

VIP, the Virtual Imaging Platform, est un portail qui permet à ses utilisateurs d'accéder simplement à leurs données, de les traiter facilement avec des logiciels préinstallés sur la plateforme. Traitements et données sont distribués sur l'infrastructure EGI. Pour répondre au besoin d'interopérabilité des données, l'API CARMIN est maintenant utilisée par VIP. Cette présentation explique les différentes étapes du fonctionnement du système mis en place. 

```{admonition} [VIP : towards data interoperability through CARMIN](https://jcad2019.sciencesconf.org/data/VIP_Axel_Bonnet.pdf), [vidéo](https://prismes.univ-toulouse.fr/player.php?code=vC6b9705) 
:class: seealso
Axel Bonnet, Pascal Wassong, Frederic Cervenansky, Camarasu-Pop Sorina, CREATIS et , Tristan Glatard, Concordia University
[JCAD 2019](https://jcad2019.sciencesconf.org)
```

```{admonition} [Virtual Imaging Platform](https://jcad2018.sciencesconf.org/data/VIP_poster.pdf)
:class: seealso
Sorina Camarasu-Pop, Axel Bonnet, Frédéric Cervenansky, CREATIS, Tristan Glatard, Concordia University
[JCAD 2018](https://jcad2018.sciencesconf.org)
```

Une autre plateforme, Pangeo, utilisée plus particulièrement dans la communauté géosciences a également été présentée lors des JCAD 2019 et 2018 :

```{admonition} [Analyse de simulations numériques de l’océan en préparation aux missions satellite : cas d’utilisation des outils PANGEO](https://jcad2019.sciencesconf.org/data/Briol_pangeo_swot_jcad2019_2019_10_10.pdf)
:class: seealso
A. Albert, F. Briol, L. Brodeau, G. Dibarboure, G. Eynard-Bontemps, J. Le Sommer, A. Ponte
[JCAD 2019](https://jcad2019.sciencesconf.org)
```

```{admonition} [Jupyter, Dask : traitement distribué simple et interactif en Python sur HPC avec l'écosystème Pangeo](https://jcad2018.sciencesconf.org/data/20181026_JCAD2018_CNES_GuillaumeEynard.pdf) 
:class: seealso
Guillaume Eynard-Bontemps, Centre National d'Etudes Spatiales
[JCAD 2018](https://jcad2018.sciencesconf.org)
```

D'autres environnements de management de workflow existent :

```{admonition} [WRENCH: Workflow Management System Simulation Workbench](https://jcad2018.sciencesconf.org/data/2018_010_23_JCAD_FSuter.pdf)
:class: seealso
Frederic Suter, Henri Casanova, Rafael Ferreira Da Silva, CC IN2P3
[JCAD 2018](https://jcad2018.sciencesconf.org)
```

Enfin, les environnements de notebooks sont des outils de plus en plus utilisés dans le cadre de l'analyse de données. Plusieurs interventions ont eu lieu sur ce sujet :

```{admonition} [Towards reproducible Jupyternotebooks](https://jcad2019.sciencesconf.org/data/talkLCourtes.pdf)
:class: seealso
Ludovic Courtès, INRIA
[JCAD 2019](https://jcad2019.sciencesconf.org)
```

```{admonition} [EGI Notebooks : Jupyter as a Service and EGI Check-In AAI](https://jcad2018.sciencesconf.org/data/EGI_Notebooks_et_Check_in_AAI.pdf)
:class: seealso
Baptiste Grenier, egi.eu
[JCAD 2018](https://jcad2018.sciencesconf.org)
```

```{admonition} [RomeoLAB, le portail web HPC : cas d'utilisation pour la pédagogie et les logiciels à la demande](https://jcad2018.sciencesconf.org/data/20181024_JCAD_romeolab.pdf)
:class: seealso
Arnaud RENARD, Université de Reims Champagne-Ardenne
[JCAD 2018](https://jcad2018.sciencesconf.org)
```

### Qualité logicielle

Ces chaînes de traitement sont très souvent associées à des instruments complexes et nécessitent ainsi de s’interfacer parfaitement avec le reste de l’instrument.
Dans ce contexte, il convient d'assurer le suivi des exigences liées au logiciel, la gestion des interfaces avec le reste de l’instrument et l’activité Assurance Qualité Logiciel. Cette dernière permet notamment de répondre à des exigences applicables à un logiciel, du développement à la maintenance de celui-ci.
L’ensemble des activités, normes, contrôles et procédures mis en place doit couvrir la totalité de la durée de vie d’un logiciel. Il est par exemple important de vérifier et valider au travers de tests la bonne santé du code et de constamment veiller à la traçabilité qui lui est liée.

Une [journée du réseau Qualité en Recherche](https://jt-aql.sciencesconf.org/) a été entièrement consacrée à ce sujet en 2019. Plusieurs exposés ont permis d'illustrer les concepts associés à la qualité logicielle :

```{admonition} [Qu'est-ce qu'un logiciel et qu'est-ce que la qualité ?](<https://jt-aql.sciencesconf.org/data/program/jt_aql_Paris_2019_v5_HV.pdf>)
:class: seealso
Henri VALEINS
```

```{admonition} [Plans de Gestion de Logiciel et Assurance Qualité Logiciel, les apports de PRESOFT](https://jt-aql.sciencesconf.org/data/program/PRESOFT_qualite_en_recherche2019v1_GR.pdf) 
:class: seealso
Geneviève Romier, CC IN2P3
```

```{admonition} [Référentiels et normes de codage](https://jt-aql.sciencesconf.org/data/program/ref_normes_codage_ZT.pdf) 
:class: seealso
Z.Tucsnak
```

```{admonition} [Qualité Logiciel dans un projet de Nanosatellite](https://jt-aql.sciencesconf.org/data/program/qualite_nanosat_v2_CG.pdf)
:class: seealso
Colin Gonzalez, AstroParticules et Cosmologie
```

  
### Retours d'expérience

Dans le domaine environnemental, les chaines logicielles sont également mises en place pour automatiser et ecnhaine un certain nombr de traitements comme :
- le contrôle qualité basé sur des paramètres physiques de l’instrument
- le contrôle qualité spécifique à un type d’instrument
- les corrections
- le filtrage
- les aggrégations
- le stockage en base de données

Plusieurs présentations issues des journées du réseau SIST illustrent des mises en oeuvre de chaîne logicielle d'analyse de données  :

```{admonition} [Filtrage interactif de données multidimensionnelles](https://sist16.sciencesconf.org/data/pages/08_P_Brockmann.pdf)  
:class: seealso
Patrick Brockmann, Laboratoire des Sciences du Climat et de l'Environnement   
[SIST 2016](https://sist16.sciencesconf.org/)    
```

```{admonition} [Chaînes de traitement en temps quasi réel des mesures de gaz à effet de serre du TGIR ICOS](https://sist18.sciencesconf.org/data/pages/07_L_Hazan_Chaines_de_traitement_ICOS.pdf)   
:class: seealso
Lynn Hazan, Laboratoire des Sciences du Climat et de l'Environnement   
[SIST 2018](https://sist18.sciencesconf.org/)   
```
    
```{admonition} [Vie d'une données sismologique de sa naissance sur le terrain jusqu'à sa distribution](https://sist18.sciencesconf.org/data/pages/08_D_Wolyniec_J_Schaeffer_Vie_d_une_donnees_sismologique.pdf)   
:class: seealso
David Wolyniec, OSU Grenoble - Jonathan Schaeffer, OSU Grenoble   
[SIST 2016](https://sist16.sciencesconf.org/)   
```

## Optimiser l'utilisation des ressources

L'analyse des données peut nécessiter l'usage de ressources assez massives en termes de puissance et de nombre, d'autant plus que la volumétrie des données a tendance à augmenter fortement.

Il est donc important de s'assurer d'optimiser l'utilisation de ces ressources. 

En particulier au niveau des codes de calcul, le réseau Calcul propose régulièrement des journées sur ces sujets :

```{admonition} [Une journée d'introduction à l'évaluation des performances des codes de calcul](https://indico.obspm.fr/event/60/)
:class: seealso
Observatoire de Paris, 2018
```

```{admonition} [Une formation sur l'évaluation de la performance des codes](https://calcul.math.cnrs.fr/2019-09-anf-perf-eval-hpc.html), en particulier à travers les outils Paraver et Scalasca.
:class: seealso
Observatoire de Haute Provence, 2019
```

Enfin, l'optimisation des ressources s'entend aussi au niveau environnemental, afin de réduire l'impact des analyses de données. Le [GDS EcoInfo](https://ecoinfo.cnrs.fr/)  a organisé en 2017 une [journée sur l'impact des logiciels sur l’environnement](https://ecoinfo.cnrs.fr/2017/01/05/conf-ecoinfo-3-fevrier-2017-impact-des-logiciels-sur-lenvironnement-quid-de-leco-conception/), dont certains exposés peuvent directement concerner la problématique de l'analyse des données :

```{admonition} [Écoconception logicielle, retours d’expérience sur la réduction de l’impact des logiciels](https://ecoinfo.cnrs.fr/wp-content/uploads/2017/01/greenspector.pdf)
:class: seealso
Olivier Philippot, GreenSpector
```

```{admonition} [TEEC: Logiciel vert et durable](https://gricad-media.univ-grenoble-alpes.fr/video/teec-logiciel-vert-et-durable)
:class: seealso
Hayri ACAR, Université Lyon 1
```

```{admonition} [Écoconception logicielle pour la gestion des datacentres de calcul](https://ecoinfo.cnrs.fr/wp-content/uploads/2017/01/ecoinfo-soft.pdf)
:class: seealso
Olivier Richard, LIG
```

```{admonition} [Calcul Intensif, Consommation et Changement Climatique](https://ecoinfo.cnrs.fr/wp-content/uploads/2017/01/20170203-Ecoconception.pdf)
:class: seealso
Xavier Vigouroux
```

```{admonition} [Eco-élasticité logicielle pour un Cloud frugal](https://ecoinfo.cnrs.fr/wp-content/uploads/2017/01/Eco-Info-3fev-PDF.pdf)
:class: seealso
Thomas Ledoux, Ecole des Mines de Nantes 
```

## Traitements sémantiques/ linguistiques

L’accroissement massif de la production scientifique (données et publications) et la multitude de canaux de diffusion existants appellent au cœur des activités de recherche, la mise en place de solutions informatiques permettant le repérage, l’extraction, l’exploration et l’analyse de corpus de données. Les méthodes et outils TDM (Text and Data Mining) apportent une aide importante pour explorer et analyser le sens des textes et en donner une représentation compréhensible par les humains et les machines.

En 2013, déjà le réseau Renatis avait accueilli Claire Nedellec et Agnès Girad (INRA)  pour illustrer l’usage possible des technologies sémantiques pour la gestion de l’information scientifique et technique ainsi que Fabien Amarger (IRIT IRSTEA) pour témoigner de la construction d’une base de connaissance partant d’un cas d’usage : l’annotation des Bulletins de Santé du Végétal 

Dans leur présentation, Claire Nedellec et Agnès Girard expliquent les **principes de l’analyse sémantique de texte** à travers un exemple en recherche documentaire et présentent le projet TirPhase.  La notion d’**indexation sémantique**  à travers un exemple en physiologie animale est abordée en début de présentation sous les traits d’une carte d’identité thématique associée au document.  Les auteurs présentent également la notion de **termino-ontologie** et définissent l’ontologie comme « un graphe où les nœuds sont des concepts et les arcs des relations entre ces concepts ». Elles expliquent que l’analyse sémantique identifie les unités sémantiques du texte et les associe aux concepts de l’ontologie. Partant de là, elle présente le **processus de conception de termino-ontologie** à partir de corpus en deux étapes : extraction automatique de termes avec l’outil Syntex et structuration et modélisation avec l’outil Protégé. La deuxième partie de la présentation est consacrée à la présentation du projet TriPhase. 
Ce projet a pour objectif d’**analyser les publications** d’un département de recherche à des fins stratégiques (analyse quantitative des termes au cours du temps) et disposer d’un moteur de recherche sémantique bibliographique spécialisé. Les auteurs expliquent les différentes phases de la construction de la termino-ontologie TriPhase et l’apport des documentalistes dans ce travail collaboratif.

Fabien Amarger, présente quant à lui un projet qui consiste à **construire une base de connaissance à partir de source et de données hétérogènes**. Il explique ce qu’est une base de connaissance et comment l’interroger.

```{admonition} [Des technologies sémantiques pour l’information scientifique et technique](http://renatis.cnrs.fr/IMG/pdf/Nedellec_Girard_Fredoc-v4.pdf)  
:class: seealso
Claire Nedellec, Agnès Girard, INRA  
Frédocs2013 - Gestion et valorisation des données de la recherche - 7 au 10 octobre 2013, Aussois   
```

```{admonition} [Annotation des Bulletins de santé du végétal (BSV) et interrogation](http://renatis.cnrs.fr/IMG/pdf/FreDoc_Irstea.pdf)  
:class: seealso
Fabien Amarger , IRIT-IRSTEA  
Frédocs2013 - Gestion et valorisation des données de la recherche - 7 au 10 octobre 2013, Aussois  
```

Plus récemment, Laurence El Khoury (DIST-CNRS) et Stéphane Schneider (INIST – CNRS) à l’occasion des Frédocs2018 ont présenté les projets [ISTEX](https://www.istex.fr/),  [VisaTM](https://objectif-tdm.inist.fr/2018/11/29/le-projet-visa-tm/) et [OpenMinteD](http://openminted.eu/) pour illustrer la mise à disposition d’une infrastructure de text-mining. 
ISTEX est une base documentaire qui propose un accès à distance et de manière pérenne à un corpus multidisciplinaire (plus de 23 millions de documents) en texte intégral. Cette base propose également des services permettant la mise en place de traitements des données : extraction, fouille de textes, production de synthèses documentaires. La première partie de l’intervention présente les objectifs, les ressources et les possibilités offertes par la plateforme. 
La seconde partie s’intéresse plus particulièrement à la fouille de texte et au projet VisaTM. Ce projet porté par l’INRA vise à étudier les conditions de production de services TDM à haute valeur ajoutée basés sur l’analyse sémantique à destination des chercheurs pour une généralisation des approches TDM dans les activités de recherche.
Le Projet européen H2020 OpenMinteD présenté en 3e partie est une e-infrastructure encourageant et facilitant l’utilisation des technologies de fouille de textes. Sa connexion à ISTEX permet l’exploration de corpus. Plateforme open source, ouverte et pérenne elle offre aux chercheurs la possibilité de découvrir, créer, partager et réutiliser des logiciels, des documents et des ressources pour le text-mining, le TALN, l’Extraction d’Information en travaillant à partir de sources documentaires licitement utilisables tels qu’ISTEX, OPENAIRE et CORE. 

```{admonition} [Bases de ressources numériques et services aux chercheurs. Avec ISTEX et OpenMintedD, l'alliance pour une infrastructure de text-mining]( https://fredoc2018.sciencesconf.org/data/pages/Pres_istex_visa_omtd_ElKhouri_Schneider.pdf)  
:class: seealso
Laurence El Khoury (DIST-CNRS), Stéphane Schneider (INIST – CNRS)  
Frédocs2018 - Démarches innovantes en IST : expérimenter, proposer (se) réinventer, 3-5 octobre 2018, Albi
```