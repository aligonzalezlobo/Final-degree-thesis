# Hate Speech Detection on Twitter

## Introduction

This project has been a culmination of several months of research and development, aimed at addressing the contemporary issue of hate speech on social media platforms.

## Project Overview

### Dataset
The dataset used in this project comprises Twitter tweets, each labeled as either hate speech (1) or not hate speech (0). It is worth noting that the dataset is well-balanced, which eliminates the need for oversampling either class.

### Data Preparation
Before diving into the classification task, we performed several data preparation steps, including:
- Copying the original dataset for reference.
- Removing tweet IDs, which were not relevant for the task.
- Cleaning the text data by removing diacritics, user mentions, and URLs.
- Further cleaning by eliminating common words, punctuation, and expressions that did not contribute to the classification task.

### Task Definition
The primary task is binary classification, where the system predicts whether a given tweet contains hate speech or not. During model training, the algorithms learn to identify words and phrases that are indicative of hate speech by detecting unusually frequent words in hate speech examples compared to normal tweets.

### Data Split
To assess model generalization, we split the dataset into a training set and a test set, reserving 20% of the data for testing.

### Feature Representation
Text data is represented using the TF-IDF (Term Frequency-Inverse Document Frequency) technique, which transforms text into fixed-size vectors.

## Model 1: Logistic Regression

### Model Overview
The first classification model utilizes logistic regression, which predicts the probability of a tweet being hate speech based on its TF-IDF vector.

### Model Training
Logistic regression estimates weights for each feature (word) to determine its importance in classifying hate speech.

### Evaluation
The model was initially trained with default hyperparameters and then fine-tuned to improve performance. Evaluation metrics such as accuracy, precision, recall, and F1-score were used to assess its performance.

## Model 2: Support Vector Machines (SVM)

### Model Overview
The second classification model employs Support Vector Machines (SVM), which aims to create a margin that separates the two classes effectively.

### SVM Training
SVM aims to find a balance between maximizing the margin width and limiting margin violations using a user-defined hyperparameter (C).

### Evaluation
Similar to logistic regression, the SVM model's performance was evaluated using various metrics, including accuracy, precision, recall, and F1-score.

## Model Comparison

### Performance Metrics
- Accuracy: Measures overall correctness.
- Precision: Measures the fraction of true positive predictions.
- Recall: Measures the fraction of actual positives correctly predicted.
- F1-score: Combines precision and recall for a balanced measure.

### ROC Curve and AUC
ROC curves visualize the trade-off between true positive rate and false positive rate, and AUC (Area Under the Curve) summarizes the curve's performance.

### DET Curve
The Detection Error Tradeoff curve provides an alternative visualization of classifier performance.

## Conclusions

In summary, this project focused on the detection of hate speech on Twitter using machine learning techniques. Both logistic regression and SVM models performed exceptionally well, with marginal differences in performance metrics. The choice between these models may depend on the specific goals of the application, emphasizing either high precision or high recall.

## Acknowledgments

I would like to express my gratitude to Luis Javier Rodriguez Fuentes for their contributions and support during this project.
