# BRFSS 2021 Mental Health Analysis

This project analyzes data from the **2021 Behavioral Risk Factor Surveillance System (BRFSS)** to explore how various factors such as employment status, e-cigarette use, and flu vaccination are associated with self-reported mental health outcomes. These data come from a survey conducted by the CDC in 2021.

## Project Overview

The primary goal is to examine predictors of poor mental health using linear regression models and data visualization. Key variables include:

- `MENTHLTH`: Number of days in the past 30 when mental health was not good
- `EMPLOY`: Employment status
- `ECIGUSER`: E-cigarette usage
- `FLUSHOT`: Flu vaccination status

## Analysis Highlights

- **Data Cleaning**: Removed missing values and outliers to improve model accuracy
- **Exploratory Visualization**: Boxplots compare poor mental health days across employment categories
- **Linear Regression Models**:
  - Model 1: `MENTHLTH ~ EMPLOY + ECIGUSER + FLUSHOT`
  - Model 2: `MENTHLTH ~ EMPLOY + ECIGUSER`
- **Model Comparison**: AIC values suggest Model 1 (with all predictors) has a slightly better fit

## Key Findings

- Individuals who are **unable to work** and those who **currently use e-cigarettes** report the most poor mental health days.
- Respondents who are **retired**, **self-employed**, or **received the flu shot** report slightly better mental health outcomes.
- Removing the flu shot variable had minimal impact on model performance.
- AIC comparison favored the full model:  
  - Model 1 AIC: 2,761,372  
  - Model 2 AIC: 2,765,961

## How to Run

1. Clone or download this repository
2. Install required R packages (e.g., `tidyverse`, `QuantPsyc`, `ggplot2`)
3. Open the notebook in Jupyter with R kernel support
4. Run the notebook cells in order

## Dataset

This project uses the publicly available **BRFSS 2021 dataset**, which can be downloaded from the CDC [here](https://www.cdc.gov/brfss/annual_data/annual_2021.html).

## Further Analysis Ideas

- Test **interaction effects** (e.g., employment × e-cigarette use)
- Perform subgroup analyses by age, gender, or income
- Convert `MENTHLTH` to a binary variable and explore **logistic regression** approaches

## Contact

For questions or collaboration, feel free to reach out.

