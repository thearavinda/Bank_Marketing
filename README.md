#  Bank Marketing Prediction with Machine Learning

This project focuses on building a classification model to **predict whether a customer will subscribe to a term deposit** based on their responses to a direct marketing campaign. The dataset is imbalanced and includes both numerical and categorical features.

---

##  Dataset

- **Source**: UCI Machine Learning Repository  
- **Datasetlink**:https://archive.ics.uci.edu/dataset/222/bank+marketing
  
---

##  Feature Overview

The dataset contains 41,188 records and the following features:

###  Client Information
- `age`: Age of the client (numeric)
- `job`: Type of job (categorical)
- `marital`: Marital status (categorical)
- `education`: Education level (categorical)
- `default`: Has credit in default? (`yes`, `no`, `unknown`)
- `housing`: Has housing loan? (`yes`, `no`, `unknown`)
- `loan`: Has personal loan? (`yes`, `no`, `unknown`)

###  Last Contact Info (During Campaign)
- `contact`: Type of communication (`cellular`, `telephone`)
- `month`: Last contact month (`jan` to `dec`)
- `day_of_week`: Last contact day of the week
- `duration`: Last contact duration in seconds (numeric)

> 

###  Campaign-Related
- `campaign`: Number of contacts during this campaign
- `pdays`: Days since client was last contacted (999 means not previously contacted)
- `previous`: Number of contacts performed before this campaign
- `poutcome`: Outcome of the previous marketing campaign

###  Social and Economic Indicators
- `emp.var.rate`: Employment variation rate
- `cons.price.idx`: Consumer price index
- `cons.conf.idx`: Consumer confidence index
- `euribor3m`: Euribor 3-month rate
- `nr.employed`: Number of employees

---

##  Project Workflow

1. **Data Preprocessing**
   - Handled `unknown` values in categorical features
   - Removed duplicate records
   - Detected and clipped outliers using IQR
   - Label encoding for binary columns and one-hot encoding for others

2. **Exploratory Data Analysis**
   - Visualizations:
     - Pairplot for numerical relationships
     - Violin plot of age vs job vs deposit
     - Boxplots comparing age and duration by deposit outcome
   - Detected class imbalance

3. **Train-Test Split**
   - Used `train_test_split()` with stratification on the target variable

4. **Handling Imbalance**
   - Applied **SMOTE (Synthetic Minority Over-sampling Technique)** on the training data

5. **Model Building**
   -  Logistic Regression  
   -  Decision Tree  
   -  Random Forest

6. **Evaluation Metrics**
   - Accuracy
   - Precision, Recall, F1 Score
   - Confusion Matrix
   - Classification Report

---

##  Results Summary

| Model                  | Accuracy |
|------------------------|----------|
| Logistic Regression    | ~83.8%   |
| Decision Tree          | ~85.9%   |
| **Random Forest**      | **~89.7%** |

>  **Random Forest** outperformed the other models on test data after balancing with SMOTE.

---

## 🛠 Tools & Libraries Used

- Python
- Pandas, NumPy
- Scikit-learn
- imbalanced-learn (SMOTE)
- Matplotlib, Seaborn

---



