# Titanic Machine Learning from Disaster
* Created a ML model that given a passengers information predicts whether he/she survived with an accuracy of 80% approx.
* Data is taken from kaggle Titanic competetion.
* Done some Data Preprocessing (Outlier Detection, Handling Missing Values, Feature Engineering) on original data.
* Optimized various ML models with GridSearchCV to reach the best model
## Code and Resources Used
**Python version:** 3.8  
**Packages:** numpy, pandas, matplotlib, seaborn, collections, scikit-learn  
**Dataset:** https://www.kaggle.com/c/titanic  
## Data Description
https://www.kaggle.com/c/titanic/data  
Basicaly we have all the information of the passengers who boarded the Titanic, based on this we need to predict whether the passenger survived the shipwreck or not.
## Data Cleaning
After, getting the data i needed to clean it up so that it was usable for my model. I made the following changes to our raw data:
*    Droped PassengerId column as it did not add any value
*    Droped Cabin and Ticket columns, these were categorical columns having too many categories in them with a chance of having new unseen categories in test data
## Data Preprocessing
Explained it in the project file.
## Model Performance
GradientBoosting model outperformed every other model on both test and validation dataset.  
*    **GradientBoosting Classifier** 79.88%
*    **Voting Classifier** 78.77%
*    **Logistic Regression:**  77.09%
*    **Support Vector Machine Classifier:** 77.09%
*    **RandomForest Classifier** 77.09%
*    **KNeighbors Classifier:** 75.41%
*    **ExtraTrees Classifier** 75.41%
*    **Adaptive Boosting Classifier** 74.86%
