# Iris Flower Classification

**Intern:** Kelvin Apau
**Track:** Data Science
**Internship:** Oasis Infobyte (OIBSIP)
**Task:** Task 1, Iris Flower Classification

## What this project does

There are three kinds of iris flower: Setosa, Versicolor and Virginica. This project trains models to tell which kind a flower is, using four measurements: sepal length, sepal width, petal length and petal width (all in cm).

## Tools used

Python, pandas, scikit-learn, matplotlib, seaborn and Jupyter Notebook.

## Data

The Iris dataset comes built into scikit-learn (`load_iris()`). It has 150 flowers, 50 of each species, and no missing values.

## Steps in the notebook (`KelvinApau_Task1.ipynb`)

1. Load the data into a pandas table.
2. Explore the data: shape, missing values, data types, descriptive statistics and species counts.
3. Make charts: a pairplot and box plots, split by species.
4. Split the data into 120 flowers for training and 30 for testing.
5. Train four models: K-Nearest Neighbours, Logistic Regression, Decision Tree and Random Forest.
6. Test each model with accuracy and a confusion matrix. KNN also has a classification report.
7. Compare the models and check which features the Random Forest relied on most.
8. Write a conclusion.

## Results

| Model | Accuracy on the 30 test flowers |
|---|---|
| K-Nearest Neighbours | 100% |
| Logistic Regression | about 97% |
| Decision Tree | about 93% |
| Random Forest | 90% |

**Best model: K-Nearest Neighbours.** It got all 30 test flowers right.

## What the data showed

- Petal length and petal width are the most useful measurements. The pairplot, the box plots and the Random Forest feature importance all agree.
- Sepal width is the least useful measurement.
- Setosa was never confused with the other two species. Every mistake made by the other three models was between Versicolor and Virginica, whose measurements are very similar.
- The test set has only 30 flowers, so one mistake changes the accuracy by about 3%. The ranking of the models could change with a different split.

## Screenshots

The `screenshots` folder has the main charts:

- `01_pairplot.png`
- `02_boxplots.png`
- `03_feature_importance.png`

## How to run it

1. Install the tools: `pip install pandas matplotlib seaborn scikit-learn jupyter`
2. Open the notebook: `jupyter notebook KelvinApau_Task1.ipynb`
3. Choose Run All.
