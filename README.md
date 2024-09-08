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

2. Identify which predictive problem is needed
   - We are interested in predicting the tip amount based on other features such as the total bill, party size, and customer demographics (e.g., sex, smoker status), as well as contextual factors (e.g., day of the week, time of day).

3. Encode the categorical variables to numeric values using if conditions
   - A categorical variable is a type of variable that represents data which can be divided into groups or categories that do not have a natural ordering. These are often known as qualitative variables and can represent types or
     labels, as opposed to quantitative variables which represent numerical values that you can perform arithmetic operations on.

4. For each independent numeric value, find its correlation coefficient with respect to the tip

   ```MS Excel
   Sex_correl= CORREL(B2:B244,AI2:AI244)
   ```
   
5. Build an appropriate model with the dataset
   - Select 'Data- Data Analysis- Regression'
   - Select 'Input Y= the tip values' and 'Input X= the numeric values of the categorical variables'
   - Select 'Output Range= An empty cell on the worksheet'
   - Select OK
  
6. Calculate the predicted tip values per independent variable
   Predicted tip= Intercept + (Coefficient for Independent Variable x  Independent Variable Value)

7. Calculate the Root Mean Square Error (RMSE) of the model
   - Residual= Actual Tip - Predicted Tip
   - Square of the Residuals= (Residuals)^2
   - Average Square of the Residuals= Average of the Square of Residuals Column
   - Root Mean Square Error(RMSE)= The Square Root of the Average Square of the Residuals   

## Results
1. Identify features that are independent and dependent

   ![1_Independent_Dependent_Variables](https://github.com/user-attachments/assets/2a8eb4cd-7a13-4594-8a6c-6452eece7a2d)

2. Identify which predictive problem is needed
   The predictive problem is a regression problem, where the goal is to model and predict a continuous outcome (the tip amount).

3. Encode the categorical variables to numeric values using if conditions

   ![2_Categorical_Variables](https://github.com/user-attachments/assets/8b037542-a2c2-4721-bab3-990dec89ec65)

4. For each independent numeric value, find its correlation coefficient with respect to the tip
   Repeat the formula for all categorical variables

5. Build an appropriate model with the dataset
   For the Sex and Tip model:

   ![3_Regression](https://github.com/user-attachments/assets/b36f4635-1af6-40e1-929f-a840af37c560)

6. Calculate the predicted tip values per independent variable
   ```MS Excel
   sex_pred_tip= =$AM$28+($AM$29*B2)
   ```
   For sex_pred_tip column cell D2: 2.84313953488372+(0.246478299511184*B2)= 2.843139535

7. Calculate the Root Mean Square Error (RMSE) of the model for the Sex and Tip (Row 2)
   - Residual= Actual Tip - Predicted Tip = -1.833139535
   - Square of the Residuals= (Residuals)^2 = 3.360400554
   - Average Square of the Residuals= Average of the Square of Residuals Column= 1.896445388
   - Root Mean Square Error(RMSE)= The Square Root of the Average Square of the Residuals= 1.377114878

   
## References
- Simplilearn Business Analytics with Excel Certification Training
- ChatGPT 4o



