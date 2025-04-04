# NM Missouri Univerity CSIS 44-670 Lab 4 - Titanic Dataset

author: Aaron Gillespie  
date: 2025-04-04

# Purpose

This code base is being created in the course of completing module 4 of CSIS 44-670 from NW Missouri University. This `README.md` accompanies a Jupyter Notebook in which we will analyze data representing the passengers from the RMS Titanic, which sank in a very famous James Cameron movie (also real life). We are utilizing this dataset to, which [some research suggests](https://www.geeksforgeeks.org/python-titanic-data-eda-using-seaborn/) is a commonly utilized dataset for getting started with Machine Learning. In essence, this is the `hello world!` of my adventures with machine learning. 

## Lab 4 - Predicting Fare

For more detail see the the Jupyter Notebook `ml04_gillespie.ipynb`, which contains comments throughout that explain the code and its objectives.

# Outcome

1. What features were most useful?

    In my original 4 cases, `Class`, `Sex`, and `Embark_Town` were most useful. Of those, I believe `Class` is the most impactful (I believe this because I once commented out Sex and Embark_Town and found that the R^2 value dropped by much less than the 2/3rd you'd expect if they were all equally important). 

2. What regression model performed the best?

    In this case the **Polynomial Regression** based on Case 4 predicted the best. It approached the ceiling that was found for linear regressions that factored in **all** available features. 

### 6.2 Discuss Challenges

1. Was fare hard to predict? Why?

    I think fare is hard to predict given the data we have available. Some folks just paid more. We CAN make **some** reasonable predictions using Class and potentially some other features, but the ceiling for how high I was able to get the R^2 value of any of my models was still less than 0.5. This means that, at best, I was able to find correlations explaining 50% of the variation of the output given all the inputs I tested. 

2. Did skew or outliers impact the models?

    I'd say outliers definitely impact the predictive power of the model. It isn't so much that they caused the predictions to perturb wildly from the average, but instead that the presence of the quantity of outliers that actually existed just go to show that there probably isn't any algorithm we could come up with using the parameters available to us in this dataset to truly approach anything close to R^2 = 1. I don't really see any skew to speak of.

### 6.3 Optional Next Steps

1. Try different features besides the ones used.

    I added a 5th case using all the available features. This case did perform better than any of the other 4 tested. I assume using literally **all** of the features isn't particularly necesary (as some are surely correlates of one another, not meaningfully separable). This work was done above, alongside cases 1 through 4.


## Model Comparison

| Model | R² | MSE | MAE |
|-------|----|------|-----|
| Linear | 0.361 | 924.73 | 21.35 |
| Ridge | 0.361 | 923.94 | 21.33 |
| ElasticNet | 0.390 | 882.04 | 19.24 |
| Polynomial degree 3 | 0.449 | 797.81 | 17.11 |