
# DBSCAN

- Applied clustering technique of **DBSCAN** (Density-Based Spatial Clustering of Applications with Noise) to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Also performed hyperparameter tuning, where the considered hyperparameter was :
        
          epsilon (local radius for expanding clusters)


- Vectorizers used : 

        1. Average W2V (Word2Vec)
        2. TFIDF W2V

##
-  ## STEPS (after preprocessing): 
    1) In each model, find the best value of **'epsilon'** using the K-distance graph (eps VS data-pts sorted by distance).

    2) After hyperparameter tuning ,apply sklearn DBSCAN with the obtained best value of epsilon.

    3) Now, perform cluster analysis by adding a new column 'Cluster_number' to the original dataframe.

    4) Also, plot a barplot showing the number of reviews in each cluster.
    
    5) Finally, plot wordclouds for each of the cluster. 

    6) Repeat this process for each model.

    7) Now, get the mean Silhouette-Score for each of the models.

    7) At the end, compare the models using **Silhouette Score** as the comparision-factor .

## 
- ## Terms definition : 
    1. **Epsilon** : The maximum distance two points can be from one another while still belonging to the same cluster.

    2. **Min_pts** : The fewest number of points required to form a cluster.
    
    2. **Silhouette Score** : The silhouette score for a data point measures how similar it is to its assigned cluster from -1 (dissimilar) to 1 (similar).
        - Calculating the mean silhouette coefficient provides for a simple scoring method of a given clustering.

        - Its analysis is as follows :

            - +1 Score −> Near +1 Silhouette score indicates that the sample is far away from its neighboring cluster.

            -  0 Score −> 0 Silhouette score indicates that the sample is on or very close to the decision boundary separating two neighboring clusters.

            - -1 Score −> -1 Silhouette score indicates that the samples have been assigned to the wrong clusters.


- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


