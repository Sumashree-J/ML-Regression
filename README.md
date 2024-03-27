# 1.-Machine-Learning
Linear Regression and FDR for Trading Data

This notebook offers an in-depth explanation of linear regression and False Discovery Rate (FDR) control. It highlights the significance of relationships between the dependent variable (Estimated Share Price) and other available variables in the dataset, while controlling for false positives to ensure accurate conclusions.

Let’s first understand these methodologies

-	**Linear Regression**: We use linear regression to understand the relationship between a dependent variable (Estimated Share Price) and other available features in the dataset. The goal is to identify the impact of various features on the price of the stock.

- **FDR Control**: We apply FDR to control for false positives in the discovered relationships between different attributes in the dataset, which is done by adjusting the p-values using Benjamini Hochberg(BH) procedure. This helps to avoid making incorrect conclusions based on the data.

Prerequisites

1. Python
2. Required libraries: pandas, numpy, scipy, matplotlib, seaborn, and statsmodels
3. Dataset - The dataset used in the notebook is provided within this repository. 

Steps 

- Setup: Import the necessary libraries and load the dataset.
- Data Exploration: Conduct a thorough analysis of the dataset to understand the key variables and identify any missing data, focusing on preprocessing which is essential to the success of building a reliable model.
  - _"As we all know, the saying 'garbage in, garbage out’. It's crucial to invest time and effort in understanding the data and its preprocessing."_
- Data Visualization: Visualize the relationships between the variables by plotting graphs to help in understanding the behavior of the dataset.
- Linear Regression: Implement the linear regression model, evaluate its performance, and interpret the results.
   - Interpretation: Examine the overall performance of the model, and pay close attention to the significance of various variables.If the model appears to perform well (high R-square) but has few significant variables, this could be an indication of multicollinearity in the data which has to be addressed as it can lead to unreliable estimates.
- FDR Control: Adjust the False Discovery Rate (FDR) using Benjamini Hochberg(BH) procedure and plot the corresponding Q-values to visualise how this adjustment is trimming off the false positives.
  - Interaction Terms: Examine the dataset for any potential interaction terms to further refine the model.
  - Inspect whether the change in the coefficient of determination R2 between the base model & interaction model is significantly different from zero.
  - Why? Because the increase in R² indicates how much variance in response variable (Estimated_Shares_Outstanding) is additionally explained by the interaction term (Capital Expenditure x intangible assets)

Contributions
- Feel free to submit pull requests or start an issue if you find a bug or have any suggestions for improving this notebook.
