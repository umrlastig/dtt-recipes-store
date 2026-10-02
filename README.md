# Recettes pour le JNT

Le concept de « jumeau numérique de territoire » (JNT) n'évoque pas toujours la même chose à tous. Ici, nous utilisons la définition suivante proche de celle d'un jumeau numérique : un modèle numérique d'un territoire et une relation bidirectionnelle entre le modèle et ce territoire qui permet d'une part d'améliorer ce modèle numérique à l'aide d'ajouts venant de la réalité (nouvelles données, nouveaux concepts) et d'autre part d'améliorer la réalité à l'aide de simulations et résultats venant du numérique. Le « modèle numérique » correspond au modèle virtuel qui décrit la réalité (par exemple, une maquette 3D).

Un enjeu auquel je m'intéresse est le partage de connaissances entre ceux qui mettent en œuvre des JNT, que ce soit pour construire à plusieurs un même JNT ou pour s'inspirer des expériences les uns des autres. Je propose un modèle qui permette de partager et réutiliser ces connaissances, sous forme de recettes plus ou moins complètes, que je vous invite à écrire. Ces recettes doivent donc être compréhensible par d'autres, et apporter une information utile.

Dans mon modèle, une recette se présente sous forme de rubriques. Une rubrique peut ne pas être renseignée si cela n'est pas pertinent dans votre cas. Pour la renseigner vous êtes invités à écrire un texte libre annoté. Concernant le contenu du texte, des éléments sont suggérés dans l'exemple. Concernant les annotations, certaines sont recommandées et il est possible d'en proposer de nouvelles, en les définissant dans le tableau en fin de recette. Lorsque vous indiquez la valeur d'une annotation, essayez dans la mesure du possible de vous raccrocher à des vocabulaires non ambigus en donnant des identifiants ou des URL. Enfin, lorsque dans votre texte vous employez un terme spécifique, essayez s'il vous plait d'inclure un identifiant
partagé s'il en existe un ou encore de proposer une définition que vous joignez en fin de recette.

Le but de cette expérimentation est d'évaluer la pertinence des rubriques, des annotations et des identifiants existants qui permettent de rendre vos recettes éditables et partageables.

## Comment contribuer ?

> [!NOTE]
> Si vous n'avez pas les droits d'accès sur ce dépôt, ou avez une question, vous pouvez ouvrir une [issue](issues) pour demander.
> 
> Si vous ne souhaitez pas utiliser GitHub pour contribuer, vous pouvez toujours suivre les instructions en conservant votre fichier sur votre ordinateur, puis me l'envoyer par mail une fois fini à l'adresse `theo(point)szanto(arobase)ign(point)fr`

Pour partager vos connaissances, créez une copie du fichier [`recipe.md`](recipe.md) à la racine de ce dépôt, puis remplissez-la en suivant les consignes décrites dans ce README (la description de chaque rubriqe et annotation se trouve ci-dessous).

> [!IMPORTANT]
> Merci de ne pas éditer directement le fichier `recipe.md` et de bien en faire une copie !!!
> Sinon, les suivants n'auront plus de modèle pour faire leur propre document.

Nommez votre document avec un nom distinctif suivi de l'extension `.md`, si possible en évitant les espaces et les caractères spéciaux / accentués (exemple : `recette-pour-visualisation-3d-dans-luanti.md`).

Ensuite, inscrivez votre recette dans l'[index des recettes](INDEX.md), avec un lien vers le document Markdown.

Merci !

---

# Rubriques et annotations d'une recette

