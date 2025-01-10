# Enhancing the Existing Credit Card Customer Churn Prediction Models


## 1.1 Project Aim


## 1.2 Project Objectives


## 2.0 Literature Review
- **(ÜNLÜ, 2021):** Applied Bayesian Optimization as the fine-tuning method with SVM with different kernels, specifically Linear kernel, Polynomial kernel, Radial basis kernel, and Sigmoid function. 
- **(Rahman & Kumar, 2020):** Achieved highest accuracy after used 10-fold cross-validaion, oversampling and adjustment in number of trees for Random Forest algorithm.
- **(Miao & Wang, 2022):** Employed Gridsearch and 5-fold cross-validation on Random Forest Algorithm to achieve best performance.

## Gap Analysis
1. Does the number of trees in a Random Forest model (e.g., 100, 1000) significantly impact its performance?
2. Does the number of folds in cross-validation significantly impact the performance of Random Forest models?
3. Does the combination of cross-validation and the number of trees significantly improve the performance of a Random Forest?

## 3.0 Methodology
### 3.1 **Dataset:** 
The [predicting credit card customer segmentation](https://www.kaggle.com/datasets/thedevastator/predicting-credit-card-customer-attrition-with-m) dataset was obtained from Kaggle.

### 3.2 Pre-processing Method
- **Data wrangling:** Modifying, organising, and turning raw data into a format that analysts can use for effective decision-making.
  - **Replacing Null Values:** The null values are replaced with mean values calculated with the same library to avoid the skewness in making predictions.
  - **Imputation:** To maintain the inherent variability of the data by estimating missing values based on the available information.
- **Label Encoding:** Convert categorical data into numerical representation.
- **Data Splitting:** A 80-20 split to provide a good balance between training and testing.
- **Oversampling:** Employed the Synthetic Minority Over-sampling Technique (SMOTE) to deal with class imbalance.

### 3.3 Fine-Tuning Method
- **The Number of Trees:** Adding additional trees can strengthen the model and make it less prone to overfitting.
- **Cross-validation:** Cross-validation with 5-folds and 10-folds are used to assess the performance of the Random Forest model.

### Selected Model
- **Random Forest Classifier:** Its ability in mitigating overfitting and identify the probability of a customer to churn with a binary outcome.

### Performance Evaluation
- **Accuracy:** The overall correctness in predictions.
- **Precision:** The proportion of true positives among positive predictions.
- **Recall Ratio:** The proportion of correctly identified positive observations.
- **F1-Score:** Harmonic mean of precision and recall, useful for imbalanced datasets.
- **Area Under ROC Curve (AUC-ROC):** Measure of separability, indicating how much the model is capable of distinguishing between classes.

### Implementation:
- **4.1 Experimental Design:**
| Experiment | Pre-processing | Fine-tuning | Model |

## Comparison

