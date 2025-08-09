#  Bank Marketing Campaign Prediction – Deep Learning Project

## 📌 Project Overview
This project predicts whether a customer will subscribe to a term deposit after a marketing campaign using the **Bank Marketing dataset**.  
A complete **data science pipeline** was implemented — from data cleaning & exploratory analysis to feature engineering and building a deep learning model.

---

##  Workflow Summary

### **1. Exploratory Data Analysis (EDA)**
- Removed duplicates to avoid bias.
- Replaced `unknown` values in categorical features with the mode of the respective column.
- Removed redundant columns that did not contribute to the prediction.
- Created a **visualization class** with:
  - `countplot` for class distribution.
  - `histogram` and `boxplot` methods for outlier detection.
- Removed outliers using the **IQR method**.
- Created a **heatmap** to find correlations between features.

### **2. Data Preprocessing**
- Encoded categorical features into numerical format.
- Applied **train-test split**.
- Scaled numerical features.
- Applied **SMOTE** to balance the dataset.

### **3. Model Building – Deep Learning**
- Implemented a **Keras Sequential** model with:
  - Multiple Dense layers.
  - Dropout layers to prevent overfitting.
  - Sigmoid activation for binary classification.
- Used **binary cross-entropy loss** and the **Adam optimizer**.
- Applied **EarlyStopping** to avoid overfitting.
- Achieved strong performance with balanced accuracy.

### **4. Model Evaluation**
- Generated accuracy & loss curves for training and validation sets.
- Created a **confusion matrix** and **classification report** for performance assessment.
- Evaluated the model using:
  - **Accuracy score**
  - **Precision, Recall, F1-score**
  - **Confusion Matrix heatmap**

---

##  Project Structure

---

## 🛠️ Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Scikit-learn** (Preprocessing, SMOTE, Evaluation Metrics)
- **Keras / TensorFlow** (Deep Learning Model)
- **Matplotlib / Seaborn** (Data Visualization)

---

## 📊 Dataset
The dataset comes from the [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing).  
It contains information on marketing campaigns of a Portuguese banking institution, including:
- Client demographics
- Past campaign outcomes
- Contact details
- Socio-economic indicators

Target variable:  
`y` → **Yes** (subscribed) / **No** (not subscribed) to term deposit.




