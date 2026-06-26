# 🍽️ Zomato Customer Feedback Analysis & Restaurant Rating Prediction

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Regression-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📌 Project Overview

This project performs an end-to-end analysis of customer feedback collected from Zomato restaurants. It combines **Exploratory Data Analysis (EDA), Natural Language Processing (NLP), Feature Engineering, Statistical Analysis, and Machine Learning** to understand customer behavior and predict restaurant ratings.

The notebook demonstrates the complete Data Science lifecycle starting from raw data preprocessing to model evaluation and comparison.

---

# 🎯 Objectives

- Analyze customer reviews and restaurant metadata.
- Discover factors influencing restaurant ratings.
- Clean and preprocess textual reviews.
- Engineer meaningful numerical features.
- Compare multiple Machine Learning regression models.
- Predict restaurant ratings based on restaurant characteristics.

---

# 📂 Dataset

The project uses two datasets:

### 1. Restaurant Metadata

Contains restaurant-level information such as:

- Restaurant Name
- Cost for Two
- Cuisine Types
- Location
- Restaurant Information

### 2. Customer Reviews

Contains customer feedback including:

- Restaurant Name
- Review Text
- Reviewer
- Rating

---

# 🛠 Technologies Used

| Category | Libraries |
|----------|-----------|
| Programming | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Missingno |
| NLP | NLTK, TF-IDF |
| Machine Learning | Scikit-Learn, XGBoost |
| Model Saving | Pickle |

---

# 📊 Exploratory Data Analysis

The notebook performs extensive EDA including:

- Dataset overview
- Missing value analysis
- Duplicate removal
- Statistical summaries
- Rating distribution
- Cost distribution
- Cuisine analysis
- Restaurant popularity
- Correlation heatmaps
- Pairplots
- Boxplots
- Histograms
- Violin plots
- Scatter plots

More than **15 visualizations** were created to understand customer behavior and restaurant characteristics.

---

# 🧹 Data Preprocessing

The following preprocessing techniques were applied:

## Data Cleaning

- Removed duplicate records
- Missing value treatment
- Cost column cleaning
- Rating conversion to numeric
- Outlier capping
- Median imputation

---

## Text Preprocessing

Customer reviews were processed using:

- Lowercasing
- Punctuation removal
- URL removal
- Number removal
- Stopword removal
- Whitespace normalization
- Lemmatization
- Tokenization
- POS Tagging

---

## Feature Engineering

Created multiple features including:

- Cuisine Count
- Review Length
- Price Range
- North Indian Cuisine Flag
- Chinese Cuisine Flag
- Standardized Cost

---

## Feature Extraction

TF-IDF Vectorization was used for transforming customer reviews into numerical vectors.

---

# 📈 Statistical Analysis

The notebook includes statistical hypothesis testing:

- Independent T-Test
- Pearson Correlation Test

These tests evaluate relationships between:

- Restaurant Cost vs Rating
- Cuisine Type vs Rating
- Review Length vs Rating

---

# 🤖 Machine Learning Models

Three regression models were implemented.

## 1️⃣ Random Forest Regressor

Advantages:

- Handles nonlinear relationships
- Robust to outliers
- Feature importance estimation

---

## 2️⃣ Ridge Regression

Advantages:

- L2 Regularization
- Prevents overfitting
- Fast baseline model

---

## 3️⃣ XGBoost Regressor

Advantages:

- Gradient Boosting
- High predictive capability
- Handles complex datasets efficiently

---

# ⚙ Hyperparameter Tuning

GridSearchCV was used for:

### Ridge Regression

Parameters:

- alpha

### XGBoost

Parameters:

- n_estimators
- max_depth
- learning_rate

Cross-validation was performed to determine the best configuration.

---

# 📊 Model Benchmark Results

## Performance Comparison

| Model | Mean Squared Error (MSE) | R² Score |
|--------|-------------------------:|----------:|
| Random Forest Regressor | **17351.9791** | **-0.0042** |
| Ridge Regression | **17354.9981** | **-0.0043** |
| Tuned XGBoost Regressor | **17354.9981** | **-0.0043** |

---

# 🏆 Best Performing Model

Based on the notebook results:

🥇 **Random Forest Regressor**

Performance:

- Lowest Mean Squared Error
- Highest R² Score (although still negative)

---

# 📉 Performance Analysis

The benchmark results indicate that:

- All models produced very similar performance.
- The negative R² values suggest that the current feature set is insufficient for accurately predicting restaurant ratings.
- Customer ratings appear to depend on additional factors not captured in the dataset.

Potential reasons include:

- Limited feature engineering
- Sparse textual representation
- Missing restaurant-specific attributes
- Customer subjectivity in ratings

---

# 🚀 Future Improvements

Possible improvements include:

- Deep Learning-based NLP models (BERT, RoBERTa)
- Sentiment Analysis
- Word Embeddings
- CatBoost
- LightGBM
- Feature Selection
- Hyperparameter Optimization
- Ensemble Learning
- Explainable AI using SHAP
- Cross-validation with larger datasets

---

# 📦 Project Workflow

```
Raw Dataset
      │
      ▼
Data Cleaning
      │
      ▼
EDA
      │
      ▼
Text Preprocessing
      │
      ▼
Feature Engineering
      │
      ▼
TF-IDF Vectorization
      │
      ▼
Train-Test Split
      │
      ▼
Model Training
      │
      ▼
Hyperparameter Tuning
      │
      ▼
Model Evaluation
      │
      ▼
Performance Comparison
      │
      ▼
Model Serialization
```

---

# 📁 Project Structure

```
Zomato-Customer-Feedback-Analysis/
│
├── Zomato Customer Feedback Analysis.ipynb
├── zomato_model.pkl
├── README.md
├── requirements.txt
└── datasets/
    ├── Zomato Restaurant names and Metadata.csv
    └── Zomato Reviews.csv
```

---

# 📊 Key Insights

- Restaurant cost alone is not a strong predictor of customer ratings.
- Cuisine diversity shows only a weak relationship with ratings.
- Review length has limited correlation with customer ratings.
- More advanced NLP techniques are needed for meaningful prediction.

---

# 💾 Model Export

The trained Random Forest model is saved as:

```
zomato_model.pkl
```

This model can be loaded later for inference on unseen restaurant data.

---

# 🔮 Future Scope

- Real-time restaurant recommendation system
- Customer sentiment dashboard
- Restaurant ranking engine
- Review summarization using LLMs
- AI-powered restaurant quality prediction
- Interactive Streamlit deployment
- Cloud deployment on AWS/GCP/Azure

---

# 👨‍💻 Author

**Ishank Mishra**

AI • Machine Learning • Data Science • NLP

If you found this project useful, consider giving it a ⭐ on GitHub.
