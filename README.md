# Sales Forecasting Using Machine Learning

## Project Overview

This project predicts daily sales for Rossmann stores using historical sales data and store-level information.

The project demonstrates a complete machine learning workflow, including:

* Data exploration
* Data cleaning
* Feature engineering
* Time-based train/validation splitting
* Categorical encoding
* Model training
* Model evaluation
* Sales prediction

## Dataset

The project uses the Rossmann Store Sales dataset from Kaggle.

Dataset source:

https://www.kaggle.com/competitions/rossmann-store-sales/data

The dataset contains historical sales information for Rossmann stores along with information about promotions, holidays, competition, and store characteristics.

## Machine Learning Approach

### Features

The model uses features including:

* Store
* Day of week
* Promotion
* State holiday
* School holiday
* Store type
* Assortment
* Competition distance
* Competition information
* Promo2 information
* Year
* Month
* Day
* Weekend indicator
* Quarter
* Week of year
* Month start/end indicators

The `Customers` column was not used because future customer counts are not available when making predictions.

## Validation Strategy

Because this is a forecasting problem, a random train/test split was not used.

Instead, historical dates were used for training and the most recent 42 days were used for validation.

This better represents the real-world situation of predicting future sales from past data.

## Models

The project includes:

1. Baseline model
2. Random Forest Regressor
3. HistGradientBoosting Regressor

The models were evaluated using:

* RMSE
* MAE
* R²

## Final Model

The final production model is a Random Forest Regressor trained using the available historical training data.

Predictions for closed stores are set to zero.

## Project Structure

```text
sales-forecasting-ml/
│
├── data/
├── notebooks/
│   └── 01_sales_forecasting.ipynb
├── .gitignore
├── requirements.txt
└── README.md
```

## How to Run

Clone the repository and install the dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook
```

Then run:

```text
notebooks/01_sales_forecasting.ipynb
```

## Skills Demonstrated

* Python
* Pandas
* NumPy
* Data Visualization
* Exploratory Data Analysis
* Feature Engineering
* Scikit-learn
* Regression
* Time-based validation
* Model evaluation
* Machine learning workflow
* ## Author
TANVIR AHMED
