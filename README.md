# credit-risk-classification

### Instructions
The instructions for this Challenge are divided into the following subsections:

Split the Data into Training and Testing Sets

Create a Logistic Regression Model with the Original Data

Write a Credit Risk Analysis Report

#### Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

note
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

Split the data into training and testing datasets by using train_test_split.

Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:

Fit a logistic regression model by using the training data (X_train and y_train).

Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluate the model’s performance by doing the following:

Generate a confusion matrix.

Print the classification report.

Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Write a Credit Risk Analysis Report
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

An overview of the analysis: The purpose of this analysis is to create and evaluate a data model to determine if it is conducive to use in predictions for the loan approval question.

The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

Our analysis of the model: 

* Precision: This measures the accuracy of the positive predictions. It is calculated as the ratio of true positives to the sum of true positives and false positives.

    * For class 0: 1.00 (perfect precision)
    * For class 1: 0.84 (some false positives)

* Recall: This measures the ability of the model to identify all relevant instances. It is calculated as the ratio of true positives to the sum of true positives and false negatives.

    * For class 0: 0.99 (very high recall)
    * For class 1: 0.94 (also high recall)

* F1-score: This is the harmonic mean of precision and recall, providing a balance between the two. It is especially useful when you need a single metric to evaluate model performance.

    * For class 0: 1.00 (perfect)
    * For class 1: 0.89 (good)

* Support: This indicates the number of actual occurrences of the class in the specified dataset.

    * For class 0: 18,765 instances
    * For class 1: 619 instances

* Overall Metrics:

    * Accuracy: The overall ratio of correctly predicted instances (both classes) to the total instances. Here, it's 0.99, indicating that 99% of the predictions were correct.

    * Macro Average: This is the average of the precision, recall, and F1-score across classes, treating all classes equally.

        * Macro Precision: 0.92
        * Macro Recall: 0.97
        * Macro F1-score: 0.94

    * Weighted Average: This average takes into account the number of instances in each class, giving more weight to larger classes.

        * Weighted Precision: 0.99
        * Weighted Recall: 0.99
        * Weighted F1-score: 0.99

#### Summary:
The model performs exceptionally well on class 0, with perfect precision and F1-score.
Class 1 has decent performance, with good precision and recall, but it has a higher rate of false positives (lower precision).
The overall accuracy and weighted averages indicate strong model performance overall, but the imbalance in the support (much more data for class 0 than class 1) suggests that care should be taken when interpreting these results, especially for the minority class (class 1).