# Diabetes Classification with IBM Watson AutoAI

A binary classification experiment that predicts whether a patient has diabetes (`Outcome` = 1) or not (`Outcome` = 0), built with **IBM Watson Studio AutoAI** in 2023. The repository contains the two notebooks AutoAI generated from the experiment.

## Experiment setup

| Setting | Value |
|---|---|
| Prediction type | Binary classification |
| Target column | `Outcome` (positive label: 1) |
| Train / holdout split | 90% / 10% |
| Optimization metric | Accuracy |
| Candidate estimators | Random Forest, Decision Tree, Logistic Regression, XGBoost |

AutoAI automatically compared the candidate algorithms, applied feature engineering and hyperparameter optimization, and ranked the resulting pipelines.

## Notebooks

- **Experiment notebook**: reconnects to the finished AutoAI experiment, compares all pipelines, inspects and visualizes the best one, then deploys it to Watson Machine Learning and scores it as a web service.
- **P16 notebook**: rebuilds Pipeline 16 as a plain scikit-learn pipeline (autoai-libs preprocessing, feature selection and a `RandomForestClassifier`) so it can be retrained and inspected locally.

## Running the notebooks

Both notebooks need an IBM Cloud account with Watson Studio and Watson Machine Learning. Replace the placeholders `PUT_YOUR_APIKEY_HERE` (and `PUT_YOUR_TARGET_SPACE_ID_HERE` for deployment) with your own values when running them.

> **Never commit a real API key.** Load it from an environment variable or enter it at runtime with `getpass`, and revoke any key that has been pushed to a public repository.

## Tech stack

IBM Watson Studio AutoAI, Watson Machine Learning, Python, scikit-learn, autoai-libs, Jupyter Notebook.

## Author

Said Muhammad Wildan
