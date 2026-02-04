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

### Real-World Pricing Logic
This project models the pricing behavior of the RIDE app in Addis Ababa. According to local fare data, the total cost of a trip is calculated using a fixed base fee plus a rate for every kilometer and minute traveled:

Total Fare = Base Fee + (Distance × KM Rate) + (Time × Minute Rate)

* Base Fee: A one-time fixed charge that starts as soon as the meter begins (typically between 130 ETB and 172 ETB depending on the car type).

* Distance Rate: A charge for every kilometer traveled, currently standard at 18 ETB/km.

* Time Rate: A charge for the duration of the trip, usually 3–4 ETB per minute, which helps account for heavy traffic congestion.

Traffic Influence: While the formula is fixed, traffic indirectly increases the fare by adding more minutes to the "Time Rate" portion of the calculation.

## Vehicle Rate

| Type of Car | Base Fee (ETB) | Time Rate (ETB/min) | Distance Rate (ETB/km) | Night Time Rate (ETB/min) | Night Distance Rate (ETB/km) |
|:---|:---:|:---:|:---:|:---:|:---:|
| **MIDSIZE4** | 171 | 4 | 18 | 4 | 24 |
| **Comfort \| New Cars** | 172 | 4 | 19 | 4 | 25 |
| **MINIVAN 7** | 245 | 3 | 28 | 4 | 31 |
| **Ride Any EV** | 170 | 4 | 18 | 4 | 24 |

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


