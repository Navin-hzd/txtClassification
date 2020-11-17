# txtClassification
This is the data analysis on Consumer complaints of financial institutions dataset which can be found at 
https://catalog.data.gov/dataset/consumer-complaint-database download on September 17, 2020.

Since the original dataset is big to upload, the random sample of the original dataset is uploaded with 10000 rows.
Please be noted that in the original code, the name of the file is uploaded is 'complaints.csv'. 

There are two .ipynb files. 
1-DataPreparingAndAnalysis.ipynb contains data preparing and some analysis on different features of the dataset.
2- TxtClassRandomForest.ipynb contains data preprocessing on the prepared data. After preprocessing, Random Forest classifier is applied on the dataset.
I use TfidfVectorizer to find tfidf. To find the best classifier parameter I use Random Hyperparameter Grid Instead of searching manually by using RandomizedSearchCV.

Random search allowed us to narrow down the range for each hyperparameter. Now that we know where to concentrate our search, we can explicitly specify every combination of settings to try. We do this with GridSearchCV, a method that, instead of sampling randomly from a distribution, evaluates all combinations we define.

After finding the best parameter for the Random Forest Classifier, I find the final RF (using train set test set validation) showing confusion matrix, accuracy, classification report.

I also use cross validation, 10 fold cross validation and Stratified 10-fold cross validation showing confusion matrix, accuracy, classification report.
