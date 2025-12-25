# AI Task 1 – Machine Failure Prediction (Mini ML Implementation)

## Objective
The objective of this task is to predict whether an industrial machine operation will result in failure or not using classical machine learning techniques.  
The focus of this implementation is on correctness, clarity, explainability, and proper evaluation rather than model complexity.

---

## Problem Type
- Supervised Learning
- Binary Classification

Target Variable:
- `Target`  
  - 1 → Machine Failure  
  - 0 → No Failure

---

## Dataset Description
The dataset consists of approximately 10,000 rows of industrial machine operation data.  
Each row represents a single operation and includes:

- Machine/Product Type (categorical)
- Process measurements:
  - Air temperature
  - Process temperature
  - Rotational speed
  - Torque
  - Tool wear time
- Failure indicator (target variable)
- Failure description (text)

The dataset is hosted in this repository for reproducibility and ease of experimentation.

---

## Data Preprocessing
The following preprocessing steps were applied:

- Removed non-predictive identifier columns:
  - `UDI`
  - `Product ID`
- Removed `Failure Type` column to prevent target leakage.
- Numerical features were scaled using `StandardScaler`.
- Categorical feature (`Type`) was encoded using One-Hot Encoding.
- Train-test split performed using an 80:20 ratio with stratification.

---

## Model Selection
A **Logistic Regression** model was selected for this task because:

- It is well-suited for binary classification problems.
- It provides an interpretable baseline.
- It avoids unnecessary complexity.
- It strictly follows the task constraints (no deep learning, no AutoML).

---

## Model Evaluation
The model was evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

These metrics provide a balanced understanding of model performance, especially for failure prediction tasks.

---

## Results
The model achieved reasonable performance in predicting machine failures.  
Most critical functionalities were correctly classified, demonstrating that process parameters contribute meaningfully to failure prediction.

---

## Improvements & Future Work
If given more time, the following improvements could be explored:

- Handling class imbalance using resampling techniques
- Feature engineering for additional insights
- Hyperparameter tuning
- Trying other classical ML models (e.g., Random Forest)
- Incorporating time-series data if available

---

## Files in This Repository
- `AI_Task_1.ipynb` – Jupyter Notebook implementation
- `Dataset.csv` – Dataset used for training and evaluation
- `README.md` – Project documentation

---

## Author
**Yashraj Kalshetti**  
B.Tech Computer Science & Engineering (2022–2026)
