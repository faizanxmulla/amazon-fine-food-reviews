
# Naive Bayes

- Applied Multinomial Naive-Bayes to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Also performed hyperparameter tuning, where the considered hyperparameter was:
        
          Alpha 
          - Considered a wide range of alpha values, starting as low as 0.00001 .

- Vectorizers used : 

        1. BoW (Bag of Words)
        2. TFIDF (term frequency–inverse document frequency)


-  ## STEPS : 
    1) First split the dataset into train, test & validation sets.

    2) Then apply sklearn-Multinomial Naive-Bayes on each vectorizer for this model.

    3) In each model, find out the best hyperparameter (alpha) and then plot the misclassification-error v/s value of alpha graph.

    4) After hyperparameter tuning, find AUC on testdata & plot ROC curve for both train as well as test data. 
    
    5) Also visualize the confusion matrix with predicted and original labels of train and test data points ,using seaborn heatmaps.

    6) Finally, get the top 10 important features for both positive and negative classes separately.

    7) Repeat this process for each model.

    8) At the end , compare the models using AUC as the comparision-factor .





- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


