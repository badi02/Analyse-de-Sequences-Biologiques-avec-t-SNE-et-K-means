# Analyse-de-S-quences-Biologiques-avec-t-SNE-et-K-means
Ce projet effectue plusieurs étapes pour analyser les données extraites du fichier CSV "uniprot.csv" et effectuer une réduction de dimensionnalité avec t-SNE suivi d'une classification des données avec l'algorithme K-means.

# Chargement des données:
Le code commence par charger les données à partir du fichier CSV et affiche les cinq premières lignes.

# Calcul du nombre unique d'espèces:
Il détermine le nombre unique d'espèces dans la colonne 'Species' et l'affiche. Dans cet exemple, le résultat est 770.

# Affichage de la forme des données:
Il affiche la forme du DataFrame après avoir sélectionné uniquement les colonnes 'ID' et 'Sequence'. Dans cet exemple, il y a 17166 lignes et 2 colonnes.

# Création de n-grammes:
Une fonction ngrams est définie pour générer des n-grammes à partir de la séquence de chaque ligne, puis une nouvelle colonne 'Features' est créée en appliquant cette fonction.

# Vectorisation des features:
Utilisation de CountVectorizer pour convertir les séquences de features en vecteurs numériques. La taille du vocabulaire est affichée (8780 dans cet exemple).

# Transformation en tableau NumPy
Les données vectorisées sont converties en un tableau NumPy, puis transformées en DataFrame pour une meilleure lisibilité.

# Statistiques sur les données vectorisées:
Il affiche la somme totale des valeurs dans le DataFrame, la somme minimale, la valeur minimale et la valeur maximale.

# Standardisation des données:
Les données sont standardisées à l'aide de StandardScaler pour les préparer à l'analyse de cluster.

# Imputation des valeurs manquantes:
Les valeurs manquantes sont imputées en remplaçant les NaN par la moyenne de chaque colonne.

# Réduction de dimension avec t-SNE:
Le code applique l'algorithme t-SNE pour réduire la dimension des données à deux composants.

# Application de K-means:
K-means est utilisé pour regrouper les données réduites en clusters.

# Visualisation des résultats:
Les résultats de t-SNE et de K-means sont combinés, puis une visualisation en nuage de points est créée avec des couleurs représentant les clusters.

# Visualisation par clusters:
Le code divise les clusters en groupes plus petits (ici, 10 clusters par figure) et génère des visualisations distinctes pour chaque groupe de clusters.
