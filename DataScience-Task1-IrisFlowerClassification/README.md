# Iris Flower Classification

**Intern:** Kelvin Apau
**Track:** Data Science
**Internship:** Oasis Infobyte (OIBSIP)
**Task:** Task 1, Iris Flower Classification

## What this project does

There are three kinds of iris flower: Setosa, Versicolor and Virginica. This project teaches a computer to tell which kind a flower is, using four measurements: sepal length, sepal width, petal length and petal width (all in cm).

## Tools used

Python, pandas, scikit-learn, matplotlib, seaborn and Jupyter Notebook.

## Data

The Iris dataset comes built into scikit-learn (`sklearn.datasets.load_iris()`), so there is nothing to download. It has 150 flowers, 50 of each species, and no missing values.

## Steps in the notebook

1. Load the data and put it into a pandas table.
2. Explore the data: shape, data types, missing values and descriptive statistics.
3. Make charts: a pairplot and box plots, coloured by species.
4. Discuss which measurements separate the species best.
5. Split the data 80% for training and 20% for testing.
6. Train four models: Logistic Regression, K-Nearest Neighbours, Decision Tree and Random Forest.
7. Test each model with accuracy, a confusion matrix and a classification report (precision, recall and F1).
8. Check which features the Random Forest relied on most.
9. Pick the best model and explain why.

## Results

| Model | Accuracy on test flowers |
|---|---|
| K-Nearest Neighbours | 100% |
| Logistic Regression | about 97% |
| Decision Tree | about 93% |
| Random Forest | 90% |

**Best model: K-Nearest Neighbours.** It got all 30 test flowers right, and its confusion matrix has no mistakes.

## What I learned from the data

- Petal length and petal width are the most useful measurements. They separate the three species clearly.
- Sepal width is the least useful because all three species overlap on it.
- Setosa was classified correctly by every model. The only mistakes were between Versicolor and Virginica, which look more alike.
- The test set has only 30 flowers, so one extra mistake changes the accuracy by about 3%. The ranking of the models could change with a different split, so this does not prove that Random Forest is a weak model.

## Screenshots

The `screenshots` folder has the main charts from the notebook:

- `01_pairplot.png`
- `02_boxplots.png`
- `03_confusion_logistic_regression.png`
- `04_confusion_knn.png`
- `05_confusion_decision_tree.png`
- `06_confusion_random_forest.png`
- `07_model_accuracy_comparison.png`
- `08_feature_importance.png`

## How to run it

1. Install the tools: `pip install pandas matplotlib seaborn scikit-learn jupyter`
2. Open the notebook: `jupyter notebook Iris_Flower_Classification.ipynb`
3. Choose Run All.
