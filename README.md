# Pattern Recognition – Spambase Classification

## Project Overview

This project develops a basic email classification system for identifying
spam and non-spam emails using the UCI Spambase dataset.

Two machine learning classification algorithms are implemented and evaluated:

- K-Nearest Neighbours (KNN)
- Gaussian Naïve Bayes

The project was developed as part of the Pattern Recognition module
(BCSAI 6214) for the Bachelor of Artificial Intelligence programme.

## Dataset

The project uses the **UCI Spambase Dataset**, which contains 4,601 email
instances and 57 input features.

The target variable is:

- `0` – Non-spam
- `1` – Spam

The dataset contains word-frequency, character-frequency, and capital-letter
related features extracted from email messages.

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the Spambase dataset.
2. Inspected the dataset structure and statistical information.
3. Checked the class distribution and missing values.
4. Separated the input features from the target variable.
5. Divided the dataset into training and testing sets using an 80:20 split.
6. Applied standardisation to the features used by KNN because KNN is a
   distance-based algorithm.

## Machine Learning Models

### K-Nearest Neighbours (KNN)

Several values of K were examined using 5-fold cross-validation on the
training data. The final KNN model used:

- Number of neighbours (K): 3
- Feature scaling: StandardScaler

### Gaussian Naïve Bayes

A Gaussian Naïve Bayes classifier was trained using the numerical features
from the training dataset.

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

## Results

The final test-set results were:

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| KNN | 89.79% | 87.26% | 86.78% | 87.02% |
| Gaussian Naïve Bayes | 83.39% | 71.78% | 95.32% | 81.89% |

The results show different performance characteristics between the two
classifiers. KNN achieved higher accuracy, precision, and F1-score on the
test set, while Gaussian Naïve Bayes achieved higher recall.

## Project Files

- `Pattern_Recognition_Spambase_Classification.ipynb` – Complete
  implementation, experiments, evaluation results, and visualisations.

## Tools and Libraries

The project was implemented using Python and the following libraries:

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Repository Purpose

This repository contains the implementation and experimental results for the
Pattern Recognition assignment on spam email classification.
