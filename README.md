# Breast Cancer Prediction Model

This project uses machine learning algorithms to predict whether a breast tumor is benign (non-cancerous) or malignant (cancerous) based on various features. The dataset used is from a breast cancer study.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [New Predictions](#new-predictions)
- [Results](#results)

## Introduction

This project aims to provide a machine learning solution to classify breast tumors as non-cancerous or cancerous. It utilizes multiple classification algorithms to find the best performing model based on F1 score, accuracy, precision, recall.

## Dataset 

The dataset used in this project is `breast-cancer.csv`. It contains features like mean radius, mean texture, mean perimeter, etc., which are used to predict the diagnosis.

## Installation

To run this project, you need Python and several libraries. Follow the steps below to install the required dependencies:

1. Clone the repository:
    ```bash
    git clone https://github.com/NK19Coder/Breast_cancer.git 
    ```

2. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Load the dataset:
    ```python
    import pandas as pd
    data = pd.read_csv('breast-cancer.csv')
    ```

2. Train the model and make predictions using the provided script `breast_cancer_prediction.py`.

3. Use the trained model to make predictions on new data:
    ```python
    new_subject = {
    'id': 0, 
    'radius_mean': 14.0,
    'texture_mean': 20.0,
    'perimeter_mean': 90.0,
    'area_mean': 700.0,
    'smoothness_mean': 0.1,
    'compactness_mean': 0.15,
    'concavity_mean': 0.2,
    'concave points_mean': 0.05,
    'symmetry_mean': 0.2,
    'fractal_dimension_mean': 0.06,
    'radius_se': 0.5, 
    'texture_se': 1.0, 
    'perimeter_se': 3.0,
    'area_se': 40.0,
    'smoothness_se': 0.005, 
    'compactness_se': 0.025,
    'concavity_se': 0.03,
    'concave points_se': 0.01,
    'symmetry_se': 0.02, 
    'fractal_dimension_se': 0.003,
    'radius_worst': 15.0,
    'texture_worst': 25.0,
    'perimeter_worst': 100.0,
    'area_worst': 800.0,
    'smoothness_worst': 0.12,
    'compactness_worst': 0.2,
    'concavity_worst': 0.25,
    'concave points_worst': 0.08,
    'symmetry_worst': 0.3,
    'fractal_dimension_worst': 0.08 }

```bash
new_subject_df = pd.DataFrame([new_subject])
```
```bash
column_names = new_subject_df.columns
```
```bash
prediction = best_model.predict(new_subject_df)
```
```bash 
print(f'The prediction for the new subject is: {"Diagnoised with cancer" if prediction[0] == 1 else "Non-cancerous"}')
```

## Model Training and Evaluation

The script `breast_cancer_prediction.py` trains multiple models and evaluates them based on the F1 score, accuracy, precision, recall. It selects the best performing model for making predictions. 

## New Predictions

The script also provides an example of how to use the trained model to predict the outcome for a new subject based on their features.

## Results

The performance of various models is evaluated using cross-validation. The model with the highest F1 score, accuracy, precision, recall is selected as the best model. 

 
