
# 🚗 Car Price Prediction | CodeAlpha Data Science Internship

## 📌 Project Overview

This project focuses on predicting the selling prices of used cars using machine learning techniques. It was completed as part of the **CodeAlpha Data Science Internship**.

The project explores the factors that influence used-car prices, performs exploratory data analysis (EDA), and builds and evaluates multiple regression models to identify the most suitable model for price prediction.

The main objective is to develop a reliable model that can help buyers, sellers, and dealerships estimate used-car prices and make more informed decisions.

## 🎯 Project Objectives

- Analyze the dataset to understand the factors affecting used-car selling prices.
- Perform data cleaning and exploratory data analysis.
- Investigate the relationships between vehicle characteristics and selling prices.
- Build and compare multiple regression models.
- Evaluate model performance using appropriate regression metrics.
- Select the best-performing model for predicting used-car prices.
- Provide actionable insights and recommendations based on the findings.

## 📂 Project Structure

```text
CodeAlpha_Car_Price_Prediction/
│
├── Car_Price_Prediction.ipynb   # Analysis, visualizations, and model development
├── car data.csv                 # Dataset (if included)
├── README.md                    # Project documentation
├── requirements.txt             # Project dependencies (if included)
└── ridge_model.pkl              # Saved model (if included)
```

*Note: Adjust the filenames and folders above to match the actual contents of your repository.*

## 📊 Dataset Description

The project uses a used-car dataset containing information about vehicles and their selling prices.

The dataset includes features such as:

| Feature | Description |
|---|---|
| `Present_Price` | Original or current ex-showroom price of the car, as recorded in the dataset |
| `Car_Age` | Age of the car in years |
| `Kms_Driven` | Total distance covered by the car |
| `Fuel_Type` | Type of fuel used by the vehicle |
| `Seller_Type` | Whether the seller is an individual or dealer |
| `Transmission` | Manual or automatic transmission |
| `Owner` | Number of previous owners, as recorded in the dataset |
| `Selling_Price` | Target variable representing the car's selling price |

The exact features depend on the dataset version used in the project. Additional engineered features, such as `Km_per_Year`, may also be included in the analysis.

## 🛠️ Technologies and Tools

The project was developed using the following technologies:

- **Python** – Programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **Scikit-learn** – Machine learning, preprocessing, and model evaluation
- **Jupyter Notebook** – Interactive development and documentation
- **Git and GitHub** – Version control and project hosting

## 🔍 Project Workflow

### 1. Data Loading and Cleaning

- Loaded the dataset into a Pandas DataFrame.
- Inspected the dataset structure, data types, and missing values.
- Checked for duplicate records and potential data-quality issues.
- Prepared the relevant features for analysis and modeling.

### 2. Exploratory Data Analysis (EDA)

Exploratory analysis was performed to understand the dataset and identify patterns affecting used-car prices.

The analysis included:

- Descriptive statistics.
- Distribution plots and histograms.
- Boxplots to inspect price distributions and potential outliers.
- Correlation analysis.
- Feature comparisons against selling price.
- Analysis of depreciation and price retention.
- Examination of the relationships between vehicle age, original price, and resale value.

### 3. Feature Engineering and Preprocessing

Relevant features were prepared for model development. Vehicle age was represented using `Car_Age`, and other features were selected or transformed as required by the modeling pipeline.

Preprocessing was applied to ensure that the models could work with the available numerical and categorical data.

### 4. Model Development

Four regression models were trained and evaluated:

1. Linear Regression
2. Ridge Regression
3. Random Forest Regressor
4. Gradient Boosting Regressor

These models were compared to determine which provided the best predictions on unseen data.

### 5. Model Evaluation

The models were evaluated using the following metrics:

- **R² Score:** Measures how much variation in selling prices is explained by the model.
- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted prices.
- **Root Mean Squared Error (RMSE):** Measures prediction error while giving greater weight to larger errors.

For MAE and RMSE, lower values indicate better predictive performance. A higher R² score generally indicates a better fit.

## 📈 Model Performance

Based on the recorded test-set results, Ridge Regression was the best-performing model.

| Model | R² Score | MAE (Lakhs) | RMSE (Lakhs) |
|---|---:|---:|---:|
| Ridge Regression | 0.958 | 0.735 | 1.083 |
| Linear Regression | Update with actual result | Update with actual result | Update with actual result |
| Random Forest Regressor | Update with actual result | Update with actual result | Update with actual result |
| Gradient Boosting Regressor | Update with actual result | Update with actual result | Update with actual result |

*Note: Replace the placeholder values with the actual evaluation results from your notebook. The Ridge Regression results shown here are based on the project's recorded results.*

### 🏆 Best Model: Ridge Regression

Ridge Regression achieved an R² score of 0.958, explaining approximately 95.8% of the variation in selling prices in the test set. Its MAE was 0.735 lakhs, while its RMSE was 1.083 lakhs.

These results suggest that Ridge Regression provides a strong baseline for estimating used-car prices on this dataset. However, performance may vary for vehicles with characteristics that are underrepresented in the training data.

## 💡 Key Insights

The analysis produced several important findings:

- **Original price matters most:** `Present_Price` was the strongest predictor of a car's selling price.
- **Vehicle age is important:** `Car_Age` was the second most influential feature, reflecting the role of depreciation in resale value.
- **Complex models did not perform best:** Ridge Regression outperformed the more complex tree-based models on the recorded test set.
- **Price retention varies across groups:** Although some fuel-type, transmission, and brand groups had higher raw selling prices, their differences should be interpreted alongside their original prices.
- **High-priced vehicles are harder to predict:** The model underpriced the most expensive vehicle by approximately 3 lakhs, highlighting a limitation at the upper end of the price range.
- **More data could improve reliability:** The relatively small test set means that the reported performance should be interpreted with caution.

## 💼 Business Recommendations

Based on the findings, the following recommendations are proposed:

- Buyers and sellers should consider the original vehicle price and age when estimating a fair resale value.
- Dealerships can use the model to support preliminary valuations of ordinary used cars.
- High-priced vehicles should receive additional manual review before a final selling price is set.
- Future versions should include more vehicles and additional features, such as vehicle condition, engine specifications, and location.
- Further validation using repeated cross-validation or a larger test set should be performed to assess how well the model generalizes.

## 🚀 How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook, then install the required libraries.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/Bwalii/CodeAlpha_Car_Price_Prediction.git
   ```

2. Navigate to the project directory:

   ```bash
   cd CodeAlpha_Car_Price_Prediction
   ```

3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open the Car Price Prediction notebook.

5. Ensure the dataset path is correct, then run the notebook cells sequentially.

## 🔮 Future Improvements

Potential improvements include:

- Collecting a larger and more representative used-car dataset.
- Adding relevant vehicle specifications and market information.
- Testing additional regression algorithms and tuning their hyperparameters.
- Comparing performance using repeated cross-validation.
- Building a simple web application using Streamlit or Flask.
- Deploying the selected model to make price estimates accessible to users.

## 👨‍💻 Author

**Bwalii**

- GitHub: [@Bwalii](https://github.com/Bwalii)
- Project Repository: [CodeAlpha_Car_Price_Prediction](https://github.com/Bwalii/CodeAlpha_Car_Price_Prediction)

## 🙏 Acknowledgements

This project was completed as part of the **CodeAlpha Data Science Internship**, providing practical experience in data analysis, exploratory visualization, regression modeling, and machine learning evaluation.

## 📄 License

This project is intended for educational and portfolio purposes. If you plan to distribute or reuse the code or dataset, add an appropriate license and follow the dataset's usage terms.
