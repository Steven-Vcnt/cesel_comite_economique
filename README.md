# cesel_comite_economique

Etude comparative de l'insertion et de l'emploi des jeunes à partir de données publiques

## Méthodologie d’analyse

Les étapes suivantes ont été réalisées pour préparer et analyser les données socio-économiques des communes :

- **Chargement et nettoyage des données** : Les données brutes issues de l’INSEE ont été importées, puis filtrées pour exclure les communes ou colonnes ne respectant pas les critères de confidentialité ou contenant trop de valeurs manquantes.

- **Enrichissement des données** : Un mapping a été effectué pour associer chaque code commune à son libellé, puis une clé unique CITY_ID a été créée pour chaque commune.

- **Sélection des variables pertinentes** : Une analyse en composantes principales (PCA) a permis d’identifier les variables ayant le plus d’incidence sur la variabilité des données. Ces variables ont été sélectionnées pour la suite de l’analyse.

- **Préparation des features** : Un sous-ensemble de variables d’intérêt a été sélectionné manuellement pour constituer la table de features utilisée dans les analyses de similarité et de clustering.

- **Normalisation et réduction de dimension** : Les données ont été normalisées (StandardScaler), puis une réduction de dimension a été appliquée (PCA) pour faciliter les analyses de proximité et de clustering.

- **Recherche de villes similaires** : Un algorithme KNN a été utilisé sur les données réduites pour identifier les communes les plus similaires à Levallois-Perret.

- **Transformation des données pour l’analyse temporelle** :Les données ont été transformées au format long, puis pivotées pour obtenir un tableau où chaque ligne correspond à une commune et une catégorie, et chaque colonne à une année (2010, 2015, 2021). Une colonne supplémentaire a été calculée pour mesurer l’évolution entre 2015 et 2021.

- **Préparation pour l’export et la visualisation** : Les données finales ont été exportées pour une utilisation dans Power BI ou d’autres outils de visualisation.

- **Sources** : 
    - https://www.insee.fr/fr/statistiques/5359146#documentation
    - https://www.insee.fr/fr/metadonnees/source/operation/s2146/documentation-methodologique
