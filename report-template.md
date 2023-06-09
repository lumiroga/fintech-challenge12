# Module 12 Report Template

## Overview of the Analysis

An analysis was made in order to generate a model that evaluates the health of a loan based on historical data, given two classifications healthy or unhealthy loan. The following parameters were used:

* loan size
* interest rate
* borrower income
* debt to income
* num of accounts
* derogatory marks
* total debt
* loan status

* Having this model we can predict the health of a credit based on above values for a given loan and reduce the risk of getting unpaid loans and also, automating the process for loan approvals.

* Given the nature of the data, were healthy loans are more common than unhealthy loans, from the given historic data we get the following results:
  * Healthy Loans: 75,036
  * Unhealthy Loans: 2,500

* For the Prediction model the following stages need to be followed:
  * Process Source Data and split training and testing data
  * Create the data model
  * Train the model
  * Predict with testing data
  * Evaluate results and precision.

* For this model the best method is Logistic Regression which is ideal for classifing between two different classes (in this case Healthy and Unhealthy loans)


## Results

Given the nature of the data (imbalanced between healthy and unhealthy loans), two methods needed to be tested and compared

* Machine Learning Model 1: Logistics Regression with Standard Data
  * Model Accuracy: 95.20 % 
  * Results: 
|                    | **precision** | **recall** | **f1-score** | **support** |
|--------------------|---------------|------------|--------------|-------------|
| **Healthy Loan**   | 1.00          | 0.99       | 1.00         | 18765       |
| **Unhealthy Loan** | 0.85          | 0.91       | 0.88         | 619         |
|                    |               |            |              |             |
| accuracy           |               |            | 0.99         | 19384       |
| macro avg          | 0.92          | 0.95       | 0.94         | 19384       |
| weighted avg       | 0.99          | 0.99       | 0.99         | 19384       |

  * Precision is 100% for Healthy loans and 85% for Unhealthy loans
  * Recall is 99% for Healthy Loans and 91% for Unhealthy loans


* Machine Learning Model 2: Given the nature of the model data is randomly oversampled to balance the types of loans, this is called oversampling. The same Logistic Regression is then applied. The following results were obtained.
  * Model Accuracy: 99.37%
  * Results:
|                    | **precision** | **recall** | **f1-score** | **support** |
|--------------------|---------------|------------|--------------|-------------|
| **Healthy Loan**   | 1.00          | 0.99       | 1.00         | 18765       |
| **Unhealthy Loan** | 0.84          | 0.99       | 0.91         | 619         |
|                    |               |            |              |             |
| accuracy           |               |            | 0.99         | 19384       |
| macro avg          | 0.92          | 0.99       | 0.95         | 19384       |
| weighted avg       | 0.99          | 0.99       | 0.99         | 19384       |

  * Precision is 100% for Healthy loans and 84% for Unhealthy loans
  * Recall is 99% for Healthy Loans and 99% for Unhealthy loans

## Summary

The results from the two models are very close, however there is a slight increase in the Recall for the Oversampled model, this is better for our business requirement, since reduces the risk of having false negatives (1% chance).

The oversampled model should be the model to use for our business necessity.
