# CardioInsight
Overview

Predicting heart health with machine learning. This project uses a Random Forest model and SHAP (SHapley Additive exPlanations) to diagnose cardiovascular disease risk.

The project covers the entire machine learning workflow from data preprocessing and feature scaling to model training, evaluation, and explainability using the classic UCI Heart Disease dataset.


Key Features

Machine Learning Model: Implements a RandomForestClassifier for prediction.
Data Preprocessing: Includes data cleaning and feature scaling using StandardScaler.
Model Persistence: Saves the trained model (rf_cvd_model.joblib) and scaler (scaler.joblib) for future inference.
Model Explainability: Uses SHAP to generate visualizations (like summary and force plots) to understand why the model makes a specific prediction for a patient.

Project Workflow

1. Data Loading: Loads the processed.cleveland.data file from the UCI dataset.
2. Preprocessing: Cleans data, scales numerical features, and splits the data into training and testing sets.
3. Model Training: Trains a Random Forest Classifier on the training data.
4. Evaluation: Checks the model's performance on the test set.
5. Model Saving:Saves the fitted StandardScaler and the trained Random Forest model.
6. Explainability (SHAP): Loads the saved models and uses a SHAP Explainer to analyze feature importance and individual patient predictions.

Setup Instructions

1.  Clone the Repository
     git clone [https://github.com/Hassansyed21/Cardiolnsight.git](https://github.com/Hassansyed21/Cardiolnsight.git) cd Cardiolnsight
 
2. Install Dependencies
    pip install -r requirements.txt
   
3. Download the Dataset
    This repository does not include the dataset. You must download it from the UCI Machine Learning Repository.
   Link: [https://archive.ics.uci.edu/dataset/45/heart+disease](https://archive.ics.uci.edu/dataset/45/heart+disease)
   Download the file named processed.cleveland.data and place it in your project folder.

4. Run the Notebook
    Open Cardiovascular_Disease_Diagnosis.ipynb in Jupyter Notebook or Google Colab.
    The notebook is set up to load the processed.cleveland.data file you just downloaded.

File Structure
/Cardiolnsight

|-- README.md. <-- This file

|-- Cardiovascular_Disease_Diagnosis.ipynb. <--The main project notebook

|-- rf_cvd_model.joblib. <--The saved,trained Random Forest model

|-- scaler.joblib. <--The saved,fitted StandardScaler

|-- requirements.txt. <--Python libraries

|-- .gitignore. <--Files to ignore

|-- LICENSE. <-- MIT License


Note on Dataset

This model was trained on the "Heart Disease" dataset from the UCI Machine Learning Repository. The dataset is not included in this repository.

To run the notebook, you must first download the processed.cleveland.data file from here: [https://archive.ics.uci.edu/dataset/45/heart+disease](https://archive.ics.uci.edu/dataset/45/heart+disease)

Note: The processed.cleveland.data file does not contain a header. You will need to add the column names manually, which is handled inside the notebook.

License

This project is licensed under the MIT License see the LICENSE file for details
