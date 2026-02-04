# 🚕 Ride Price Estimation System
Created by: Mekdes Dereje Dejene
## Project Overview

This is a mini-project that built a machine learning system to predict ride-hailing prices in Ethiopia specifically in Addis Ababa. The goal was to see if a model could learn to estimate fares based on trip distance, time, and other factors like traffic and weather.

What this project does:
1. Predicts Price: Estimates the exact cost of a ride in Birr (Regression).
2. Classifies Cost: Decides if a ride is "High Cost" or "Low Cost" (Classification).

The dataset used in this project is synthetically generated to simulate realistic Ethiopian ride-hailing pricing behavior.

## Dataset Description

* Dataset name: `rides.csv`
* Number of rows: 160
* Target variable: `ride_price` (continuous)
* Source: Synthetic data created using Python
* Pricing logic:
  Ride price is calculated based on:

  * Base fee by vehicle type
  * Distance (km)
  * Duration (minutes)
  * Traffic level
  * Small random noise for realism

The dataset includes both **numerical** and **categorical** features to reflect real-world ride conditions.

## Features Used

* distance_km: The length of the trip.
* duration_min: How long the trip took in minutes.
* vehicle_type: The type of car.
* traffic_level: How busy the roads were.
* time_of_day: When the trip happened.
* weather: Environmental conditions.

## Steps Used
* Data Setup: I loaded the data and checked for any errors.
* Splitting: I split the data into a Training set and a Testing set.
* Preprocessing: I converted text categories into numbers and scaled the data.
* Modeling: I used Linear Regression for the price and Logistic Regression for the cost categories.

## How to Run (Google Colab)
1. Open Google Colab and upload the `.ipynb` notebook.
2. Click the folder icon on the left and upload `rides.csv`.
3. Go to Runtime > Run all to see the price predictions and classification results.

## Key Findings
* Distance and Time are the most important features for predicting the price.
* Traffic significantly increases the ride cost.
* The model can accurately learn pricing patterns without being given a specific formula.
* Data quality and feature design strongly affect model performance.


