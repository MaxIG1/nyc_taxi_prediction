Public_Transport_Forecasting
==============================

Forecasting of Taxi Demand in New York with different Models mit Mean Absolute Error Percentage of only five Percent.

Project Organization
------------
├── README.md          <- The top-level README.

├── data

│   ├── interim        <- Intermediate data that has been transformed.

│   ├── processed      <- The final, canonical data sets for modeling.

│   └── raw            <- The original, immutable data dump.

├── models             <- Trained and serialized models, model predictions, or model summaries

├── notebooks          <- Jupyter notebooks with the analysis and data preparation steps

├── reports            

│   └── figures        <- Generated graphics and figures to be used in reporting

==============================

# Taxi Demand Forecasting in New York City

## Overview
This project explores the foundations of statistical analysis to develop a demand forecasting model for public transport in New York City. The goal is to predict taxi demand in different city clusters to help drivers and companies optimize operations and profitability.


The project uses a dataset spanning from April 1, 2014, to September 30, 2014, with around 4.5 million taxi trips.
Various time series models were explored, including SARIMA, SARIMAX, harmonic regression, TBATS, and Random Forest.

The Random Forest model emerged as the most effective in predicting taxi demand.

## How to Use
Clone this repository to your local machine.
Explore the Jupyter notebooks in the repository in the notebooks folder for detailed analysis and code.

## Final Random Forest Models:

The final model for each cluster can be found here: \models\Tracking\905503404134756615
If you like to open it up with mlflow ui, the name of the experiment is  Random_Forest_Final_with_Models

If you like to load it in Pyhthon here is the code 

import mlflow
logged_model = 'runs:/2b649e7023f442898e7f849174e3eba1/final_random_forest_0'

#### Load model as a PyFuncModel.
loaded_model = mlflow.pyfunc.load_model(logged_model)

#### Predict on a Pandas DataFrame.
import pandas as pd
loaded_model.predict(pd.DataFrame(data))

(taken from the mlflow ui)

## Final Processed Data:

The final processed data can be found here: data/processed/

## Conclusion
This project demonstrates the effectiveness of the Random Forest model in predicting taxi demand in New York City. Further optimization and feature engineering could enhance the model's accuracy. 

For detailed information, refer to the project's Jupyter notebooks.


## Requirements
Please see the requirements.txt in folder notebooks for creating a virtual environment.


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
