# CANSSI-Ferry-delay-prediction

[Competition Overview]:(https://www.kaggle.com/c/canssi-ncsc-ferry-delays/overview)

[Leaderboard]:(https://www.kaggle.com/c/canssi-ncsc-ferry-delays/leaderboard)

## Objective of the case study
The case study is about predicting ferry delays in BC Ferry sailings around Vancouver harbours given the main features date, vessel name,departure terminal,weather information).

## Evaludation metric
The evaluation metric is AUC.

# Main challenges and corresponding solutions of the case study.

1: The data is significantly imbalanced which is a sensitive issue in classification.

- Oversampling (Smote), undersampling and built-in weight hyperparameter tuning.

2: There are a variety of reasons that accounted for ferry delay.

- Deleted the rare delayed instances for which we did not have information to predict such as unknown, staffing issues.

3: Missing data imputation in the wether and traffic dataset.

- Missing and incorrect values were imputed by the average of nearest observations and validated simply by visualization.



# Classifiers and model training.

- Logistic regression, Random forest, Xgboost, LightGBM,Voting.

- Models are optimized by the hyperparameter tuning approach (random search).

# Result:

An ensemble of random forest, xgboost, LightGBM finally achieves **0.71455** on the public leaderboard and **0.712** on the private leaderboard.

