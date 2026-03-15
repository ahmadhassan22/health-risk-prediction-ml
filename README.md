# Health Risk Prediction using Machine Learning

This project builds a machine learning pipeline to predict whether an individual is **Healthy or Unhealthy** based on lifestyle and medical indicators.

The goal is to demonstrate a **complete supervised machine learning workflow**, including data preprocessing, model training, hyperparameter tuning, ensemble methods, and evaluation.

---

# Problem Statement

Early identification of health risks can help individuals take preventive action and assist healthcare professionals in decision making.

This project trains multiple machine learning models to classify a person's health status based on input features such as lifestyle, diet, and biological indicators.

---

# Machine Learning Pipeline

The project follows a full ML workflow:
Data Loading
↓
Data Cleaning
↓
Exploratory Data Analysis (EDA)
↓
Feature Engineering
↓
Train-Test Split
↓
Feature Scaling (RobustScaler)
↓
Model Training
↓
Hyperparameter Tuning (GridSearchCV)
↓
Ensemble Learning
↓
Model Evaluation
↓
Final Model Selection


---

# Dataset

Dataset: **Novagen Health Dataset**

The dataset contains health-related features such as:

- Lifestyle indicators
- Medical attributes
- Dietary patterns
- Biological measures

Target variable:
0 → Healthy
1 → Unhealthy


---

# Models Implemented

The following supervised learning models were trained and evaluated:

- Logistic Regression
- Decision Tree Classifier
- Bagging Classifier
- AdaBoost Classifier
- Gradient Boosting Classifier
- Support Vector Classifier (SVC)

---

# Model Performance Comparison

| Model | Test Accuracy |
|------|---------------|
| Logistic Regression | 0.82 |
| Decision Tree | 0.90 |
| Bagging | 0.94 |
| Gradient Boosting | 0.92 |
| AdaBoost | 0.83 |
| **Support Vector Classifier** | **0.9466** |

**Best Model:** Support Vector Classifier (SVC)

---

# Model Evaluation

The final model was evaluated using:

- Confusion Matrix
- ROC Curve
- ROC-AUC Score

These metrics confirm that the model provides strong classification performance with good generalization.

---

# Example Visualization

The project includes:

- Feature distribution plots
- Boxplots for outlier detection
- Correlation heatmap
- Confusion matrix
- ROC curve

---

# Confusion Matrix


# Technologies Used

- Python
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Joblib

---

# Project Structure
health-risk-prediction-ml/

│

├── novagen_dataset.csv
├── novagen_health_risk_classifier.ipynb

│

├── health_prediction_model.pkl
├── scaler.pkl

│

├── README.md
├── requirements.txt
└── .gitignore


---

# How to Run the Project

Clone the repository:
git clone https://github.com/ahmadhassan22/health-risk-prediction-ml.git


Install dependencies:
pip install -r requirements.txt


Run the notebook to reproduce the results.

---

# Model Deployment

The trained model and scaler are saved using **Joblib**, allowing the model to be reused for predictions without retraining.

Example prediction function:

python
def predict_health(data):
    data_scaled = scaler.transform([data])
    prediction = svc.predict(data_scaled)[0]
    return "Healthy" if prediction == 0 else "Unhealthy"

# Future Improvements

Possible extensions include:

Model explainability using SHAP

Deployment as a FastAPI REST API

Building a web interface for predictions

Hyperparameter optimization with RandomSearchCV

Adding more datasets for improved generalization

# Author

Ahmad Hassan
Master’s Student — AI & NLP
Harbin Institute of Technology, Shenzhen
