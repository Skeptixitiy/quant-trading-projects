# Fair Value Gap (FVG) Regression

## Overview
This notebook, `Reg_FVG.ipynb`, is a financial analysis tool that tests the predictive power of **Fair Value Gaps (FVGs)**. It uses a linear regression model to determine if the presence of bullish or bearish FVGs has a statistically significant relationship with a stock's future price movement. The notebook downloads OHLC data, identifies FVGs, and performs a rigorous statistical analysis.

## Features
* **Data Acquisition:** Downloads historical data using the `yfinance` library.
* **FVG Identification:** Programmatically identifies bullish and bearish FVGs.
* **Regression Analysis:** Performs Ordinary Least Squares (OLS) regression.
* **Statistical Validation:** Includes a null hypothesis test to validate the model's findings.
* **Outputs:** Generates a regression summary table and a correlation histogram.

## How to Run
1.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
2.  Open the `Reg_FVG.ipynb` notebook and run all cells in order.
3.  Modify the stock ticker and date range in the `get_data()` function to analyze other stocks or time periods.

## Project Structure
* `Reg_FVG.ipynb`: The main analysis notebook.
* `requirements.txt`: Python dependencies.

## Methodology
The notebook follows these steps:
1.  Fetches historical stock data using `yfinance`.
2.  Identifies Fair Value Gaps.
3.  Calculates the `1 Period % Change` as the target variable.
4.  Fits an OLS regression model.
5.  Performs null hypothesis testing by shuffling the target variable to assess significance.
6.  Visualizes the results with a correlation histogram.

## Results
The analysis aims to determine if there is a statistically significant relationship between FVGs and next-period returns. The notebook provides a full regression summary table for detailed analysis.

## Requirements
* Python 3.7+
* `yfinance`
* `pandas`
* `numpy`
* `statsmodels`
* `matplotlib`