PROJET D'ANALYSE DE DONNEE SPOTIFY :

1_ Presentation du projet 

ce projet consiste a analyser une dataset Spotify contenante es informations sur les morceux , les albums , ales artiste , leur popularite et leurs dates de sortie . 

L'objectif est d'explorer les donnees afin de mieux comprendre la repartition des morceaux selon les types d'albums, leur evolution au fil des annees et les caracteristiques des morceaux presents dans le dataset.

Ce projet a été realise dans le cadre d'un apprentissage de l'analyse de donnees avec Python et Pandas.



2_Objectif et question d'analyse : 
L'analyse cherche à répondre aux questions suivantes :

Quels types d'albums sont les plus représentés dans le dataset ?

Quel type d'album possède la popularité moyenne la plus élevée ?

Comment évolue le nombre de morceaux enregistrés selon leur année de sortie ?

Quels artistes sont les plus représentés dans le dataset ?

Quelle est la durée moyenne des morceaux selon le type d'album ?

3_ Technologies utilisées : 

Python  : langage utiliser pour lanalyse 
Pandas : vhargement nettoyage transforamtion et analyse des donnee
Matplotlib : creation des visualisation 
Jupyter : environnement de travail pour les analyses 


4_ Préparation et nettoyage des données

Le dataset a été inspecté afin de comprendre sa structure, ses colonnes et les types de données disponibles.

Les principales étapes du nettoyage ont consisté à :

Identifier les valeurs manquantes et les données invalides.

Vérifier et convertir les dates de sortie au format datetime.

Supprimer les durées invalides.

Supprimer les colonnes entièrement vides.

Traiter les lignes sans date de sortie exploitable pour les analyses temporelles.

5_ Analyse exploratoire

L'exploration a permis d'étudier plusieurs caractéristiques du dataset :

La répartition des types d'albums.

La popularité moyenne selon le type d'album.

Le nombre de morceaux par année.

Les sorties de morceaux entre 2000 et 2023.

Les artistes les plus représentés.

La durée moyenne des morceaux selon le type d'album.

Une jointure a également été réalisée avec une table de correspondance des types d'albums afin d'ajouter une description à chaque catégorie. Le nombre de lignes a été vérifié avant et après la jointure.

6_ Visualisations et résultats

Les graphiques ont été enregistrés dans le dossier figures.

Popularité moyenne selon le type d'album



Ce graphique compare la popularité moyenne des morceaux selon leur type d'album : album, single ou compilation.

8. Conclusions

L'analyse permet d'explorer la composition du dataset Spotify, les types d'albums les plus présents, la représentation des artistes et les caractéristiques temporelles des morceaux.

Les graphiques permettent de comparer les catégories et de repérer des tendances dans les données.

Les conclusions définitives doivent être complétées à partir des résultats numériques obtenus dans les notebooks, notamment pour identifier le type d'album le plus populaire et les périodes où le nombre de morceaux est le plus élevé.

8_ Limites de l'analyse

Les résultats dépendent du dataset utilisé et de la qualité des informations disponibles.

Les dates de sortie manquantes ou imprécises peuvent limiter l'analyse temporelle. De plus, le nombre de morceaux associés à un artiste ne représente pas nécessairement sa popularité réelle sur Spotify.

La popularité des morceaux peut également évoluer dans le temps. Les résultats décrivent donc les données présentes dans le dataset et ne permettent pas, à eux seuls, de tirer des conclusions sur l'ensemble du catalogue Spotify actuel.


9_ Installation et utilisation 


### 1. Cloner le projet

```bash
git clone https://github.com/linatalmat/spotify-analysis-2026.git
cd spotify-analysis-2026

//CREE UN ENVIRONNEMENT VIRTUEL //

python -m venv .venv

//ACTIVER LENV // 
.\.venv\Scripts\Activate.ps1

//INTALLER LES DEPENDACES //
pip install -r requirements.txt