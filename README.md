# HeartInsights Data Analysis

Project collaborators: Yasmin-9, qudsia99

## Overview
This repository contains the code and data used for analyzing the Framingham Longitudinal Study data to gain insights into cardiovascular health trends. The analysis focuses on exploring the relationship between smoking status, age, and prevalent coronary heart disease (CHD).

## Dependencies
* pandas
* numpy
* matplotlib.pyplot
* scipy.stats
* pathlib

## Data Cleaning
The original dataset frmgham2.csv was cleaned and filtered to focus on relevant columns. The cleaned data was saved as clean_data.csv.

## Data Analysis
### Section 1: General Trends
Descriptive statistics were computed for the data at the beginning (Period 1) and the end (Period 3) of the study. The analysis included:
* Participant count
* Data distribution
* General trends in the data

### Section 1B: Hypothesis Testing
#### Hypothesis 1: No Correlation between Smoking Status and Prevalent CHD
Chi-squared tests were conducted to test the hypothesis that there is no correlation between smoking status and prevalent CHD. The results indicated that there was no statistically significant correlation between the two variables for both Period 1 and Period 3.

#### Hypothesis 2: Correlation between Age, Smoking Status, and Prevalent CHD
The data was segmented into age groups to analyze the prevalence of CHD across different age groups. The analysis revealed trends in CHD prevalence based on age, suggesting potential correlations that warrant further investigation.

# Section 2: This section examines the relationship between sex, cholesterol levels, and CHD prevalence in two periods, aiming to understand their correlation with CHD incidence.

# Data Preparation
## Initial Data Loading and Filtering
* The data was initially loaded from the cleaned CSV file.
* The relevant columns (ID, SEX, PREVALENT CHD, PERIOD) were extracted into a new DataFrame called sex_df.
  
## Filtering by CHD and Period
* The data was filtered to include only individuals with a PREVALENT CHD value of 'YES' to focus on CHD cases.
* The filtered data was further split based on the two periods, Period 1 and Period 3.

# Analysis
## Period 1 Analysis
### Sex and CHD Prevalence
* The number of males and females with CHD in Period 1 was calculated and plotted.
* The bar chart titled "Fig 2.1: CHD Distribution by Gender for Period 1" shows the distribution of CHD cases by gender for Period 1.
### Sex, Smoking, and CHD Prevalence
* A subset of the data was further filtered to include only individuals with a SMOKING STATUS of 'YES'.
* The number of male and female smokers with CHD in Period 1 was calculated and plotted.
* The bar chart titled "Fig 2.3: CHD Distribution by Smoking Status and Gender for Period 1" shows the distribution of CHD cases by smoking status and gender for Period 1.

### Period 3 Analysis
### Sex and CHD Prevalence
* The number of males and females with CHD in Period 3 was calculated and plotted.
* The bar chart titled "Fig 2.2: CHD Distribution by Gender for Period 3" shows the distribution of CHD cases by gender for Period 3.
### Sex, Smoking, and CHD Prevalence
* he number of male and female smokers with CHD in Period 3 was calculated and plotted.
* The bar chart titled "Fig 2.4: CHD Distribution by Smoking Status and Gender for Period 3" shows the distribution of CHD cases by smoking status and gender for Period 3.

# Section 2b: This section explores the link between cholesterol levels and CHD across two periods, examining their distribution and correlation with smoking status.

## Data Preparation
### Initial Data Loading and Filtering
* The data was loaded and relevant columns (ID, SEX, PREVALENT CHD, PERIOD, TOTAL CHOLESTROL, SMOKING STATUS, CIGS PER DAY) were extracted into a DataFrame called chol_df.
### Filtering by CHD and Period
* The data was filtered to include only participants with a PREVALENT CHD value of 'YES' to focus on CHD cases.
* The filtered data was further split based on the two periods, Period 1 and Period 3.

