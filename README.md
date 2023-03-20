# Data-Drift-Test

## Contexte du Projet
**La dérive en apprentissage automatique**, également appelée "drift de données", fait référence à un changement dans les données d'entrée d'un modèle d'apprentissage automatique au fil du temps. Ce changement peut être dû à différents facteurs tels que l'évolution des habitudes des utilisateurs, des changements dans les conditions environnementales, ou encore des erreurs dans les capteurs ou les dispositifs de collecte de données.

Lorsque les données d'entrée changent, le modèle qui a été entraîné sur des données antérieures peut perdre en précision et en fiabilité. Cela peut se traduire par une diminution de la performance du modèle, voire par une invalidation complète du modèle.

La dérive de données est un problème courant dans les applications d'apprentissage automatique en temps réel, comme la reconnaissance vocale, la détection de fraudes, ou encore la surveillance de la santé. Pour résoudre ce problème, il est nécessaire de mettre à jour régulièrement les données d'entraînement du modèle et de ré-entraîner le modèle sur ces nouvelles données.

Dans ce projet, on va implémenter des métriques permettant de mesurer la dérive d'un modèle dans un usecase de e-commerce.

## DATA
Le jeu de données est décomposé en 4 périodes correspondant aux 4 trimestres de l'année. On trouvere les données correspondant à chaque période dans les fichiers period_0.csv, period_1.csv, ..., period_3.csv.
chaque fichier contient les variables suivantes : 
* Target Variable * 
variable TotalCart : chiffre d'affaire total d'un client sur la période donnée

* Features *
Age : âge du client en années.

Seniority : ancienneté du client en années.

Orders : Nombre de commandes effectuées sur la période précédente.

Items : Nombre d'items commandés sur la période précédente.

AverageDiscount : Réduction moyenne accordée au client sur la période précédente en pourcentage.

TopCategory : Catégorie de produits favorite du client.

BrowsingTime : Temps total passé sur le site web sur la période précédente en secondes.

EmailsOpened : Nombre de mails marketing ouverts par le client sur la période précédente.

SupportInteractions : Nombre d'interactions que le client a eu avec le service client sur la période précédente.

## Contenu

*Notebook (Python)*

Le fichier contient 4 parties:
- 1er Partie : 
  - Entrainement et évaluation de 3 modéles sur les données de la période 0.
    -  Random Forest Regressor
    -   Gradient Boosting Regressor
    -    Rinear Regression.
  - Analyse de Performance de chaque modéle.
- 2eme Partie : 
  - Entrainement de Gradient Boosting Regressor sur toute la période 0.
  - Test de ce modéle sur les données des périodes 1, 2 et 3. 
  - Analyse de resultats
- 3eme Partie : 
  - Définition et Implementation de metrics pour explorer les caractéristiques des données et de détecter une possible dérive.
    - Divergence de Kullback–Leibler : mesure la différence entre deux distributions de probabilité
    - Divergence de Jensen-Shannon : mesure la similarité entre deux distributions.
    - Distance de Wasserstein : mesure la dissimilarité entre deux distributions de probabilité en mesurant la quantité de "travail" nécessaire pour transformer une distribution en une autre.
- 4eme Partie : 
  - Étude de la dérive du modèle en s'appuyant sur les métriques définies précédemment.
  - Analyse des resultats.

    



