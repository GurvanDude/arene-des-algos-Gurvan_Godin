# Arène des Algos

Projet réalisé dans le cadre du cours de Machine Learning.

## Objectif

L'objectif de ce projet est de comparer plusieurs algorithmes de Machine Learning sur différents jeux de données afin d'observer leurs performances et leurs comportements.

Les expériences ont été réalisées sur :

* Breast Cancer Wisconsin
* Wine

## Algorithmes testés

* Régression Logistique
* K-Nearest Neighbors (KNN)
* Arbre de Décision
* KMeans (clustering non supervisé)

## Résultats sur Breast Cancer

Classement obtenu :

1. Régression Logistique
2. KNN
3. Arbre de Décision

Le dataset est relativement bien séparé et les trois modèles obtiennent de bonnes performances.

## Résultats sur Wine

Classement obtenu :

1. Régression Logistique : 100 %
2. Arbre de Décision : 94.44 %
3. KNN : 72.22 %

Le changement de dataset modifie le classement. Cela montre qu'un algorithme performant sur un problème n'est pas forcément le meilleur sur un autre.

## Clustering non supervisé

Un KMeans à 2 clusters a été appliqué sur le dataset Breast Cancer sans utiliser les étiquettes.

Les clusters obtenus correspondent globalement aux vraies classes, ce qui montre qu'une structure naturelle est présente dans les données.

## Impact du scaling

L'ajout d'un StandardScaler a eu des effets très différents selon les modèles :

| Algorithme            | Gain observé |
| --------------------- | ------------ |
| KNN                   | +22.22 %     |
| Régression Logistique | 0 %          |
| Arbre de Décision     | 0 %          |

KNN est l'algorithme qui bénéficie le plus du scaling car il repose directement sur le calcul de distances.

## Data Leakage

Une expérience de fuite de données a été réalisée en ajustant le scaler sur l'ensemble du dataset avant le découpage train/test.

Dans notre cas, aucune amélioration de score n'a été observée.

Cette expérience montre néanmoins qu'une fuite de données peut être difficile à détecter et doit toujours être évitée.

## Algorithme recommandé

Parmi les modèles testés, la Régression Logistique est celui qui offre les meilleurs résultats sur les deux datasets étudiés.

Elle présente également l'avantage d'être rapide à entraîner, simple à interpréter et très performante sur les données utilisées dans ce projet.

## Conclusion

Ce projet a permis de comparer plusieurs approches de classification, d'explorer le clustering non supervisé et d'étudier l'impact du scaling ainsi que les risques liés au data leakage.

Les résultats montrent qu'il est important de tester plusieurs modèles et de respecter une méthodologie rigoureuse avant de tirer des conclusions sur leurs performances.