### Analysis
#### Cholesterol and CHD Correlation
* The minimum and maximum cholesterol levels across the entire sample were calculated.
* Cholesterol levels were categorized into four bins: 'abnormally low', 'healthy', 'at risk', and 'abnormally high'.
* The distribution of cholesterol levels among participants with CHD in Period 1 was plotted in a bar chart titled "Fig 2b.1: Analysis of Cholesterol Levels in participants with CHD".
#### Cholesterol Levels by Sex
* The distribution of cholesterol levels among male and female participants with CHD in Period 1 was plotted in a grouped bar chart titled "Fig 2b.2: Analysis of Cholesterol Levels in Participants with CHD by Sex in Period 1".
#### Cholesterol, Smoking, and CHD
* A pivot table was created to analyze the relationship between cholesterol levels, smoking status, and CHD in Period 1.
* A bar chart titled "Fig 2b.3: Relationship between Smoking, CHD and Cholesterol levels" was plotted to visualize this relationship.
#### Analysis for CHD, Cholesterol, and Smoking in Period 3
* The data was filtered to focus on Period 3.
* Similar analyses were performed as in Period 1, including the distribution of cholesterol levels among participants with CHD and the relationship between cholesterol levels, smoking status, and CHD.
#### Statistical Testing
* Quartiles, Interquartile Range (IQR), and potential outliers were calculated for cholesterol levels among participants with CHD in Period 3.
* A boxplot titled "Fig 2b.5: Boxplot of participants with CHD in Period 3" was plotted to visualize the distribution of cholesterol levels and identify outliers.
#### Findings
* The majority of participants with CHD in Period 3 had 'abnormally high' cholesterol levels.
* No outliers were found below the lowerbound range, indicating that all identified outliers had 'abnormally high' cholesterol levels.

# Section 3: This section examines the connection between BMI and CHD across two periods, exploring its impact across various demographic groups like sex and smoking status.

# Data Preparation
## Data Loading and Cleaning
* The data was loaded from the clean_data.csv file into a DataFrame named bmi_df.
* The PREVALENT CHD column was converted to integer format with values 1 (for 'YES') and 0 (for 'NO').
* BMI was categorized into four groups: 'Underweight', 'Healthy Weight', 'Overweight', and 'Obesity'.

# Analysis for Period 1
## Descriptive Statistics and Visualization
* A new DataFrame bmiP1_df was created to filter the data for Period 1.
* Descriptive statistics were performed to understand the distribution of CHD across different categories such as sex, smoking status, and BMI.
* Pie charts and bar charts were created to visualize the distribution of CHD across BMI categories and smoking status.

# Analysis for Period 3
## Descriptive Statistics and Visualization
* A new DataFrame bmiP3_df was created to filter the data for Period 3.
* Similar descriptive statistics and visualizations as in Period 1 were performed to analyze the distribution of CHD across different categories.

# Findings
## Period 1
* The majority of participants with CHD in Period 1 were in the 'Obesity' category.
* Non-smokers had a higher prevalence of CHD compared to smokers in Period 1.
* Males had a higher prevalence of CHD compared to females in Period 1.
## Period 3
* Similar trends were observed in Period 3 with the majority of participants with CHD falling into the 'Obesity' category.
* The distribution of CHD across smoking status and sex remained consistent with Period 1.

# Conclusion 
This study examined the relationship between Body Mass Index (BMI) and Coronary Heart Disease (CHD) prevalence across two periods, revealing a notable association between higher BMI categories, such as 'Obesity', and increased CHD risk. Lifestyle factors like smoking and gender also influenced CHD occurrence, with non-smokers and males exhibiting higher prevalence rates. The findings emphasize the importance of weight management, lifestyle modifications, and gender-specific interventions in mitigating CHD risk, underscoring the need for comprehensive cardiovascular health strategies.

# HeartInsights Repo Organization
* csv folder: contains original and cleaned dataset
* Framingham Longitudinal Data Documentation: Documentation for the original dataset
* Project Proposal: Project proposal for the heartinsight data analysis project
* main.ipynb: contains code for the data analysis

