# Health Classification 🏥

A minor machine learning project dedicated to classifying an individual's health status (Healthy or Unhealthy) based on various medical and lifestyle features. 

## 🎯 Project Objective
The goal of this project is to build a robust diagnostic tool using supervised machine learning algorithms. By analyzing multiple health indicators, the models predict whether an individual falls into a healthy or unhealthy category, focusing heavily on minimizing false negatives (prioritizing high Recall).

## 📊 Dataset Features
The dataset encompasses several key health indicators and lifestyle choices, including:
- **Demographics:** Age
- **Physical Metrics:** BMI (Body Mass Index)
- **Vitals & Blood Work:** Blood Pressure, Cholesterol, Glucose Level, Heart Rate, Blood Group
- **Lifestyle Factors:** Sleep Hours, Exercise Hours, Stress Level, Diet Type (Vegan, Vegetarian)

## 🛠️ Methodology & Machine Learning Approach

### 1. Data Preprocessing
- **Label Encoding:** Applied to categorical features such as Diet Type and Blood Group.
- **Feature Scaling:** `StandardScaler` was used to standardize continuous numerical variables to optimize distance-based algorithms and ensure stable convergence.
- **Data Splitting:** 80% for training and 20% for testing.

### 2. Base Models Evaluated
- Logistic Regression
- Gaussian Naive Bayes
- Decision Tree Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Classifier (SVC)

### 3. Ensemble Techniques
To improve generalization and performance, advanced ensemble models were constructed and compared:
- **Heterogeneous Ensembles:** Stacking Classifier, Voting Classifier
- **Bagging Methods:** Random Forest, Bagging Classifier
- **Boosting Methods:** Gradient Boosting Classifier, AdaBoost Classifier

## 📈 Evaluation & Results
All models were evaluated using multiple metrics including Accuracy, Precision, Recall, F1-Score, and Confusion Matrix. 

In healthcare diagnostic models, avoiding "false negatives" (failing to identify an unhealthy person) is critical. Therefore, **Recall** was treated as the primary metric, with **Precision** as the secondary metric.

**Results:** The **Stacking Classifier** yielded the best overall performance based on Recall and Precision, making it the most reliable model for this health classification task.

## 💻 Tech Stack & Requirements
- **Language:** Python
- **Libraries:** `pandas`, `scikit-learn`

## 🚀 How to Run
1. Ensure all required libraries are installed (`pip install pandas scikit-learn`).
2. Run the `health_classification.ipynb` notebook to execute the preprocessing steps, train the algorithms, and view the comparative metrics.
