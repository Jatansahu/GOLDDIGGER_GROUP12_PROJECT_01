# CDC Data: Nutrition, Physical Activity, & Obesity

# Introduction

In this GitHub repository, you'll find code and documentation for our Data Mining course project. Our project focuses on exploring and analyzing data (EDA) and creating regression models. We aim to provide a deep understanding of the dataset we've been given and build and test regression models using a step-by-step approach. This project allows us to gain practical experience in working with data, cleaning it, and making it ready for analysis. We also get to create and improve regression models as part of our learning process.

# TEAM-12 GOLD DIGGER

### - Rahul Upadhyay - 202218003
### - Muskan Khare - 202218037
### - Jatan Sahu - 202218061
### - Bhoomi Prajapati - 202218063
### - Bhargav Vidja - 202101201

# Project Pipeline
![Final_Chart](https://github.com/Jatansahu/GOLDDIGGER_GROUP12_PROJECT_01/assets/115174048/6e2fb8f2-638e-4594-82e0-a3230f0ef1f5)

# Table of Contents

## [ 1. Dataset description ](#1-dataset-description)
## [ 2. Data Understanding - EDA_dataset.ipynb ](#2-data-understanding---eda_datasetipynb)
## [ 3. Data Visualisation - EDA_category.ipynb ](#3-data-visualisation---eda_categoryipynb)
## [ 4. Data Preparation and Feature Selection ](#4-data-preparation-and-feature-selection)
## [ 5. Machine Learning Pipeline ](#5-machine-learning-pipeline)

## 1. Dataset description

This dataset includes data on adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. This data is used for DNPAO's Data, Trends, and Maps database, which provides national and state specific data on obesity, nutrition, physical activity, and breastfeeding. In this analysis, we have performed exploratory data analysis on the dataset and thereby partitioned the dataset in various categories and analyzed and predicted obesity rates based on those factors. We have employed various machine learning techniques along with hyperparameter tuning to improve our test results. We aim to achieve a good prediction through our model.

Our dataset contains the following atrributes :- 

`YearStart` - Year start

`YearEnd` - Year End (for single-year indicator, year end=year start)

`LocationAbbr` - Location abbreviation

`LocationDesc` - Location description

`Datasource` - Name or abbreviation of Data Source

`Class` - Class Description

`Topic` - Topic Description

`Question` - Question Description

`Data_Value_Unit` - Description of unit e.g. %, etc

`Data_Value_Type` - Description of type of data e.g. Value, Percentage, Number

`Data_Value` - Data value (percentage, text)

`Data_Value_Alt` - Numeric representation of data value

`Data_Value_Footnote_Symbol` - Symbol that would be used to flag footnotes

`Data_Value_Footnote` - Footnote text

`Low_Confidence_Limit` - Low 95% Confidence Interval value

`High_Confidence_Limit` - High 95% Confidence Interval value

`Sample_Size` - Sample Size

`Total` - Total/Overall breakout category

`Age(years)` - Age (years) breakout category

`Education` - Education breakout category

`Gender` - Gender breakout category

`Income` - Income breakout category

`Race/Ethnicity` - Race/Ethnicity breakout category

`GeoLocation` - Latitude & Longitude to be provided for formatting GeoLocation or Geocode in the format (latitude, longitude)

`ClassID` - Lookup identifier value for Class

`TopicID` - Lookup identifier value for Topic

`QuestionID` - Lookup identifier value for Question

`DataValueTypeID` - Lookup identifier value for Data_Value_type

`LocationID` - Lookup identifier value for Location

`StratificationCategory1` - Lookup Identification value, such as Age Group, Gender

`Stratification1` - Data stratified by this value, such as Male, Female, Total

`StratificationCategoryId1` - Lookup identifier value for Stratification1

`StratificationID1` - Lookup identifier value for StratificationCategory1

**Note** : This dataset description was sourced from-
https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7

## 2. Data Understanding - EDA_dataset.ipynb
 - The EDA provided valuable insights into our dataset, enabling us to proceed with confidence to the prediction phase.
 - We observed patterns in the distribution of Data_Value, Data_Value_Footnote, LocationID, and StratificationCategory1, which will inform our modeling efforts.
 - Obesity rates were analyzed across states, revealing varying rates and highlighting states with the highest obesity prevalence.
 - Different classes (Obesity/Weight Status, Fruits and Vegetables, Physical Activity) showed variations in average obesity rates, suggesting the influence of topic categories.
 - We noted consistent obesity rates across various subgroups.
 - High correlations among certain variables guided our decision to drop redundant features for model simplification.

These findings collectively equip us for the next phase of our project, where we will build predictive models based on these insights.

## 3. Data Visualisation - EDA_category.ipynb

The dataset was divided based on stratification categories, and missing values were handled by removing irrelevant features. 
### Outcomes:
 - Histograms and boxplots helped analyze data distribution and range.
 - Bar plots revealed insights such as an inverse relationship between income and obesity rates, variation in rates among racial/ethnic groups, lower obesity rates with higher education levels, and lower rates for females compared to males.
 - Scatter plots showed that the non-Hispanic white demographic group had the most samples with large sample sizes, females had lower obesity rates than males, and lower data values correlated with higher income and education levels.

Additionally, question and class counts were examined, and correlation analysis with label encoding was performed. Notably, 'low_confidence_limit' and 'high_confidence_limit' were highly correlated and should be excluded from modeling to prevent overfitting. These findings will guide feature selection in subsequent machine learning tasks.
[Several plots in our EDA_category.ipynb file utilize the Plotly library, which creates interactive visualizations not viewable directly in the GitHub file. To access and interact with these visualizations, you can simply click the "Open in Colab" link provided at the beginning of the document.]


## 4. Data Preparation and Feature Selection

In this module, we engage in data processing tasks, which encompass the selection of essential columns and the handling of missing values. Drawing from the insights gained through both of the conducted Exploratory Data Analysis (EDAs), we proceed to partition our datasets into six subdatasets, each categorized based on stratification criteria. Subsequently, we carry out additional preprocessing on each of these subdatasets, ultimately converting them into CSV files. These CSV files serve as the foundational data for our subsequent model prediction tasks.

## 5. Machine Learning Pipeline

The machine learning pipeline comprises key stages. It begins with data splitting and standardization, where we divide the dataset, standardize it, and move to model selection. In this stage, we consider models like linear regression, polynomial regression, Ridge regression, k-Nearest Neighbors (kNN), and Random Forest. 

Models used for Evaluation

**Model 1:** Linear Regression Hyperparameters: None (No specific hyperparameters tuned)

**Model 2:** Polynomial Regression  Hyperparameters: degree(2, 3)

**Model 3:** Ridge Regression Hyperparameters: Alpha (Regularization strength): [0.01, 0.1, 1.0]

**Model 4:** K-Nearest Neighbors Regression Hyperparameters: Number of Neighbors (n_neighbors): [3, 5, 7]

**Model 5:** Random Forest Regression Hyperparameters: Number of Estimators (n_estimators): [100, 200, 300] Maximum Depth of Trees (max_depth): [5, 10, 20, 30] Minimum Samples for Split (min_samples_split): [2, 5, 10]

Subsequently, hyperparameter tuning and model evaluation optimizes model hyperparameters using GridSearchCV, with evaluation on the validation set. Selecting the best model and evaluating on the test set follows, where the top-performing model on the validation set is assessed on an independent test dataset. Finally, model comparison showcases results, highlighting the best hyperparameters and critical metrics like RMSE, MAE, and R2 Score. These stages encompass data preparation, model selection, and thorough evaluation.


