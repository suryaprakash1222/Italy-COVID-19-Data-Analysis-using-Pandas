Italy COVID-19 Data Analysis using Pandas
<p align="center">
<img src="https://img.shields.io/badge/Python-Pandas-blue?style=for-the-badge" alt="Python Pandas badge">
<img src="https://img.shields.io/badge/Analysis-COVID--19-green?style=for-the-badge" alt="COVID-19 analysis badge">
<img src="https://img.shields.io/badge/Portfolio-GitHub-black?style=for-the-badge" alt="GitHub portfolio badge">
</p>

Project Snapshot
A hands-on data analysis project built with Python, Pandas, and Matplotlib using Italy’s day-wise COVID-19 dataset. The project demonstrates practical data handling, cleaning, feature engineering, aggregation, dataset merging, and visualization.

What This Project Shows
Data acquisition from online sources.

Data inspection and exploration with Pandas.

Cleaning invalid and anomalous values.

Date handling and time-based feature extraction.

Group-wise and month-wise analysis.

Merging multiple datasets.

Normalized metrics for population-based comparison.

Visual reporting using Matplotlib.

Tools and Libraries
Tool / Library	Purpose
Python	Core programming language
Pandas	Data manipulation and analysis
Matplotlib	Charts and visualizations
urllib.request	Downloading datasets from URLs
Dataset
This project uses:

Italy COVID-19 day-wise data.

Location and population metadata for merging and per-capita calculations.

The data is downloaded directly from online sources inside the Python script, making the workflow reproducible.

Workflow
Data Acquisition
Downloaded CSV files using urllib.request.

Saved files locally for analysis.

Loaded the files into Pandas DataFrames.

Data Exploration
Used info() to inspect data types and missing values.

Used describe() to summarize numeric columns.

Checked the dataset size using shape.

Reviewed columns using columns.

Inspected sample records using head(), tail(), and sample().

Data Cleaning
Identified invalid negative values in daily case records.

Corrected anomalous values using neighboring rows.

Converted the date column into datetime format.

Feature Engineering
Extracted year, month, day, weekday, and day name from the date column.

Calculated positivity-related metrics.

Computed cumulative totals for cases, tests, and deaths.

Analysis Performed
Calculated total COVID cases and deaths.

Calculated overall death rate and positivity rate.

Filtered days with high case counts.

Filtered records with above-average positivity rate.

Compared Sunday averages with overall averages.

Performed month-wise totals and averages.

Data Merging
Loaded a second dataset containing location and population data.

Renamed and cleaned columns for merge compatibility.

Merged datasets using country as the common key.

Normalized Metrics
Calculated new cases per million population.

Calculated new deaths per ten million population.

Output and Visualization
Created a final processed output DataFrame.

Exported the result to CSV.

Saved charts using Matplotlib.

Pandas Skills Demonstrated
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

Daily new cases trend.

New cases vs new deaths comparison.

Monthly stacked bar chart for cases and deaths.

Why This Project Matters
This repository is designed as a portfolio project to show practical Pandas knowledge, structured analytical thinking, and hands-on data analysis workflow.

It highlights the ability to work through a complete mini-project from raw dataset to final output.

Repository Contents
Pandas_Handbook_Italy_COVID_Analysis.ipynb — personal learning handbook for code revision.

Python project code for Italy COVID-19 analysis.

Exported CSV output.

Saved visualizations.

README.md — portfolio overview for GitHub.

Author
Surya Prakash
Data Analyst / Business Analyst
India
