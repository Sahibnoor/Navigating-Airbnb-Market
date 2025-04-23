# 🏡 Navigating the Airbnb Market – Buenos Aires

This repository contains the capstone project for **Course 655: Data Mining in Business**, completed as part of the **MS in Business Analytics (MSBA)** program at **UMass Amherst – Isenberg School of Management**. The project explores Airbnb pricing dynamics in Buenos Aires and develops a machine learning pipeline for price prediction, enhanced by sentiment and topic analysis of guest reviews.

## 🎯 Objective

To help Airbnb hosts:
- Predict listing prices using property features and guest reviews
- Understand guest sentiments and satisfaction drivers
- Make informed, data-driven pricing decisions to maximize occupancy and revenue

## 📁 Project Structure

- `Capstone Project Report.pdf` — Final project report summarizing methodology, analysis, and business insights  
- `Group8_AI_Project_Milestone_2_Code.ipynb` — Complete notebook with data cleaning, modeling, sentiment analysis, and visualizations  
- `README.md` — Project overview and context

## 🔧 Project Components

### 🧹 Data Preprocessing
- Null handling (mode imputation, filtering missing targets)
- Outlier removal (prices below 10,000 or above 62,000)
- One-hot encoding (property_type, room_type, availability)
- Review sentiment scoring (TextBlob with polarity thresholds)
- Merging listing data with processed review data

### 📊 Exploratory Data Analysis
- Descriptive statistics on price, beds, min/max nights, sentiment
- Histograms and distribution plots for categorical features
- Correlation matrix for feature selection
- Geo-mapping to visualize popular Airbnb areas

### 🗣 Topic Modeling
Used **Latent Dirichlet Allocation (LDA)** on guest reviews to extract dominant topics:
- Cleanliness, amenities, and host responsiveness
- Check-in experience and communication
- Location quality and neighborhood safety

### 🤖 Modeling
Compared multiple regression models to predict listing prices:

| Model             | RMSE        | R² Score |
|------------------|-------------|----------|
| Linear Regression| Failed (extreme outliers) | N/A |
| Decision Tree    | ~11,734     | 0.27     |
| Random Forest    | ~10,584     | 0.41     |
| XGBoost          | ~10,583     | 0.41     |
| **Gradient Boosting** | **~10,246** | **0.45** |

→ **Gradient Boosting** outperformed others, balancing accuracy and complexity.

## 💡 Key Insights

- Most listings are 1–2 bedrooms, centrally located, and have flexible stay lengths
- Sentiment scores alone are weakly correlated to review ratings but reveal deeper guest experiences via topic modeling
- Gradient Boosting captured non-linear pricing patterns better than linear models

## 🧠 Recommendations

### For Airbnb:
- Develop host tools for sentiment-based performance tracking
- Incorporate dynamic pricing strategies using ML models

### For Hosts:
- Adjust prices based on listing attributes and market seasonality
- Focus on guest experience elements tied to higher sentiment and return intent

### For Customers:
- Gain more price transparency and booking confidence through better review insights
- Use refined filters to match preferences with listing attributes

## 🛠 Tools & Libraries

- Python  
- Pandas, NumPy  
- Scikit-learn, XGBoost, GradientBoosting  
- NLTK, TextBlob, Gensim (for NLP + LDA)  
- Matplotlib, Seaborn  
- Jupyter Notebook / Google Colab

## 🏫 Course Info

- **Course:** SCH-MGMT 655 – Data Mining in Business  
- **Program:** MS in Business Analytics  
- **University:** UMass Amherst – Isenberg School of Management  
- **Year:** 2024  

---

