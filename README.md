# DATA_MINING_PROJECT_01
 This GitHub repository contains the code and documentation for the Data Mining course project focusing on Exploratory Data Analysis (EDA) and Regression Analysis. The project aims to provide a comprehensive analysis of the dataset assigned to the team, along with building and evaluating regression models using an end-to-end Machine Learning pipeline.
 
![Final_Chart](https://github.com/Jatansahu/GOLDDIGGER_GROUP12_PROJECT_01/assets/115174048/6e2fb8f2-638e-4594-82e0-a3230f0ef1f5)


## Contents

1. **data/:** This directory holds the dataset assigned to our team. The dataset is named `dataset.csv` 

2. **notebooks/:** This directory contains Jupyter notebooks that cover various aspects of the project:
   - `EDA.ipynb`: Exploratory Data Analysis notebook with summary statistics, visualization, and insights about the dataset.
   - `Regression_Analysis.ipynb`: Regression analysis notebook showcasing the identification of regression problems, building Machine Learning pipelines, and evaluating regression models.

3. **scripts/:** This directory contains Python scripts used for the project:
   - `preprocessing.py`: Script for dataset preprocessing and transformation.
   - `regression_models.py`: Script containing the code for building regression models, hyperparameter tuning, and evaluation.

4. **reports/:** This directory contains project reports in PDF format:
   - `EDA_Report.pdf`: Report summarizing the Exploratory Data Analysis.


## About Dataset 

https://www.kaggle.com/datasets/spittman1248/cdc-data-nutrition-physical-activity-obesity


### CDC Data: Nutrition, Physical Activity, & Obesity

This dataset includes data on adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. This data is used for DNPAO's Data, Trends, and Maps database, which provides national and state specific data on obesity, nutrition, physical activity, and breastfeeding. I was particularly curious on whether socioeconomic status has an impact on obesity. In my analysis, I compare the obesity rate in each state, and then perform a linear regression on the obesity rate for each educational status and the income bracket.

**Exploratory Data Analysis**

- The EDA provided valuable insights into our dataset, enabling us to proceed with confidence to the prediction phase.
- We observed patterns in the distribution of Data_Value, Data_Value_Footnote, LocationID, and StratificationCategory1, which will inform our modeling efforts.
- Obesity rates were analyzed across states, revealing varying rates and highlighting states with the highest obesity prevalence.
- Different classes (Obesity/Weight Status, Fruits and Vegetables, Physical Activity) showed variations in average obesity rates, suggesting the influence of topic categories.
- We noted consistent obesity rates across various subgroups.
- High correlations among certain variables guided our decision to drop redundant features for model simplification.

These findings collectively equip us for the next phase of our project, where we will build predictive models based on these insights.
