# Predictive Maintenance for Industrial Equipment

This project applies machine learning algorithms to predict when industrial equipment is likely to fail using a Random Forest Classifier. The goal is to enable predictive maintenance to minimize downtime and optimize operational efficiency.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Setup](#setup)
- [Results](#results)
- [License](#license)

## Overview

Predictive Maintenance uses machine learning algorithms to analyze historical data and predict when equipment is likely to fail. This project implements a Random Forest Classifier to achieve accurate failure predictions using sensor data from industrial machinery.

## Features

- Data Preprocessing with Feature Engineering
- Model Training using Random Forest Classifier
- Evaluation using Accuracy Score and Classification Report
- Visualization of Results

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

## Dataset

- The dataset used is named `equipment_data.csv`.
- It contains sensor readings and operational data for multiple pieces of equipment.
- The dataset was preprocessed using time-based feature extraction.


## Model Training

A Random Forest Classifier was trained using the following configuration:

- **Estimators**: 100
- **Max Depth**: 9
- **Min Samples Split**: 20
- **Max Features**: 8

```python
model = RandomForestClassifier(n_estimators=100, random_state=40, min_samples_split=20, max_features=8, max_depth=9)
model.fit(X_train, y_train)
```

## Evaluation

The model's performance was evaluated using Accuracy Score and Classification Report.

```python
from sklearn.metrics import accuracy_score, classification_report

y_test_pred = model.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_test_pred))
print(classification_report(y_test, y_test_pred))
```

## Results

The model achieved the following accuracy:

```plaintext
Accuracy: 0.509
```

The classification report provides detailed performance metrics.

## License

This project is licensed under the MIT License. Feel free to use and modify it as per your requirements.
