# Sales Prediction

**Intern:** Kelvin Apau
**Track:** Data Science
**Internship:** Oasis Infobyte (OIBSIP)
**Task:** Task 5, Sales Prediction

## What this project does

A company spends money on advertising in three places: TV, Radio and Newspaper. This project predicts how much it will sell from those three budgets, and finds out which channel matters most.

Iris (Task 1) chose between labels. This project predicts a number, which is called regression.

## Tools used

Python, pandas, scikit-learn, matplotlib, seaborn and Jupyter Notebook.

## Data

`Advertising Budget and Sales.csv` has 200 rows: the TV, Radio and Newspaper advertising budgets and the resulting sales. There are no missing values. The file has an extra row counter column, which I dropped.

## Steps in the notebook (`KelvinApau_Task5.ipynb`)

1. Load and clean the data (drop the row counter and give the columns short names).
2. Explore the data: missing values and summary statistics.
3. Make charts: a pairplot, a scatter plot of Sales against each channel, and a correlation heatmap.
4. Split the data into 160 rows for training and 40 for testing.
5. Train two models: Linear Regression and Random Forest Regressor.
6. Measure each model with MAE, RMSE and R2.
7. Draw a residual plot for the best model.
8. Check which channel matters most, using the Random Forest importance and the Linear Regression coefficients.
9. Write a conclusion.

## Results

| Model | MAE | RMSE | R2 |
|---|---|---|---|
| Linear Regression | 1.46 | 1.78 | 0.90 |
| Random Forest | 0.62 | 0.77 | 0.98 |

**Best model: Random Forest.** Its average miss is less than half the size of Linear Regression's.

## What the data showed

- TV has the strongest link with sales (correlation 0.78), then Radio (0.58). Newspaper is weak (0.23).
- The sales against TV chart curves upward instead of following a straight line. This is the likely reason the Random Forest beat Linear Regression, because it can follow a curve.
- The residual plot has no clear pattern, so the errors look random.
- TV matters most overall (Random Forest importance 0.62). Radio gives the most sales for each unit spent (Linear Regression coefficient 0.19 against 0.04 for TV). Newspaper is almost zero in both models.
- The test set has only 40 rows, so one big miss can change the scores and the results could change with a different split.

## Screenshots

The `screenshots` folder has the main charts:

- `01_pairplot.png`
- `02_sales_vs_each_channel.png`
- `03_correlation_heatmap.png`
- `04_residual_plot.png`
- `05_feature_importance.png`

## How to run it

1. Install the tools: `pip install pandas matplotlib seaborn scikit-learn jupyter`
2. Keep the CSV file in the same folder as the notebook.
3. Open the notebook: `jupyter notebook KelvinApau_Task5.ipynb`
4. Choose Run All.
