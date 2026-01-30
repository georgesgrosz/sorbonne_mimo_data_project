## Introduction
Le sujet du projet est l'étude de la base de données annuelle des accidents corporels de la circulation routière. On se cncentre sur les années 2005 à 2018.
Cette base de données comporte les informations sur chaque accident corporel qui a eu lieu en France sur la période. La saisie des informations décrivant l’accident est effectuée par l’unité des forces de l’ordre (police, gendarmerie, etc.) qui est intervenue sur le lieu de l’accident. Ces saisies sont rassemblées dans une fiche intitulée Bulletin d’Analyse des Accidents Corporels. L’ensemble de ces fiches constitue le fichier national des accidents corporels de la circulation dit « Fichier BAAC » administré par l’Observatoire national interministériel de la sécurité routière "ONISR".

Ces données répertorient l'intégralité des accidents corporels de la circulation, intervenus durant une année précise en France métropolitaine, dans les départements d’Outre-mer (Guadeloupe, Guyane, Martinique, La Réunion et Mayotte depuis 2012) avec une description simplifiée. Cela comprend des informations de localisation de l’accident, telles que renseignées ainsi que des informations concernant les caractéristiques de l’accident et son lieu, les véhicules impliqués et leurs victimes.

## Constitution des groupes
Les groupes sont formés de deux personnes. Pour chaque groupe, les années étudiées sont les suivantes :
Groupe 1 : années 2005 à 2010 incluses
Groupe 2 : années 2009 à 2014 incluses
Groupe 3 : années 2013 à 2018 incluses

## Pré-requis

Avant de répondre aux questions du projet Data, il est conseillé de lire le fichier `description-des-bases-de-donnees-annuelles.pdf` qui décrit les différentes tables et leur contenu.
Il faut se rendre sur https://www.data.gouv.fr/fr/datasets/base-de-donnees-accidents-corporels-de-la-circulation/
 et télécharger les fichiers correspondants aux années assignées à votre groupe projet dans un répertoire "Données" à créer.
Plus précisement pour chacune des années de la période étudiée, il faut télécharger les fichiers
- caracteristiques
- lieux
- vehicules
- usagers

Important : Dans votre dossier devra figurer l'outil utilisé avec sa version et les années étudiées.
Les points "Bonus" sont facultatifs.

Pour toutes les questions ci-dessous, les réponses attendues doivent avoir le format suivant : 
1 - Prompt utilisé, 
2 - Code Python produit (quand applicable), 
3 - Résultat de l'exécution du code Python (quand applicable) 
4 - Solution proposée ou commentaires sur les corrections/ajustements/itérations réalisés.

##
## Questions 1 - Caractéristiques de l'accident
##

## Question 1.1
Lire tous les fichiers `caracteristiques_20xx.csv` qui se trouvent dans le répertoire "Données" et pour chacun d'eux, afficher les 5 premières lignes,  la taille du fichier, le nombre de colonnes et le nombre de lignes.

Bonus : Créer un tableau de synthèse avec pour chaque fichier, la taille du fichier, le nombre de colonnes et le nombre de lignes et une dernière ligne qui cumule chaque colonne.

## Question 1.2
En se basant sur le fichier attaché `description-des-bases-de-donnees-annuelles.pdf`, écrire un programme Phyton qui transforme les données des fichiers `caracteristiques_20xx.csv` conformément à la description des différents champs.

Par exemple, le champ lum est décrit de la manière suivante:

```
lum
Lumière : conditions d’éclairage dans lesquelles l'accident s'est produit :
1 – Plein jour
2 – Crépuscule ou aube
3 – Nuit sans éclairage public
4 – Nuit avec éclairage public non allumé
5 – Nuit avec éclairage public allumé
```

Ainsi, la valeur 1 pour le champ lum doit être transformée en "Plein jour", la valeur 2 en "Crépuscule ou aube", etc. 

Appliquez l'ensemble des transformations nécessaires à chacun des fichiers `caracteristique_20xx.csv` pour les transformer conformément à la description des différents champs et générer un fichier nommé `caracteristiques_20xx_complet.csv` par année.

## Question 1.3
Afin d'identifier les erreurs de codage dans les fichiers sources, ajouter un journal des lignes ignorées par fichier (lignes pour lesquelles au moins une valeur n'a pas pu être transformée ou n'est pas renseignéee).

## Question 1.4
Afin d'analyser la pertinence des valeurs utilisées dans les attributs définis sur des domaines énumérés (par exemple lum), étudiez la répartition en % des valeurs pour tous les attributs énumérés et commenter. Commentez les résultats et approfondissez quand les % de valeurs hors domaine sont importants.

Analysez les données transformées `caracteristique_20xx.csv` des deux fichiers les plus récents traités et répondez aux questions suivantes:
## Question 1.5
Combien d'accidents cumulés ont eu lieu en sur ces deux annnées ?

## Question 1.6
Combien d'accidents ont eu lieu sur ces deux années en agglomération ?

## Question 1.7
Affichez le nombre d'accidents par critère de luminosité sur la période.

##
## Questions 2 - Lieux de l'accident
##

On s'intéresse maintenant aux fichier lieux_20xx.csv.
## Question 2.1
En vous basant sur le fichier `description-des-bases-de-donnees-annuelles.pdf`, transformer tous les fichiers `lieux-20xx.csv` pour la période étudiée conformément à la description des différents champs de manière analogue à ce qui estfait dans la question 1.2.

Basé sur les fichiers transformés `lieux_20xx.csv`, répondez aux questions suivantes:

