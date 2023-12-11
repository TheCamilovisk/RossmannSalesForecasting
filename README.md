# Time Series Forecasting for Retail Sales

## Table of Contents
- [Introduction](#introduction)
- [Packages Used](#packages-used)
- [Installation Instructions](#installation-instructions)
- [Kaggle CLI Installation and Setup](#kaggle-cli-installation-and-setup)
    - [Installation](#installation)
    - [Setup](#setup)
- [Used Data Sources](#used-data-sources)
- [Summary of the Approaches Used](#summary-of-the-approaches-used)
- [Acknowledgements](#acknowledgements)

## Introduction

This repository contains a collection of Jupyter notebooks detailing a study on time series forecasting methodologies applied to the retail sales domain. The study evaluates the performance of different forecasting models on the Kaggle Rossman Store Sales dataset. The aim is to forecast future sales for multiple stores using a variety of approaches, including SARIMAX, Prophet, and XGBoost regressor, with a particular focus on a multi-store perspective using the XGBoost framework.

## Packages Used

A series of Python packages have been utilized in this project, including but not limited to:
- NumPy
- pandas
- matplotlib
- pmdarima
- Prophet
- XGBoost
- scikit-learn
- seaborn

For a complete list of packages and their versions, see `requirements.txt`.

## Installation Instructions

To replicate the findings and run the notebooks in your local environment, please follow these steps:

1. Clone the repository to your local machine.
2. Ensure that Python 3.x is installed.
3. Install the required packages using the command:

```shell
pip install -r requirements.txt
```

## Kaggle CLI Installation and Setup

The Kaggle API is an efficient way to download Kaggle datasets directly into your working environment. Follow the steps below to install the Kaggle CLI and set it up.

### Installation

1. Install the Kaggle API using pip:

```sh
pip install kaggle
```

### Setup
1. After installation, you need to authenticate using an API token from Kaggle:

    - Go to your Kaggle account, scroll to the API section and click on the "Create New API Token" button.
    - This will download a **`kaggle.json`** file containing your API credentials.

2. Place the **`kaggle.json`** file in the appropriate location:

    - On Windows, put it in **`C:\Users\<Windows-username>\.kaggle\kaggle.json`**

    - On Linux and MacOS, put it in **`~/.kaggle/kaggle.json`** and run the following command to ensure the file remains private:

```shell
chmod 600 ~/.kaggle/kaggle.json
```

## Used Data Sources

The dataset used in this project is the [Rossman Store Sales dataset](https://www.kaggle.com/competitions/rossmann-store-sales) available on Kaggle. This dataset includes historical sales data for 1,115 Rossman stores, along with associated promotional and temporal information.

## Summary of the Approaches Used

The following forecasting methodologies were explored:

1. **Exploratory Data Analysis (EDA):** Initial analysis to understand the trends, seasonality, and anomalies in the sales data.
2. **SARIMAX:** Seasonal AutoRegressive Integrated Moving Average with eXogenous factors model for single-store forecasting.
3. **Prophet:** A forecasting tool developed by Facebook for its robustness in capturing seasonality and trends with little need for manual tuning.
4. **XGBoost Regressor:** Gradient boosting framework used for single-store sales forecasting.
5. **XGBoost Multi-Store Model:** An extension of the XGBoost model to forecast sales across multiple stores by incorporating store-specific features.

Each notebook in the repository corresponds to a different stage of the project:
- [`00 - EDA.ipynb`](https://github.com/TheCamilovisk/RossmannSalesForecasting/blob/9b67db7c1485dee551f0799ae85ddac1a70d502d/00%20-%20EDA.ipynb): Exploratory Data Analysis
- [`01 - ARIMA_model.ipynb`](https://github.com/TheCamilovisk/RossmannSalesForecasting/blob/9b67db7c1485dee551f0799ae85ddac1a70d502d/01%20-%20ARIMA_model.ipynb): SARIMAX Model Implementation
- [`02 - Prophet_model.ipynb`](https://github.com/TheCamilovisk/RossmannSalesForecasting/blob/9b67db7c1485dee551f0799ae85ddac1a70d502d/02%20-%20Prophet_model.ipynb): Prophet Model Implementation
- [`03.1 - XGBoost_model.ipynb`](https://github.com/TheCamilovisk/RossmannSalesForecasting/blob/9b67db7c1485dee551f0799ae85ddac1a70d502d/03.1%20-%20XGBoost_model.ipynb): XGBoost Single-Store Model
- [`03.2 - XGBoost_multi_store_model.ipynb`](https://github.com/TheCamilovisk/RossmannSalesForecasting/blob/9b67db7c1485dee551f0799ae85ddac1a70d502d/03.2%20-%20XGBoost_multi_store_model.ipynb): XGBoost Multi-Store Model

## Acknowledgements

This project was made possible thanks to the availability of the Rossman Store Sales dataset on Kaggle and the contributions of the various authors and maintainers of the Python packages used.
