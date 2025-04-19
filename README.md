# Dowdle's Module 6 Final Introduction
This project demonstrates a complete workflow for building a regression model to predict a car’s fuel efficiency (`mpg`) based on its physical and over-time characteristics. The notebook guides the user through building a series of increasingly sophisticated models. It starts with a simple two‐feature linear regression and moves to pipelines incorporating imputation, scaling, and polynomial feature expansion. The goal is to investigate how well we can estimate miles per gallon. The goal is both to achieve high predictive accuracy and to demonstrate a reproducible, pipeline‐based workflow in scikit‑learn. [Clickable link to notebook](https://github.com/Bdowdle4/ml-regression-dowdle/blob/main/regression-dowdle.ipynb)

****

## Dataset
[Clickable link to my data file](https://github.com/Bdowdle4/ml-regression-dowdle/blob/main/data/auto-mpg.csv)

The dataset used in this project is the UCI Auto MPG Dataset. This dataset contains 7 features and 1 ID extracted from the original dataset, and it is used to predict fuel consumption in miles per gallon. Key aspects of the dataset include:
>Features: `cylinders`, `displacement`, `horsepower`, `weight`, `acceleration`, `model_year`, and `origin`. Plus a `car_name` identifier.
>
>Target Variable: `mpg` 
>
>Data Source: The dataset is publicly available from the UCI Machine Learning Repository and is widely used for regression tasks. [Original Dataset](https://archive.ics.uci.edu/dataset/9/auto+mpg)

****

## Methodology
The notebook follows a structured approach:

>Data Exploration: Visualizing feature distributions and relationships. Identifying potential outliers and anomalies. Generating summary statistics to understand underlying data patterns.
>
>Data Preprocessing: Cleaning and preparing the dataset. Handling missing values, feature engineering, and scaling/logging numerical features. Splitting the data into training and testing sets for model validation.
>
>Model Building: Testing multiple machine learning algorithms (linear regression 2-feature, linear regression 3-feature, pipeline with imputation, scaling and LR, and pipeline with degree‑3 polynomial expansion before scaling and regression) to determine the best performing model.
>
>Model Evaluation: Assessing models using metrics such as R², MAE, and RMSE. Use both hold‑out and cross‑validation metrics to interpret generalization. Comparing model performances to select the most robust approach.

****

## Feature Importance Analysis:
Determining the significance of each feature in the prediction process. Drawing insights about the predictors that most effect the classification outcome.

> Examining coefficients and error reductions across models. Polynomial pipeline interaction and squared terms validate the insights.
>
> `weight` proves to be the most influential predictor. `model_year` reflects improvements over time in regulatory or technological advancements.
>
> The impact of weight and fuel efficiency changes non-linearly with age. Newer, heavier cars have less fuel effiency penalties than older, heavier cars. This project confirms that vehicle mass is critical to understanding fuel economy.

****

## Findings
The key takeaways from the project include:

>Data Insights: The exploration phase revealed interesting patterns within the dataset. Visualizations highlighted the distribution of the features and potential imbalances, providing insights that guided the preprocessing steps.
>
>Model Performance: Among the evaluated models the best performing regression achieved 90% variance explanation. This indicates that the chosen features and preprocessing techniques were effective. Detailed metrics provided clarity on each model’s strengths and limitations.
>
>Feature Relevance: Analysis of feature importance underscored that the chosen features had a significant impact on the model's predictions. Determining a vehicles fuel efficiency is attainable using just 3 of the 8 available variables.

****

## Summary
Overall, the regression approach was a success. Even the simple models captured the majority of the relationship between vehicle attributes and fuel economy. And the carefully structured pipelines allowed interpretable experimentation. Targeted handling of missing and skewed data and cross‑validation made the improved models more robust and generalizable. The project identified the value of starting with a baseline before layering in non‑linear and preprocessing steps.

As a requirement of this project, I also completed a [peer review](https://github.com/Bdowdle4/ml-regression-dowdle/blob/main/peer_review.md) of another classmates project. I chose a classmate that did a different dataset than myself.

****

## Future Work
Given more time, this analysis could be extended by incorporating additional predictors. Some I would try are `horsepower` or `displacement`. Another option would be to one‑hot encode `origin` or `make` into both linear and non‑linear models. Finally, a more complex model approach like regularized regressions (Ridge/Lasso), ensemble methods (Random Forest, Gradient Boosting), or systematic hyperparameter tuning.

****

## Instructions On How To Set Up Your Virtual Environment and Run Your Notebook Locally
### Virtual Enviornment Set Up (Windows Users)
**Task 1. Create .venv** Run the following command from the project root directory. Use PowerShell (not cmd):

```shell
py -m venv .venv
```

**Accept VS Code Suggestions** If VS Code asks: We noticed a new environment has been created. 
Do you want to select it for the workspace folder? Click Yes. 

**Task 2. Activate** Run the following command from the project root directory. Use Powershell:

```powershell
.venv\Scripts\activate
```

### Run Jupyter Notebook Locally
**Before Starting** Ensure the .venv is activated. If it is already active, you don't need to reactivate it.

**Install the Jupyter Extension for VS Code** Open the Extensions view in VS Code by pressing Ctrl+Shift+X (Windows). Search for "Jupyter" and install the official extension.

**Open the Notebook in VS Code** Open the notebook in VS Code. The file will have a .ipynb extension.

**Task 1. Select Notebook Kernel** Open the project notebook in VS Code. The file will have a .ipynb extension.
- If prompted, select a Python interpreter that corresponds to your .venv.  
- If not prompted, click the kernel selector in the top-right corner of the notebook editor and choose the interpreter associated with your Python Environment / .venv.
- Or:
   - From VS Code Menu, select View / Command Palette... (CTRL SHIFT P)
   - Type: Python: Select Interpreter 
   - Choose your .venv from the list

**Task 2. Start and Run a Jupyter Notebook** Open the project notebook in VS Code. The file will have a .ipynb extension.

1. Execute cells:  
   - Click on a cell and press Shift+Enter to execute it and move to the next cell.  
   - Alternatively, use Ctrl+Enter to execute the current cell without moving.

2. Save your notebook periodically to avoid losing progress. Or make sure the File / Autosave option is on.

**ALWAYS: Fully Execute Notebooks before add-commit-push** Keep your notebooks organized and execute them fully before running git add-commit-push to GitHub.

****

## Repository Checklist

Verify your repository contains:

- [x] Useful .gitignore (that keeps .venv out of GitHub)
- [x] Professional Jupyter Notebook with with proper name, numbered sections and reflections 
- [x] Useful README.md
- [x] Useful requirements.txt
- [x] Dataset, stored in a data folder
- [x] Peer Review (peer_review.md)
