
# Logistic Regression


- Applied Logistic Regression to the Amazon-Fine-Food-Review dataset available on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

- Also performed hyperparameter tuning, where the considered hyperparameters were :
        
         1. penalty
         2. C (inverse of regularization strength)

- Vectorizers used : 

        1. BoW (Bag of Words)
        2. TFIDF (term frequency–inverse document frequency)
        3. Average W2V (Word2Vec)
        4. TFIDF W2V


-  ## STEPS (after preprocessing): 
    1) First split the dataset into train, test & validation sets.

    2) Then apply sklearn Logistic-Regression on each vectorizer for this model.

    3) In each model, find out the best hyperparameter (C and penalty).

    4) After hyperparameter tuning, find AUC on testdata & plot ROC curve for both train as well as test data. 
    
    5) Also visualize the confusion matrix with predicted and original labels of test data points ,using seaborn heatmaps.

    6) Now, perform perturbation test to check for multicollinearity.

    7) Then calculate sparsity on weight vector obtained after using L1 regularization.

    8) Finally, get the top 10 important features for both positive and negative classes separately.

    6) Repeat this process for each model.

    7) At the end , compare the models using AUC as the comparision-factor .


- ## Terms definition : 
    1. **Perturbation** : It means adding noise, usually to the training data but sometimes to the learnt parameters. It can help kick the model out of a local minimum, and acts in practice as a form of regularization.

    2. **Multicollinearity** : It occurs when two or more independent variables are highly correlated with one another in a regression model.


- ## Steps to perform perturbation-test : 
    1. Get the weights W after fitting the model with the data X.

    2. Add a noise to the X (X' = X + e) and get the new data set X' (if X is a sparse matrix, X.data+=e)

    3. Fit the model again on data X' and get the weights W'.

    4. Add a small eps value(to eliminate the divisible by zero error) to W and W’ i.e W=W+10^-6 and W’ = W’+10^-6

    1. Now find the % change between W and W' --> (| (W-W') / (W) |)*100)

    1. Calculate the 0th, 10th, 20th, 30th, ...100th percentiles, and observe any sudden rise in the values of percentage-change-vector.
    Ex: consider your 99th percentile is 9.3 and your 100th percentiles are 1054.6, there is sudden rise from 9.3 to 1054.6, 

    7. Now calculate the 99.1, 99.2, 99.3,..., 100th percentile values and get the proper value after which there is sudden rise the values, assume it is 2.5

    1. Print the feature names whose % change is more than a threshold x(in our example it's 2.5)


- ## Tools used : 
    *Scikit-learn, NLTK ,Numpy, Pandas, Seaborn, Matplotlib etc.*


