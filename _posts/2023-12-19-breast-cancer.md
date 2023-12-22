---
title: "Supervised, Semi-Supervised, and Unsupervised Learning: Classification on Breast Cancer data"
date: 2023-12-19
categories:
  - Data Science
---

This project embarks on an exploratory journey through different realms of machine learning: supervised, semi-supervised, and unsupervised learning, using the Breast Cancer Wisconsin (Diagnostic) Data Set and the Banknote Authentication Data Set. The focus is on implementing various classification and clustering techniques, and comparing their effectiveness through a series of Monte-Carlo simulations.

![Alt text for image](/assets/images/breast-cancer.png)

<!--more-->

## Part 1: Breast Cancer Wisconsin (Diagnostic) Data Set
### Data Preparation and Analysis
- **Data Download**: Retrieving the dataset and dividing it into a training set (70%) and a test set (30%).

### Supervised Learning with SVM
- **L1-Penalized SVM**: Training an L1-penalized SVM and using 5-fold cross-validation for penalty parameter selection. Reporting average metrics and plotting the ROC for one of the runs.

### Semi-Supervised Learning (Self-training)
- **Training with Partial Labels**: Implementing a self-training approach with partially labeled data. Gradually adding unlabeled data to the training set based on their distance to the SVM decision boundary. Evaluating performance and reporting average metrics.

### Unsupervised Learning with K-Means
- **Cluster Analysis**: Running k-means clustering on the dataset, assuming k=2. Analyzing cluster centers and predicting labels based on majority polling. Computing average accuracy, precision, recall, F1-score, AUC, and reporting the ROC and confusion matrix for the last run of the Monte-Carlo simulation.

### Spectral Clustering
- **Kernel-based Clustering**: Implementing spectral clustering with an RBF kernel. Comparing the balance of clusters with the original dataset and using the fit-predict method for classification.

### Results

The Semi-Supervised SVM performs the best on the test set, very closely followed by the Supervised SVM. The next best model is the K-Means model, which is to be expected as it doesn't have the training labels to learn from as it is unsupervised. And finally, the worst performing model by quite a large margin is the Spectral Clustering model, which is also unsupervised.

In summary:

Semi-Supervised SVM
Supervised SVM
Unsupervised K Means
Unsupervised Spectral Clustering

## Part 2: Passive vs Active Learning Using SVMs on Banknote Authentication Data Set
### Data Preparation and Active Learning Simulation
- **Dataset Splitting**: Randomly selecting a test and training set.
- **Passive Learning**: Implementing passive learning by incrementally increasing the training set.
- **Active Learning**: Employing active learning by selectively adding data points closest to the SVM hyperplane, these are the ones for which we have most uncertainty.

### Monte Carlo Simulation and Analysis
- **Simulation and Learning Curve**: Conducting a Monte Carlo simulation to average the test errors for both active and passive learning. Plotting the learning curve and drawing conclusions from the results.

### Results

As is expected, the passive and active learning methods both converge to having similar performance on the test set after seeing enough training instances with the active learning model reaching this plateau in performance faster than the passive learning model.

[View Jupyter Notebook](https://nbviewer.org/github/Payapulli/Payapulli.github.io/blob/main/jupyter-notebooks/breast-cancer-SVM-KMeans.ipynb) | 
[View Project on GitHub](https://github.com/DSCI-552/homework-8-Payapulli) |
[View Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)