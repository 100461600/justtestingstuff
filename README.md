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
P1_AA_Mohammadali_Alessandro/
├── data/
│   ├── bank_00.pkl                  # Main dataset (training & evaluation)
│   └── bank_competition.pkl         # Competition dataset (no target variable)
├── notebooks/
│   ├── 01_EDA.ipynb                 # EDA, preprocessing, HPO, model selection
│   └── 02_predictions.ipynb         # Load final model & generate competition predictions (TO DO)
├── mystreamlit.py                   # Streamlit deployment app (TO DO)
├── modelo_final.joblib              # Saved final model pipeline (TO DO)
├── predicciones.csv                 # Predictions on competition dataset (TO DO)
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

---

## 📓 Notebooks

### `01_EDA.ipynb`
Covers the full analysis pipeline:
- Simplified EDA (variable types, missing values, cardinality, class balance)
- Special analysis of `pdays` variable
- Evaluation strategy (train/test split, metric choice, inner CV)
- KNN & Decision Trees (default + HPO)
- Linear Models & SVMs (default + HPO)
- Final model selection & evaluation on test set
- Competition predictions

### `02_predictions.ipynb` *(coming soon)*
Loads `modelo_final.joblib` and `bank_competition.pkl`, runs predictions, saves `predicciones.csv`.

---

## 🌐 Streamlit App *(coming soon)*

A web interface allowing bank managers to input client data and get a deposit subscription prediction in real time.

```bash
streamlit run mystreamlit.py
```

---

## 📅 Progress

- [x] Repository setup
- [x] Data loaded
- [ ] EDA completed
- [ ] Evaluation strategy defined
- [ ] KNN & Trees
- [ ] Linear Models & SVMs
- [ ] Final model selected & saved
- [ ] Competition predictions generated
- [ ] Streamlit app deployed
- [ ] Open task completed
