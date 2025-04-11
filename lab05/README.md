# NM Missouri Univerity CSIS 44-670 Lab 5 - Ensemble ML Models

author: Aaron Gillespie  
date: 2025-04-11

# Purpose

This code base is being created in the course of completing module 4 of CSIS 44-670 from NW Missouri University. This `README.md` accompanies a Jupyter Notebook in which we will analyze data about wine. 

## Lab 5 - Ensemble Models

For more detail see the the Jupyter Notebook `ml05_gillespie.ipynb`, which contains comments throughout that explain the code and its objectives.

# Outcome

This Lab was pretty straightfoward. In our results we compared our findings with that of our classmates.

> Referenced work by [Brett Neely](https://github.com/bncodes19) - see [his GitHub Repo for this lab](https://github.com/bncodes19/applied-ml-bneely/blob/main/lab05/ensemble-neely.ipynb)

Brett chose to analyze the `AdaBoost (100)` and `MLP Classifier` models, (3 & 9, respectively, from the table). The results Brett obtained were as follows:

||Model|Train Accuracy|Test Accuracy|Train F1|Test F1|
|---|---|---|---|---|---|
|0|AdaBoost (100)|0.834246|0.82500|0.820863|0.815803|
|1|MLP Classifier|0.851446|0.84375|0.814145|0.807318|

Merging Brett's results and the results I obtained for the `Gradient Boosting (100)` and `Voting (RF + LR + KNN)` models & sorting them by test **accuracy**:

||Model|Train Accuracy|Test Accuracy|Train F1|Test F1|
|---|---|---|---|---|---|
|5|Gradient Boosting (100)|0.960125|0.85625|0.95841|0.841106|
|7|Voting (RF + LR + KNN)|0.913213|0.85000|0.89328|0.818465|
|9|MLP Classifier|0.851446|0.84375|0.814145|0.807318|
|3|AdaBoost (100)|0.834246|0.82500|0.820863|0.815803|

**Accuracy** is a measure of what proportion of the predictions were correct. The formula for accuracy is what you'd expect:

$$\text{Accuracy} = \frac{\text{Number of Correct Predictions}}{\text{Total Number of Predictions}}$$

The highest accuracy model was `Gradient Boosting (100)`, which was correct in 96% of its predictions. The to the lowest accuracy model, `AdaBoost (100)`, still performed respectably, obtaining the correct result 82.5% of the time. That's the difference between earning an `A` and a `B`. Not terrible.

Sorting by the test **F1 Score** you get a slightly different order:

||Model|Train Accuracy|Test Accuracy|Train F1|Test F1|
|---|---|---|---|---|---|
|5|Gradient Boosting (100)|0.960125|0.85625|0.95841|0.841106|
|7|Voting (RF + LR + KNN)|0.913213|0.85000|0.89328|0.818465|
|3|AdaBoost (100)|0.834246|0.82500|0.820863|0.815803|
|9|MLP Classifier|0.851446|0.84375|0.814145|0.807318|

**F1 score** is a single metric that provides a balanced measure of a model's performance, combining two crucial metrics: **precision** and **recall**.

$$F1 \ Score = 2 \times \frac{Precision \times Recall}{Precision + Recall} = \frac{2 \cdot TP}{2 \cdot TP + FN + FP}$$

The model with the best F1 score was again `Gradient Boosting (100)`. The lowest accuracy model actually had a slightly better F1 score than the lowest-scoring F1 Test model: `MLP Classifier`.

### Overall conclusion

For the purposes of this dataset in prediction the classification of the quality of wine there is no "bad" models to choose from. However, there are meaningful differences in the models tested. The `Gradient Boosting (100)` model is the strongest choice. This model uses the Gradient Boosting technique with a hyperparameter of 100. 

> **Gradient Boosting** is a machine learning technique that builds an ensemble of weak prediction models, typically decision trees. It works in a stage-wise fashion, where each new model is trained to correct the errors made by the previous models. The "gradient" part refers to the use of gradient descent in the optimization process to find the best way to combine the weak learners.  
> <cite>source: Gemini</cite>
