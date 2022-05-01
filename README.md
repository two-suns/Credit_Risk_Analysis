# Credit Risk Analysis
## Overview
Employ different techniques to train and evaluate models with unbalanced classes.  Use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

#### RandomOverSampler
  - Balanced Accuracy Score:  
  ![ros_bas](https://user-images.githubusercontent.com/59906657/166168951-93eaef78-ca4d-4488-8478-e98c9e3b56b9.PNG)
  - Precision & Recall Scores:  
  ![ros_cri](https://user-images.githubusercontent.com/59906657/166169010-e7b3e5f6-7f9e-4b20-8232-46b15ece5865.PNG)

#### SMOTE
  - Balanced Accuracy Score:  
  ![smote_bas](https://user-images.githubusercontent.com/59906657/166169035-82a75bee-48cf-4ef5-a520-c9f006c70aa6.PNG)
  - Precision & Recall Scores:  
  ![smote_cri](https://user-images.githubusercontent.com/59906657/166169061-50266c47-12b4-48b7-88fb-aef3c8b3d168.PNG)

#### ClusterCentroids
  - Balanced Accuracy Score:  
  ![cc_bas](https://user-images.githubusercontent.com/59906657/166169092-c7b1b3d4-8441-427c-a671-781ac9c61873.PNG)
  - Precision & Recall Scores:  
  ![cc_cri](https://user-images.githubusercontent.com/59906657/166169099-37367ba1-4cca-4155-a8c2-ccda3b8b8d19.PNG) 

#### SMOTEENN
  - Balanced Accuracy Score:  
  ![smoteenn_bas](https://user-images.githubusercontent.com/59906657/166169112-74b0736a-9c93-4405-a91c-d080278215b8.PNG)
  - Precision & Recall Scores:  
  ![smoteenn_cri](https://user-images.githubusercontent.com/59906657/166169131-85b5bf91-00ea-4144-bbc0-332fd263a4be.PNG) 

#### BalancedRandomForestClassifier
  - Balanced Accuracy Score:  
  ![brfc_bas](https://user-images.githubusercontent.com/59906657/166169137-750d6c45-0fb1-4c02-8602-7f92a8b9be7a.PNG)
  - Precision & Recall Scores:  
  ![brfc_cri](https://user-images.githubusercontent.com/59906657/166169142-6ddb5696-06be-4589-81be-37c68e06ae0b.PNG)
 
#### EasyEnsembleClassifier
  - Balanced Accuracy Score:  
  ![eec_bas](https://user-images.githubusercontent.com/59906657/166169149-96e7b89a-5766-4df5-bb1e-02ed07b10a8d.PNG)
  - Precision & Recall Scores:  
  ![eec_cri](https://user-images.githubusercontent.com/59906657/166169157-57a6430e-3ee1-43f8-8995-506fb6ed2a62.PNG) 

## Summary
Looking at balanced accuracy score, the RandomOverSampler, SMOTE, and SMOTEENN models all scored fairly close to each other in the 63% - 67% range.  The ClusterCentroids model scored the lowest at about 54%.  The BalancedRandomForestClassifier model performed better at 79%.  The EasyEnsembleClassifier model was by far the best with a 93%.

The EasyEnsembleClassifier model is the easy choice to recommend due to the high accuracy score.  It also has very good recall scores at 91% for high risk and 94% for low risk.  This means that the model was very good at successfully finding the true positives for each type of risk.  This would be important when trying to determine someone's credit risk.
