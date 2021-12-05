
# Support Vector Machine (SVM)

- Applied various kernels of SVM to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Kernels used : 

         1. Linear SVM 
         2. RBF SVM (Radial-Basis-Function) 

- Also performed hyperparameter tuning, where the considered hyperparameters were :
        
         1. alpha in range [10^-4 to 10^4]
         2. penalty among 'l1'&'l2'

- Vectorizers used : 

        1. BoW (Bag of Words)
        2. TFIDF (term frequency–inverse document frequency)
        3. Average-W2V (Word2Vec)
        4. TFIDF-W2V


-  ## STEPS (after preprocessing): 
    1) First split the dataset into train, test & validation sets.

    2) Then apply sklearn-SGDClassifier (for linear-kernel) with hinge loss on each vectorizer for this model.

    3) In each model, find out the best hyperparameters .

    4) After hyperparameter tuning, find AUC on testdata & plot ROC curve for both train as well as test data. 
    
    5) Also visualize the confusion matrix with predicted and original labels of test data points ,using seaborn heatmaps.

    6) In case of linear kernel with BOW & TFIDF, print the top 10 best features for each of the positive and negative classes.

    6) Repeat this process for each model.

    7) Now for the sklearn-implementation of RBF kernel : 
        - reduce the number of dimensions (used sample size of 40K points)
        - repeat steps 3 to 5 for each model.

    7) At the end , compare the models using AUC as the comparision-factor .



- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


