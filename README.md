Stock Price Prediction — Internship Task 2

Objective

This project focuses on building a machine learning model to **predict the next day's closing stock price using historical market data. The dataset was fetched from Yahoo Finance using the `yfinance` Python library. The goal is to apply regression modeling techniques (Linear Regression and Random Forest) and compare their performance on real stock data.

Dataset

-Source: Yahoo Finance API via `yfinance`
- Stock Ticker: AAPL (Apple Inc.)
- Period: Last 1 Year
- Features Used:
  - `Open`
  - `High`
  - `Low`
  - `Volume`
  - `Close` (Used to compute `Next_Close` target)

Technologies Used

- Python (Jupyter Notebook)
- Pandas, NumPy
- yfinance (for data retrieval)
- Scikit-learn (for model training and evaluation)
- Matplotlib & Seaborn (for visualization)



Workflow Overview

1. Data Collection  
   Retrieved historical stock data using the `yfinance` library.

2. Data Preprocessing  
   - Selected relevant features.
   - Created a new target column: `Next_Close` (the close price of the next trading day).
   - Removed rows with missing values.

3. Exploratory Data Analysis (EDA) 
   - Explored feature correlations.
   - Visualized trends and distribution of features.

4. Model Training
   - Split data into training and test sets.
   - Trained two models:
     - Linear Regression
     - Random Forest Regressor

5. Model Evaluation
   - Used Mean Squared Error (MSE) and R² Score as metrics.
   - Plotted actual vs predicted prices for both models.

6. Insights
   - Compared model performances.
   - Observed that Random Forest performed better due to its non-linear handling capabilities.

Visualizations

- Correlation Heatmap
- Line plots of actual vs predicted stock prices

Results

| Model              | MSE        | R² Score   |
|-------------------|------------|------------|
| Linear Regression | 12.72025535707906| 0.9452913918833665|
| Random Forest     | 18.785236767935476| 0.9192064838428566|

How to Run

1. Clone the repository or open the notebook in Jupyter.
2. Install dependencies:
   ```bash
   pip install yfinance pandas scikit-learn matplotlib seaborn
