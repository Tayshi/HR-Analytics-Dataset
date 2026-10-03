# HR-Analytics-Dataset
Source : [Human Resources Data Set](https://www.kaggle.com/datasets/rhuebner/human-resources-data-set)\
Inspiration : [12 Projets Pour Devenir Data Analyst En 2026 - LeCoinStat](https://www.youtube.com/watch?v=_GAq4rECeDA)

**Problématique métier**
Une entreprise souhaite analyser la répartition des performances des employés pour comprendre les écarts et identifier les outliers.

**Objectif**
Étudier les distributions des scores de performance et des heures travaillées pour détecter les facteurs d'amélioration.


## Manipulation des données.

Question de confidentialité, on a supprimé les colonnes contenant des coordonnées, leur identifiant (ID) est suffisant.\
Pour voir plus clair, on a mit un 2e visuel pour mettre de côté les colonnes ID.\
Dans le nettoyage de données, les colonnes "Date" ont été converti, pour nos futurs calculs. Les valeurs manquantes ne concernent que ceux encore présent en entreprise (Pas de date de départ ni de raison de départ)

Une nouvelle colonne est crée pour calculer l'ancienneté des employés avec leur date de recrutement jusqu'à aujourd'hui.

## Statistiques descriptives : Moyenne, médiane, mode, quartiles, variance, écart-type.

Les différentes statistiques sont calculés sur base des 207 salariés toujours actifs.

_Ancienneté_\
La moyenne étant proche de la médiane, on peut déduire une distribution normale (Une bonne répartition de l'ancienneté en entreprise).\
Ca se justifie mieux avec le mode ayant la même valeur, qui représente les valeurs qui ressortent le plus dans la base de données.\
Quartiles, 25% (50 personnes) des employés ont moins de 11 ans d'ancienneté. Et 75% (150 personnes) ont moins de 14 ans.\
Ecart-type faible, les valeurs ne sont pas tant dispersées que ça. Pour exemple en moyenne, il y aurait maximum 2 ans de différence d'ancienneté entre les 2.

**Détection et analyse des outliers avec la règle des 1.5 * IQR.**\
En étudiant les bornes, ceux en dessous de 6.5 et au dessus de 18.5 sont atypiques. Mais dans le contexte, on peut avoir de nouveau arrivants, et quelques anciens, donc pas un soucis.

_Score_\
Les statistiques ne renvoit point un problème flagrant en étudiant les valeurs.\
On pourrait pousser l'étude sur les centiles, mais on pourra voir les valeurs dans la partie visualisations.

## Visualisation des distributions : 

_Ancienneté_\
> Histogrammes : \
Illustrant notre déduction, on a affaire à une distribution normale à première vue.

_Score_\
> Pie chart : Un aperçu sur la répartition des salariés actifs.\
Sur les 207, on a 8% (16) en PIP et Needs Improvement. Données étant explicite, l'entreprise a dû déjà se pencher sur le sujet.

_Score & Ancienneté_\
> Boxplots : \
En distinguant les outliers, exemple côté PIP, on peut déduire des ordres de priorités sur les employés à revoir, en fonction de l'ancienneté.

> Scatterplot :\
On peut avoir le détail des priorités là-dessus, et l'effectif par année.\
On pourra garder en visuel que les 2 dernièrs critères de score, ordonnés par ancienneté.