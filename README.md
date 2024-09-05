# Predicting_Restaurant_Tips_in_MS_Excel
The purpose of this project is to predict restaurant tips given input values with the mathematical equation for predicting the value of the tip.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [References](#references)

## Project Overview
MS Excel was used to analyze restaurant order information in order to predict the value of tips. 

## Data Sources
The primary dataset used for this analysis is the 'Restaurant_Tips_Dataset.xlsx' file, from the Simplilearn Business Analytics with Excel Certification Training, containing detailed information of orders made.

## Tools
MS Excel - Data cleaning, Analysis and Visualisation [Download here](https://www.microsoft.com/en-au/microsoft-365/excel)

## Data Cleaning
In the initial data preparation phase, the following tasks were performed:

1. Data loading and inspection

2. Data cleaning and preparation
   - Remove rows with at least one empty cell
     - Select 'Control+A' to select entire dataset
     - Select 'Find and Select-Special-Select Blanks' from the Home tab
   - Check for duplicates
     - Select 'Control+A' to select entire dataset
     - Select 'Remove Duplicates- Select all columns- Ok' from the Data tab

## Data Analysis
1. Identify features that are independent and dependent
   - Dependent variable
     - (also known as the response variable, outcome variable, or target variable) is the variable in an experiment or model that you are trying to predict or explain. It is called "dependent" because its value is presumed to depend         on the influence of other variables, called independent variables or predictor variables.
   - Independent variable
     - (also known as a predictor variable, explanatory variable, or input variable) is a variable that is manipulated or selected by the researcher or modeler to observe its effect on the dependent variable. It is called
       "independent" because it is not affected by other variables in the model but can influence changes in the dependent variable.

    ![1_Independent_Dependent_Variables](https://github.com/user-attachments/assets/2a8eb4cd-7a13-4594-8a6c-6452eece7a2d)


- Select 'Data' tab
- Select 'Data Analysis'
- Select 'Histogram' and click 'Ok'
- In the Histogram dialogue box click the 'Labels' checkbox as there are labels in the data
- In the 'Input Reference' select 'SalesData!D1:D51291' and in the 'Bin Reference' select 'Working!K3:K7'
- In the 'Output' select a new worksheet for the binning table, click the histogram checkbox and then ok.

2. Prepare a table of sales and profit month wise in the working sheet

```MS Excel
Sales= SUMIFS('Sales Data'!$H:$H,'Sales Data'!$U:$U,Working!$B4,'Sales Data'!$F:$F,$R$3)
```
```MS Excel
Profit=SUMIFS('Sales Data'!$K:$K,'Sales Data'!$U:$U,Working!$B4,'Sales Data'!$F:$F,$R$3)
```

3. Create a user control combo box for the product category

- Select 'Developer'
- Select 'Insert'
- Select 'Form Controls' then 'Combo box'
- Draw the box on the Working Sheet
- Right click on the box and Select 'Format Control'
- 'Input Range' is the 'List of Product Categories' in Q2:Q5
- 'Cell Link' is $R$2
- 'Drop Down Lines' is 4

4. Create a Column Chart of the month wise table and region wise table

- Select 'Months' and 'Sales' columns
- Select 'Insert, Chart, Clustered Column'
- Select 'Region' and 'Sales' columns
- Select 'Insert, Chart, Clustered Column'

## Results



## References
- Simplilearn Business Analytics with Excel Certification Training
- ChatGPT 4o



