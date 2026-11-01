
# Car Price Prediction Using Machine Learning

## Project Overview

This project focuses on predicting the selling prices of used cars using Machine Learning regression techniques.

The objective is to understand how vehicle characteristics influence resale prices and develop a predictive model that can estimate the selling price of a used car based on its available features.

The project involves data cleaning, exploratory data analysis, feature engineering, regression modelling and model evaluation.

It was completed as part of the CodeAlpha Data Science Internship.

## Project Objectives

- Understand the factors influencing used-car selling prices.
- Perform data cleaning and preprocessing.
- Conduct exploratory data analysis.
- Investigate relationships between vehicle features and selling prices.
- Engineer relevant features for predictive modelling.
- Train and compare regression algorithms.
- Evaluate model performance using appropriate metrics.
- Identify the most suitable model for price prediction.

## Dataset Description

The project uses a used-car dataset named:

`car data.csv`

The dataset contains vehicle information and historical selling prices.

The features explored include:

| Feature | Description |
|---|---|
| Present_Price | Recorded original/current price of the vehicle |
| Kms_Driven | Distance covered by the vehicle |
| Fuel_Type | Fuel category |
| Seller_Type | Type of seller |
| Transmission | Manual or automatic transmission |
| Owner | Number of previous owners |
| Car_Age | Engineered vehicle-age feature |
| Selling_Price | Target variable |

The selling price is measured in lakhs in the original dataset.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git and GitHub

## Project Workflow

### 1. Data Loading and Inspection

The dataset was loaded using Pandas.

Initial inspection was conducted to understand its structure, identify data types and examine the available variables.

### 2. Data Cleaning and Preprocessing

The dataset was examined for missing values, duplicate records and potential data-quality issues.

Relevant features were prepared for analysis and model development.

### 3. Exploratory Data Analysis

EDA was performed to understand the distribution of selling prices and examine relationships between vehicle characteristics and resale values.

The analysis included:

- Selling price distributions.
- Relationships between present price and selling price.
- Vehicle age and depreciation patterns.
- Distance driven and resale value.
- Fuel type and transmission comparisons.
- Correlation analysis.

### 4. Feature Engineering

Vehicle age was represented using the `Car_Age` feature to investigate the relationship between vehicle age and depreciation.

Relevant numerical and categorical features were prepared for regression modelling.

### 5. Model Development

Four regression algorithms were explored:

1. Linear Regression
2. Ridge Regression
3. Random Forest Regressor
4. Gradient Boosting Regressor

The models were compared to investigate their predictive performance.

### 6. Model Evaluation

The models were evaluated using three regression metrics:

**R² Score**

Measures how much of the variation in the target variable is explained by the model.

**Mean Absolute Error (MAE)**

Measures the average absolute difference between actual and predicted selling prices.

**Root Mean Squared Error (RMSE)**

Measures prediction error while giving greater weight to larger errors.

For MAE and RMSE, lower values indicate better performance. A higher R² score generally indicates a better fit.

## Model Performance

Based on the recorded test-set results, Ridge Regression achieved the strongest overall performance.

| Evaluation Metric | Ridge Regression |
|---|---:|
| R² Score | 0.958 |
| MAE | 0.735 lakhs |
| RMSE | 1.083 lakhs |

The R² score indicates that the model explained approximately 95.8% of the variation in selling prices in the evaluated test set.

The MAE indicates an average absolute prediction error of approximately 0.735 lakhs.

These results are specific to the dataset and evaluation split used in the project. They should not be interpreted as a guarantee of performance on other vehicle markets.

## Key Findings

The analysis highlighted several important relationships:

- Present price plays an important role in determining used-car selling prices.
- Vehicle age is an important factor associated with depreciation.
- Different vehicle categories can exhibit different resale-price patterns.
- Ridge Regression performed strongly compared with the other evaluated models on the recorded test set.
- High-priced vehicles can be more difficult to predict accurately, highlighting the importance of further validation.

## Practical Applications

The project demonstrates how Machine Learning can support:

- Preliminary used-car price estimation.
- Data-driven vehicle valuation.
- Used-car marketplace analytics.
- Understanding vehicle depreciation.
- Supporting buyers, sellers and dealerships with price-related decisions.

The model should be treated as an analytical estimation tool rather than a replacement for professional vehicle valuation.

## Project Structure

```text
CodeAlpha_Car_Price_Prediction/
│
├── CodeAlpha_Car_Price_Prediction.ipynb
├── car data.csv
├── car_price_model.pkl
└── README.md
```

## How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook.

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Steps

1. Clone the repository:

```bash
git clone https://github.com/Bwalii/CodeAlpha_Car_Price_Prediction.git
```

2. Navigate into the project directory:

```bash
cd CodeAlpha_Car_Price_Prediction
```

3. Launch Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `CodeAlpha_Car_Price_Prediction.ipynb`.

5. Run the notebook cells sequentially.

Ensure that `car data.csv` is available in the project directory.

## Limitations

- The dataset represents a limited sample of used-car listings.
- Market prices may vary across geographical locations and time periods.
- Vehicle condition, maintenance history and other relevant factors may not be fully represented.
- Model performance on the available dataset may differ when applied to new market conditions.

## Future Improvements

- Incorporate additional vehicle specifications.
- Include geographical and market-related variables.
- Explore additional regression algorithms.
- Perform more extensive cross-validation and hyperparameter tuning.
- Develop an interactive application for used-car price estimation.
- Test the model on additional vehicle datasets.

## Internship Information

This project was completed as part of the CodeAlpha Data Science Internship.

## Author

**Mubarak Bashir Wali**

- GitHub: [Bwalii](https://github.com/Bwalii)
- Project: [Car Price Prediction](https://github.com/Bwalii/CodeAlpha_Car_Price_Prediction)

## Acknowledgements

Thanks to CodeAlpha for providing the opportunity to gain practical experience in data preprocessing, exploratory analysis, feature engineering and Machine Learning model development.
