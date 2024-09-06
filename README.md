# Project Overview
This is a complete Exploratory Data Analysis Project of a Financial Dataset Using Python. By analyzing this data, I tried to understand the performance of the company across different countries, segments, and the performance of their various products. I understood and took note of patterns and trends in their dataset to enable give recommendations. 

# Dataset
The dataset for this project was obtained from Kaggle

# Libraries used
import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
import seaborn as sns
plt.style.use('ggplot')
%matplotlib inline
import missingno as msno

# Data Analysis (Some interesting codes I worked with)
1. # calculating correlation coefficient to verify the type of relationship existing

correlation_coefficient = joined_df['Profit'].corr(joined_df['COGS'])

print("Correlation coefficient:", correlation_coefficient)

# COGS, Profit, Product
### Select the numerical variables
num_col = joined_df[['Units Sold', 'Manufacturing Price', 'Sale Price', 'Gross Sales', 'Discounts', 'Sales', 'COGS', 'Profit']]

### Create a scatterplot matrix using Seaborn
sns.pairplot(num_col)

# Steps 
1. Importing libraries
2. Importing Dataset
3. Cleaning Dataset:
   a. checking for duplicates
   b. checking for missing values
   c. renaming columns
   d. dropping columns
   e. Visualizing missing values using missingno
   f. handling missing values using bfill
   h. identifying outliers using IQR
   i. Handling outliers using median
   j. univariate analysis
   k. bivariate analysis
   l. multivariate analysis

# Diagrams used for analysis
1. bar char
2. histogram
3. missingno
4. line plot
5. pairplot
6. heatmap
7. scatterplot

# Exploratory Data Analysis Findings
1. Country with the highest number of units sold
2. Product with the highest number of units sold
3. The relationship between cost of goods sold and profit
4. Coefficient of the relationship between the cost of goods sold and profit
5. Months with their level of sales, showing the months with the highest sales and the months with low sales
6. The product with the highest sales
7. The product with the highest profit
8. The country with the highest profit
9. The segment of the company with the highest profit
10. The product with the highest COGS

# Recommendations
1. Increasing supply to Canada appears to be a strategic move to capitalize on the strong demand
2. Increasing production or implementing targeted marketing campaigns to further boost sales. Additionally, analyzing the factors contributing to Montana's popularity could provide insights for improving the performance of other products in the lineup.
3. The company might consider expanding the availability of Montana or introducing complementary products to further drive sales. Analyzing the factors contributing to Montana's popularity could provide valuable insights for improving the performance of other products in the lineup
4. The company's operations in the United States appear to be highly successful, generating the highest profit. To capitalize on this success, the company might consider expanding its presence in the United States or implementing similar strategies in other markets with high potential. Analyzing the factors contributing to the United States' profitability could provide valuable insights for improving performance in other regions


# Limitations
I had to remove whitespaces from the columns which at the beginning posed as a challenge because I didn't catch that immediately. I removed all dollar signs and replaced all empty rows with NaN, after which I handled the missing values using bfill. 

# References 
Kaggle: 
https://www.kaggle.com/datasets/atharvaarya25/financials/code
