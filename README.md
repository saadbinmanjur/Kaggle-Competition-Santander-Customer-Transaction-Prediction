# Summary
In this Kaggle competition the Santander Bank wants to predict "*which customers will make a specific transaction in the future, irrespective of the amount of money transacted.*" [ [Link to the competition](https://www.kaggle.com/c/santander-customer-transaction-prediction) ]

The best score in Kaggle is 0.92573 (as of 27 July 2020), and I achieved a score of 0.80469. 

It seems the data has been duplicated with "fake" observations and in order to get a score over 0.90 a "magic" feature needs to be created (e.g. see [this notebook](https://www.kaggle.com/cdeotte/200-magical-models-santander-0-920)). My focus in this notebook is not to find this "magic" feature, but to go through the data science process. Nonetheless, I did some experiments and it was an interesting learning experience, and perhaps something to explore further in the future. 

Let's start.

# Results
Gaussian Naive Bayes was the best performing model of the 3 (Logistic Regression, Random Forest Classifier and Gaussian Naive Bayes), but also the fastest. RFC was the slowest one.

The main metric used during the modelling was the ROC-AUC. GNB also returned good results in other metrics such as Recall and Precission, where these are very important in an imbalanced dataset (which one is more importan will depend on specific cases, uses and policies).

After re-training the model with all the data and submitting the test data to Kaggle it returned a 80.47% score, which is the highest I ever achieved for this competition.

As next steps, a deeper look into the outliers would be a good idea. I tried to use a 3 times the Standard Deviation approach to identify outliers but it was deleting the whole dataset... Also, I didn't perform any data reduction since the models could handle all the dataset. However, experimenting with this would also be a good next step.