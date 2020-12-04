# txtClassification
This is the data analysis on Consumer complaints of financial institutions dataset which can be found at 
https://catalog.data.gov/dataset/consumer-complaint-database download on September 17, 2020.

Since the original dataset is big to upload, the random sample of the original dataset is uploaded with 10000 rows.
Please be noted that in the original code, the name of the file is uploaded is 'complaints.csv'. 

 
1-DataPreparingAndAnalysis.ipynb contains data preparing and some analysis on different features of the dataset.
2- TxtClassRandomForest.ipynb contains data preprocessing on the prepared data. After preprocessing, Random Hyperparameter Grid search Instead of searching manually( RandomizedSearchCV) is used. Random search allowed us to narrow down the range for each hyperparameter. Now that we know where to concentrate our search, we can explicitly specify every combination of settings to try. We do this with GridSearchCV, a method that, instead of sampling randomly from a distribution, evaluates all combinations we define. 

After building the optimizaed classifier, three different methods of validation are used: 10-Fold Cross Validation, 10-Fold Stratifed Cross Validation, Tran, test set split.
The performance of the classifier has been evaluated by showing confusion matrix, accuracy, classification report.

3-TxtClassSVM.ipynb: the same procedure as Random Forest but for SVM Classifier
4-TxtClassMultinomialNB.ipynb: the same procedure as Random Forest but for Multinomial Naive Bayes Classifier
5-TxtClassLogisticRegression.ipynb: the same procedure as Random Forest but for Multinomila Logistic Regression Classifier
6- TxtClassifiersComparison.ipynb: Compare the performance of diiferent classifier on a broader range of samples and validate by 10-Fold Stratified Cross Validation method
