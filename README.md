# Machine Failure Prediction Using Random Forest

## 📌 Overview
This project focuses on predicting machine failures using sensor data. The goal is to analyze various factors such as **temperature, vibration, pressure, and humidity** to determine if a machine is likely to fail.

## 📂 Dataset
- **Features:**
  - Temperature(°C)
  - Vibration(Hz)
  - Pressure(bar)
  - Humidity(%)
  - Timestamp (Categorical)
  - Machine_ID (Categorical)
  - Failure_Status (Target Variable: 0 - No Failure, 1 - Failure)

## 🛠️ Data Preprocessing & Feature Engineering
- **Handling Missing Data:**
  - Dropped columns with more than 50% missing values
  - Filled missing numerical values with the median
  - Filled missing categorical values with the mode
- **Feature Encoding:**
  - Converted categorical columns using Label Encoding & One-Hot Encoding
- **Scaling & Normalization:**
  - Applied StandardScaler to numerical features

## 📊 Model Training & Tuning
- **Baseline Model:** Random Forest Classifier
- **Hyperparameter Tuning:** Performed GridSearchCV with 5-fold cross-validation
- **Best Parameters Found:**
  ```
  max_depth: 10
  min_samples_leaf: 1
  min_samples_split: 5
  n_estimators: 100
  ```
- **Final Model Performance:**
  | Metric | Value |
  |--------|--------|
  | Accuracy | 97% |
  | Precision | 99% (Class 0), 82% (Class 1) |
  | Recall | 98% (Class 0), 90% (Class 1) |
  | F1-Score | 98% (Class 0), 86% (Class 1) |

## 📈 Results & Insights
- The model performs well, achieving **97% accuracy**.
- Precision and recall are high, meaning the model can effectively predict failures.
- Feature importance analysis (SHAP) showed **Vibration and Temperature** as key factors.
- Confusion matrix & ROC curve analysis confirmed the model's reliability.

## 🚀 Deployment (Optional)
This model can be deployed as:
1. **Streamlit Web App** for interactive predictions
2. **Flask/FastAPI API** for integration with other systems
3. **Dockerized & Deployed on Cloud (AWS/GCP/Azure)**

## 📌 Future Improvements
🔹 Try deep learning models like LSTMs for time-series predictions.  
🔹 Optimize feature selection for even better performance.  
🔹 Deploy the model in real-time industrial settings.  

## 📜 References
- Sensor failure prediction research papers
- Random Forest algorithm documentation
- SHAP for interpretability



