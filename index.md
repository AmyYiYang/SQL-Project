## Introduction
In this report, I will use SQL to conduct my exploratory analysis as well as creating a transformed feature training set for my machine learning models.While R and Python are popular in data analysis,having the ability to conduct SQL enquiries can quickly get you started on data exploration.

### Data Exploration
The purpose of this report is to present data of housing price by conducting SQL enquiries. To get started, I downloaded the train.csv from https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data. Then, I imported the csv file to a table I created in MySQL Workbench.Below are steps to create the table.
Step 1: create a new schemas "housing_price_prediction" under which table data is imported from "Table Data Import Wizard".
Step 2: browse the datase simply by using the code below.
#browse the overall dataset
SELECT * FROM housing_price_prediction.train; 
#calculate average housing price for paved street
SELECT coalesce(Street,'Pave') as Street, round(avg(SalePrice),4) as avg_sale_price FROM housing_price_prediction.train;

Step 3: advanced data exploration to create a table showing average housing price based on four features
