# Adult Income Prediction
## Objective
To predict the income of the individual from the data collected through census. Predicting the income as above $50,000 or below $50000, on the basis of the features given in the data set.
## PROBLEM STATEMENT.
This study is conducted to know the various factors of people that effects their income level. This data would help us to analyze what role different features play in predicting the income of an individual.
## Solution.
Classification has been done to predict whether a person's yearly income in falls in the income category of either greater than $50,000 or less equal to $50,000 category based on a certain set of attributes.
## Results.
After implementing three classification Machine Learning algorithms (Logistic Regression, Random Forest Classifier and Support Vector machine). Random Forest Classifier outperformed & gave the accuracy score of 89% for the model, which depicts that the model has performed good when compared to other two models.
## MODEL DESIGN.
The model was carried out through three stages:-
1.	Exploratory Data Analysis – EDA. (https://github.com/Shahid7778/Adult-income-prediction/blob/main/EDA/Exploratory%20Data%20Analysis%20-%20EDA.ipynb)
2.	Feature Engineering. (https://github.com/Shahid7778/Adult-income-prediction/blob/main/Feature%20Engineer/Feature%20Engineering.ipynb)
3.	Model Evaluation. (https://github.com/Shahid7778/Adult-income-prediction/blob/main/Model%20Evaluation/Model%20Evaluation.ipynb)
### DATA SET.
- The Data was collected from Kaggle.
Data Set Link:- https://www.kaggle.com/datasets/uciml/adult-census-income
- The dataset provided, 15 different independent features from the census data. Aim to predict if a person earns more than 50k$ per year or not.
## Exploratory Data Analysis – EDA.
Most of the features in the dataset was categorial in nature or discrete outcomes. The data consists of total 15 columns with the information of individuals reflecting their several attributes that gave the final outcome variable of earning more than or less than equal to $50,000 as their income.
Here we have considered the Salary as the dependent variable/outcome variable and have analysed the relationship between other features with the salary and presented through graphs. As some of the features was not required in the data, we have ignored them through finding the correlation between independent features through feature engineering.
## Feature Engineering.
1.	Converted the categorical data through label encoding, to convert the values as integers.
2.	Calculated the correlation between the dependent variable __(Salary)__ and other independent features to select the best features, to gain best performance scores.
3.	Removed the features which depicted the less correlation with the outcome variable.
4.	As the dependent variable/outcome variable was imbalanced and showed the data points as:
- __0 -   24720__
- __1	- 7841__

The above outcomes shows that data is imbalanced with more of ‘0’ outcomes (76%) and less of ‘1’ outcomes (24%), so implemented a over sampling technique called __SMOTE (Synthetic Minority Over-sampling Technique)__ to balance the outcomes, which gave the below results.
- __0 – 24720__
- __1 - 24720__

After the above steps the next step was the model Evaluation to train and predict the model from the required independent features to train the model.

## Model Evaluation.
In this stage, trained and tested the models on three classification models:
1.	__Logistic Regression__
2.	__Random Forest Classifier__
3.	__Support Vector Machine (SVM)__

The below model was trained and test without Hyperparameter Tuning, The Random Forest classifier outperformed best and gave the score of 88%.

Logistic Regression
Model performance for training set
- Accuracy: 0.6646
- F1 score: 0.6634
- Precision: 0.6868
- Recall: 0.6055
---------------------------
Model performance for test set
- Accuracy: 0.6606
- F1 score: 0.6596
- Precision: 0.6797
- Recall: 0.6065

=================================

Random Forest Classifier
Model performance for training set
- Accuracy: 1.0000
- F1 score: 1.0000
- Precision: 1.0000
- Recall: 0.9999
---------------------------
Model performance for test set
- Accuracy: 0.8892
- F1 score: 0.8892
- Precision: 0.8906
- Recall: 0.8873

================================ 

Support Vector machine
Model performance for training set
- Accuracy: 0.5936
- F1 score: 0.5203
- Precision: 0.9298
- Recall: 0.2027
---------------------------
Model performance for test set
- Accuracy: 0.5910
- F1 score: 0.5160
- Precision: 0.9264
- Recall: 0.1971

===================================
## Hyperparameter Tuning with Randomized Search CV
From the above scores the __Random Forest Classifier__ gave the good results, hence __Randomized Search CV__ was used for hyperparameter tuning. Then got a mild increase in the model scores.

Model performance for test set after Hyperparameter tuning
- Accuracy: 0.8921
- F1 score: 0.8921
- Precision: 0.8929
- Recall: 0.8908
## Conclusion

The final model of Random Forest Classifier gave the best output for the data, with high Precision and Scores of close to 90% after hyperparameter tuning. Hence the predicted model can give the accuracy results up to 90% to predict the data points of the individual attributes and to classify their income level.
