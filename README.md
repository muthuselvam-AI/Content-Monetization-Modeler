# YouTube Content Monetization Modeler

A Machine Learning project that predicts YouTube advertisement revenue based on video engagement metrics, audience behavior, and channel statistics.

---

# Project Overview

This project uses regression-based machine learning models to estimate YouTube ad revenue (`ad_revenue_usd`) using features such as:

* Views
* Likes
* Comments
* Watch Time
* Subscribers
* Video Category
* Country
* Device Type
* Engagement Rate

The project also includes:

* Data preprocessing
* Feature engineering
* Model evaluation
* Revenue prediction system
* Streamlit dashboard deployment

---

# Objectives

* Analyze factors influencing YouTube revenue
* Build a predictive machine learning model
* Compare multiple regression algorithms
* Deploy an interactive Streamlit application
* Generate actionable business insights

---

# Technologies Used

| Technology   | Purpose               |
| ------------ | --------------------- |
| Python       | Programming Language  |
| Pandas       | Data Manipulation     |
| NumPy        | Numerical Computation |
| Scikit-learn | Machine Learning      |
| Matplotlib   | Visualization         |
| Seaborn      | Data Analysis         |
| Streamlit    | Web Application       |
| Pickle       | Model Serialization   |

---

# Project Workflow

## 1. Data Collection

Dataset containing:

* Video statistics
* Audience interaction metrics
* Monetization-related attributes

---

## 2. Data Preprocessing

Performed:

* Duplicate removal
* Missing value handling
* Feature selection
* Label encoding
* Feature scaling

Example:

```python
df.drop_duplicates(inplace=True)
df.fillna(method='ffill', inplace=True)
```

---

## 3. Feature Engineering

Created a new feature:

```python
df['engagement_rate'] = (df['likes'] + df['comments']) / df['views']
```

### Why Engagement Rate?

It measures audience interaction quality and improves prediction performance.

---

## 4. Model Building

Regression algorithms used:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Support Vector Regressor (SVR)

---

## 5. Model Evaluation

Metrics used:

| Metric   | Description            |
| -------- | ---------------------- |
| R² Score | Model accuracy         |
| RMSE     | Prediction error       |
| MAE      | Average absolute error |

---

# Best Performing Model

## Random Forest Regressor

The Random Forest model achieved the best performance because it:

* Handles non-linear data effectively
* Reduces overfitting
* Captures complex feature relationships
* Works well with mixed data types

---

# Key Insights

## Features Influencing Revenue

### 1. Views

Higher views increase ad impressions and revenue.

### 2. Watch Time

Longer watch time improves monetization opportunities.

### 3. Subscribers

Channels with more subscribers generate stable traffic.

### 4. Engagement Rate

Higher audience engagement boosts video visibility and earnings.

### 5. Country

Revenue varies depending on audience geography and CPM rates.

### 6. Category

Different video categories generate different advertiser values.

---

# Business Insights

* Engagement matters more than raw popularity
* Audience retention strongly impacts revenue
* High-CPM countries improve monetization
* Subscriber growth increases revenue stability
* Content niche affects profitability

---

# Streamlit Dashboard

The project includes an interactive Streamlit web application where users can:

* Input video statistics
* Predict advertisement revenue
* Analyze monetization potential

---

# Folder Structure

```bash
YouTube-Content-Monetization-Modeler/
│
├── data/
│   └── youtube_revenue_dataset.csv
│
├── models/
│   ├── revenue_model.pkl
│   └── scaler.pkl
│
├── notebooks/
│   └── Content_Monetization_Modeler.ipynb
│
├── app.py
├── requirements.txt
├── README.md
└── outputs/
```

---

# Installation

## Clone Repository

```bash
git clone <repository-url>
cd YouTube-Content-Monetization-Modeler
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Run Streamlit Application

```bash
streamlit run app.py
```

---

# Example Prediction Workflow

1. Enter:

   * Views
   * Likes
   * Comments
   * Watch Time
   * Subscribers

2. Click Predict

3. Model returns estimated advertisement revenue.

---

# Sample Output

```text
Predicted Ad Revenue: $2450.75
```

---

# Visualizations Included

* Correlation Heatmap
* Revenue Distribution
* Feature Importance Analysis
* Scatter Plots
* Model Comparison Charts

---

# Future Enhancements

* XGBoost implementation
* Hyperparameter tuning
* SHAP Explainability
* Real-time YouTube API integration
* Advanced analytics dashboard
* Revenue forecasting system

---

# Conclusion

This project demonstrates how machine learning can help predict YouTube advertisement revenue using engagement and audience-related metrics.

The model provides valuable insights for:

* Content creators
* Marketing analysts
* Digital media strategists
* Monetization planning

The Streamlit dashboard makes the system interactive and deployment-ready.

---

# Author

Muthuselvam
