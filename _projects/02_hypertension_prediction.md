---
layout: page
title: Lifestyle Features and Hypertension Prediction
description: Evaluating whether lifestyle information improves hypertension prediction using leakage-controlled machine learning.
importance: 2
---

## Overview

This research investigates whether routinely available lifestyle information improves machine learning predictions of hypertension beyond demographic, socioeconomic, and anthropometric characteristics.

The study uses data from 8,024 adults in the 2017–March 2020 pre-pandemic National Health and Nutrition Examination Survey (NHANES).

**Publication:** Machine Learning for Health (ML4H) 2026 Findings Track.

**Links:** [Paper (OpenReview)](https://openreview.net/forum?id=BW9QSU8cTo) · [GitHub Repository](https://github.com/urielbenymon/nhanes-lifestyle-hypertension)

## Methodology

We compared baseline predictors against lifestyle-augmented predictors incorporating physical activity, alcohol consumption, smoking, and sleep.

Five machine learning model families were evaluated:

1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. Bagged Decision Trees
5. XGBoost

Preprocessing and hyperparameter tuning were performed within the training data to reduce information leakage. Models were evaluated using held-out test data and paired bootstrap confidence intervals.

We also conducted SHAP feature-importance analyses and sensitivity checks.

## Key Findings

- Adding lifestyle variables did not consistently improve hypertension prediction over the baseline feature set.
- Blood pressure measurements, age, and body mass index were among the most influential predictors.
- The findings underscore the importance of evaluating incremental predictive value rather than assuming that additional features necessarily improve performance.

## Reproducibility

The public repository contains the data acquisition scripts, preprocessing pipeline, model training and evaluation code, statistical analyses, and generated results.

The pipeline retrieves publicly available NHANES data directly from the CDC.
