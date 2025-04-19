# Regression Analysis Final Project - Craig Wilcox
**Author:** Brittany Dowdle   
**Date:** April 18, 2025

[Clickable Link to Notebook](https://github.com/S572396/ml-07-sruiz/blob/main/sruiz-medreg.ipynb)

****

## Clarity & Organization

The notebook has a clear structure with numbered sections. It follows the standard project workflow that we have practiced throughout this course. Each section includes a markdown, code, output, and reflection. This organization makes it easy to follow the author's thought process. Reproducibility of this project should be done easily.   
A couple of things to consider would be adding more detailed markdown headers or subheadings within each section. This would allow users to have more context and inexperienced readers to understand your steps. Some of the code outputs and reflections could use more separation. Like for the scatter matrix array, the ouput could be suppressed to improve readability.

## Feature Selection & Justification

The project tests three different features (age, BMI, and smoker status) individually to get a baseline of their predictive power.
They transformed the feature 'smoker' from categorical to numerical and ensuring spacing/capitalization was appropriately handled. And the use of a scatter matrix helped to visualize the relationship of numerical variables they were considering was a great idea. The justification for feature selection was included in reflection 3 and mention how the normal distributions of the features should provide high accuracy in results.   
A couple of things to consider would be trying multivariate approaches instead of individual. The dataset only has 7 total variables, so the model is already limited in it's ability to capture interactions. This could vastly improve the evaluation metrics. And maybe explore some statistical measures like correlation metrics, or something similar. This would provide a deeper analytical justification and could strengthen the predictive power of the features selected.

## Model Performance & Comparisons

The author uses an appropriate model (linear regression) for a continuous variable (charges). And the metrics chosen (R², RMSE, MAE) for evaluating model performance provided plenty of insights. The outputs are clearly formatted and make the results easy to compare across multiple models. There's a solid attempt to improve models by going from simple linear regression to using pipelines with different preprocessing steps. They correctly idenitifed smoking status as the most predictive feature.   
A couple of things to consider would be interpreting why smoker status was a much better predictor than to age or BMI. Maybe visualizing model predictions vs actuals would help users understand. And to try applying both pipelines with more than one feature. Using only one feature caused them to produce identical results. 

## Reflection Quality

Every section included a reflection. They were used to interpret results and decide how to proceed from the analysis. I liked that they honestly commented about the unexpected poor performance of chosen features. Section 6 reflection acknowledged limitations and noted how predetermined expectations can negatively impact a project. Their suggestion of letting the data speak for itself is something we can all use going forward!   
A couple of things to consider would be adding some depth to each of section 1-5 reflections. Some more details could help others who aren't familiar with the project understand the summarized results better. And partiularly reiewing section 5 reflection. It stated that pipeline 1 performed the best even though both pipelines had identical results.