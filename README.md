Ice Cream Sales: Exploratory Analysis and Revenue Prediction

This project investigates how weather and calendar conditions relate to ice cream sales revenue. The notebook combines data cleaning, exploratory analysis, statistical summaries, visualization, and supervised regression modeling.

## Analytical workflow

1. **Inspect and prepare the data.** Load the sales CSV, review missing values, standardize numeric precision, validate weekend indicators, and handle missing humidity and temperature values. The notebook also filters temperatures outside its selected 0–40 range and excludes rows without rainfall intensity.
2. **Explore patterns.** Summarize average, median, and range for weather variables; inspect correlations; plot weather and revenue across records; examine weekend frequency; and compare sales under extreme-temperature conditions.
3. **Build a baseline.** Fit a linear regression model and evaluate its predictions with mean absolute error, root mean squared error, and R-squared.
4. **Tune a neural network.** Use cross-validation and Optuna to search over an MLP regressor’s architecture and training parameters, then evaluate the selected model on a held-out test set.
5. **Compare and diagnose models.** Compare machine-learning models with a mean-prediction baseline and linear regression, review grouped revenue summaries, and inspect the best model’s prediction errors.

## Languages and tools

- **Python** for data preparation, statistical analysis, modeling, and visualization.
- **pandas and NumPy** for data handling and numerical operations.
- **Matplotlib and Seaborn** for charts and correlation visualization.
- **scikit-learn** for train/test splitting, linear regression, MLP regression, tree-based models, cross-validation, and evaluation metrics.
- **Optuna** for hyperparameter search.
- **Jupyter Notebook** for the end-to-end analysis.

## Project files

- `Ice_Cream_Analysis.ipynb` — end-to-end analysis and model comparison.
- `ice_cream_sales_data.csv` — source sales data expected by the notebook.

## Run the project

Keep the CSV in the same directory as the notebook. Install Python with `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, and `optuna`, then open `Ice_Cream_Analysis.ipynb` in Jupyter and run its cells from top to bottom.

## Evaluation and interpretation

The notebook reports regression metrics on held-out data and compares models against simple baselines. Correlations and grouped summaries describe associations in this dataset; they do not establish that weather or calendar conditions cause changes in sales. Model performance should be interpreted in light of the data split, feature set, and dataset coverage.
