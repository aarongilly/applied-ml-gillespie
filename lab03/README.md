# NM Missouri Univerity CSIS 44-670 Lab 3 - Titanic Dataset

author: Aaron Gillespie  
date: 2025-03-28

# Purpose

This code base is being created in the course of completing module 3 of CSIS 44-670 from NW Missouri University. This `README.md` accompanies a Jupyter Notebook in which we will analyze data representing the passengers from the RMS Titanic, which sank in a very famous James Cameron movie (also real life). We are utilizing this dataset to, which [some research suggests](https://www.geeksforgeeks.org/python-titanic-data-eda-using-seaborn/) is a commonly utilized dataset for getting started with Machine Learning. In essence, this is the `hello world!` of my advnetures with machine learning. 

## Lab 3 - Predicting Survival 

For more detail see the the Jupyter Notebook `ml03_gillespie.ipynb`, which contains comments throughout that explain the code and its objectives.

# Outcome

The classifiers were built and tested using 3 cases, all predicting whether a person would survive. The cases were based on the following inputs. 

1. `alone`
2. `age`, `class`
3. `age`, `sex`

The **test data** results created by the types of classifiers are summarized in the table below. Using the `classification_report` method from sklearn, reporting the `weighted avg` for each metric.


| Model Type               | Case   | Features Used     | Accuracy   | Precision   | Recall   | F1-Score    | Notes |
|------------              |--------|---------------    |----------  |-----------  |--------  |-----------  |-------|
| **Decision Tree**        | Case 1 | alone             | 63%        | 64%         | 63%      | 63%      | - |
|                          | Case 2 | age + class       | 61%        | 58%         | 61%      | 55%         | - |
|                          | Case 3 | age + sex         | 82%        | 82%         | 83%      | 82%         | -       |
|--------------------------|--------|-------------------|------------|-------------|----------|-------------|---------|
| **SVM (RBF Kernel)**     | Case 1 | alone             | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 2 | age + class       | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 3 | age + sex         | xx%        | xx%         | xx%      | xx%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **SVM (Linear Kernel)**  | Case 1 | alone             | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 2 | age + class       | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 3 | age + sex         | xx%        | xx%         | xx%      | xx%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **SVM (Poly Kernel)**    | Case 1 | alone             | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 2 | age + class       | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 3 | age + sex         | xx%        | xx%         | xx%      | xx%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **SVM (Sigmoid Kernel)** | Case 1 | alone             | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 2 | age + class       | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 3 | age + sex         | xx%        | xx%         | xx%      | xx%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **Neural Network (MLP)** | Case 1 | alone             | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 2 | age + class       | xx%        | xx%         | xx%      | xx%         | -       |
|                          | Case 3 | age + sex         | xx%        | xx%         | xx%      | xx%         | -       |