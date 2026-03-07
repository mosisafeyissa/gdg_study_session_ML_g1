# Ride Price Estimation System

## Project Overview

This project is a **Machine Learning mini-project** designed to estimate ride prices for trips in Ethiopia. The goal was to build an end-to-end ML workflow:

1. Design and prepare a dataset
2. Clean and engineer features
3. Train regression and classification models
4. Evaluate model performance
5. Reflect on ethical and practical considerations

The focus was **learning the ML process** rather than maximizing accuracy, using only tools learned in Semester One (NumPy, Pandas, Matplotlib, and basic sklearn models).


## Dataset Description

Since there is no publicly available dataset, a **synthetic dataset** was created with 150 rows, including both **numerical and categorical features**.

**Features:**

| Feature         | Type        | Description / Justification                                     |
| --------------- | ----------- | --------------------------------------------------------------- |
| `distance_km`   | Numeric     | Trip distance in kilometers — longer rides cost more            |
| `duration_min`  | Numeric     | Trip duration in minutes — longer trips slightly increase price |
| `time_of_day`   | Categorical | Morning, Afternoon, Evening, Night — affects traffic patterns   |
| `traffic_level` | Categorical | Low, Medium, High — heavy traffic increases ride price          |
| `weather`       | Categorical | Clear, Rain — rain increases fare slightly due to slower trips  |
| `demand_level`  | Categorical | Low, Medium, High — high demand increases price                 |
| `city`          | Categorical | Addis Ababa, Adama, Hawassa, Bahir Dar — fares vary by city     |
| `is_weekend`    | Categorical | 0 = weekday, 1 = weekend — weekend rides may be more expensive  |
| `base_fare`     | Numeric     | Randomized base fare (100–130 ETB) — fixed minimum charge       |
| `ride_price`    | Numeric     | Continuous target variable — calculated from features           |
| `high_cost`     | Binary      | Derived binary target for classification (1 = high-cost ride)   |

**Feature Choices:**
All features were chosen because they **logically affect ride price** in real-world Ethiopian ride services.

* Example: longer distance and high demand → higher price.
* Example of a feature considered but not included: **driver rating** — not all rides would have this consistently, so it was left out for simplicity.


## How to Run the Notebook

1. Clone the repository:

```bash
git clone https://github.com/mosisafeyissa/gdg_study_session_ML_g1.git
cd ride-price-ml
```

2. Open the Jupyter Notebook:

```bash
notebook/ride_price_model.ipynb
```

3. Make sure you have the required Python packages:

```bash
pip install numpy pandas matplotlib scikit-learn
```

4. Run all cells sequentially — the notebook contains:

* Data exploration and visualization
* Data cleaning and feature engineering
* Linear Regression model for price prediction
* Logistic Regression model for high-cost classification
* Evaluation, comparison, and ethical reflections

---

## Key Findings

* **Regression model**: accurately predicts continuous ride prices; MSE and R² show good performance on synthetic data.
* **Classification model**: successfully identifies high-cost rides with high accuracy; confusion matrix shows correct classification patterns.
* **Most influential features**: `distance_km`, `duration_min`, `traffic_level`, and `demand_level`.
* **Ethical considerations**: surge pricing may unfairly affect riders in certain conditions; careful monitoring is required.
* **Limitations**: dataset is synthetic, limited to 150 rows, and does not fully capture real-world variability in Ethiopia.

---

## Repository Structure

```
ride-price-ml/
│── data/
│   └── rides.csv           # Synthetic dataset
│── notebook/
│   └── ride_price_model.ipynb   # Jupyter Notebook
│── README.md               # Project overview and instructions
```
