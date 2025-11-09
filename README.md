# 📊 Subscription Prediction for Banking Offers

## 🎯 Objective

This project builds a supervised classification model to predict whether a customer will subscribe to a **term deposit** after a bank's telemarketing campaign.  
We utilize the **Bank Marketing UCI dataset** and the **PyCaret** library, enabling rapid AutoML modeling and streamlined comparison of algorithms[web:25][web:28][web:30].

---

## 📦 Project Contents

- `exploration.ipynb` — Exploratory analysis
- `modelisation.ipynb` — Model training and evaluation using PyCaret
- `README.md` — This documentation

---

## 📚 Part 1 – Machine Learning Concepts

### Key Terms in Supervised Learning

- **Supervised learning** — Learning from labeled data (known target values)
- **Labeled data** — Data with known answers (e.g., “yes” or “no” for subscription)
- **Supervised classification** — Predicting discrete categories (subscribed or not)
- **Model** — Algorithm trained to detect data patterns and predict outcomes
- **Training data** — Dataset used to fit models
- **Target** — The outcome to be predicted (`y`)
- **Training phase** — Model learns pattern from labeled data
- **Prediction phase** — Model forecasts outcomes for new samples
- **Preprocessing** — Cleaning, imputing missing data, encoding categorical variables
- **Accuracy** — Percentage of correctly predicted labels
- **AutoML** — Automated model selection, tuning, and benchmarking
- **Decision tree** — Common classification algorithm using “if...then...” rules

---

## 📊 Part 2 – Data Analysis

### Dataset Overview

The dataset describes contacts with clients during telemarketing campaigns by a Portuguese bank[web:25][web:28][web:31]:

| Column      | Description                                  |
|:------------|:---------------------------------------------|
| age         | Client’s age                                 |
| job         | Occupation                                   |
| marital     | Marital status                               |
| education   | Education level                              |
| balance     | Account balance                              |
| contact, month, duration | Campaign details                |
| poutcome    | Outcome of previous campaign                 |
| y           | Target: subscription to term deposit (yes/no)|

### Preprocessing Steps

- Replaced `unknown` values with `NaN`
- Dropped rows with missing values
- Automatically encoded categorical variables with PyCaret

### Exploratory Findings (see `exploration.ipynb`)

- Target distribution is imbalanced (majority are “no”)
- Typical subscriber profile: 30–60 years old
- Higher subscription rates among students, retirees, and executives

---

## ⚙️ Part 3 – Modeling with PyCaret

### Tool

[PyCaret](https://pycaret.gitbook.io/docs/) is a Python AutoML library ideal for rapid model testing and selection.

### Workflow

1. Initialize PyCaret with `setup()`
2. Use `compare_models()` for automated benchmarking
3. Select top-performing model by accuracy
4. Finalize and test predictions

### Results

The best performing model (e.g. `RandomForestClassifier` or `GradientBoostingClassifier`) achieved **over 85% accuracy**.  
It reliably predicts client subscription for most cases.

---

## 🧠 Conclusion

This project demonstrates:
- Core supervised learning workflow
- Real-world dataset cleansing and exploration
- PyCaret-accelerated modeling and comparison
- Deployment of an effective subscription prediction tool

With these insights, banks can **target marketing campaigns** more efficiently and increase conversion rates.

---

## 📚 Resources

- [PyCaret Documentation](https://pycaret.gitbook.io/docs)
- [StatQuest: ML Introduction](https://www.youtube.com/watch?v=Gv9_4yMHFhI)
- [DataCamp Blog: Classification Intro](https://www.datacamp.com/blog/classification-machine-learning)
