# Titanic Machine Learning from Disaster
* Build an ML model that takes the information of a passenger, predicts whether he/she survived with an accuracy of 80% approx.
* Data is taken from the Kaggle **Titanic** competition.
* Did some Data Preprocessing(Outlier Detection, Handling Missing Values and Feature Engineering) on original data.
* Optimized various ML models with GridSearchCV to reach the best model
## Code and Resources Used
**Python version:** 3.8  
**Packages:** numpy, pandas, matplotlib, seaborn, collections, scikit-learn  
**Dataset:** https://www.kaggle.com/c/titanic  
## Data Description
We have the information of all the passengers who boarded the Titanic ship to predict whether the passenger survived the shipwreck. The dataset contains the passenger class, gender, age, ticket number, cabin number, fare, number of parents/children aboard the Titanic, number of siblings/spouses aboard the Titanic, and the port of embarkment of each passenger.
For more information:-
https://www.kaggle.com/c/titanic/data  
## Data Cleaning
After downloading the dataset I needed to clean it up so that it was usable for my model. I made the following changes to our raw data:
* Droped PassengerId column as it did not add any value
* Droped Cabin and Ticket columns, these were categorical columns having too many categories in them with a chance of having new unseen categories in test data
* Droped rows with outliers
* Replaced missing values in the column Age using dictionary having medians of the age group by the Pclass feature
* For Embarked column, missing values were replaced with the most frequently occurring value
## Feature Engineering
* Categories in the Title column were grouped into various columns
* Created a column for family size
* Created Squared numeric feature columns
## Model Performance
GradientBoosting model outperformed every other model on both test and validation dataset.  
* **GradientBoosting Classifier:** 79.88%
* **Voting Classifier:** 78.77%
* **Logistic Regression:**  77.09%
* **Support Vector Machine Classifier:** 77.09%
* **RandomForest Classifier:** 77.09%
* **KNeighbors Classifier:** 75.41%
* **ExtraTrees Classifier:** 75.41%
* **Adaptive Boosting Classifier:** 74.86%
