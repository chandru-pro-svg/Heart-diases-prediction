# 🩺 Stroke Risk Estimator

An interactive machine-learning web application that estimates the probability of stroke based on patient demographics and clinical parameters using a trained **Logistic Regression** model. The tool provides real-time risk assessment alongside feature-level log-odds contributions to interpret what factors influence each prediction.

---

## 🌐 Live Demo

👉 https://heartprediction.vercel.app

---

## 📌 Project Overview

Early identification of stroke risk factors allows for timely clinical lifestyle interventions. This web application bridges machine learning with an accessible clinical screening interface.

Users can input key physiological metrics and patient demographics, or select pre-configured presets (**Average risk** / **High risk**), to instantly receive:
- **Estimated Risk Percentage:** Displayed via an interactive visual gauge.
- **Risk Stratification:** Clear flags (e.g., *High risk* with clinical review recommendation).
- **Explainable Predictions:** Breakdown of factors that moved the score via directional log-odds contributions (red bars indicate increased risk, green bars indicate protective/lower risk factors).

---

## ⚙️ Input Features

The underlying model evaluates the following patient attributes:

| Category | Feature | Description / Range |
| :--- | :--- | :--- |
| **Demographics** | **Age** | Patient age in years |
| | **Gender** | Male / Female |
| | **Ever Married** | Marital history (Yes / No) |
| | **Residence** | Geographic classification (Urban / Rural) |
| **Clinical History** | **Hypertension** | Diagnosed high blood pressure (Yes / No) |
| | **Heart Disease** | History of pre-existing heart condition (Yes / No) |
| | **Avg Glucose Level** | Average blood glucose level ($mg/dL$) |
| | **BMI** | Body Mass Index ($kg/m^2$) |

---

## 🛠️ Tech Stack & Architecture

- **Machine Learning:** Python, Scikit-Learn (Logistic Regression classifier)
- **Model Serialization:** Pickle (`stroke_model.pkl`)
- **Frontend / UI:** HTML5, CSS3, Modern Responsive JavaScript (with interactive gauge and dynamic risk breakdown bars)
- **Hosting & Deployment:** [Vercel](https://vercel.com)

---

## 📂 Repository Structure

```text
├── index.html          # Interactive frontend application & UI logic
├── stroke_model.pkl    # Serialized pre-trained Logistic Regression model
└── README.md           # Project documentation
