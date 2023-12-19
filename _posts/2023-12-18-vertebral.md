---
title: "KNN: Vertebral Column Data Set"
date: 2023-12-18
categories:
  - Data Science
---

This project involves a comprehensive analysis of the Vertebral Column Data Set created by Dr. Henrique da Mota. The data set includes six biomechanical attributes from each patient, focusing on binary classification of Normal (NO) and Abnormal (AB) conditions...

![Alt text for image](/assets/images/vertebral-column.jpeg)

<!--more-->

## Data Exploration
The dataset is explored through scatterplots and boxplots to understand the relationships and distributions of the variables.

## KNN Classification
The project's core is implementing K-Nearest Neighbors (KNN) with various metrics including Euclidean, Manhattan, and Chebyshev distances. Key points include:
- Optimizing the value of `k` based on error rates.
- Calculating metrics like confusion matrix, true positive and negative rates, precision, and F1-score.
- Analyzing the learning curve against different training set sizes.

## Advanced Techniques
Further exploration includes:
- Testing different distance metrics and summarizing their performance.
- Implementing weighted voting to reduce variance and improve decision making.

## Conclusions and Findings
We can see from our test errors using various distance metrics that the KNN model performs well on this dataset with a test error rate averaging at around 0.1.

[View Jupyter Notebook](https://nbviewer.org/github/Payapulli/Payapulli.github.io/blob/main/jupyter-notebooks/Vertebral-Column-Datset-KNN.ipynb) |
[View Project on GitHub](URL_to_your_GitHub_repository) |
[View Dataset](https://archive.ics.uci.edu/dataset/212/vertebral+column)