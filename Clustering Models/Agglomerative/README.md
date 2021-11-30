# Agglomerative Clustering

- Applied hierarchical-clustering technique of **Agglomerative Clustering** to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Vectorizers used : 

        1. Average W2V (Word2Vec)
        2. TFIDF W2V

##
-  ## STEPS (after preprocessing): 
    1) In order to find the optimal number of clusters ,plot a **dendrogram** for the model.

    2) Also, print the **cophenetic correlation** value for the model.

    2) Next apply sklearn Agglomerative-Clustering with the obtained best value of clusters.

    3) Now, perform cluster analysis by adding a new column 'Cluster_number' to the original dataframe.

    4) Also, plot a barplot showing the number of reviews in each cluster.
    
    5) Finally, plot wordclouds for each of the cluster. 

    6) Repeat this process for each model.

    7) Now, get the mean Silhouette-Score for each of the models.

    7) At the end, compare the models using **Silhouette Score** as the comparision-factor .

## 
- ## Terms definition : 
    1. **Dendrogram** : It s a type of tree diagram showing hierarchical clustering — relationships between similar sets of data.

    2. **Cophenetic Correlation** : It is a measure of how faithfully a dendrogram preserves the pairwise distances between the original unmodeled data points.

    3. **Silhouette Score** : The silhouette score for a data point measures how similar it is to its assigned cluster from -1 (dissimilar) to 1 (similar).
        - Calculating the mean silhouette coefficient provides for a simple scoring method of a given clustering.

        - Its analysis is as follows :

            - +1 Score −> Near +1 Silhouette score indicates that the sample is far away from its neighboring cluster.

            -  0 Score −> 0 Silhouette score indicates that the sample is on or very close to the decision boundary separating two neighboring clusters.

            - -1 Score −> -1 Silhouette score indicates that the samples have been assigned to the wrong clusters.


## 
## Dendrogram Theory : 
- Whenever two clusters are merged, we join them in the dendrogram and the height of the join will be the distance between these points. 

- More the distance of the vertical lines in the dendrogram, more the distance between those clusters.

- Threshold : 
    - We can set a threshold distance and draw a horizontal line.
    - Generally, the threshold is selected in such a way that it cuts the tallest vertical line in the dendrogram. 

- The number of clusters will be the number of vertical lines which are being intersected by the horizontal line drawn using the threshold. 


- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


