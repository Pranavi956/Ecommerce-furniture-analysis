# 🪑 E-commerce Furniture Sales Analysis (2024)

This project analyzes and predicts sales performance of furniture products listed on AliExpress using a dataset of 2,000 items.

---

## 📦 Dataset

- Source: AliExpress (scraped using Apify)
- Columns:
  - `productTitle`: name of the furniture
  - `originalPrice`: price before discount (mostly missing)
  - `price`: final selling price
  - `sold`: number of items sold (target variable)
  - `tagText`: shipping or deal-related tag

---

## 🎯 Objective

- Predict the number of furniture units sold based on product features using ML models.

---

## 🛠 Tech Stack

- **Python**, **pandas**, **scikit-learn**
- **matplotlib**, **seaborn**
- Jupyter Notebooks in VS Code

---

## 📘 Project Structure

| Notebook | Description |
|----------|-------------|
| `01_data_preprocessing.ipynb` | Clean price, handle missing values, encode tags |
| `02_exploratory_data_analysis.ipynb` | Visualize trends, correlations, distributions |
| `03_feature_engineering.ipynb` | Add discount feature, TF-IDF on product titles |
| `04_model_training_evaluation.ipynb` | Train Linear Regression and Random Forest, compare MSE and R² |

---

## 🧠 Model Results

| Model            | MSE    | R² Score |
|------------------|--------|----------|
| Linear Regression | ~860   | ~0.04    |
| Random Forest     | ~280   | ~0.69 ✅ |

---

## 📈 Key Insights

- Most products sold fewer than 10 units
- `price` and `sold` show weak correlation
- Product titles containing "sale", "off", etc. had higher performance
- Random Forest clearly outperforms Linear Regression

---

## ▶️ How to Run

1. Clone this repo
2. Install requirements:
   ```bash
   pip install -r requirements.txt

