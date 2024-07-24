# Taxi Fare Prediction Project

## Overview

This project aims to predict taxi fares based on various features including time, distance, and location. The key components include feature engineering, building predictive models, and analyzing feature importance to refine predictions.

## Features

1. **Data Processing**:
   - Address Conversion: Utilizes the ArcGIS library to convert addresses into geographical coordinates (longitude and latitude).
   - Removal of missing or irrelevant data.
   - Encoding categorical variables.

2. **Feature Engineering**:
   - **Cyclic Transformation**: Applies cyclic transformations to temporal data (e.g., day of the week, hour) to capture periodic patterns.
   - **Geospatial Feature Engineering**: 
     - **Clustering Methods**: 
       - **K-means Clustering**: Groups locations into clusters based on geographical coordinates.
       - **Agglomerative Clustering**: Utilizes hierarchical clustering to form clusters and determines the optimal number of clusters based on model performance.
     - **Pickup Coordinates Transformation**: Transforms pickup coordinates into a 3-D feature space to enhance model accuracy.

3. **Predictive Modeling**:
   - Trains XGBoost and Random Forest Regressor models to predict taxi fares.
   - Uses feature importance to understand the impact of various inputs.

4. **Model Evaluation**:
   - Assesses model performance using metrics like RMSE and R².
   - Saves the best performing model and clustering method.

5. **Price Prediction Simulation**:
   - **Distance and Duration Calculation**: Integrates OpenRouteService to compute distances between addresses and ETA.
   - **Predictive Modeling and Price Estimation**: Utilizes trained models to estimate taxi fares based on order time, pickup and drop-off locations. Predicts fare prices using the model, incorporating calculated using these features.




