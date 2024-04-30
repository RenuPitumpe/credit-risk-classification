# Credit Risk Analysis Report

## Overview of the Analysis

The purpose of the analysis is to develop a machine learning model that able to predict the status of the loan whether it is healthy loan or high risk loan using the given financial infomations like size of the loan, interest rate, income of the borrower, DIT ratio, number of accounts, derogatory marks, Total debt. By understanding the historical financial data, the goal was to build a model that could assist to identify loans that are more likely to default, enabling proactive risk management for lenders.

In the data set there are 7 number of financial informations are available. According to the data analysis, there were no any null values included in the given data set. There were around 78 000 number of financial data included in the dataset. To identify the correlation between the target values and the other financial data I have plotted a correlation figure using seaborn. According to that there were no any financial data which not correlated to the target value. And all the financial data values are numerical, I have checked it by getting datatypes of each column.

Consider about the variable to be predicted, we have to predict the status of the loan as the target variable. There are two status of a loan, a loan can be healthy or high risk. So in the given data set there were two labels have used for these two status, they are '0' for a healthy loan and '1' for a high risk loan. Consider about the value counts for each label there were around 75000 data was included for label '0' and 2500 number of data included for label '1'. So we can see there is huge gap between those values, it can be affected to the model performance alo. 

Consider about the stages of the machine learning process, initially we have to do a data preprocessing like handling missing values, encoding categorical values into numerical values and train test splitting. Then we have to choose a uitable model for the train. After the model selection we have train our model and then we should evaluate our model using the test data set. Then we can implement optimization activities like fine tunning, feature selection to improve the performance of the model.

Consider about the used methodologies here, I have used the logistic regression model to train data and get prediction. It is a simple and effective binary classificatin model. For the evaluations I have used confuion matrix. It is a tabular representation of actual vs predicted class lables. Then I get the evaluation metrics, It gives the precision, recall and F1 score values for each class to identify the perforemence of the model. 


## Results

* Machine Learning Model 1:
    * Accuracy Score: 0.85, the accuracy score indicate that the 85% of predictions from this model were correct.

    * Precision Score: 0.87, which indicate that 87% of instance predicted as positive were actually positive.

    * Recall Score: 0.82, indicate that 82% of the actual positives were correctly identified by the model. 


## Summary

* According to the results, the model perform very well for label '0'(healthy loan). It achives a precision of 1.00 which indicates that predicted healthy loans are indeed healthy loans. The recall value also have high value as 0.99, which indicate that the model correctly identifies most of the actual healthy loans. The value of the F1 score also perfect at 1.00. 
But consider about the predicting label '1'(high-risk-loan), the model perform leasonably well but shoul be improve. It shows the accuracy of 0.86 which indicate that about 86% of the predictions for high risk loans are actually high risk loans. The recall value is 0.94 which shows model correctly identifies 94% of the actual; high risk loans. 

* The performance gap which is described above can be happened due to the huge difference between the value counts for the each label. Like in this dataset there are around 75 000 data included for the label '0' while label '1' has only 2500 number of data. Because of that there can be some bias can occur in the model when predicting the both classes. So improve the overall accuracy of the model we can provide balance data set to this model. 

* To handle this situation we can implement resampling methods like undersampling and oversampling. And also we can use some algorithamic solutions like cost sensitive learning and ensemble methods to resolve this. 

* The performance of the model is depend on the problem we are trying to solve. In here the decision on whether it is more important to predict label '1' or '0' will be depenedent on specific objectives and priorities of the analysis. If priority to minimize the risk of lending to high risk brrowers, then predicting label '1' will be more important. If the objective is to maintain healthy loan and avoid unnecessary rejections of low risk borrowers, then predicting label '0' is more important and higher precision for label '0' would be the critical in here.