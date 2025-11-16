# 🧠 Toronto Airbnb Price Prediction  
Predicting nightly rental prices in Toronto using machine learning & real Airbnb data.

<img src="https://img.shields.io/badge/Python-3.10+-blue.svg"> <img src="https://img.shields.io/badge/ML-XGBoost-success.svg">

---

## 🔍 Overview
This project builds an end-to-end ML pipeline to analyze and predict Airbnb prices in Toronto using the **InsideAirbnb (Oct 2025)** dataset.  
It focuses on **practical data science**, **explainable modeling**, and **real-world feature engineering**.

### ✨ Objectives
- Explore 80+ listing, host, and location-based features  
- Clean & preprocess real-world messy data  
- Engineer new features (host tenure, availability ratios, etc.)  
- Compare multiple ML models: Linear Regression, Random Forest, XGBoost  
- Explain price drivers using feature importance and evaluation metrics  

---

## 📊 Dataset
- Source: InsideAirbnb (Toronto, October 2025)
  
   👉 https://insideairbnb.com/get-the-data/
- ~21,000 listings
- 80+ raw features including:
  - Geographic data (lat/long, neighborhood)
  - Host behavior & tenure
  - Availability & reviews
  - Room / property type
  - Listing metadata

---

## ⚙️ Tech Stack
| Category | Tools |
|----------|-------|
| Language | Python |
| Data | Pandas, NumPy |
| ML | Scikit-Learn, XGBoost |
| Visualization | Matplotlib |
| Environment | Jupyter Notebook |

---

## 🛠️ Feature Engineering
Key transformations:
- Price cleaning (`$` → float)
- Percent to numeric conversion (e.g. `96%`)
- Host tenure and review recency
- Per-guest ratios for room size features
- Target encoding for neighborhoods
- One-hot encoding for categorical fields

---

## 🤖 Model Performance

| Model | R² | RMSE ($) | MAE ($) |
|-------|----|----------|---------|
| **XGBoost** | 0.77 | $5,047 | $42 |
| Random Forest | 0.75 | $5,553 | $44 |
| Linear Regression | 0.68 | $6,569 | $50 |

**Best Model:** XGBoost (≈77% variance explained)

---

## 🔑 Most Important Features
Based on XGBoost importance:

1. Latitude / Longitude
2. Host tenure (days)
3. Availability (365 days)
4. Days since last review
5. Host listing volume
6. Minimum nights
7. Review metrics
8. Neighborhood encoding

---

## 📈 Example Visuals
_(Plots included in the notebook)_
- Price distribution
- Model comparison charts
- Top feature importances

---

## 🚀 Future Enhancements
- Hyperparameter tuning
- SHAP interpretability
- Geospatial mapping
- Streamlit web app
- Text embedding of listing descriptions
- Time-series & dynamic pricing modeling

---

## 📁 Project Structure

```
price-predictor-airbnb-toronto/
│── bnb_listings.csv 
│── mAirbnb_Toronto_Price_Prediction.ipynb 
│── README.md 
```
