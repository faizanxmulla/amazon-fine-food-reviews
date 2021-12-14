
# Truncated SVD

- Applied Truncated SVD (Singular Value Decomposition) to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).


- Vectorizers used : 

         TFIDF (term frequency–inverse document frequency)


-  ## STEPS : 
    1) First take the top 3000 features from the TFIDF vectorizers using idf_ score.

    2) Then calculate the co-occurence matrix.

    3) Now choose the n_components in Truncated SVD, with maximum explained variance. (also plot the plot of cumulative explained variance ratio)

    4) After Truncated-SVD, apply K-Means clustering and choose the best number of clusters based on the elbow curve.
    
    5) Print the wordclouds of each cluster.

    6) Finally, write a function that takes a word and returns the most similar words using cosine similarity, between the vectors.



- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


