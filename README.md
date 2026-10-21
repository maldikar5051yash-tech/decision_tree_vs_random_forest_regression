# Decision Tree vs Random Forest - Regression

## Vehicle Fuel Efficiency Prediction

This project is an end-to-end machine learning regression project that compares the performance of a **Decision Tree Regressor** and a **Random Forest Regressor**.

The objective is to predict the fuel efficiency of a vehicle in **Miles Per Gallon (MPG)** using different vehicle characteristics and compare the performance of a single Decision Tree with an ensemble-based Random Forest.

## Dataset

The project uses the **Auto MPG Dataset** from the UCI Machine Learning Repository.

Dataset Source:  
https://archive.ics.uci.edu/dataset/9/auto+mpg

The dataset contains vehicle-related attributes such as:

- Cylinders
- Displacement
- Horsepower
- Weight
- Acceleration
- Model Year
- Origin

The target variable is:

**MPG (Miles Per Gallon)**

## Project Workflow

The project follows an end-to-end machine learning workflow:

1. Dataset loading
2. Data cleaning
3. Missing value handling
4. Duplicate checking
5. Exploratory Data Analysis (EDA)
6. Train-test split
7. Feature selection
8. Decision Tree Regressor training
9. Random Forest Regressor training
10. Model evaluation
11. Performance comparison
12. Data visualization
13. Feature importance analysis
14. Model saving using Pickle
15. Flask web application for MPG prediction

## Exploratory Data Analysis

EDA is performed to understand the dataset and relationships between vehicle characteristics and fuel efficiency.

The analysis includes:

- MPG distribution
- Correlation heatmap
- Weight vs MPG
- Horsepower vs MPG
- Feature relationship analysis

## Feature Selection

`SelectKBest` with `f_regression` is used to identify the most useful input features for predicting MPG.

The same selected features are used by both machine learning algorithms to ensure a fair comparison.

## Machine Learning Models

### Decision Tree Regressor

The Decision Tree Regressor predicts a continuous MPG value by splitting the dataset into regions based on vehicle characteristics.

### Random Forest Regressor

The Random Forest Regressor combines predictions from multiple Decision Trees.

Using multiple trees can reduce overfitting and often provides better generalization than relying on a single Decision Tree.

## Evaluation Metrics

Both models are evaluated using standard regression metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

For MAE, MSE, and RMSE, lower values indicate better performance.

For R² Score, a higher value generally indicates that the model explains more of the variation in the target variable.

## Model Comparison

Decision Tree and Random Forest are trained and evaluated using the same train-test split.

Their performance is compared using tables and visualizations to determine which model performs better on the Auto MPG dataset.

## Visualizations

The project contains visualizations including:

- MPG distribution
- Correlation heatmap
- Weight vs MPG
- Horsepower vs MPG
- Feature selection scores
- Actual vs Predicted MPG
- MAE comparison
- RMSE comparison
- R² Score comparison
- Random Forest feature importance

## Web Application

A Flask web application is included to demonstrate predictions from both trained regression models.

The user enters vehicle characteristics and receives:

**Decision Tree Prediction**
- Predicted MPG

**Random Forest Prediction**
- Predicted MPG

This makes it easy to compare predictions from both algorithms for the same vehicle.

## Project Structure

```text
Decision-Tree-vs-Random-Forest-Regression/
│
├── Regression_Project.ipynb
├── app.py
├── decision_tree_regressor.pkl
├── random_forest_regressor.pkl
├── regression_selector.pkl
├── regression_feature_names.pkl
├── regression_selected_features.pkl
├── requirements.txt
│
├── templates/
│   └── index.html
│
└── README.md
```

## Installation

Install the required libraries using:

```bash
pip install -r requirements.txt
```

## Run the Application

Start the Flask server:

```bash
python app.py
```

After starting the application, open:

```text
http://127.0.0.1:5000
```

in a web browser.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Flask
- HTML
- CSS
- Pickle
- Google Colab

## Conclusion

This project demonstrates the performance difference between a single Decision Tree and a Random Forest for a regression problem.

Both algorithms use the same dataset, selected features, and train-test split, making the comparison fair.

The project also demonstrates the complete machine learning workflow from data preprocessing and exploratory analysis to model evaluation and deployment through a simple Flask application.
