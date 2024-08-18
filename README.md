# Poisonous Mushroom Prediction

This repository contains my solution to the Kaggle competition on predicting whether a mushroom is poisonous or edible in target 'class' using a dataset of mushroom characteristics.

## Dataset

The dataset provided for this competition includes:
- **train_data.csv**: The training dataset used for building the predictive models.
- **test_data.csv**: The test dataset used for evaluating the model's performance.
- **sample_submission.csv**: A sample submission file used as a template for submitting predictions.

## Project Overview

### 1. Data Exploration

Initially, I performed exploratory data analysis (EDA) to understand the structure and characteristics of the dataset. This included checking for missing values, analyzing feature distributions, and identifying important features that could influence the prediction of whether a mushroom is poisonous or not.

### 2. AutoGluon Model

For the initial modeling, I used [AutoGluon](https://auto.gluon.ai/stable/index.html), an open-source AutoML library that simplifies the process of applying machine learning. AutoGluon automates key aspects of model building, including hyperparameter tuning, model selection, and ensembling.

#### AutoGluon Approach:
- AutoGluon was employed to automatically train various models on the training dataset.
- It performed extensive hyperparameter optimization and model ensembling to achieve high predictive performance.
- The model achieved an impressive accuracy of 99% on the validation set, without any signs of overfitting or underfitting.

A confusion matrix was generated to evaluate the model's performance further, confirming the high accuracy and balanced predictions across classes.

### 3. LightGBM Classifier with GridSearch

In addition to AutoGluon, I implemented a LightGBM classifier to explore its performance on this dataset.

#### Steps Taken:
- **GridSearch**: A GridSearch was performed to find the best hyperparameters for the LightGBM model. This involved tuning parameters such as learning rate, max depth, number of estimators, and the number of leaves.
- **Model Training**: The best parameters obtained from the GridSearch were used to train the LightGBM model on the training dataset.
- **Model Testing**: The trained model was then tested on the provided test dataset.

The predictions from the test dataset were saved in a file named `class_submission.csv`, which is ready for submission.

## Results

- **AutoGluon Model**: Achieved 99% accuracy without overfitting or underfitting.
- **LightGBM Classifier**: Successfully tuned and applied, with predictions saved in `class_submission.csv`.

## Conclusion

This project demonstrates the effectiveness of using automated machine learning (AutoML) tools like AutoGluon alongside traditional model tuning methods such as GridSearch with LightGBM. The high accuracy and balanced performance of the models indicate a robust solution to the problem of predicting mushroom edibility.

## Files in Repository

- `train_data.csv`: The training dataset.
- `test_data.csv`: The test dataset.
- `sample_submission.csv`: The sample submission file.
- `class_submission.csv`: The final predictions using the LightGBM model.
- `notebooks/`: Jupyter notebooks containing the code for data exploration, modeling with AutoGluon, and LightGBM with GridSearch.
- `README.md`: This document.

---
