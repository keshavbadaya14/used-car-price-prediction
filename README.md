# Used Car Price Prediction

## Project Overview

This project aims to predict the selling price of used cars using machine learning techniques. The dataset contains information about vehicle specifications such as brand, model year, mileage, fuel type, transmission, accident history, and engine details.

The goal is to build a regression model capable of estimating the market value of a used car based on its characteristics.

---

## Dataset Information

The dataset contains:

* Brand
* Model
* Model Year
* Mileage
* Fuel Type
* Engine Information
* Transmission
* Exterior Color
* Interior Color
* Accident History
* Clean Title Status
* Price (Target Variable)

---

## Data Preprocessing

The following preprocessing steps were performed:

* Converted mileage from text to numerical values
* Converted price from text to numerical values
* Handled missing values in:

  * fuel_type
  * accident
  * clean_title
* Removed unnecessary features
* Created additional features for better prediction

---

## Feature Engineering

New features created:

### Car Age

Car age was calculated from the manufacturing year.

```python
car_age = 2026 - model_year
```

### Horsepower Extraction

Horsepower was extracted from the engine description.

### Engine Size Extraction

Engine displacement (L) was extracted from the engine description.

---

## Exploratory Data Analysis

Key observations:

* Price distribution is highly right-skewed.
* Approximately 50% of cars cost less than $30,000.
* Approximately 75% of cars cost less than $50,000.
* The dataset contains luxury vehicles with prices above $1 million.
* Mileage and car age show a negative relationship with price.

---

## Models Used

### Linear Regression

Used as a baseline regression model.

### Decision Tree Regressor

Captures non-linear relationships between features.

### Random Forest Regressor

Uses bagging and ensemble learning to improve prediction performance.

---

## Model Performance

| Model                   | R² Score |
| ----------------------- | -------- |
| Linear Regression       | 0.787    |
| Decision Tree Regressor | 0.726    |
| Random Forest Regressor | 0.822    |

Random Forest achieved the best performance.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

---

## Author

Keshav Badaya
