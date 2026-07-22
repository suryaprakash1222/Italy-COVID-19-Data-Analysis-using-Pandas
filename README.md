Italy COVID-19 Data Analysis using Pandas
A portfolio project built with Python, Pandas, and Matplotlib to perform end-to-end analysis on Italy’s day-wise COVID-19 data. This project demonstrates practical hands-on work in data collection, cleaning, exploration, transformation, aggregation, dataset merging, and visualization.

Overview
In this project, I worked with a real-world COVID-19 dataset for Italy and used Pandas to perform a complete analysis workflow from raw CSV files to final analytical outputs.

The project focuses on demonstrating practical Pandas skills that are directly relevant to data analyst and business analyst roles, including:

Loading data from online sources

Inspecting and understanding dataset structure

Selecting and filtering records

Cleaning invalid observations

Creating calculated columns

Working with datetime features

Performing monthly and weekday-level analysis

Building cumulative metrics

Merging multiple datasets

Exporting results

Creating visualizations

Objective
The goal of this project is to showcase hands-on proficiency with Pandas by solving a real analytical problem using a structured workflow. Rather than using Pandas only for small examples, this project applies it to a realistic dataset and demonstrates how Python can be used for data preparation, exploratory analysis, feature engineering, and reporting.

Tools and Libraries
Python

Pandas

Matplotlib

urllib.request

Workflow
1. Data acquisition
Downloaded Italy COVID-19 day-wise data from an online source using urllib.request

Loaded the CSV file into a Pandas DataFrame

Downloaded a second dataset containing location and population data for merge operations

2. Data exploration
Inspected the dataset using .info(), .describe(), .shape, and .columns

Accessed rows and columns using direct indexing, .loc[], and .at[]

Reviewed samples, head, and tail records to understand the structure of the dataset

3. Data cleaning
Identified records with invalid negative values in new_cases

Corrected anomalous values using neighboring observations

Converted the date column into proper datetime format

4. Feature engineering
Extracted year, month, day, weekday, and day name from the date column

Created analytical metrics such as positivity rate

Computed cumulative totals for cases, tests, and deaths

5. Analysis performed
Calculated total COVID cases and total deaths

Calculated death rate and positivity rate

Identified high-case days where daily cases exceeded a threshold

Filtered records where daily positivity rate exceeded the overall positivity rate

Compared Sunday average cases with overall average cases

Performed month-wise total and average analysis for key COVID metrics

6. Dataset merging
Cleaned and prepared a location metadata dataset

Renamed columns for consistency

Merged the COVID dataset with location data using a common country field

7. Population-normalized metrics
Calculated new cases per million population

Calculated new deaths per ten million population

8. Output generation
Created a final output dataset with selected reporting columns

Exported the processed result to CSV

Built multiple charts using Matplotlib and saved them as image files

Key Pandas Concepts Demonstrated
This project reflects hands-on usage of the following Pandas capabilities:

read_csv()

DataFrame inspection and summary methods

Column selection and row slicing

.loc[] and .at[]

Boolean filtering

.copy()

.sum(), .mean(), .describe()

.sort_values()

.drop()

pd.to_datetime()

DatetimeIndex

.groupby()

.cumsum()

.merge()

.to_csv()

Visual Outputs
The project includes visualizations created from the processed dataset, such as:

Daily new COVID cases trend

New cases vs new deaths comparison

Month-wise stacked bar chart for cases and deaths

Business and Analytical Value
This project demonstrates the kind of workflow expected in real analytics work:

Converting raw external data into analysis-ready datasets

Detecting and handling data quality issues

Creating derived metrics for better interpretation

Combining datasets to enrich analysis

Producing summarized outputs and charts for reporting

It also shows the ability to move beyond basic syntax and use Pandas as a practical data analysis tool for structured problem solving.

Repository Contents
Pandas_Handbook_Italy_COVID_Analysis.ipynb — personal learning handbook with step-by-step code explanations

Project code for Italy COVID-19 data analysis using Pandas

Output CSV generated after analysis

Visualization files generated from the dataset

Why this project matters
This repository is intended as a portfolio project to demonstrate practical Pandas knowledge. It highlights data handling, analytical thinking, and workflow organization in a way that is relevant for Python-based data analysis roles.

Author
Surya Prakash
Data Analyst / Business Analyst
India
