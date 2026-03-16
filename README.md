# Fake News Detection – Machine Learning Project (Phase 2)

## Project Overview

This project focuses on analyzing and preprocessing a fake news dataset in order to prepare it for machine learning models. The goal is to explore patterns in news articles and apply text preprocessing techniques that will help in building an accurate fake news detection system.

The dataset contains both **real and fake news articles**, and the task is to understand the structure of the data, visualize important features, and clean the textual data before using it in machine learning models.

---

## Project Objectives

The main objectives of this project are:

* To analyze the dataset using statistical methods.
* To visualize different features of the dataset for better understanding.
* To apply text preprocessing techniques to clean the data.
* To prepare the dataset for future machine learning model training.

The project also aims to answer the following questions:

1. How accurately can machine learning models detect fake news articles using textual features such as titles and article content?
2. How do different text preprocessing techniques affect the performance of fake news detection models?

---

## Dataset Description

The dataset was obtained from Kaggle and contains two CSV files:

* **True.csv** – Contains real news articles
* **Fake.csv** – Contains fake news articles

Both datasets include the following features:

* **title** – Headline of the news article
* **text** – Full content of the news article
* **subject** – Category of the news
* **date** – Date the article was published

A new column **label** was added during preprocessing:

* **1 = True News**
* **0 = Fake News**

After labeling, both datasets were merged to create a single dataset containing **44,898 news articles**.

---

## Data Analysis and Visualization

Several statistical and visual analyses were performed to understand the dataset.

### Statistical Analysis

The following checks were performed:

* Dataset structure using `info()`
* Statistical summary using `describe()`
* Missing value analysis
* Class distribution of fake vs real news

The dataset was found to contain **no missing values** and the classes are relatively balanced.

### Visual Analysis

Different visualizations were created to understand the data better:

* Distribution of fake vs real news articles
* Distribution of news subjects
* Distribution of article text length
* Distribution of news title length

These visualizations helped identify patterns in article structure and dataset composition.

---

## Data Preprocessing

To prepare the dataset for machine learning models, several preprocessing steps were applied:

1. **Convert text to lowercase**
   Ensures consistency so that words like "News" and "news" are treated the same.

2. **Remove punctuation and special characters**
   Cleans the text by removing symbols that do not contribute to meaningful analysis.

3. **Remove stopwords**
   Common words such as "the", "is", and "and" were removed to reduce noise.

4. **Combine title and text columns**
   The title and article content were merged into a single feature called **content** to improve text analysis.

5. **Remove unnecessary columns**
   Columns used only for visualization were removed to keep the dataset clean.

---

## Final Processed Dataset

The final dataset contains the following columns:

* **subject** – News category
* **label** – Target variable (Fake or Real)
* **content** – Combined news title and article text

The processed dataset was saved as:

`processed_fake_news_dataset.csv`

This file will be used in the **next phase of the project**, where machine learning models will be trained and evaluated.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Kaggle Notebook

---

## Project Structure

```
FakeNews-ML-Project
│
├── fake_news_analysis.ipynb
├── processed_fake_news_dataset.csv
└── README.md
```

---

## Future Work

In the next phase of this project, machine learning models will be developed to classify news articles as **fake or real**. Different feature extraction techniques and classification algorithms will be tested to evaluate their accuracy and performance.

---

## Author

**Azeem Raza**
BS Computer Science
Machine Learning Course Project
