# Analyse exploratoire des données Spotify — 2023

## 1. Présentation du projet

Ce projet porte sur l'analyse exploratoire de données musicales associées à Spotify en 2023. Il a pour objectif d'exploiter Python et ses bibliothèques d'analyse de données afin de nettoyer, préparer, explorer et visualiser un jeu de données.

L'analyse permet d'étudier différentes caractéristiques des données musicales, notamment la popularité, la durée et la répartition des sorties selon les variables disponibles.

Ce travail s'inscrit dans le cadre de ma formation en Data et Intelligence Artificielle et met en pratique les principales étapes d'un projet d'analyse de données.

## 2. Objectifs

Les objectifs du projet sont les suivants :

- Comprendre la structure et les caractéristiques du jeu de données.
- Identifier et traiter les valeurs manquantes et les données incohérentes.
- Préparer un jeu de données exploitable pour l'analyse.
- Réaliser une analyse exploratoire des données (EDA).
- Étudier les distributions et les relations entre les variables.
- Créer des visualisations permettant de mettre en évidence les principales tendances.
- Présenter les résultats de manière claire et structurée.

## 3. Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Python | Langage de programmation |
| Pandas | Manipulation et nettoyage des données |
| NumPy | Calculs numériques |
| Matplotlib | Création de graphiques |
| Seaborn | Visualisation statistique |
| Jupyter Notebook | Développement et documentation des analyses |
| Git et GitHub | Gestion des versions et hébergement du projet |

## 4. Structure du projet

```text
spotify-analysis-2026/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 02_nettoyage.ipynb
│   └── 03_analyse.ipynb
├── figures/
├── requirements.txt
├── .gitignore
└── README.md
```

Le dossier `data/raw/` est destiné aux données brutes, tandis que `data/processed/` contient les données préparées après nettoyage.

Le dossier `notebooks/` regroupe les notebooks consacrés au nettoyage et à l'analyse exploratoire. Les visualisations exportées peuvent être conservées dans le dossier `figures/`.

Les fichiers CSV volumineux ne sont pas inclus dans le dépôt GitHub. Ils doivent être téléchargés et placés localement avant l'exécution des notebooks.

## 5. Source des données

Le projet s'appuie sur un jeu de données musical associé à Spotify en 2023.

