# Flight AI

## AI Travel Analyst for Flight Price Analysis and Prediction

Flight AI is a datadriven flight price analysis and prediction project developed as part of the Data Science and Visualisation track.

The project explores the factors associated with flight prices and uses machine learning to predict flight prices based on flight characteristics, travel conditions, and booking information.

The project also includes a Cheapest Booking Time Analysis to help travelers identify booking windows associated with lower observed fares.

---

 1. Project Overview

Flight prices vary depending on several factors such as airline, travel class, route, distance, number of stops, season, and how far in advance the ticket is booked.

The objective of Flight AI is to analyze these factors using the provided flight dataset and develop a machine learning model capable of predicting flight prices.

The project consists of:

- Data cleaning and preprocessing
- Exploratory data analysis
- Feature engineering
- Flight price prediction
- Model evaluation
- Feature importance analysis
- Cheapest booking time analysis
- Interactive dashboard

---

## 2. Problem Statement

Travelers often have difficulty understanding why flight prices vary and when they should book a flight.

This project aims to:

1. Analyze the major factors associated with flight prices.
2. Identify patterns in flight pricing.
3. Build a machine learning model for flight price prediction.
4. Identify important features influencing predictions.
5. Analyze booking windows to identify periods associated with lower observed fares.

---

## 3. Dataset Used

The project uses the mandatory dataset provided by the organizers.

The dataset contains 100,000 flight records and 18 original columns.

Important attributes include:

- Flight ID
- Airline
- Source
- Destination
- Departure Date
- Departure Time
- Arrival Time
- Duration
- Total Stops
- Distance
- Travel Class
- Days Before Departure
- Season
- Weekday
- Aircraft Type
- Booking Channel
- Passenger Count
- Price

The dataset contains both numerical and categorical variables and includes missing values that require preprocessing.

---

## 4. Methodology

The project follows the following workflow:

Dataset

Data Inspection

Data Cleaning

Feature Engineering

Data Analysis

Train/Test Split

Feature Preprocessing

Machine Learning Model

Model Evaluation

Feature Importance

Cheapest Booking Time Analysis

Interactive Application

---

## 5. Data Cleaning and Preprocessing

The dataset was inspected for:

- Missing values
- Duplicate records
- Inconsistent values
- Mixed-format duration values
- Invalid or inconsistent date/time information
- Missing categorical values

Duplicate records were removed before modeling.

Duration values were converted into numerical duration in minutes.

Additional date and time features were extracted from the original date/time fields.

Categorical variables were handled separately from numerical variables.

---

## 6. Feature Engineering

The following features were derived or cleaned for modeling:

- Duration in minutes
- Cleaned number of stops
- Journey year
- Journey month
- Journey day
- Journey day of week
- Departure hour
- Arrival hour

The original weekday information was checked against the weekday calculated from the departure date.

The calculated weekday was used as the modeling feature because it can be deterministically derived from the actual date.

---

## 7. Exploratory Data Analysis

Six major analyses were performed.

### 7.1 Airline vs Price

Airline showed substantial differences in average observed flight prices.

Qatar Airways had the highest average observed fare among the airlines in the cleaned modeling data.

### 7.2 Travel Class vs Price

Travel class showed a strong relationship with price.

First Class had the highest average observed fare, followed by Business and Premium Economy, while Economy had the lowest average price among known classes.

### 7.3 Number of Stops vs Price

Flights with more stops showed higher average observed prices in this dataset.

Nonstop flights had the lowest average price among the three observed stop categories.

### 7.4 Distance vs Price

Distance had a Pearson correlation of approximately 0.651 with flight price.

This indicates a moderately strong positive relationship between distance and observed price.

### 7.5 Booking Window vs Price

Booking time showed a clear relationship with price.

Flights booked 0–7 days before departure had an average price of approximately ₹89,756.

Flights booked 91–180 days before departure had the lowest observed average price among the available booking windows at approximately ₹60,593.

