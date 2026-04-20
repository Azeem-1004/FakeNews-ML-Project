Fake News Detection – Machine Learning Project (Phase 2, Phase 3 & Phase 4)
📌 Project Overview

This project focuses on analyzing, preprocessing, feature engineering, and building machine learning models to detect fake news. The objective is to classify news articles as real or fake based on textual and engineered features.

The dataset contains both real and fake news articles, and multiple techniques were applied to improve classification performance.

🎯 Project Objectives
Analyze and visualize the dataset
Apply text preprocessing techniques
Perform feature engineering
Train multiple machine learning models
Evaluate model performance using statistical metrics
Identify the best-performing model
❓ Research Questions
How accurately can machine learning models detect fake news using textual features?
How do preprocessing and feature engineering techniques affect model performance?
Which machine learning model performs best for fake news classification?
📊 Dataset Description

Dataset obtained from Kaggle:

True.csv – Real news articles
Fake.csv – Fake news articles
Features:
title – News headline
text – Article content
subject – News category
date – Publication date
Target Variable:
label
1 = Real News
0 = Fake News

📌 Final dataset size: 44,898 articles

📌 Phase 2 — Data Analysis & Preprocessing
📊 Statistical Analysis
Dataset structure analyzed using info()
Summary statistics using describe()
No missing values found
Balanced class distribution observed
📈 Visual Analysis
Fake vs Real news distribution
Subject category distribution
Article length distribution
Title length distribution
🧹 Data Preprocessing
Converted text to lowercase
Removed punctuation and special characters
Removed stopwords
Combined title + text → content
Removed unnecessary columns
📌 Phase 3 — Feature Engineering
🔢 TF-IDF Feature Extraction

Text was converted into numerical features using TF-IDF (5000 features).

🔍 Feature Importance Analysis

Models used:

Random Forest
Decision Tree
Extra Trees
Logistic Regression
LightGBM
Key Insights:
“reuters”, “said”, “washington” → Strong indicators of real news
“video”, “just”, “image” → More common in fake news
Ensemble models performed more reliably than single decision trees
🛠 Feature Engineering

New features created:

content_length – Length of article
word_count – Number of words
uppercase_ratio – Ratio of uppercase words

These features improved contextual understanding of text.

📦 Clustering Feature
K-Means clustering applied (k = 5)
Cluster labels added as a new feature
Helped capture hidden patterns in data
⚖️ Standardization
Numerical features standardized using StandardScaler
💾 Final Dataset

Saved as:

final_feature_engineered_dataset.csv
📌 Phase 4 — Model Training & Evaluation
🤖 Machine Learning Models Used
Logistic Regression
Support Vector Machine (SVM)
Random Forest
📊 Model Performance Results
🔹 Logistic Regression
Accuracy: 0.9886
Precision/Recall/F1: ~0.99
Strong baseline model with stable performance
🔹 Support Vector Machine (SVM)
Accuracy: 0.9949
High performance on TF-IDF high-dimensional data
Better than Logistic Regression in most metrics
🔹 Random Forest
Accuracy: 0.9981
Precision/Recall/F1: 1.00 for both classes
Best-performing model overall
📈 Evaluation Summary

All models were evaluated using:

Accuracy
Precision
Recall
F1-score
Confusion Matrix

The dataset showed strong separability between fake and real news, leading to high model performance across all classifiers.

🏆 Final Model Comparison
Model	Accuracy	Performance
Logistic Regression	0.9886	Good
SVM	0.9949	Very Good
Random Forest	0.9981	Best
🧾 Final Conclusion

Machine learning models performed exceptionally well in detecting fake news using TF-IDF and engineered features. Logistic Regression and SVM provided strong baseline and improved performance respectively, while Random Forest achieved the highest accuracy and near-perfect classification results. Therefore, Random Forest is selected as the final model for this project.

🚀 Technologies Used
Python
Pandas, NumPy
Scikit-learn
Matplotlib, Seaborn
LightGBM
Kaggle Notebook

📁 Project Structure
FakeNews-ML-Project
│
├── true-and-fake-news-dataset.ipynb
└── README.md

👨‍💻 Author

Azeem Raza
BS Computer Science
Machine Learning Course Project