## Question 2.2
Afin d'identifier les erreurs de codage dans les fichiers sources, ajouter un journal des lignes ignorées par fichier (lignes pour lesquelles au moins une valeur n'est pas présente dans les listes de valeurs prooposées dans la document `description-des-bases-de-donnees-annuelles.pdf`).

## Question 2.3
De manière analigue au point 1.4 et afin d'analyser la pertinence des valeurs utilisées dans les attributs définis sur des domaines énumérés (par exemple catr), étudiez la répartition en % des valeurs pour tous les attributs énumérés et commenter. Commentez les résultats et approfondissez quand les % de valeurs hors domaine sont importants. 

## Question 2.4
Combien d'accidents ont eu lieu sur autoroute par année et quel pourcentage cela représente par rapport à tous les accidents ?

## Question 2.5
En faisant le cumul sur toutes les années étudiées, affichez le nombre d'accidents par type de route.

## Question 2.6
Quel est l'état de surface le plus accidentogène par année avec le % associé ?

##
## Questions 3 - Véhicules de l'accident
##

## Question 3.1
De manière analogue au point 1.2 et en vous basant sur le fichier `description-des-bases-de-donnees-annuelles.pdf`, transformer les champs avec des valeurs énumérées (catv, obs, obsm, choc, manv, etc.) des fichiers `vehicules_20xx.csv` conformément à la description des différents champs.

## Question 3.2
Comment gérer les valeurs invalides dans le champ `occutc` (Nombre d’occupants) ?

Analysez les données transformées `vehicules-2024.csv` et répondez aux questions suivantes:

## Question 3.3
Quelle est la répartition des accidents par catégorie de véhicule ?

## Question 3.4
Combien d'accidents impliquent des deux-roues motorisés ?
## Question 3.5
Affichez la répartition par type de motorisation.


## Question 4 - Usagers de l'accident

De manière analogue au point 1.2 et en vous basant sur le fichier `description-des-bases-de-donnees-annuelles.pdf`, transformer les fichiers `usagers_20xx.csv` conformément à la description des différents champs.

Questions de preprocessing:
1. Comment calculer l'âge à partir de l'année de naissance (`an_nais`) ?
2. Comment gérer les valeurs manquantes dans les champs d'équipement de sécurité (secu1, secu2, secu3) ?
3. Quelles transformations sont nécessaires pour les champs catégoriels (catu, grav, sexe, trajet, etc.) ?

Analysez les données transformées `usagers-2024.csv` et répondez aux questions suivantes:
1. Quelle est la répartition des accidents par gravité ?
2. Combien d'usagers étaient des piétons ?
3. Affichez la répartition par catégorie d'usager (conducteur, passager, piéton).

## Question 6 - Jointure des données

Joindre les données transformées (silver) pour créer un dataset unifié (gold).

1. Quelles sont les clés de jointure entre les différentes tables ?
2. Quel type de jointure utiliser (inner, left, right, outer) et pourquoi ?
3. Combien d'enregistrements contient le dataset gold après jointure ?
4. Y a-t-il des incohérences ou des valeurs manquantes après la jointure ?

## Question 7 - Analyse des données (format Gold)

Analysez le dataset gold (après jointure) et répondez aux questions suivantes:

1. **Analyse temporelle:**
   - À quelles heures de la journée y a-t-il le plus d'accidents ?
   - Y a-t-il des jours de la semaine plus dangereux que d'autres ?
   - Quelle est l'évolution mensuelle des accidents en 2024 ?

2. **Analyse géographique:**
   - Quels sont les 10 départements avec le plus d'accidents ?
   - Quelle est la répartition des accidents entre agglomération et hors agglomération ?

3. **Analyse des usagers:**
   - Quelle est la gravité moyenne des accidents selon la catégorie d'usager ?
   - Y a-t-il une corrélation entre l'âge et la gravité de l'accident ?
   - Combien d'usagers portaient un équipement de sécurité au moment de l'accident ?

4. **Analyse des véhicules:**
   - Quelles catégories de véhicules sont impliquées dans les accidents les plus graves ?
   - Y a-t-il une relation entre le type de motorisation et la gravité de l'accident ?

5. **Analyse croisée:**
   - Quelle est la combinaison la plus fréquente entre type de route et catégorie de véhicule impliquée ?
   - Y a-t-il une relation entre les conditions atmosphériques et la gravité des accidents ?

## Question 8 - Afficher une carte

Générer une carte interactive affichant les accidents routiers avec le module `folium`.

1. Filtrer les accidents pour une zone géographique spécifique (par exemple, Paris ou un département).
2. Afficher les accidents sur une carte en utilisant les coordonnées latitude/longitude.
3. Colorer les points selon le critère de gravité de l'accident.
4. Ajouter des informations au survol (tooltip) avec les détails de l'accident.

**Exemple:** Afficher tous les accidents survenus à Paris en 2024, colorés par gravité.

## Question 9 - Pour aller plus loin

Utilisant `dagster`, créez un pipeline qui permet de traiter les données et de les stocker avec une approche médaillon:
- **Raw:** Données brutes téléchargées depuis data.gouv.fr
- **Silver:** Données transformées et nettoyées (une table par source)
- **Gold:** Données jointes et enrichies (dataset unifié)
- **Analytics:** Analyses et visualisations (cartes, statistiques, etc.)

Le pipeline doit inclure:
1. Téléchargement des données (raw)
2. Preprocessing de chaque source (silver)
3. Jointure des données (gold)
4. Génération des analyses et visualisations (analytics)