### 7.6 Season vs Price

Seasonality was also associated with differences in observed flight prices.

Summer had the highest average price among the known seasons, while Monsoon had the lowest.

---

## 8. Machine Learning

A Linear Regression model was first developed as a baseline.

The baseline model achieved:

- MAE: ₹23,858.63
- RMSE: ₹52,668.19
- R²: 0.5547

A Random Forest Regressor was then evaluated as a non-linear machine learning model.

Final model results will be added after model evaluation is completed.

---

## 9. Model Results

 Model  MAE  RMSE  R² 
 Linear Regression  ₹23,858.63  ₹52,668.19  0.5547 
 Random Forest  ₹15,593.06  ₹49,182.55  0.6117 

Random Forest was selected as the final model because it outperformed the Linear Regression baseline across all three evaluation metrics.

The Random Forest reduced MAE by approximately 34.6% compared with the baseline and increased the R² score from 0.5547 to 0.6117.
## 10. Feature Importance

The Random Forest feature-importance analysis identified the following major predictive features:

1. Duration_Minutes - 51.60%
2. Distance_km - 15.83%
3. Travel_Class_Economy - 8.77%
4. Days_Before_Departure - 5.26%
5. Travel_Class_Business - 1.72%
6. Travel_Class_First - 1.71%

Duration and distance together account for approximately 67.4% of the model's feature importance.

Feature importance represents the model's predictive behavior and should not be interpreted as causal influence.

## 11. Technologies Used

### Programming Language

- Python

### Data Science

- Pandas
- NumPy
- Scikit-learn

### Visualization

- Matplotlib

### Machine Learning

- Linear Regression
- Random Forest Regression

### Application

- Streamlit

### Development Environment

- Google Colab
- GitHub

---

## 12. Results

Final model performance:

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 23,858.63 | 52,668.19 | 0.5547 |
| Random Forest | TBD | TBD | TBD |

The Random Forest results will be added after final evaluation.

---

## 13. Challenges Faced

### Missing Data

The dataset contained missing values across several columns.

### Mixed Duration Formats

Duration values appeared in multiple formats, including hour/minute representations and minute-based values.

These were converted into a common numerical representation in minutes.

### Inconsistent Weekday Information

The supplied weekday information was compared with the weekday calculated from the departure date.

The calculated weekday was used for modeling because it is derived directly from the date.

### Model Selection

Linear Regression was used as a baseline before testing a non-linear tree-based model.

This allowed model improvement to be measured rather than selecting a complex model without comparison.

---

## 14. Future Improvements

Possible future improvements include:

- More extensive hyperparameter tuning
- Additional route level features
- Advanced model explainability using SHAP
- More detailed price forecasting
- Real-time flight data integration
- Improved recommendation logic
- Interactive dashboard enhancements

---

## 15. Screenshots

<img width="2971" height="1765" alt="season_vs_price" src="https://github.com/user-attachments/assets/fd9d6e45-c5ed-42b1-8788-cadf05924f0d" />
<img width="3271" height="1765" alt="booking_window_vs_price" src="https://github.com/user-attachments/assets/f76bdf00-0866-4980-83ee-98eddfb42f55" />
<img width="2970" height="1765" alt="distance_vs_price" src="https://github.com/user-attachments/assets/d902d873-4d56-40b3-850d-2e6867e4630b" />
<img width="2971" height="1765" alt="stops_vs_price" src="https://github.com/user-attachments/assets/829b5d53-e370-46a0-9188-ef5b69a06844" />
<img width="2971" height="1765" alt="travel_class_vs_price" src="https://github.com/user-attachments/assets/72dc6b35-8529-48f1-8424-72d287d1e022" />
<img width="3571" height="1765" alt="airline_vs_price" src="https://github.com/user-attachments/assets/155b3fdb-37d0-40a6-954e-74b9838fbddb" />







---

## 16. Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/flightpredicter-ai.git
cd flightpredicter-ai
