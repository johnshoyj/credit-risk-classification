# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis to use supervised learning as a method for categorizing loans into healthy and high-risk based on a number of features, or characteristics, of the borrower and loan. The model used loan size, interest rate, borrower income, debt to income ratio, number of accounts, number of derogatory marks, and total debt as the predictors of the categorical outcome variable: loan status. Loan status was indicated as either a "0" or healthy loan, or 1 or high-risk loan. 

The stages of machine learning were to separate out the data into an array or outcome variable, and a features dataframe which held the predictor variables. The next step was the use sklearn's train_test_split module to split the features dataframe and outcome variable into an x (predictor) training and testing dataset and a y (outcome) training and testing dataset. Next, I imported the LogisticRegression module from sklearn and instantiated the model. Then I fit the model using the x and y training data. The next step was to use the fitted data to make some predictions on the x testing data. After the predictions were made, a confusion matrix and classification report were run to determine the accuracy, precision, and recall of the model.  

The results of the confusion matrix were as follows:

True Positive (TP): 583, The number of instances that are actually positive and were correctly classified as positive.
False Positive (FP): 110, The number of instances that are actually negative but were incorrectly classified as positive.
False Negative (FN): 36, The number of instances that are actually positive but were incorrectly classified as negative.
True Negative (TN): 18655, The number of instances that are actually negative and were correctly classified as negative.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of the machine learning model.

* Machine Learning Model:
  * Description of Model Accuracy, Precision, and Recall scores.

Overall, the model model has very high accuracy (99% of the time correct), but has higher precision and recall when predicting a healthy loan than it does with the high-risk loan. Of all the loans classified as healthy loans, 100% were healthy (precision), and of all the actual heathly loans 99% were classified as being healthy (recall). Whereas, of all the loans classified as high-risk only 84% were high risk (precision), and of all the actual high-risk loans 94% were classified as being high-risk (recall).  



## Summary

Summarize the results of the machine learning model, and include a recommendation on the models use, if any. For example:
The model is highly accurate for predicting healthy loans, but incorrectly classified 16% as high-risk. This error in the model would cost the organization on lost potential healthy loan originations.  There would likely be an extremely high rate of healthy loans originated based on this model, but it would also miss out on other potential healthy loans by miscategorizing them. If the model would be used, it would be a relatively high risk aversion model. So the organization would need to determine how much risk they are willing to accept and adjust accordingly. If the organization wanted to improve the model precision around high-risk loans there could be more analysis completed to determine which of the predictor variables has the largest effect size on the outcome.



