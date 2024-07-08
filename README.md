# E-commerce Customer Behavior Analysis and Segmentation

This project analyzes customer behavior and segments customers in an e-commerce context using machine learning techniques. The dataset includes information about customers' demographics, product preferences, and purchasing patterns.

## Table of Contents

- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Project Goals](#project-goals)
- [Methods and Techniques](#methods-and-techniques)
- [Results](#results)

## Introduction

Understanding customer behavior is crucial for e-commerce businesses to personalize marketing strategies, improve customer satisfaction, and optimize product offerings. This project leverages machine learning algorithms to predict customer purchases and segment customers based on their characteristics.

## Dataset Overview

The dataset includes the following columns:
- Customer ID
- Gender
- Age
- Salary
- Product ID
- Price
- Purchased (Target variable)

## Project Goals

1. **Customer Purchase Prediction**:
   - Build and evaluate machine learning models to predict whether a customer will purchase a product.

2. **Customer Segmentation**:
   - Utilize clustering algorithms to segment customers based on demographic and behavioral attributes.

3. **Feature Importance Analysis**:
   - Determine which factors (e.g., Age, Salary, Product Price) influence customer purchasing decisions the most.

## Methods and Techniques

### Data Preprocessing
- Encoding categorical variables (Gender, Product ID)
- Scaling numerical features (Age, Salary, Price)

### Model Evaluation

Two different splitting methods were used to evaluate model performance:

#### Stratified Splitting

| Model    | Accuracy | Precision | Recall   | F1 Score |
|----------|----------|-----------|----------|----------|
| LogReg   | 0.820    | 0.783     | 0.783    | 0.783    |
| DecTree  | 0.780    | 0.747     | 0.711    | 0.728    |
| RandFor  | 0.785    | 0.750     | 0.723    | 0.736    |
| SVM      | 0.790    | 0.773     | 0.699    | 0.734    |
| NaiveBay | 0.780    | 0.760     | 0.687    | 0.722    |
| KNN      | 0.765    | 0.725     | 0.699    | 0.712    |

#### Default Random Splitting

| Model    | Accuracy | Precision | Recall   | F1 Score |
|----------|----------|-----------|----------|----------|
| LogReg   | 0.815    | 0.753     | 0.782    | 0.767    |
| DecTree  | 0.750    | 0.679     | 0.679    | 0.679    |
| RandFor  | 0.770    | 0.716     | 0.679    | 0.697    |
| SVM      | 0.795    | 0.740     | 0.731    | 0.735    |
| NaiveBay | 0.795    | 0.734     | 0.744    | 0.739    |
| KNN      | 0.760    | 0.679     | 0.731    | 0.704    |

### Results

- Stratified splitting generally improves model performance metrics compared to default random splitting.
- Logistic Regression and SVM show more consistent results across both splitting methods.
- Decision Tree and Random Forest perform better with stratified splitting, indicating the importance of balanced class distributions in training and testing sets.

## Usage

### Requirements

- Python 3.x
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn
