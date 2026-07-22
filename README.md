Italy COVID-19 Data Analysis using Pandas
Project Overview
This repository showcases a hands-on data analysis project built with Python, Pandas, and Matplotlib using Italy's day-wise COVID-19 dataset.

The project demonstrates how Pandas can be used for real-world data analysis tasks such as data loading, inspection, cleaning, transformation, aggregation, merging, and visualization.

Objective
The goal of this project is to demonstrate practical proficiency in Pandas by working on a real dataset and performing a complete analysis workflow from raw data to analytical outputs.

This project reflects the kind of work expected in data analyst and business analyst roles where raw data must be cleaned, explored, transformed, and converted into useful insights.

Tools and Libraries
Tool / Library	Purpose
Python	Core programming language
Pandas	Data manipulation and analysis
Matplotlib	Data visualization
urllib.request	Downloading datasets from URLs
Dataset Used
This project uses:

Italy COVID-19 day-wise data

Location and population metadata for merge operations

The datasets are downloaded directly from online sources inside the Python script.

Project Workflow
1. Data Acquisition
Downloaded CSV data from public URLs using urllib.request

Saved the files locally for analysis

Loaded the files into Pandas DataFrames

2. Data Exploration
Inspected dataset structure using:

info()

describe()

shape

columns

Reviewed sample rows using:

head()

tail()

sample()

Accessed specific records using:

direct indexing

.loc[]

.at[]

3. Data Cleaning
Identified invalid negative values in daily case records

Corrected anomalous values using neighboring rows

Converted the date column into datetime format

4. Feature Engineering
Created new date-based columns:

year

month

day

weekday

day name

Calculated positivity-related metrics

Computed cumulative totals for:

total cases

total tests

total deaths

5. Analysis Performed
Calculated total COVID cases and deaths

Calculated overall death rate

Calculated overall positivity rate

Identified days with high COVID case counts

Filtered records with above-average positivity rate

Compared Sunday average cases with overall average cases

Performed month-wise totals and average analysis

6. Data Merging
Loaded a second dataset containing location and population data

Renamed and cleaned columns for merge compatibility

Performed DataFrame merge operation using country as the common key

7. Normalized Metrics
Calculated new cases per million population

Calculated new deaths per ten million population

8. Output and Visualization
Created a final processed output DataFrame

Exported the result to CSV

Built and saved charts using Matplotlib

Pandas Concepts Demonstrated
This project includes practical use of the following Pandas operations:

pd.read_csv()

DataFrame.info()

DataFrame.describe()

DataFrame.copy()

.loc[]

.at[]

Boolean filtering

.sum()

.mean()

.sort_values()

.drop()

pd.to_datetime()

pd.DatetimeIndex()

.groupby()

.cumsum()

.merge()

.to_csv()

Sample Code
python
import pandas as pd

covid_df = pd.read_csv("italy-covid-daywise.csv")
covid_df["date"] = pd.to_datetime(covid_df["date"])
covid_df["month"] = pd.DatetimeIndex(covid_df.date).month

monthly_summary = covid_df.groupby("month")[["new_cases", "new_deaths", "new_tests"]].sum()
print(monthly_summary)
Visual Outputs
The project includes charts such as:

Daily new cases trend

New cases vs new deaths comparison plot

Monthly stacked bar chart for cases and deaths

Business and Analytical Value
This project demonstrates the ability to:

Work with external real-world datasets

Detect and handle data quality issues

Engineer meaningful analytical features

Combine datasets for richer analysis

Build reporting-oriented outputs using Python

Use Pandas beyond basic practice problems

Repository Contents
Pandas_Handbook_Italy_COVID_Analysis.ipynb — personal learning handbook for code revision

Python project code for COVID-19 analysis

Exported CSV output

Saved visualizations

README.md — project overview for GitHub portfolio

Why This Project Matters
This repository is designed to function as a portfolio project that demonstrates practical Pandas knowledge, structured analytical thinking, and hands-on data analysis workflow.

It highlights not just syntax knowledge, but the ability to work through a complete mini-project from raw dataset to final output.

Author
Surya Prakash
Data Analyst / Business Analyst
India
