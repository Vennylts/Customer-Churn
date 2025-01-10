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
#### **4.1 Experimental Design:**
There will be 5 experiments to be conducted, each with the objective of enhancing the accuracy of customer attrition predictions. Throughout all five experiments, the pre-processing techniques and the model will remain constant, while different fine-tuning methods will be employed such as experimenting on the number of trees of the Random Forest and k-folds cross-validation where k refers to the number of times the dataset will be divided into.
- **Fine-tuning 1: Vary the Number of Trees Experiment**
  - **Experiment 1:** The number of trees = 100
  - **Experiment 2:** The number of trees = 1000
- **Fine-Tuning 2: Vary the Number of k-Folds Cross-Validation Experiment**
  - **Experiment 3:** 5-fold cross-validation
  - **Experiment 4:** 10-fold cross-validation
- **Combining Both Best Hypothesised Fine-Tuning Methods Experiment**
  - **Experiment 5:** 1. The number of trees = 1000
                      2.  10-fold cross-validation

## 5.0 Performance Comparison
### **Fine-tuning 1: Vary the Number of Trees Experiment**
| Experiment  | Number of Tree | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
| ----------- | -------------- | -------- | --------- | ------ | -------- | ------- |
| 1           | 100            | 0.948    | 0.815     | 0.875  | 0.844    | 0.919   |
| 2           | 1000           | 0.948    | 0.813     | 0.872  | 0.843    | 0.917   |

### **Fine-Tuning 2: Vary the Number of k-Folds Cross-Validation Experiment**
| Experiment  | Number of cross-validation folds (k) | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
| ----------- | -------------------- | -------- | --------- | ------ | -------- | ------- |
| 3           | 5            | 0.977    | 0.972     | 0.983  | 0.977    | 0.997   |
| 4           | 10           | 0.979    | 0.971     | 0.987  | 0.979    | 0.998   |

### **Combining Both Best Hypothesised Fine-Tuning Methods Experiment**
| Experiment  | Number of Tree | Number of cross-validation folds (k) | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
| ----------- | -------------- | -------------- | -------- | --------- | ------ | -------- | ------- |
| 5           | 1000           | 10 | 0.980    | 0.972     | 0.989  | 0.980    | 0.998   |

