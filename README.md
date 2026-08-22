# Flight AI

## AI Travel Analyst for Flight Price Analysis and Prediction

Flight AI is a data-driven flight price analysis and prediction project developed as part of the Data Science and Visualisation track.

The project explores the factors associated with flight prices and uses machine learning to predict flight prices based on flight characteristics, travel conditions, and booking information.

The project also includes a Cheapest Booking Time Analysis to help travelers identify booking windows associated with lower observed fares.

---

 1. Project Overview

Flight prices vary depending on several factors such as airline, travel class, route, distance, number of stops, season, and how far in advance the ticket is booked.

The objective of FlightWise AI is to analyze these factors using the provided flight dataset and develop a machine learning model capable of predicting flight prices.

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
↓
Data Inspection
↓
Data Cleaning
↓
Feature Engineering
↓
Exploratory Data Analysis
↓
Train/Test Split
↓
Feature Preprocessing
↓
Machine Learning Model
↓
Model Evaluation
↓
Feature Importance
↓
Cheapest Booking Time Analysis
↓
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

Non-stop flights had the lowest average price among the three observed stop categories.

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

## 9. Model Evaluation

The models are evaluated using:

### Mean Absolute Error (MAE)

Measures the average absolute difference between predicted and actual prices.

### Root Mean Squared Error (RMSE)

Measures prediction error while giving greater weight to larger errors.

### R² Score

Measures the proportion of variance in flight prices explained by the model.

The final model will be selected based on test-set performance and practical interpretability.

---

## 10. Cheapest Booking Time Analysis

The project analyzes flight prices across different booking windows:

- 0–7 days
- 8–14 days
- 15–30 days
- 31–60 days
- 61–90 days
- 91–180 days

The analysis indicates that booking closer to departure is associated with higher observed prices in the supplied dataset.

The 91–180 day window had the lowest observed average fare among the available booking windows.

This result represents an observed relationship in the dataset and should not be interpreted as a guarantee of future ticket prices.

---

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
- Additional route-level features
- Advanced model explainability using SHAP
- More detailed price forecasting
- Real-time flight data integration
- Improved recommendation logic
- Interactive dashboard enhancements

---

## 15. Screenshots

Screenshots of the exploratory analysis and Streamlit application will be added here.

---

## 16. Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/flightwise-ai.git
cd flightwise-ai
