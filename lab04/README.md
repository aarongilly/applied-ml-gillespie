# NM Missouri Univerity CSIS 44-670 Lab 4 - Titanic Dataset

author: Aaron Gillespie  
date: 2025-04-04

# Purpose

This code base is being created in the course of completing module 4 of CSIS 44-670 from NW Missouri University. This `README.md` accompanies a Jupyter Notebook in which we will analyze data representing the passengers from the RMS Titanic, which sank in a very famous James Cameron movie (also real life). We are utilizing this dataset to, which [some research suggests](https://www.geeksforgeeks.org/python-titanic-data-eda-using-seaborn/) is a commonly utilized dataset for getting started with Machine Learning. In essence, this is the `hello world!` of my adventures with machine learning. 

## Lab 4 - Predicting Fare

For more detail see the the Jupyter Notebook `ml04_gillespie.ipynb`, which contains comments throughout that explain the code and its objectives.

# Outcome

#TODO

%%

| Model Type               | Case   | Features Used     | Accuracy   | Precision   | Recall   | F1-Score    | Notes |
|------------              |--------|---------------    |----------  |-----------  |--------  |-----------  |-------|
| **Decision Tree**        | Case 1 | alone             | 63%        | 64%         | 63%      | 63%         | -     |
|                          | Case 2 | age               | 68%        | 68%         | 68%      | 64%         | -     |
|                          | Case 3 | age + sex         | 82%        | 82%         | 83%      | 82%         | Winner winner       |
|--------------------------|--------|-------------------|------------|-------------|----------|-------------|---------|
| **SVM (RBF Kernel)**     | Case 1 | alone             | 63%        | 64%         | 63%      | 63%         | -       |
|                          | Case 2 | age               | 63%        | 66%         | 63%      | 52%         | -       |
|                          | Case 3 | age + sex         | 64%        | 68%         | 64%      | 63%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **SVM (Linear Kernel)**  | Case 1 | alone             | 63%        | 64%         | 63%      | 63%         | -       |
|                          | Case 2 | age               | 61%        | 38%         | 61%      | 47%         | -       |
|                          | Case 3 | age + sex         | 78%        | 78%         | 78%      | 78%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **SVM (Poly Kernel)**    | Case 1 | alone             | 63%        | 64%         | 63%      | 63%         | -       |
|                          | Case 2 | age               | 61%        | 38%         | 61%      | 47%         | -       |
|                          | Case 3 | age + sex         | 68%        | 74%         | 68%      | 61%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **SVM (Sigmoid Kernel)** | Case 1 | alone             | 63%        | 64%         | 63%      | 63%         | -       |
|                          | Case 2 | age               | 54%        | 53%         | 54%      | 53%         | -       |
|                          | Case 3 | age + sex         | 55%        | 55%         | 55%      | 55%         | -       |
| -------------------      | ------ | ---------------   | ---------- | ----------- | -------- | ----------- | ------- |
| **Neural Network (MLP)** | Case 1 | alone             | 63%        | 64%         | 63%      | 63%         | -       |
|                          | Case 2 | age               | 63%        | 66%         | 63%      | 52%         | -       |
|                          | Case 3 | age + sex         | 79%        | 79%         | 79%      | 79%         | Close second       |

%%