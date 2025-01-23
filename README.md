# Pharma Counterfeit Sales Analysis

## Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)

## Overview
This project focuses on analyzing counterfeit pharmaceutical sales data using machine learning techniques. The goal is to predict counterfeit sales based on various features such as medicine type, area distribution, and other relevant attributes.

## Problem Statement
Counterfeit medicines are fake medicines that are either contaminated or contain the wrong or no active ingredient. They could have the right active ingredient but at the wrong dose. Counterfeit drugs are illegal and harmful to health. 

- **10% of the world's medicine is counterfeit**, and the problem is even worse in developing countries, where **up to 30% of medicines are counterfeit**.
- Millions of pills, bottles, and sachets of counterfeit and illegal medicines are traded worldwide.
- The World Health Organization (WHO) and Interpol are working to dismantle criminal networks involved in this trade, but counterfeit medicine operations continue to emerge.

Governments face the challenge of deploying resources effectively to counter these illegal operations. To address this, they have decided to focus on high-net-worth illegal operations first. This project uses collected data to **predict counterfeit sales figures** based on the characteristics of illegal operations, helping authorities prioritize their efforts.



## Dataset
The dataset used in this project contains information about counterfeit pharmaceutical sales, including:
- **Medicine_ID**: Unique identifier for each medicine.
- **Counterfeit_Weight**: Weight of counterfeit medicines.
- **DistArea_ID**: Distribution area ID.
- **Active_Since**: Duration since the medicine has been active.
- **Medicine_MRP**: Maximum Retail Price of the medicine.
- **Medicine_Type**: Type of medicine.
- **SidEffect_Level**: Side effect level of the medicine.
- **Availability_rating**: Availability rating of the medicine.
- **Area_Type**: Type of area.
- **Area_City_Type**: City type of the area.
- **Area_dist_level**: Distribution level of the area.
- **Counterfeit_Sales**: Target variable indicating counterfeit sales.

The dataset is split into training and test sets:
- **Training Data**: `counterfeit_train.csv`
- **Test Data**: `counterfeit_test.csv`

## Installation
To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/Pharma-Analysis.git
   cd Pharma-Analysis
    ```
2. **Install dependencies**:
Ensure you have Python 3.x installed. Then, install the required libraries:

 ```bash
pip install -r requirements.txt
 ```

## Usage
Open the Pharma.ipynb notebook in Jupyter or vs code.

Run each cell sequentially to load the data, preprocess it, train the model, and generate predictions.

The final predictions are saved in a CSV file named output.csv.

## Model Details
The model used in this project is a Gradient Boosting Regressor from the scikit-learn library. The model was trained using GridSearchCV for hyperparameter tuning. The best parameters found were:

- n_estimators: 100
- learning_rate: 0.1
- max_depth: 3
- min_samples_split: 2
- min_samples_leaf: 1

The model achieved a Mean Absolute Error (MAE) of approximately 752.97.

## Results
The model's predictions for the test dataset are saved in output.csv. The expected score (based on the MAE) is 0.546.
