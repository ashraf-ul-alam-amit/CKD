# Chronic Kidney Disease (CKD) Prediction
**Course No**: CSE 3200  
**Course Title**: Software Development Project II

## Overview

This project aims to develop a machine learning model to predict Chronic Kidney Disease (CKD) based on patient attributes. Early detection through this model can help prevent CKD progression and improve patient outcomes.

## Methodology

1. **Data Collection and Pre-processing**
   - **Dataset**: Includes 24 features (11 numerical, 13 categorical) and a binary target for CKD classification.
   - **Handling Missing Values**: Imputed using mean for numerical and mode for categorical features.

2. **Feature Transformation and Selection**
   - **Transformation**: Categorical features encoded with `LabelEncoder`.
   - **Selection**:
     - **ExtraTreesClassifier**: Determines feature importance.
     - **SelectKBest**: Chooses top features based on statistical tests.
     - **Correlation Heatmap**: Removes highly correlated features.
   - **Extraction**:
     - **Balancing**: Applied `RandomOverSampler` to address class imbalance.
     - **Scaling**: Features scaled using `MinMaxScaler` to range (-1, 1).
     - **PCA**: Reduced features while retaining 95% variance, resulting in 11 features.

3. **Model Selection and Training**
   - **Models**: Logistic Regression, Support Vector Classifier (SVC), and RandomForestClassifier.
   - **Training**: Performed using 10-fold cross-validation.
   - **Best Model**: RandomForestClassifier achieved 99.7% accuracy.

4. **Deployment**
   - **API**: Deployed the model using Flask.
   - **Web Interface**: Built with HTML and CSS for user interaction.
