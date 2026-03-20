# Fake News Detection – Machine Learning Project (Phase 2 & Phase 3)

## Project Overview

This project focuses on analyzing, preprocessing, and performing feature engineering on a fake news dataset to prepare it for machine learning models. The goal is to understand patterns in news articles and improve model performance through effective feature extraction and engineering techniques.

The dataset contains both **real and fake news articles**, and the project involves transforming raw text into meaningful features for classification.

---

## Project Objectives

* Analyze and visualize the dataset
* Apply text preprocessing techniques
* Perform feature engineering
* Identify important features using multiple machine learning algorithms
* Evaluate the impact of new features on model performance

### Research Questions

1. How accurately can machine learning models detect fake news using textual features?
2. How do preprocessing and feature engineering techniques affect model performance?

---

## Dataset Description

The dataset was obtained from Kaggle and contains:

* **True.csv** – Real news articles
* **Fake.csv** – Fake news articles

### Features:

* **title** – News headline
* **text** – Article content
* **subject** – News category
* **date** – Publication date

A new column **label** was added:

* **1 = True News**
* **0 = Fake News**

The final dataset contains **44,898 articles**.

---

# Phase 2 — Data Analysis & Preprocessing

## Statistical Analysis

* Checked dataset structure using `info()`
* Generated summary statistics using `describe()`
* Verified missing values (none found)
* Analyzed class distribution (balanced dataset)

## Visual Analysis

The following visualizations were created:

* Distribution of fake vs real news
* Subject distribution
* Article text length distribution
* Title length distribution

These helped in understanding dataset patterns and structure.

---

## Data Preprocessing

The following preprocessing steps were applied:

1. **Lowercasing text**
2. **Removing punctuation and special characters**
3. **Removing stopwords**
4. **Combining title and text into a single column (content)**
5. **Dropping unnecessary columns**

The processed dataset was saved for future use.

---

# Phase 3 — Feature Engineering

## TF-IDF Feature Extraction

Text data was converted into numerical features using **TF-IDF**, generating 5000 features for model input.

---

## Feature Importance Analysis

Five different algorithms were used to identify important features:

* Random Forest
* Decision Tree
* Extra Trees
* Logistic Regression
* LightGBM

### Key Findings:

* Words like **"reuters", "said", "washington"** are strong indicators of real news
* Words like **"video", "just", "image"** are more common in fake news
* Decision Tree showed overfitting (relying on one feature)
* Ensemble methods (Random Forest, Extra Trees, LightGBM) provided more reliable results

---

## Feature Engineering

New features were created to enhance model performance:

* **content_length** – Length of article
* **word_count** – Number of words
* **uppercase_ratio** – Ratio of uppercase words

These features capture structural and stylistic differences in news articles.

---

## Feature Evaluation

The new features were evaluated using **LightGBM**:

* TF-IDF already provided very high accuracy
* New features resulted in a **small but positive improvement**

This shows that additional features provide extra contextual information.

---

## K-Means Clustering

K-Means clustering was applied to create a new feature:

* Articles were grouped into **5 clusters**
* Cluster labels were added as a feature

This helps capture hidden patterns in the dataset.

---

## Standardization

Numerical features were standardized using **StandardScaler** to ensure consistent scaling across features.

---

## Final Dataset

The final dataset includes:

* **content** – Processed text
* **subject** – Category
* **label** – Target variable
* **engineered features** (length, word count, uppercase ratio)
* **cluster feature**

Saved as:

`final_feature_engineered_dataset.csv`

---

## Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* LightGBM
* Kaggle Notebook

---

## Project Structure

```
FakeNews-ML-Project
│
├── true-and-fake-news-dataset.ipynb
└── README.md
```

---

## Conclusion

This project demonstrates how preprocessing and feature engineering significantly improve the quality of data for machine learning tasks. While TF-IDF features were highly effective, additional engineered features and clustering provided further insights.

Overall, feature engineering played a crucial role in enhancing the dataset for fake news detection.

---

## Future Work

In the next phase, machine learning models will be trained and evaluated using the engineered dataset to build an accurate fake news detection system.

---

## Author

**Azeem Raza**
BS Computer Science
Machine Learning Course Project
