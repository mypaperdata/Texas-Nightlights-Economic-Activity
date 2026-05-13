# Nighttime Lights as a Proxy for Local Economic Activity: Evidence from Texas Cities

This repository contains the code and processing pipeline for the paper:

> **Nighttime Lights as a Proxy for Local Economic Activity: Evidence from Texas Cities**  
> Orhan Erdem  
> University of North Texas

## Overview

This project examines whether satellite-derived nighttime lights can serve as high-frequency proxies for local economic activity. Using monthly VIIRS Day/Night Band imagery, Google Earth Engine (GEE), and Texas municipal sales tax allocation data, the study evaluates the predictive performance of linear models, machine learning models, and deep learning architectures.

The paper focuses particularly on whether predictive validity varies systematically across cities of different population scales.

## Main Components

The project includes:

- Google Earth Engine pipeline for extracting monthly nighttime-light features
- Construction of city-level monthly radiance measures
- Generation of 64 × 64 nighttime-light image tiles
- Linear regression models
- Multilayer perceptron (MLP) models
- Convolutional neural network (CNN) models
- Hybrid CNN-tabular models
- Evaluation across population-based city groups

## Data Sources
- "Sales_Tax_Allocation_TX_City.xlsx"
- "Texas_City_Night_Lights_Mean_Sum.csv"
- "Population Texas Cities.xlsx"

### Nighttime Lights
- VIIRS Day/Night Band monthly composites
- Accessed through Google Earth Engine

### Economic Activity
- Texas Comptroller monthly city sales tax allocation data

## Main Notebook

- `Nightlights_v6.ipynb`

This notebook contains:
- data preparation,
- feature engineering,
- image-tile generation,
- model training,
- evaluation,
- and figure generation.

## Methodological Highlights

- Time-based train/validation/test split
- Prevention of temporal leakage
- Comparison of pooled vs within-group predictive performance
- Fixed-effects robustness analysis
- Hybrid image-tabular deep learning framework

## Software and Libraries

Main Python libraries include:

- pandas
- numpy
- matplotlib
- scikit-learn
- tensorflow / keras
- Google Earth Engine API

## Reproducibility Notes

Some large intermediate files (e.g., image tensors and processed panels) are not included in the repository due to storage limitations. The repository focuses on providing the full analytical workflow and reproducible processing pipeline.

Users may need:
- access to Google Earth Engine,
- Texas sales tax data,
- and local storage paths configured for their environment.

## Citation

If you use this code or repository, please cite:

Erdem, O. *Nighttime Lights as a Proxy for Local Economic Activity: Evidence from Texas Cities.*

## Contact

Orhan Erdem  
University of North Texas  
orhan.erdem@unt.edu