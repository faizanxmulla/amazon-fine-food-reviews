# KMeans Clustering

- Applied clustering technique of **KMeans** to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Also performed hyperparameter tuning, where the considered hyperparameter was :
        
          n_clusters (k)


- Vectorizers used : 

        1. BoW (Bag of Words)
        2. TFIDF (term frequency–inverse document frequency)
        3. Average W2V (Word2Vec)
        4. TFIDF W2V

##
-  ## STEPS (after preprocessing): 
    1) In each model, find the best ‘k’ using the elbow-knee method (plot k vs inertia_).

    2) After hyperparameter tuning ,apply sklearn KMeans with the best value of 'k'.

    3) Now, perform cluster analysis by adding a new column 'Cluster_number' to the original dataframe.

    4) Also, plot a barplot showing the number of reviews in each cluster.
    
    5) Finally, plot wordclouds for each of the cluster. 

    6) Repeat this process for each model.

    7) Now, get the mean Silhouette-Score for each of the models.

    7) At the end, compare the models using **Inertia** or **Silhouette Score** as the comparision-factor .

## 
- ## Terms definition : 
    1. **Inertia** : It is the sum of distances of all the points within a cluster from the centroid of that cluster. The lesser the inertia value, the better the clusters are.

    2. **Silhouette Score** : The silhouette score for a data point measures how similar it is to its assigned cluster from -1 (dissimilar) to 1 (similar).
        - Calculating the mean silhouette coefficient provides for a simple scoring method of a given clustering.

        - Its analysis is as follows :

            - +1 Score −> Near +1 Silhouette score indicates that the sample is far away from its neighboring cluster.

            -  0 Score −> 0 Silhouette score indicates that the sample is on or very close to the decision boundary separating two neighboring clusters.

            - -1 Score −> -1 Silhouette score indicates that the samples have been assigned to the wrong clusters.


- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


