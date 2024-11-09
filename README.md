# Car Sales Prediction

This project aims to predict the selling price of used vehicles using advanced data science and machine learning techniques. Two regression models, **Random Forest** and **Gradient Boosting**, were implemented and compared to evaluate prediction accuracy. The dataset used, "Vehicle Sales Data," contains comprehensive data on vehicles, from factory specifications to condition and market metrics.

## Contents

- [Project Objective](#project-objective)
- [Dataset](#dataset)
- [Project Steps](#project-steps)
- [Models Used](#models-used)
- [Results](#results)
- [Visualisations](#visualisations)
- [Conclusion](#conclusion)
- [Dependencies](#dependencies)
- [How to Run the Project](#how-to-run-the-project)

## Project Objective

The objective of this project is to develop machine learning models that can accurately predict the selling price of used vehicles, using details such as the year, make, model, condition, and market value (Manheim Market Report).

## Dataset

The **"Vehicle Sales Data"** dataset provides detailed information on vehicle sales, including:
- **Year**, **Make**, **Model**, and **Trim**.
- **Body Type** and **Transmission Type**.
- **Mileage** (Odometer) and **Condition Rating**.
- **Exterior Colour** and **Interior Colour**.
- **Market Value** (MMR) and **Selling Price**.
- **Sale Date** and **Seller Information**.

### Data Pre-processing and Cleaning

Data cleaning steps included:
- Identifying and removing missing values in essential columns (`condition`, `odometer`, and `sellingprice`).
- Normalising numeric variables for consistent scaling.

## Project Steps

1. **Exploratory Data Analysis**: Assessing distributions and correlations among variables, as well as evaluating missing data.
2. **Data Visualisation**: Generating histograms, scatter plots, and bar charts to understand relationships between variables.
3. **Data Cleaning**: Filtering missing values for key variables.
4. **Data Preparation**: Normalising data and splitting it into training and testing sets.
5. **Model Application**: Evaluating **Random Forest** and **Gradient Boosting** regression models.
6. **Results Evaluation**: Comparing performance metrics, **MSE** and **R²**, for both models.

## Models Used

- **Random Forest Regressor**: Implemented with `max_depth=5` and `n_estimators=200`, this model showed strong general predictive capability.
- **Gradient Boosting Regressor**: Implemented with `learning_rate=0.05`, `max_depth=3`, and `n_estimators=250`, this model outperformed the Random Forest in terms of accuracy, with a lower MSE and an R² closer to 1.

## Results

The evaluation metrics for both models are as follows:

| Model             | MSE           | R²      |
|-------------------|---------------|---------|
| Random Forest     | 3,022,753.33  | 0.9682  |
| Gradient Boosting | 2,234,953.32  | 0.9765  |

The **Gradient Boosting** model demonstrated superior performance, with a lower MSE and a higher R², indicating greater accuracy in the predictions.

## Visualisations

### Price and Sales Distribution by Year
- Most sales were recorded between 2012 and 2014, with prices concentrated in the range of 0 to 50,000.
- Vehicles with automatic transmission are predominant across all price categories.

### Feature Importance
- The **MMR** (market value) variable is the most influential, followed by the **Condition** rating of the vehicle.

## Conclusion

Both models achieved high accuracy in predictions, with **Gradient Boosting** showing slightly better performance than **Random Forest**. The **MMR variable** was the most influential, followed by the **Condition** of the vehicle.

## Dependencies

The main libraries used are:

- `pandas`
- `seaborn`
- `matplotlib`
- `statsmodels`
- `scikit-learn`
- `numpy`

## How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/RicardoLlima/Car_Sales_Prediction.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the project in a Jupyter Notebook:
   ```bash
   jupyter notebook Project_CD.ipynb
   ```

4. Follow the steps in the notebook to perform data analysis and visualisation, model fitting, and result evaluation.
