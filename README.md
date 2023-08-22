# Predicting Bank Churn (Imbalanced Classifier)

<p align="center">
  <img src="/images/bank.png" 
   width="400"
   height="300"
  alt="Image of gold recovery stages">
</p>

# Project Overview

This repository hosts an imbalanced classification machine learning project that maximizes F1 Score in predicting customer bank churn. Imbalance classification techniques of weighting and upsampling were applied and logistic regression, decision tree classification, and random forest classification models were fit and tuned. After identifying the best model, the model was tested on a test set calculating final F1 score and ROC-AUC.

# Installation and Setup

## Codes and Resources Used

  - <b>Editor Used</b>: Visual Studio Code
  - <b>Python Version</b>: 3.10.9

## Python Packages Used

  - <b>General Purpose</b>: ```numpy```
  - <b>Data Manipulation</b>: ```pandas```
  - <b>Data Visualization</b>: ```matplotlib```
  - <b>Machine Learning</b>: ```sklearn```
    
# Data

## Source Data

<b>Features</b>  
    * *RowNumber* - data string index  
    * *CustomerId* - unique customer identifier  
    * *Surname* - surname  
    * *CreditScore* - credit score  
    * *Geography* - country of residence  
    * *Gender* - gender  
    * *Age* - age  
    * *Tenure* - period of maturation for a customer's fixed deposit (years)  
    * *Balance* - account balance  
    * *NumOfProducts* - nmber of banking products  
    * *HasCrCard* - customer has a credit card  
    * *IsActiveMember* - customer's activeness  
    * *EstimatedSalary* - estimated salary  

<b>Target</b>  
    * *Exited* - customer has left  


## Data Acquisition

The data were provided by TripleTen's Data Science bootcamp. The full dataset is loaded into the notebook but is proprietary information and cannot be shared online.

## Data Preprocessing

Data were checked for missing values and duplicates. Tenure has 9.09% missing data and was imputed with median imputation. There were no other missing values or duplicates.
 
# Code Structure
```
  ├── README.md          
  │
  ├── images
  │   └── bank.png  
  │   └── roc_auc.png    
  │
  └── notebooks  
     └── bank_churn_analysis.ipynb
 
```

# Results and Evaluation

Initial class balance:

<p align="left">
  <img src="/images/class_balance.png" 
  alt="ROC-AUC of Test Set">
</p>

Two methods were applied to balance the classes: weighted class values and upsampling. Classificaiton decision tree, classification random forest, and logistic regression models were tuned with each balancing method. The model with the highest F1 score was the Random forest classifier with weighted data, achieving an F1 of 0.59 with a tree depth of 11 and 50 trees.  

<p align="center">
  <img src="/images/roc_auc.png" 
  alt="ROC-AUC of Test Set">
</p>

This random forest classifier was able to achieve an F1 score of 0.60 and an ROC-AUC of 0.74 on the test set. The F1 score is consistent with the F1 score achieved on the validation set.

Overall, this model fits the data moderately well. While not a perfect predictor, the bank can be confident in using this model to help identify which customers are likely to churn


# Future Work

# Acknowledgments/References

TripleTen's Data Science bootcamp for providing the project and the data.