- Dataset Kaggle : [Most Streamed Spotify Songs 2023](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023)
- Notebook Kaggle de référence : [Most Streamed Spotify Songs 2023 — Adham Tarek](https://www.kaggle.com/code/adhamtarek147/most-streamed-spotify-songs-2023)

Le fichier utilisé localement est nommé `spotify-albums_data_2023.csv`.

Pour reproduire le projet, téléchargez le fichier correspondant depuis la source et placez-le dans le dossier `data/raw/`.

**Remarque :** le nom du fichier local et le titre du dataset Kaggle ne sont pas identiques. Il convient de vérifier que le fichier téléchargé correspond bien aux données utilisées dans les notebooks.

## 6. Nettoyage et préparation des données

Le notebook `02_nettoyage.ipynb` est consacré à la préparation du jeu de données.

Les opérations effectuées comprennent notamment :

- L'examen de la structure initiale des données.
- L'identification des valeurs manquantes.
- La recherche de données incohérentes.
- Le traitement des durées invalides.
- La suppression des colonnes entièrement vides ou non pertinentes pour l'analyse.
- Le traitement des lignes dont la date de sortie est manquante, selon les besoins de l'analyse.
- La sélection et la préparation des variables.
- L'exportation du jeu de données nettoyé au format CSV.

Le fichier préparé est enregistré sous le nom :

`data/processed/spotify_albums_clean.csv`

Lors du traitement, le jeu de données initial comportait environ 438 973 lignes et 26 colonnes. Après nettoyage, le fichier obtenu comportait environ 438 948 lignes et 20 colonnes.

Ces dimensions correspondent aux résultats observés au cours du nettoyage.

## 7. Analyse exploratoire des données

Le notebook `03_analyse.ipynb` présente l'exploration du jeu de données préparé.

L'analyse vise à mieux comprendre les caractéristiques des données et à identifier des tendances descriptives à partir des variables disponibles.

Les axes d'analyse comprennent notamment :

- L'étude de la distribution des variables numériques.
- L'analyse de la popularité des titres.
- La comparaison des durées selon les catégories disponibles.
- L'étude de l'évolution des sorties musicales dans le temps.
- L'identification des artistes les plus représentés, lorsque les données le permettent.
- L'exploration des relations entre différentes variables.

Les observations sont appuyées par des statistiques descriptives et des visualisations. Les conclusions détaillées doivent être interprétées à partir des résultats effectivement présentés dans le notebook.

## 8. Visualisation des données

Les visualisations permettent de faciliter la compréhension des résultats et de comparer les différentes caractéristiques du jeu de données.

Les graphiques réalisés dans le cadre du projet portent notamment sur :

- L'évolution des sorties musicales au fil du temps.
- La comparaison de la durée moyenne selon le type d'album.
- La comparaison de la popularité moyenne entre différentes catégories.
- La représentation des artistes les plus présents dans le jeu de données.
- La distribution des variables numériques.

Les graphiques sont réalisés à l'aide de Matplotlib et Seaborn. Les figures exportées sont conservées dans le dossier `figures/`, lorsqu'elles sont enregistrées.

## 9. Installation et exécution

### Prérequis

- Python installé sur l'ordinateur.
- Git.
- Jupyter Notebook.
- Les données nécessaires à l'exécution des notebooks.

### Étape 1 : Cloner le dépôt

```bash
git clone https://github.com/linatalmat/spotify-analysis-2026.git
cd spotify-analysis-2026
```

### Étape 2 : Créer un environnement virtuel

Sous Windows :

```bash
python -m venv .venv
```

Activer l'environnement dans PowerShell :

```powershell
.\.venv\Scripts\Activate.ps1
```

### Étape 3 : Installer les dépendances

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Si certaines bibliothèques nécessaires ne sont pas présentes dans `requirements.txt`, elles peuvent être installées avec :

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Étape 4 : Ajouter les données

Téléchargez le fichier CSV depuis la source Kaggle indiquée précédemment et placez-le dans le dossier `data/raw/`.

Vérifiez que le nom du fichier et son emplacement correspondent aux chemins utilisés dans le notebook de nettoyage.

### Étape 5 : Exécuter les notebooks

Lancer Jupyter Notebook :

```bash
python -m jupyter notebook
```

Exécutez les notebooks dans l'ordre suivant :

1. `notebooks/02_nettoyage.ipynb`
2. `notebooks/03_analyse.ipynb`

Le notebook de nettoyage doit être exécuté en premier afin de produire le fichier préparé utilisé pour l'analyse exploratoire.

## 10. Limites du projet

Cette analyse présente plusieurs limites :

- La qualité des résultats dépend de la qualité et de la couverture du jeu de données.
- Les variables disponibles ne permettent pas nécessairement d'expliquer l'ensemble des facteurs influençant le succès d'un titre.
- Les relations observées sont descriptives et ne démontrent pas, à elles seules, un lien de causalité.
- Les résultats dépendent de la période et des caractéristiques représentées dans le dataset.
- La reproduction de l'analyse nécessite de disposer du fichier CSV correspondant.

## 11. Perspectives d'amélioration

Plusieurs évolutions pourraient enrichir ce projet :

- Développer un tableau de bord interactif avec Power BI.
- Créer une application de visualisation avec Streamlit.
- Approfondir l'analyse statistique des caractéristiques musicales.
- Comparer les tendances entre plusieurs périodes.
- Enrichir le jeu de données avec d'autres sources musicales.
- Ajouter des indicateurs permettant de faciliter la comparaison des titres et des artistes.

## 12. Compétences mobilisées

Ce projet m'a permis de mettre en pratique les compétences suivantes :

- Analyse exploratoire de données.
- Nettoyage et préparation de données avec Pandas.
- Manipulation de données numériques avec NumPy.
- Visualisation de données avec Matplotlib et Seaborn.
- Utilisation de Jupyter Notebook.
- Organisation d'un projet Python.
- Gestion de versions avec Git et GitHub.
- Documentation et communication des résultats.

## 13. Conclusion

Ce projet met en application les principales étapes d'un processus d'analyse de données, depuis la préparation du jeu de données jusqu'à l'exploration et la visualisation des résultats.

Il m'a permis de développer ma pratique de Python et de ses bibliothèques d'analyse, tout en renforçant ma compréhension de la qualité des données et de l'interprétation des résultats.

Le projet constitue une base qui pourra être enrichie par des analyses complémentaires et des outils de visualisation interactifs.
