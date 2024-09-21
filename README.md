# DSCO Data Science: Money Laundering Prediction
This is a notebook created from participating in the Data Science Club Olympiad (DSCO) of Binus University, The problem presented is predicting money laundering activities using transaction data provided by IBM.
Each team participating in the Olympiad consists of three members.

Our Team:
  * https://github.com/foxyglue
  * https://github.com/ljervino
  * https://github.com/DavidPaulOng

## Project Overview
This project focuses on a dataset containing financial transactions, with a specific variable indicating whether a transaction is an act of money laundering. The goal is to build a predictive model that can effectively identify potential money laundering activities based on historical transaction data.
The data used is provided by IBM and accessed from Kaggle: https://www.kaggle.com/datasets/ealtman2019/ibm-transactions-for-anti-money-laundering-aml/data?select=HI-Large_Trans.csv

## Problems 
The common problems of fraud detection is the large amount of data that is in the majority class compared to the minority class. Striking a balance between identifying potential fraud and avoiding false positives is crucial. Too many false positives can lead to inconvenience for legitimate users and erode trust in the system.

<p align="left" width="100%">
    <img width="30%" src = "https://github.com/user-attachments/assets/f3f7af56-67db-4ca2-a192-eaa31370711c"> 
</p>

This dataset contains a large amount of data that it is hard to parse. The approach that we took is using the python library Dask which is used to segregate data into smaller more managable chunks


## Approach and techniques
  * Currency Standardization
  * Outlier Removal
  * Log Transformation
  * Undersampling
  * Feature Engineering

## Model Performance
<table >
  <thead>
    <th>Model</th>
    <th>Class</th>
    <th>Precision</th>
    <th>Recall</th>
    <th>F1-score</th>
    <th>Accuracy</th>

  </thead>
  <tr></tr>
  <tr>
    <tr>
      <td>Random Forest</td>
      <td>Not Fraud</td>
      <td>0.81</td>
      <td>0.81</td>
      <td>0.81</td>
      <td>0.81</td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Fraud</td>
      <td>0.81</td>
      <td>0.81</td>
      <td>0.81</td>
      <td></td>
    </tr>
</tr>


<tr>
  <tr>
    <td>Logistic Regression</td>
    <td>Not Fraud</td>
    <td>0.85</td>
    <td>0.89</td>
    <td>0.87</td>
    <td>0.86</td>
    
  </tr>
  <tr></tr>
  
  <tr>
    <td></td>
    <td>Fraud</td>
    <td>0.88</td>
    <td>0.84</td>
    <td>0.86</td>
    <td></td>
    
  </tr>
</tr>

<tr>
    <tr>
      <td>K-Nearest Neighbors</td>
      <td>Not Fraud</td>
      <td>0.84</td>
      <td>0.92</td>
      <td>0.88</td>
      <td>0.88</td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Fraud</td>
      <td>0.91</td>
      <td>0.83</td>
      <td>0.88</td>
      <td></td>
    </tr>
</tr>


</table>
