# Stroke Mortality Prediction Model

# Project Overview

This repository contains a machine learning project focused on predicting the probability of death within 2 weeks after stroke. The project implements and compares various predictive models including penalized regression techniques (Ridge, Lasso, Elastic Net) and tree-based models (XGBoost).
Dataset
The analysis is based on data from 13,063 stroke patients with known outcomes, utilizing:

20 baseline variables including age, gender, systolic blood pressure
2 treatment variables
Binary outcome: death (1) or survival (0) within 2 weeks

# File Structure

assignment2025.csv: Original dataset containing stroke patient data (699 KB)
Machine_Learning_Candidate_492838_Final.R: R script with complete analysis code (41 KB)
Machine_Learning_Candidate_492838_Slides.pptx: PowerPoint presentation summarizing the findings (25,052 KB)

# Methodology
The project implements several machine learning approaches:
Data Preparation

80/20 train-test split
K-fold cross-validation (k=10, k=5 for XGBoost)
Class imbalance handling (95.3% survival rate)

# Models Implemented

Ridge Regression (α = 0, λ = 0.046)

Effectively handles multicollinearity
AUC: 0.809, Sensitivity: 0.760, Specificity: 0.748


Lasso Regression (α = 1, λ = 0.042)

Performs feature selection by eliminating some variables
AUC: 0.792, Sensitivity: 0.709, Specificity: 0.797


Elastic Net Regression (α = 0.3, λ = 0.058)

Combines Ridge and Lasso approaches
AUC: 0.816, Sensitivity: 0.799, Specificity: 0.707


XGBoost Models

Basic implementation and advanced tuned version
Handles non-linear relationships and class imbalance



# Performance Metrics

AUC (Area Under ROC Curve)
Sensitivity (TP/(TP+FN)) - ability to detect deaths
Specificity (TN/(TN+FP)) - ability to identify survivors
F1 Score - harmonic mean of precision and recall
Balanced Accuracy - average of sensitivity and specificity

# Key Findings

Elastic Net regression achieved the best overall performance (AUC: 0.816)
Different models show trade-offs between sensitivity and specificity
Most important predictors include:

# Stroke subtype
Consciousness level
Age
Treatment variables
Specific symptoms


# Requirements
The analysis was performed using R with the following packages:

Data manipulation: tidyverse, dplyr
Visualization: ggplot2, ggcorrplot, GGally
Machine learning: glmnet, mboost, xgboost, randomForest
Model evaluation: caret, pROC

# Usage

Clone this repository
Ensure all required R packages are installed
Run the Machine_Learning_Candidate_492838_Final.R script
View results in the console or export to your preferred format
