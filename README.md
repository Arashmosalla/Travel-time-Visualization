# Data Preprocessing Visualization for ANPR Systems

## Overview
This repository contains the **visualization component** of the data preprocessing methodology developed in my thesis. The goal is to analyze the dataset after it has undergone initial preprocessing and flagging, focusing on **distribution analysis** of key speed metrics. 

The dataset originates from an **Automatic Number Plate Recognition (ANPR) system** and was subjected to an initial processing phase to classify records into different categories based on data quality and driving behavior. This visualization examines how preprocessing impacts the dataset, particularly by analyzing **space mean speed** and the **mean of two point speeds**.

## Dataset & Initial Processing
Before reaching this visualization stage, the dataset was **preprocessed and flagged** based on several criteria:

- **Retained Records**: Data points that were considered valid after preprocessing.
- **Insufficient Data**: Records excluded due to incomplete information or unreliable timestamps from the ANPR system.
- **Dropped Records**: Extreme outliers detected using the **Locally Weighted Scatterplot Smoothing (LOWESS)** algorithm, where residuals exceeded three standard deviations (3STD).
- **Stop-by Events**: Instances where driver behavior suggested stopping, identified based on the **relative difference between point speeds and space mean speed**. These records were removed to ensure uninterrupted driving behavior.

## Purpose of This Code
This code is designed **solely for visualization and analysis**, rather than step-by-step preprocessing. The primary objective is to explore **the distribution of key speed metrics** and understand how preprocessing affects the dataset. The analysis focuses on:

- **Space Mean Speed**: The average speed computed based on time-weighted observations.
- **Mean of Two Point Speeds**: The combined speed from two ANPR cameras.

Through this visualization, we aim to evaluate how well the dataset aligns with the assumptions of the model being applied.

## Future Updates
This repository currently focuses **only on visualization**. The **detection logic and full preprocessing implementation** will be added in a future update, which will include:
- The complete preprocessing pipeline for detecting stop events and handling outliers.
- Enhanced reproducibility with parameterized preprocessing steps.
- Additional insights into data transformations before visualization.