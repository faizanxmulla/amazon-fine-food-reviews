
# Ensemble Models

- Applied ensemble techniques like Random-Forest & Gradient-Boosting Decision-Trees (GBDT) to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Also performed hyperparameter tuning, where the considered hyperparameters were :
        
         1. n_estimators 
         2. max_depth 

- Vectorizers used : 

        1. BoW (Bag of Words)
        2. TFIDF (term frequency–inverse document frequency)
        3. Average W2V (Word2Vec)
        4. TFIDF W2V


-  ## STEPS (after preprocessing): 
    1) First split the dataset into train, test & validation sets.

    2) Then apply sklearn-Random-Forest classifier on each vectorizer for this model.

    3) In each model, find out the best hyperparameter (max_depth and n_estimator) and then plot heatmaps for both train and validation data.

    4) After hyperparameter tuning, find AUC on testdata & plot ROC curve for both train as well as test data. 
    
    5) Also visualize the confusion matrix with predicted and original labels of test data points ,using seaborn heatmaps.

    6) Repeat this process for each model.

    7) For GBDT use the XGBoost library, and repeat the same steps performed in case of Random-Forest .

    8) At the end , compare the models using AUC as the comparision-factor .





- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