- [Contexte](#contexte)
- [Acteurs / Partenaires](#acteurs--partenaires)
- [Identification des sources de données](#identification-des-sources-de-données)
- [Processus](#processus)
- [Problèmes](#problèmes)
- [Utilisation des données ou du modèle numérique](#utilisation-des-données-ou-du-modèle-numérique)
- [Recommandations](#recommandations)
- [Perspectives](#perspectives)
- [Annexes](#annexes)
- [Glossaire](#glossaire)
- [Annotations proposées](#annotations-proposées)

## Contexte

_Cette rubrique décrit les enjeux du monde réel et le modèle numérique envisagé._

**Annotations conseillées :**
- `stake` : Enjeu du monde réel que ce JNT veut adresser
- `territory` : Territoire concerné
- `funding` : Information sur le financement / projet
- `digital-model` : Type de modèle numérique visé

**Exemple :**
> Ce projet vise à #[stake: améliorer l'aménagement du réseau cyclable] dans la #[territory: ville de Loos-en-Gohelle]. Il est financé par le projet #[funding: CityFAB]. Une #[digital-model: représentation 3D de la ville dans Luanti] a été créée dans le but d'organiser une concertation citoyenne pour recueillir l'avis des citoyens sur plusieurs propositions d'aménagement.

## Acteurs / Partenaires

_Cette rubrique décrit des acteurs et partenaires impliqués dans le processus JNT, à quelque étape que ce soit._

**Annotations conseillées :**
- `profile` : Profil de l'acteur
- `role` : Rôle au sein de ce JNT (commanditaire, ingénieur…)
- `expertise` : Expertise(s) possédée(s) par l'acteur (aussi bien expertise locale que scientifique) qui sont utiles dans le cadre de ce JNT

**Exemple :**
> Théo SZANTO (*), #[profile: doctorant en géomatique au LASTIG], a joué le rôle d'#[role: ingénieur JNT]. Ses compétences mises en œuvre ont été #[skill: expert en données IGN] et #[skill: expert et développeur Luanti].
> 
> Mathilde XX, #[profile: membre de l'équipe municipale de Loos-en-Gohelle], #[role: ingénieure JNT]. #[skill: connaissance du territoire concerné], #[skill: informatique bureautique].
> 
> Rachid XX, #[profile: chercheur UGE sur la cyclabilité], #[role: aider à l'étude de cyclabilité].
> 
> Samuel XX, #[profile: référent local IGN], #[role: assistance à identifier données disponibles et à mutualiser les expérimentations avec d'autres acteurs].
> 
> 
> (*) Théo SZANTO : <https://orcid.org/0009-0009-7714-935X>

## Identification des sources de données

_Cette rubrique décrit le travail d'identification des sources de données considérées, en précisant si elles ont été retenues ou non, en identifiant bien les sources, en précisant éventuellement où est la documentation si elle a été utilisée ainsi que les métadonnées._

**Annotations conseillées :**
- `dataset` : données
- `documentation` : Usage de la documentation et des métadonnées (si possible avec lien)

**Exemple :**
> Les données de base proviennent de la #[dataset: BD TOPO (*)] de l'IGN. Les couches utilisées sont les bâtiments, les routes, et les cours d'eau. #[documentation: L'outil bdtopoexplorer.ign.fr s'est montré utile pour comprendre les attributs disponibles, notamment sur les bâtiments].
> 
> Le #[dataset: Nuages de Points LiDAR HD (*)] également de l'IGN a servi pour le relief des toits et la végétation.
> 
> 
> (*) identifiants associés (sur cartes.gouv.fr, data.europa.eu, wikidata) :
> - BD TOPO : <https://cartes.gouv.fr/rechercher-une-donnee/dataset/IGNF_BD-TOPO>, sameAs: <https://www.wikidata.org/wiki/Q2876973>
> - LiDAR HD : <https://data.europa.eu/data/datasets/ignf_nuages-de-points-lidar-hd?locale=en>

## Processus

_Cette rubrique décrit les étapes du processus, les traitements réalisés, sans viser l'exhaustivité, en utilisant au besoin des macro-tâches, et en cherchant à rentrer dans le détail quand cela semble important, par exemple pour décrire un traitement novateur de façon à aider à le reproduire._

**Annotations conseillées :**
- `process` : nom du traitement
- `tool` : Outil(s) utilisé(s) dans ce traitement
- `input` : Source(s) de données en entrée
- `output` : Résultat(s) en sortie
- `expertise` : Expertise(s) nécessaire(s) pour réaliser ce traitement

**Exemple :**
> La première étape a été l'#[process: import des données BD TOPO]. Après téléchargement de #[input: la BD TOPO sur le département au format GeoPackage], #[tool: QGIS] a été utilisé pour extraire #[output: un GeoPackage sur la zone d'intérêt]. Des #[expertise: connaissances SIG de base] ont été nécessaires.
> 
> Ensuite, il a fallu #[process: extraction des points de végétation du nuage de points LiDAR HD]. Pour cela, une pipeline #[tool: PDAL] a été développée (voir annexe 1). Elle transforme les #[input: tuiles kilométriques LAZ classifiées] en #[output: un seul fichier LAZ avec seulement les classes de végétation]. Il a été nécessaire de maîtriser #[expertise: les pipelines PDAL] et #[expertise: la notation JSON].

## Problèmes

_Cette rubrique décrit des problèmes rencontrés, sans viser l'exhaustivité, comme pour les traitements, mais plus en ciblant ceux qui semblent particulièrement utiles à partager et en décrivant les solutions qui ont été trouvées ou s'ils n'ont pas été résolus._

**Annotations conseillées :**
- `problem` : problème (manque de documentation…)
- `solution` : Solution mise en œuvre (si elle existe)

**Exemple :**
> Un problème d'#[problem: alignement des données] a été constaté entre les bâtiments de la #[dataset: BD TOPO] et le nuage de point #[dataset: LiDAR HD]. Pour combiner proprement les deux, #[solution : le logiciel #[tool: Roofer] a été utilisé].
> 
> Un problème de #[problem: qualité des données] concernant la #[dataset: BD TOPO] : l'attribut "materiaux_des_murs" n'était pas toujours rempli, rendantimpossible son utilisation pour un rendu visuel. L'alternative a été d'#[solution: utiliser une palette symbolique selon l'attribut "usage_1"], lui obligatoire.
> 
> Ce problème a été difficile à diagnostiquer en raison d'une faible #[problem: qualité de la documentation], qui ne mentionnait pas les critères de remplissage de cet attribut, ou son taux de remplissage moyen. En conséquence, il a fallu #[solution: faire une analyse statistique sur les données] pour constater qu'environ 66% seulement possédaient une valeur pour cet attribut sur la zone d'étude.

## Utilisation des données ou du modèle numérique

_Description de l'utilisation des résultats des traitements décrits précédemment, que ce soit le modèle numérique ou des données intermédiaires._

**Annotation conseillée :**
- `environnement` : Environnement logiciel

**Exemple :**
> Le modèle numérique produit s'utilise dans #[environment: Luanti]. Il représente la ville de Loos-en-Gohelle et permet à un utilisateur connaissant déjà le territoire de reconnaître les lieux, pour s'y repérer soit en vue immersive, soit en survol de la zone.

## Recommandations

_Conseils et recommandations relatifs au travail décrit dans cette recette, pièges à éviter, questions fréquentes posées au sein des acteurs et partenaires._

## Perspectives

_Évolutions futures possibles ou à venir._

## Annexes

_Liens vers des documents externes pour compléter les informations de la recette._

**Annotations conseillées :**
- `nature` : Nature de l'annexe (rapport, article scientifique, code…)
- `link` : Lien vers le document externe

