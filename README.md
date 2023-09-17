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

#---------------------------------------------------------------------------------------------------------------

# CDC Data: Nutrition, Physical Activity, & Obesity

This dataset includes data on adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. This data is used for DNPAO's Data, Trends, and Maps database, which provides national and state specific data on obesity, nutrition, physical activity, and breastfeeding. In this analysis, we have performed exploratory data analysis on the dataset and thereby partitioned the dataset in various categories and analyzed and predicted obesity rates based on those factors. We have employed various machine learning techniques along with hyperparameter tuning to improve our test results. We aim to achieve a good prediction through our model.


# Table of Contents

## 1. [ EDA(whole dataset) ](#1-edawhole-dataset)
## 2. [ EDA(category wise) ](#2-edacategory-wise)
## 3. [ Data Preparation and Feature Selection ](#3-data-preparation-and-feature-selection)
## 4. [ Machine Learning Pipeline ](#4-machine-learning-pipeline)


# Introduction

In this GitHub repository, you'll find code and documentation for our Data Mining course project. Our project focuses on exploring and analyzing data (EDA) and creating regression models. We aim to provide a deep understanding of the dataset we've been given and build and test regression models using a step-by-step approach. This project allows us to gain practical experience in working with data, cleaning it, and making it ready for analysis. We also get to create and improve regression models as part of our learning process.

# Team Members

### - Rahul Upadhyay - 202218003
### - Muskan Khare - 202218037
### - Jatan Sahu - 202218061
### - Bhoomi Prajapati - 202218063
### - Bhargav Vidja - 202101201

# Project Pipeline

## 1. EDA(whole dataset)
 - The EDA provided valuable insights into our dataset, enabling us to proceed with confidence to the prediction phase.
 - We observed patterns in the distribution of Data_Value, Data_Value_Footnote, LocationID, and StratificationCategory1, which will inform our modeling efforts.
 - Obesity rates were analyzed across states, revealing varying rates and highlighting states with the highest obesity prevalence.
 - Different classes (Obesity/Weight Status, Fruits and Vegetables, Physical Activity) showed variations in average obesity rates, suggesting the influence of topic categories.
 - We noted consistent obesity rates across various subgroups.
 - High correlations among certain variables guided our decision to drop redundant features for model simplification.

These findings collectively equip us for the next phase of our project, where we will build predictive models based on these insights.

## 2. EDA(category wise)

The dataset was divided based on stratification categories, and missing values were handled by removing irrelevant features. 
### Outcomes:
 - Histograms and boxplots helped analyze data distribution and range.
 - Bar plots revealed insights such as an inverse relationship between income and obesity rates, variation in rates among racial/ethnic groups, lower obesity rates with higher education levels, and lower rates for females compared to males.
 - Scatter plots showed that the non-Hispanic white demographic group had the most samples with large sample sizes, females had lower obesity rates than males, and lower data values correlated with higher income and education levels.

Additionally, question and class counts were examined, and correlation analysis with label encoding was performed. Notably, 'low_confidence_limit' and 'high_confidence_limit' were highly correlated and should be excluded from modeling to prevent overfitting. These findings will guide feature selection in subsequent machine learning tasks.
[Several plots in our EDA_category.ipynb file utilize the Plotly library, which creates interactive visualizations not viewable directly in the GitHub file. To access and interact with these visualizations, you can simply click the "Open in Colab" link provided at the beginning of the document.]


## 3. Data Preparation and Feature Selection
## 4. Machine Learning Pipeline

