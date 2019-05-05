# Data Mining Project

## Introduction

### Overview on Raw Data
### TakeAways
### Path Design
![Machine Learning Process](https://cdn-images-1.medium.com/max/2400/1*-bqV4YyZtlz9EUxi8levjw.jpeg)

----

## Preprocessing

### Normalization
#### Min-Max Method
#### Dealing with Categorical Features
- Encoder
- Dummy

### Imputation
- Random Forest Imputation

### Dealing with Imbalanced Data
- SMOTE

----

## Modelling 

### Feature Selection
- Embedded
- Filter  
delete fnlwgt
Four pairs of features have correlationship: education & education num,marital status & occupation,relationship & race,sex & hours. We firstly run model without one of these features, and choose the feature with higher importance to accuracy.  
We delete eduction, occupation, relationship and sex 

### Model Implementation
- Logisitics Regression


There are two main parameters can be adjusted in logistics model. The first one is the penalty type, the second is C penalty amount.  
We use validation curve to choose parameter.  
We find that l1 penalty is always better than l2 penalty: 0.77 vs 0.75  
C has limited influence to performance.

Also, we have tested the performance of feature selection. Feature selection is not importance to l1 penalty but can significant improvement on l2 penalty, 0.5 to 0.75.  
- Random Forest


We dont need feature selection random forest. And we use validation curve to adjust parameter. Max depth of the tree is the most importance parameter. We choose 9, get 0.86
- SVM (RBF Kernel)

We have test 4 kinds of kernel functions: linear,poly,rbf and sigmoid. Only rbf kernel have good performance. The parameter adjustment to SVM has no significant influence. We get 0.71. 

----

## Test and Improvment

### Evaluation method
- Lift Graph
- Hyperparameter Tuning
- Cross Validation

### Evaluation Metrics

### Test Result
