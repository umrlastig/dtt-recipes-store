# Recette

<!--
Merci de respecter la structure du document, et ne pas changer les titres.
Pensez à donner un nom distinctif à votre document, puis à l'inscrire dans l'index (INDEX.md) !
Remplacer les exemples par votre contenu, et laissez vides les rubriques que vous ne souhaitez pas remplir.
-->

- [Contexte](#contexte)
- [Acteurs / Partenaires](#acteurs-partenaires)
- [Identification des sources de données](#identification-des-sources-de-donnees)
- [Processus](#processus)
- [Problèmes](#problemes)
- [Utilisation des données ou du modèle numérique](#utilisation-des-donnees-ou-du-modele-numerique)
- [Recommandations](#recommandations)
- [Perspectives](#perspectives)
- [Annexes](#annexes)
- [Glossaire](#glossaire)
- [Annotations proposées](#annotations-proposees)

## Contexte

<!--
Exemple : Ce projet vise à #[stake: améliorer l'aménagement du réseau cyclable] dans la #[territory: ville de Loos-en-Gohelle]. Il est financé par le projet #[funding: CityFAB]. Une #[digital-model: représentation 3D de la ville dans Luanti] a été créée dans le but d'organiser une concertation citoyenne pour recueillir l'avis des citoyens sur plusieurs propositions d'aménagement.
-->


## Acteurs / Partenaires

<!--
Exemple : Théo SZANTO (*), #[profile: doctorant en géomatique au LASTIG], a joué le rôle d'#[role: ingénieur JNT]. Ses compétences mises en œuvre ont été #[skill: expert en données IGN] et #[skill: expert et développeur Luanti].

Mathilde XX, #[profile: membre de l'équipe municipale de Loos-en-Gohelle], #[role: ingénieure JNT]. #[skill: connaissance du territoire concerné], #[skill: informatique bureautique].

Rachid XX, #[profile: chercheur UGE sur la cyclabilité], #[role: aider à l'étude de cyclabilité].

Samuel XX, #[profile: référent local IGN], #[role: assistance à identifier données disponibles et à mutualiser les expérimentations avec d'autres acteurs].


(*) Théo SZANTO : <https://orcid.org/0009-0009-7714-935X>
-->


## Identification des sources de données

<!--
Exemple : Les données de base proviennent de la #[dataset: BD TOPO (*)] de l'IGN. Les couches utilisées sont les bâtiments, les routes, et les cours d'eau. #[documentation: L'outil bdtopoexplorer.ign.fr s'est montré utile pour comprendre les attributs disponibles, notamment sur les bâtiments].

Le #[dataset: Nuages de Points LiDAR HD (*)] également de l'IGN a servi pour le relief des toits et la végétation.


(*) identifiants associés (sur cartes.gouv.fr, data.europa.eu, wikidata) : 
- BD TOPO : <https://cartes.gouv.fr/rechercher-une-donnee/dataset/IGNF_BD-TOPO>, sameAs: <https://www.wikidata.org/wiki/Q2876973>
- LiDAR HD : <https://data.europa.eu/data/datasets/ignf_nuages-de-points-lidar-hd?locale=en>
-->


## Processus

<!--
Exemple : La première étape a été l'#[process: import des données BD TOPO]. Après téléchargement de #[input: la BD TOPO sur le département au format GeoPackage], #[tool: QGIS] a été utilisé pour extraire #[output: un GeoPackage sur la zone d'intérêt]. Des #[expertise: connaissances SIG de base] ont été nécessaires.

Ensuite, il a fallu #[process: extraction des points de végétation du nuage de points LiDAR HD]. Pour cela, une pipeline #[tool: PDAL] a été développée (voir annexe 1). Elle transforme les #[input: tuiles kilométriques LAZ classifiées] en #[output: un seul fichier LAZ avec seulement les classes de végétation]. Il a été nécessaire de maîtriser #[expertise: les pipelines PDAL] et #[expertise: la notation JSON].
-->


## Problèmes

<!--
Exemple : un problème d'#[problem: alignement des données] a été constaté entre les bâtiments de la #[dataset: BD TOPO] et le nuage de point #[dataset: LiDAR HD]. Pour combiner proprement les deux, #[solution : le logiciel #[tool: Roofer] a été utilisé].

Un problème de #[problem: qualité des données] concernant la #[dataset: BD TOPO] : l'attribut "materiaux_des_murs" n'était pas toujours rempli, rendant impossible son utilisation pour un rendu visuel. L'alternative a été d'#[solution: utiliser une palette symbolique selon l'attribut "usage_1"], lui obligatoire.

Ce problème a été difficile à diagnostiquer en raison d'une faible #[problem: qualité de la documentation], qui ne mentionnait pas les critères de remplissage de cet attribut, ou son taux de remplissage moyen. En conséquence, il a fallu #[solution: faire une analyse statistique sur les données] pour constater qu'environ 66% seulement possédaient une valeur pour cet attribut sur la zone d'étude.
-->


## Utilisation des données ou du modèle numérique

<!--
Exemple : Le modèle numérique produit s'utilise dans #[environment: Luanti]. Il représente la ville de Loos-en-Gohelle et permet à un utilisateur connaissant déjà le territoire de reconnaître les lieux, pour s'y repérer soit en vue immersive, soit en survol de la zone.
-->


## Recommandations




## Perspectives




## Annexes




## Glossaire

Terme | Définition et/ou lien(s)
--- | ---
terme 1 | définition 1...
terme 2 | définition 2...


## Annotations proposées

Annotation | Description
--- | ---
annotation 1 | description 1...
annotation 2 | description 2...

