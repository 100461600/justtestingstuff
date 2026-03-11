# 🏦 Bank Deposit Subscription Prediction

> UC3M · 2025-26 · Aprendizaje Automático — Primera Práctica

---

## 👥 Authors

| Name | NIA |
|------|-----|
| Mohammadali Hassani | 100461600 |
| Alessandro Jerry Gever Alemu | 100461651 |

---

## 📌 Project Overview

This project aims to predict whether a bank client will subscribe to a term deposit (`deposit` variable), using demographic, financial, and interaction data. The full ML pipeline is covered: exploratory analysis, preprocessing, model selection, hyperparameter tuning, evaluation, and deployment.

---

## 📂 Repository Structure

```
├── notebook_main.ipynb          # EDA, preprocessing, HPO, model selection
├── notebook_predictions.ipynb   # Load final model & generate competition predictions
├── mystreamlit.py               # Streamlit deployment app
├── modelo_final.joblib          # Saved final model pipeline
├── predicciones.csv             # Predictions on competition dataset
├── data/
│   ├── bank_00.pkl              # Main dataset (training & evaluation)
│   └── bank_competition_00.pkl  # Competition dataset (no target variable)
└── README.md
```

---

## 🔧 Methods Used

- **Baseline:** Dummy classifier
- **Basic:** K-Nearest Neighbors (KNN), Decision Trees
- **Advanced:** Logistic Regression (plain & L1), Support Vector Machines (SVM)
- **Open task:** TBD

---

## ⚙️ Setup & Requirements

```bash
pip install numpy pandas scikit-learn matplotlib seaborn streamlit joblib
```

Run the Streamlit app:

```bash
streamlit run mystreamlit.py
```

---

## 🌱 Reproducibility

All results use a fixed random seed:

```python
SEED = 100461600
```

---

## 📊 Dataset

The dataset contains client demographic, financial, and campaign interaction variables. Target variable: `deposit` (yes/no).

| Variable | Description |
|----------|-------------|
| `age` | Client age in years |
| `job` | Type of job |
| `marital` | Marital status |
| `education` | Education level |
| `default` | Has credit in default? |
| `balance` | Average annual balance |
| `housing` | Has housing loan? |
| `loan` | Has personal loan? |
| `contact` | Contact communication type |
| `day_of_week` | Last contact day of week |
| `month` | Last contact month |
| `duration` | Last contact duration (seconds) |
| `campaign` | Number of contacts this campaign |
| `pdays` | Days since last contact (-1 = never contacted) |
| `previous` | Contacts before this campaign |
| `poutcome` | Previous campaign outcome |
| `deposit` | **Target:** subscribed to deposit? |
