# Challenge XII | Fintech <img src="https://instructure-uploads-pdx.s3.us-west-2.amazonaws.com/account_150420000000000001/attachments/590996/columbia.png" height="48" width="48">
---
This project is the tenth challenge for the Columbia Fintech Bootcamp.

This challenges is about  Supervised Learning Models

The data used is a set of Historic Loan information and whether the loan was healthy or not


The source data is in the following file: 
* [Lending Data](./Resources/lending_data.csv)

---

# Results report:

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
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky"></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>precision</b></span></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>recall</b></span></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>f1-score</b></span></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>support</b></span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold"><b>Healthy Loan</b></span></td>
    <td class="tg-0pky">1.00</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">1.00</td>
    <td class="tg-0pky">18765</td>
  </tr>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold"><b>Unhealthy Loan</b></span></td>
    <td class="tg-0pky">0.85</td>
    <td class="tg-0pky">0.91</td>
    <td class="tg-0pky">0.88</td>
    <td class="tg-0pky">619</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">accuracy</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">19384</td>
  </tr>
  <tr>
    <td class="tg-0pky">macro avg</td>
    <td class="tg-0pky">0.92</td>
    <td class="tg-0pky">0.95</td>
    <td class="tg-0pky">0.94</td>
    <td class="tg-0pky">19384</td>
  </tr>
  <tr>
    <td class="tg-0pky">weighted avg</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">19384</td>
  </tr>
</tbody>
</table>

  * Precision is 100% for Healthy loans and 85% for Unhealthy loans
  * Recall is 99% for Healthy Loans and 91% for Unhealthy loans


* Machine Learning Model 2: Given the nature of the model data is randomly oversampled to balance the types of loans, this is called oversampling. The same Logistic Regression is then applied. The following results were obtained.
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky"></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>precision</b></span></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>recall</b></span></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>f1-score</b></span></th>
    <th class="tg-0pky"><span style="font-weight:bold"><b>support</b></span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold"><b>Healthy Loan</b></span></td>
    <td class="tg-0pky">1.00</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">1.00</td>
    <td class="tg-0pky">18765</td>
  </tr>
  <tr>
    <td class="tg-0pky"><span style="font-weight:bold"><b>Unhealthy Loan</b></span></td>
    <td class="tg-0pky">0.84</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">0.91</td>
    <td class="tg-0pky">619</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">accuracy</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">19384</td>
  </tr>
  <tr>
    <td class="tg-0pky">macro avg</td>
    <td class="tg-0pky">0.92</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">0.95</td>
    <td class="tg-0pky">19384</td>
  </tr>
  <tr>
    <td class="tg-0pky">weighted avg</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">0.99</td>
    <td class="tg-0pky">19384</td>
  </tr>
</tbody>
</table>

  * Precision is 100% for Healthy loans and 84% for Unhealthy loans
  * Recall is 99% for Healthy Loans and 99% for Unhealthy loans

## Summary

The results from the two models are very close, however there is a slight increase in the Recall for the Oversampled model, this is better for our business requirement, since reduces the risk of having false negatives (1% chance).

The oversampled model should be the model to use for our business necessity.





---

## Technologies

The main language is Python, with the following auxiliary modules/libraries.
Python version is 3.7, developed in an independent conda virtual environment

### pandas
This module handles DataFrames (dynamic tables), to maniupulate, store data, do automatic calculations and adding dynamic data.

### pathlib
This module helps abstracting the OS discrepancies between folder structures and files.

### numpy
Library for generic Math calculations (in this case average)

### sklearn

Library for machine learning model creation, processing, testing, evaluation and reporting (in this case Logistic Regression Supervised learning algorithm)

### imblearn

For machine learning performance reporting

---


### Clone repository
```bash
git clone https://github.com/lumiroga/fintech-challenge12.git
```
---

## Usage

Open the terminal

Go to solution folder in your local computer

```bash
cd ./fintech-challenge12
jupyter credit_risk_resampling.ipynb
```


---

## Contributors

[lumiroga](https://github.com/lumiroga)

---

## License

* mpl-2.0 | Mozilla Public License 2.0