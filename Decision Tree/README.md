
# Decision Tree


- Applied Decision Tree to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Also performed hyperparameter tuning, where the considered hyperparameters were :
        
         1. max_depth
         2. min_samples_split

- Vectorizers used : 

        1. BoW (Bag of Words)
        2. TFIDF (term frequency–inverse document frequency)
        3. Average W2V (Word2Vec)
        4. TFIDF W2V


-  ## STEPS (after preprocessing): 
    1) First split the dataset into train, test & validation sets.

    2) Then apply sklearn Decision Tree on each vectorizer for this model.

    3) For each model, find out the best hyperparameters (max_depth & min_samples_split).

    4) After hyperparameter tuning, find AUC on testdata & plot ROC curve for both train as well as test data. 
    
    5) Also visualize the confusion matrix with predicted and original labels of test data points ,using seaborn heatmaps.

    6) Finally, visualize the decision-trees of BoW & TFIDF using Graphviz.

    7) Repeat this process for each model.

    8) At the end , compare the models using AUC as the comparision-factor .



- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


