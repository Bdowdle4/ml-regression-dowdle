# Dowdle's Module 6 Final Introduction
This project explores the use of regression techniques to predict a car’s fuel efficiency (`mpg`) based on its physical and temporal characteristics. By building a series of increasingly sophisticated models—from a simple two‐feature linear regression to pipelines incorporating imputation, scaling, and polynomial feature expansion—we investigate how well we can estimate miles per gallon given readily available vehicle attributes. The goal is both to achieve high predictive accuracy and to demonstrate a reproducible, pipeline‐based workflow in scikit‑learn.   
[Clickable link to notebook](https://github.com/Bdowdle4/ml-regression-dowdle/blob/main/regression-dowdle.ipynb)

****

## Dataset
[Clickable link to my data file](https://github.com/Bdowdle4/ml-regression-dowdle/blob/main/data/auto-mpg.csv)

The dataset used in this project is the UCI Auto MPG Dataset. This dataset contains 7 features and 1 ID extracted from the original dataset, and it is used to predict fuel consumption in miles per gallon. Key aspects of the dataset include:
>Features: `cylinders`, `displacement`, `horsepower`, `weight`, `acceleration`, `model_year`, and `origin`. Plus a `car_name` identifier.
>
>Target Variable: `mpg` 
>
>Data Source: The dataset is publicly available from the UCI Machine Learning Repository and is widely used for binary classification tasks. [Original Dataset](https://archive.ics.uci.edu/dataset/9/auto+mpg)

****

## Methodology
The notebook follows a structured approach:

>Data Exploration: Visualizing feature distributions and relationships. Identifying potential outliers and anomalies. Generating summary statistics to understand underlying data patterns.
>
>Data Preprocessing: Cleaning and preparing the dataset. Handling missing values, encoding variables, and scaling numerical features. Splitting the data into training and testing sets for model validation.
>
>Model Building: Testing multiple machine learning algorithms (linear regression, pipeline with imputation, scaling and LR, and pipeline with degree‑3 polynomial expansion before scaling and regression) to determine the best performing model. Applying hyperparameter tuning to optimize model performance.
>
>Model Evaluation: Assessing models using metrics such as R², MAE, and RMSE—using both hold‑out and cross‑validation metrics. Comparing model performances to select the most robust approach.

****
## Feature Importance Analysis:
Determining the significance of each feature in the prediction process. Drawing insights about the predictors that most effect the classification outcome.

>By examining coefficients and error reductions across models, vehicle weight emerges as the single most influential predictor—its heavier values consistently drive lower mpg. Model year is the next most important feature, reflecting technological and regulatory advancements over time. In the polynomial pipeline, interaction and squared terms of weight and year further underscore how the impact of weight on fuel efficiency changes non‑linearly with age: newer, heavier cars suffer less mpg penalty than older counterparts. This analysis confirms that both magnitude and evolution of vehicle mass are critical for understanding fuel economy.


****

## Findings
The key takeaways from the project include:

>A baseline linear regression using only `weight`, `model_year`, and `origin` explains 84% of the variance in `mpg` (R² ≈ 0.84, RMSE ≈ 3.3 mpg). Extending this model with a pipeline that imputes missing values, adds degree‑3 polynomial features, and standardizes inputs boosts performance to R² ≈ 0.90 and reduces test‑set RMSE to ~2.7 mpg. Feature scaling proved essential after polynomial expansion, and the results highlight the dominant linear and non‑linear effects of vehicle mass and model year on fuel efficiency.


****

## Summary
Overall, simple, interpretable models captured the majority of the relationship between vehicle attributes and fuel economy, while carefully structured pipelines allowed easy experimentation with more complex feature transformations. Thorough exploratory data analysis, targeted handling of missing and skewed data, and cross‑validation ensured that our improvements were robust and generalizable. The project underscores the value of starting with a parsimonious baseline before layering in non‑linear and preprocessing steps.

As a requirement of this project, I also completed a [peer review](https://github.com/Bdowdle4/ml-regression-dowdle/blob/main/peer_review.md) of another classmates project. I chose a classmate that did a different dataset than myself.

****

## Future Work
Given more time, this analysis could be extended by incorporating additional predictors—such as `horsepower`, `displacement`, and one‑hot encoded `origin` or `make`—into both linear and non‑linear models. Regularized regressions (Ridge/Lasso), ensemble methods (Random Forest, Gradient Boosting), and systematic hyperparameter tuning would likely yield further gains. Finally, residual diagnostics and error analysis could guide targeted feature engineering or the inclusion of domain‑specific interactions (e.g., origin × weight) to capture remaining patterns.

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

- [ ] Useful .gitignore (that keeps .venv out of GitHub)
- [ ] Professional Jupyter Notebook with with proper name, numbered sections and reflections 
- [ ] Useful README.md
- [ ] Useful requirements.txt
- [ ] Dataset, stored in a data folder
- [ ] Peer Review (peer_review.md)
