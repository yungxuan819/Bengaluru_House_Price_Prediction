# 🏠 Bengaluru House Price Prediction

A machine learning project that predicts **residential property prices in Bengaluru, India** using real estate listing data. Covers the full pipeline from data cleaning and feature engineering to model training and evaluation.

---

## 📁 Project Structure

```
Bengaluru_House_Price_Prediction/
│
├── Bengaluru_House_Price_Prediction.ipynb   # Main notebook: cleaning, EDA & ML models
└── Bengaluru_House_Data.csv                 # Dataset: ~13,000 property listings
```

---

## 📊 Dataset

The dataset contains approximately **13,000 residential property listings** from Bengaluru with the following features:

| Column | Description |
|--------|-------------|
| `area_type` | Type of area (Super built-up, Plot, Built-up, Carpet Area) |
| `availability` | Move-in availability (date or "Ready to Move") |
| `location` | Neighbourhood / locality in Bengaluru |
| `size` | Number of bedrooms (e.g. "2 BHK", "3 Bedroom") |
| `society` | Name of the housing society |
| `total_sqft` | Total area in square feet |
| `bath` | Number of bathrooms |
| `balcony` | Number of balconies |
| `price` | Property price in lakhs (target variable) |

Source: [Bengaluru House Price Data — Kaggle](https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data)

---

## 🔍 Project Overview

### Data Cleaning
- Handling missing values across location, size, and bath columns
- Parsing the `size` column to extract a uniform bedroom count
- Handling non-numeric and range-based values in `total_sqft` (e.g. "1000–1200")
- Removing outliers using price-per-sqft analysis and BHK-based logic
- Reducing high-cardinality in `location` by grouping rare localities into "other"

### Exploratory Data Analysis (EDA)
- Price distribution across locations and property sizes
- Price per square foot comparisons across neighbourhoods
- Correlation between features and house prices

### Prediction Models
- Regression models trained to predict property price (in lakhs)
- Feature engineering including `price_per_sqft`
- Model selection and evaluation using cross-validation and metrics such as R²

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook

### Installation

```bash
git clone https://github.com/yungxuan819/Bengaluru_House_Price_Prediction.git
cd Bengaluru_House_Price_Prediction
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Run

```bash
jupyter notebook Bengaluru_House_Price_Prediction.ipynb
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| pandas | Data cleaning & manipulation |
| NumPy | Numerical operations |
| matplotlib / seaborn | Data visualizations |
| scikit-learn | ML models & evaluation |
| Jupyter Notebook | Development environment |
