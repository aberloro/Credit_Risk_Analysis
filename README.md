# Credit_Risk_Analysis

## Overview of Project

 ### Purpose
 Machine learning can be leveraged to evaluate credit card risk, though credit risk data will be unbalanced (more good loans tha risky ones). The purpose of this project is to use different techniques to resample or balance the data and evaluate which techniques better classify borrowers by credit risk. 

 ### Deliverables
  - 1: Use resampling models to predict credit risk: 
     - Oversample with RandomOverSampler and SMOTE algorithms
     - Undersample with ClusterCentroid algorithm
  - 2: Use SMOTEENN algorithm to predict credit risk
  - 3: Use Ensemble Classifiers to predict credit risk:
     - BalancedRandomForestClassifier
     - EasyEnsembleClassifier
  - 4: Written report on credit risk analysis techniques
 
 ### Resources
  - Data Sources: LoanStats_2019Q1.csv
  - Technology: Visual Studio Code, Jupyter Notebook, Python 3.7, imbalanced-learn library, scikit-learn library

## Results
  ### Random Oversampling
   - Accuracy score: 0.64
   - Precision: High risk: 0.01; Low risk: 1.00
   - Recall: High risk: 0.62; Low risk: 0.65
   - F1 Score: 0.79
   --img--

  ### SMOTE Oversampling
   - Accuracy score: 0.63
   - Precision: High risk: 0.01; Low risk: 1.00
   - Recall: High risk: 0.62; Low risk: 0.64
   - F1 Score: 0.78
   --img--

  ### Cluster Centroid Undersampling
   - Accuracy score: 0.53
   - Precision: High risk: 0.01; Low risk: 1.00
   - Recall: High risk: 0.61; Low risk: 0.45
   - F1 Score: 0.62
   --img--

  ### SMOTEENN Resampling
   - Accuracy score: 0.64
   - Precision: High risk: 0.01; Low risk: 1.00
   - Recall: High risk: 0.70; Low risk: 0.57
   - F1 Score: 0.73
   --img--

  ### Balanced Random Forest Ensemble Classifier
   - Accuracy score: 0.79
   - Precision: High risk: 0.04; Low risk: 1.00
   - Recall: High risk: 0.67; Low risk: 0.91
   - F1 Score: 0.95
   --img--

  ### AdaBoost Ensemble Classifier
   - Accuracy score: 0.93
   - Precision: High risk: 0.07; Low risk: 1.00
   - Recall: High risk: 0.91; Low risk: 0.94
   - F1 Score: 0.97
   --img--

## Summary
When considering credit risk, lenders will want to minimize approvals to high risk borrowers.  There is a tradeoff between model sensitivity and precision.  A highly sensitive model will find all the low risk borrowers and miss-classify some high risk borrowers as safer than they are.  A highly precise model will not capture all low risk borrowers, but will avoid the false-positive identification of risky borrowers. Lenders should employ models with high precision in order to minimize approval of high-risk borrowers.

The AdaBoost Ensemble Classifier is the top choice for high-risk borrower classification. The AdaBoost Ensemble Classifier had the highest precision in identifying high-risk borrowers.  The overall accuracy score indicates the model accurately classified low vs high risk borrowers 93% of the time, and the high F1 score indicates a relative balance between precision and sensitivity in the model.  

The second-choice model is the other ensemble classifier, Balanced Random Forest. BRF performed with slightly less accuracy and precision in high-risk classification than AdaBoost, though did *much* better than the resampling models.  None of the oversampling, undersampling, or combo-SMOTEENN techniques are accurate or precise enough to classify high risk borrowers.  
