README
LinkedIn Jobs Analysis (Kaggle – India Data)

This project analyzes a LinkedIn job postings dataset from Kaggle, focusing on understanding regional hiring patterns and competition levels for data roles in India.
​

Project Overview

The analysis answers two main questions:
​

Which region (city, state) has the highest number of job postings?

What is the average number of applications received for Data Analyst roles?

The work is implemented in a Google Colab notebook (LinkedIn_Job.ipynb) and exported as PDF in this repository.
​

Dataset

Source: Kaggle – LinkedIn job dataset by shashankshukla123123.
​

Size: 7,927 raw rows, 16 columns before cleaning.
​

Scope: Jobs located in India across multiple tech and data roles.
​

Key columns used:
​

job – job title

location – city, state, country or area

companyname – employer

worktype – on-site, remote, hybrid

noofapplication – number of applications

fulltimeremote, noofemploy, posteddayago, linkedinfollowers

Methods and Cleaning Steps

Main preprocessing steps:
​

Dropped unused columns such as jobID, companyid, and helper columns.
​

Removed duplicate rows (reduced to 7,848 entries).
​

Standardized job and companyname to title case for consistency.
​

Cleaned job strings (removed salary text, symbols, and extra punctuation).
​

Parsed location into:

country (verified only India is present),

city,

regionstate in the form City, State with a custom function handling cases like “Greater Bengaluru Area”.
​

Cleaned noofapplication by extracting numeric values from text and converting them to float, treating missing values as 0 where needed.
​

The final cleaned dataset is exported as linkedinjobsfinal.csv for future analysis.
​

Key Findings

Top hiring region

The region with the most job postings is Bengaluru, Karnataka with 1,324 postings, making it the primary hiring hub in the dataset.
​

A bar chart of the top 10 regions by job count highlights Bengaluru as a clear outlier in job volume.
​

Competition for Data Analyst roles

Filtered the dataset to job titles containing “Data Analyst”.
​

Total Data Analyst postings: 224.
​

Total applications for these postings: 24,283.
​

Average applications per Data Analyst posting: ≈108 applications per job.
​

These results show that while data roles are widely available, competition is very intense for Data Analyst positions.
​

Files in this Repository

LinkedIn_Job.ipynb (original notebook, if included) – full analysis and code.

LinkedIn_Job.ipynb - Colab.pdf – exported notebook with all steps, outputs, and visualizations.
​

linkedinjobsfinal.csv – cleaned dataset ready for further analysis or modeling.
​

How to Run

Open the notebook in Google Colab or Jupyter.

Ensure the Kaggle dataset is available locally or use opendatasets to download from Kaggle.
​

Run the cells in order:

Data loading

Cleaning and feature engineering

Exploratory analysis and visualizations

Summary statistics and conclusions

AI Assistance and Integrity

AI tools were used as a technical assistant to:
​

Debug Python code and fix data type errors.

Write regular expressions for cleaning the noofapplication column.

Standardize text formatting for job and companyname fields.
​

All research questions, analytical decisions, and interpretations (including the 108:1 competition ratio) were reviewed and validated by the project author.
