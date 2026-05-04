***(Due to size limitations, the dataset flights.csv is not included in this repository. We used this Kaggle Dataset for our AI Model:
https://www.kaggle.com/datasets/usdot/flight-delays/data)***


## Flight Delay Prediction Using Machine Learning

Course: CAP 4630 – Intro to Artificial Intelligence
Semester: Spring 2026

## Team Members:

- Ena Tarumi
- Beyza Yavuz

## Project Overview:

Flight delays affect millions of passengers and cost airlines billions of dollars annually.
This project builds a machine learning model to predict whether a flight will be delayed or on time using historical flight data from the 2015 U.S. DOT dataset.

## Objectives:
- Predict flight delays using machine learning models
- Classify flights as: Delayed (≥ 15 minutes) or On Time
- Compare model performance using standard evaluation metrics
- Analyze which features most influence delays

## Dataset
Source: U.S. DOT On-Time Performance Dataset (2015)

Size: ~5.8 million flight records

Type: Structured tabular data

Features include:
- Airline
- Origin airport
- Destination airport
- Departure time
- Flight distance
- Arrival delay (target variable)

## Methodology:

1. Data Preprocessing
- Removed rows with missing critical values
- Created binary target variable: Delay ≥ 15 min → 1, On-time → 0

One-hot encoded categorical features:
- Airline
- Origin airport
- Destination airport
  

2. Feature Engineering
- Used numerical features such as departure time and distance
- Handled class imbalance in dataset
- Sampled 200,000 rows for efficient training


3. Model Training
- Decision Tree Classifier (scikit-learn)
- Train/Test split: 80/20
- Pipeline used for preprocessing + model training


4. Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix


## Results:
- Accuracy: 83.8% (can be anything, since its adjusted based on flight time/miles/airline
- Model performs well at predicting on-time flights
- Slight difficulty detecting delayed flights due to class imbalance

## Key Insights:
- Departure time is the most important feature in predicting delays
- Origin and destination airports also have strong influence
- Airline has relatively low impact compared to timing and route

## Visualizations:
- Confusion matrix shows strong performance on majority class (on-time flights)

Feature importance highlights:
- Departure time (highest impact)
- Airport features (moderate impact)
- Distance (lower impact)

## Challenges:
- Large dataset (~5.8M rows) required sampling for performance
- Class imbalance between delayed vs on-time flights
- Feature encoding increased dimensionality significantly

## Future Improvements:
- Try more advanced models (Random Forest, XGBoost)
- Use techniques for class imbalance (SMOTE or class weighting)
- Add external features such as:
- Weather conditions
- Seasonal trends
- Hyperparameter tuning for better performance

## Repository Structure:

```
flight-delay-prediction-ai/
│
├── app.py
├── train_model.py
├── flight_delay_project.ipynb
│
├── airlines.csv
├── airports.csv
│
└── README.md

```


## Links
📊 Google Colab Notebook: https://colab.research.google.com/drive/1ZsmtvLx19XyZv5duFC84_zu41Mv8Xfwg

🎥 Presentation Recording: https://youtu.be/loKBo4HVHNU


## What We Learned
- How to build a full machine learning pipeline
- Data preprocessing and encoding techniques
- Evaluating classification models using multiple metrics
- How class imbalance affects prediction performance


## Summary

This project demonstrates a complete machine learning workflow for predicting flight delays using real-world aviation data. Despite class imbalance, the model achieves solid performance and provides meaningful insights into key delay factors.
