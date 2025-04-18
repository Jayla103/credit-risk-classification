# Module 12 Report Template

## Overview of the Analysis
In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
    The purpose of this analysis was to build a machine learning model that can predict credit risk. The main goal was to determine whether a loan is likely to be paid back ("healthy loan") or if the borrower is at risk of defaulting ("high-risk loan").

* Explain what financial information the data was on, and what you needed to predict.
    The dataset included financial information for each applicant and their loan, such as loan size, interest rate, income, debt-to-income ratio, number of existing accounts, any derogatory marks, and total debt. Using this data, the model was designed to predict the likelihood of someone defaulting on a loan.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    The target variable we were trying to predict was the loan status, which had two categories: "healthy loan" and "high-risk loan." The data was imbalanced, with about 75,036 healthy loans and only 2,500 high-risk ones.

* Describe the stages of the machine learning process you went through as part of this analysis.
    The machine learning process started with cleaning the data and doing a bit of exploratory analysis to better understand what we were working with. After that, I selected the features (X) and target variable (y), split the data into training and testing sets, trained the model, and then evaluated its performance using the test set.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
    For the modeling, I used LogisticRegression, since it works well for binary classification problems like this. To handle the class imbalance, I also used RandomOverSampler to balance the dataset and make sure the model had an equal number of healthy and high-risk loans to learn from.


## Results
Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

Model 1
    Achieved a high accuracy of 99%, meaning it made very few mistakes overall.
    Precision was 93%, so when it predicted a loan as high-risk, it was right 93% of the time.
    Recall was 95%, which means it was able to correctly identify 95% of all actual high-risk loans.

Model 2
    Also hit 99% accuracy, showing strong overall performance.
    Precision stayed the same at 93%, so it was just as good at correctly flagging high-risk loans.
    Recall improved to 99%, which means this model caught almost every single high-risk loan — a solid improvement over Model 1.


## Summary
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
    IBoth models performed well and predicted both 0s and 1s with 99% accuracy.
    However, Model 2 had a slightly higher recall score when it came to predicting 1s — the high-risk loans. Because of that, I’d recommend going with Model 2 for this task.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    In this case, it feels more important to accurately identify high-risk loans than healthy ones, since the cost of missing a high-risk borrower is likely much higher.
