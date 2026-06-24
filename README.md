# HexSoftwares_Heart_Disease_Detection-Model
Task 2,  Project 02 Heart Disease Detection

# Heart Disease Detection using Machine Learning and Deep Learning

## Project Overview

This project is developed as part of the **Hex Softwares Machine Learning Internship Program**. The goal of this project is to build a **Heart Disease Detection Model** that can analyze medical attributes of a patient and detect whether heart disease is likely to be present.

The notebook uses both **Machine Learning** and **Deep Learning** approaches and compares their performance using standard classification metrics.

> **Note:** This project is for learning and internship demonstration purposes only. It should not be used as a real medical diagnosis system.

---

## Objective

The main objective of this project is to:

- Load and inspect a heart disease dataset
- Clean and preprocess the data
- Perform exploratory data analysis
- Train multiple ML and DL classification models
- Evaluate all models using accuracy, precision, recall, F1-score, classification report, and confusion matrix
- Compare model performance
- Analyze feature importance
- Build a simple detection system
- Save the best model and supporting files

---

## Dataset Information

The dataset used in this project is `dataset_heart.csv`.

### Dataset Shape

| Property | Value |
|---|---:|
| Rows | 270 |
| Columns | 14 |
| Input Features | 13 |
| Target Column | `heart_disease` |
| Problem Type | Binary Classification |
| Missing Values | 0 |
| Duplicate Rows | 0 |

### Features Used

The dataset contains the following medical attributes:

- `age`
- `sex`
- `chest_pain_type`
- `resting_blood_pressure`
- `serum_cholesterol`
- `fasting_blood_sugar`
- `resting_ecg`
- `max_heart_rate`
- `exercise_angina`
- `oldpeak`
- `st_segment`
- `major_vessels`
- `thal`
- `heart_disease`

### Target Mapping

The original target column had values:

- `1`
- `2`

For binary classification, the target was converted into:

| Original Value | Converted Value | Meaning |
|---:|---:|---|
| 1 | 0 | No Heart Disease |
| 2 | 1 | Heart Disease |

### Class Distribution

| Class | Count | Percentage |
|---|---:|---:|
| No Heart Disease | 150 | 55.56% |
| Heart Disease | 120 | 44.44% |

The dataset is fairly balanced for a binary classification project.

---

## Exploratory Data Analysis

The notebook includes visual analysis for:

- Target class distribution
- Age distribution
- Gender-wise heart disease count
- Chest pain and heart disease relationship
- Cholesterol distribution
- Correlation heatmap

These visualizations help understand the relationship between patient health features and heart disease status.

---

## Data Preprocessing

The preprocessing steps include:

- Cleaning column names
- Renaming unclear column names
- Checking missing values
- Checking duplicate values
- Converting target labels into `0` and `1`
- Separating input features and target variable
- Splitting data into training and testing sets
- Applying `StandardScaler` for scaled models

The data was split into:

| Split | Shape |
|---|---|
| Training Features | `(216, 13)` |
| Testing Features | `(54, 13)` |
| Training Target | `(216,)` |
| Testing Target | `(54,)` |

---

## Models Used

This project uses **5 Machine Learning models** and **2 Deep Learning models**.

### Machine Learning Models

1. Logistic Regression
2. K-Nearest Neighbors Classifier
3. Support Vector Classifier
4. Random Forest Classifier
5. XGBoost Classifier

### Deep Learning Models

6. Artificial Neural Network (ANN) / Multi-Layer Perceptron (MLP)
7. Deep Neural Network

---

## Model Evaluation Metrics

Each model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Classification Report
- Confusion Matrix

---

## Model Performance Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.8519 | 0.7857 | 0.9167 | 0.8462 |
| Artificial Neural Network / MLP | 0.8519 | 0.7857 | 0.9167 | 0.8462 |
| Support Vector Classifier | 0.8148 | 0.7692 | 0.8333 | 0.8000 |
| XGBoost Classifier | 0.8148 | 0.7692 | 0.8333 | 0.8000 |
| Random Forest Classifier | 0.8148 | 0.7692 | 0.8333 | 0.8000 |
| K-Nearest Neighbors | 0.7963 | 0.7241 | 0.8750 | 0.7925 |
| Deep Neural Network | 0.5370 | 0.4894 | 0.9583 | 0.6479 |

---

## Best Performing Model

The best model based on the notebook output was:

| Best Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.8519 | 0.7857 | 0.9167 | 0.8462 |

The Artificial Neural Network / MLP achieved the same accuracy and F1-score, but Logistic Regression was selected as the best model because it is simpler, faster, and easier to interpret for a small tabular medical dataset.

---

## Feature Importance Analysis

Feature importance was analyzed using:

- Random Forest Classifier
- XGBoost Classifier

### Important Features from Random Forest

Top important features included:

1. `chest_pain_type`
2. `max_heart_rate`
3. `thal`
4. `major_vessels`
5. `oldpeak`

### Important Features from XGBoost

Top important features included:

1. `thal`
2. `chest_pain_type`
3. `major_vessels`
4. `exercise_angina`
5. `oldpeak`

These results show that chest pain type, thalassemia, number of major vessels, exercise-induced angina, and oldpeak are strong indicators in the detection task.

---

## Detection System

The notebook also includes a simple detection system where sample patient data is passed into the trained model. The system returns one of the following results:

- No Heart Disease Detected
- Heart Disease Detected

Example manual patient data in the notebook produced:

```text
Heart Disease Detected
```

---

## Saved Outputs

The notebook saves important project outputs inside the folder:

```text
heart_disease_prediction_outputs
```

---


## Author

**Fani2323**  
Machine Learning Intern  
Hex Softwares Internship Program
Computer Science Student
---

