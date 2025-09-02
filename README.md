# ❤️ Heart Disease Predictor

A Machine Learning project built using Logistic Regression to predict the presence of heart disease based on patient medical data.

---

## 📊 Project Overview

This project uses the UCI Heart Disease dataset to train a binary classification model that predicts whether a person has heart disease or not, based on various health metrics.

---

## 🧠 Model Used

- **Logistic Regression** – a supervised learning algorithm used for binary classification tasks.

---

## 📁 Dataset Description

The dataset consists of 303 records and 14 columns:

| Feature | Description |
|---------|-------------|
| age | Age in years |
| sex | Sex (1 = male; 0 = female) |
| cp | Chest pain type (0–3) |
| trestbps | Resting blood pressure (mm Hg) |
| chol | Serum cholesterol (mg/dl) |
| fbs | Fasting blood sugar > 120 mg/dl (1 = true; 0 = false) |
| restecg | Resting ECG results (0–2) |
| thalach | Maximum heart rate achieved |
| exang | Exercise-induced angina (1 = yes; 0 = no) |
| oldpeak | ST depression induced by exercise |
| slope | Slope of peak exercise ST segment (1–3) |
| ca | Number of major vessels (0–3) |
| thal | Thalassemia (3 = normal; 6 = fixed defect; 7 = reversible defect) |
| target | Heart disease (1 = yes; 0 = no) |

---

## ✅ Steps Performed

1. **Data Loading and Exploration**
   - Loaded dataset using `pandas`
   - Checked for missing values and understood data distribution using `.info()` and `.describe()`

2. **Data Preprocessing**
   - Separated features and labels
   - Split dataset into training and testing sets (80:20 ratio)

3. **Model Training**
   - Used `LogisticRegression` from `scikit-learn`
   - Trained on 242 records
   - Handled convergence warning by analyzing solver and scaling suggestions

4. **Model Evaluation**
   - Achieved **Training Accuracy:** 83.88%
   - Achieved **Testing Accuracy:** 80.32%
   - Used `accuracy_score` for evaluation

5. **Prediction System**
   - Built a prediction function that takes user input and returns the result

---

## 🧪 Example Prediction

```python
input_data = (51, 1, 3, 125, 213, 0, 0, 125, 1, 1.4, 2, 1, 2)
input_data = np.asarray(input_data).reshape(1, -1)
prediction = model.predict(input_data)

if prediction[0] == 0:
    print("✅ Good News: The patient does not have heart disease.")
else:
    print("⚠️ The Patient should visit the doctor.")
