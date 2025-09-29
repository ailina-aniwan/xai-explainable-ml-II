# AIPI 590 - XAI - Explainable ML II

## Global Explanations - California Housing 

This repository contains my assignment submission for the Explainable AI course. The notebook explores global explanation methods (PDP, ICE, and ALE) using the California Housing dataset.

## Dataset
The notebook uses the *California Housing dataset*, which is based on 1990 census data and is included in scikit-learn. The prediction task is to estimate the median house value (in units of $100,000) from features such as median income, average occupancy, average rooms, latitude, longitude, and several others. This dataset is widely used as a benchmark for regression tasks.

## Model
An *XGBoost Regressor* was trained on the California Housing dataset, with a train/test split handled using scikit-learn. This model serves as the basis for applying and demonstrating the global explanation techniques.

## Methods
The notebook compares three global explanation techniques:  
- Partial Dependence Plots (PDP)
- Individual Conditional Expectation (ICE) 
- Accumulated Local Effects (ALE)

## Exploratory Analysis
A correlation heatmap was used to examine feature relationships.  
- Strong correlation observed between `AveRooms` and `AveBedrms`.  
- Moderate correlation between `MedInc` and `AveRooms`.  
- Multicollinearity was noted, which influences PDP interpretation but is 
  handled more reliably by ALE.  

## Results
- PDP confirmed a strong positive effect of median income on predicted house values, with diminishing effects at higher income levels.  
- ICE showed heterogeneity that some neighborhoods respond more strongly to income than others.  
- ALE provided a correlation-adjusted view and showed the interaction between income and average rooms.  
- Comparison: PDP gives average trends, ICE shows variation, and ALE provides the most reliable effects under correlation.

## Run the Notebook

- Open the notebook directly in Google Colab by clicking this badge: [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ailina-aniwan/xai-explainable-ml-II/blob/main/global_explanations_california_housing.ipynb)

- Run all cells in order (click on `Run all`). The notebook is self-contained: it loads the dataset directly from an online source and reproduces all analysis.