<!-- PROJECT HEADER -->
<p align="center">
  <img src="assets/banner.png" alt="Project Banner" width="80%">
</p>

<h1 align="center">LinkedIn Jobs Analysis – India Tech Market</h1>

<p align="center">
  Data cleaning • Exploratory analysis • Job market insights
  <br />
  <a href="https://colab.research.google.com/drive/your-notebook-link"><strong>Open in Colab »</strong></a>
  <br />
  <br />
  <a href="#about-the-project">About</a>
  ·
  <a href="#data-pipeline">Data Pipeline</a>
  ·
  <a href="#key-findings">Key Findings</a>
  ·
  <a href="#how-to-run">How to Run</a>
  ·
  <a href="#future-work">Future Work</a>
</p>

---

## About the Project

This project analyzes a LinkedIn job postings dataset focused on the Indian market to understand where tech opportunities are concentrated and how competitive they are for Data roles. The notebook walks through the entire workflow: from raw CSV to interpretable business insights. [file:1]

**Core objectives:**

- Identify which **region** has the highest number of job postings. [file:1]  
- Quantify how competitive **Data Analyst** roles are in terms of applications per posting. [file:1]

---

## Dataset & Scope

- Source: Kaggle – LinkedIn job postings dataset. [file:1]  
- Size: 7,900+ job postings after cleaning (India-only subset). [file:1]  
- Focus fields: job title, location, company, work type, number of employees, applications, and posting age. [file:1]

The analysis is implemented in a single, reproducible Google Colab notebook.

---

## Data Pipeline

The notebook implements a structured data pipeline:

1. **Ingestion**
   - Import CSV from Kaggle using `opendatasets` into Colab. [file:1]

2. **Cleaning & Standardization**
   - Drop unused identifiers (for example, `jobID`, `companyid`, helper columns). [file:1]  
   - Remove duplicates, resulting in 7,848 unique postings. [file:1]  
   - Standardize job titles and company names to title case. [file:1]  
   - Clean `job` strings (remove salary snippets, quotes, extra whitespace). [file:1]

3. **Location Engineering**
   - Derive `country`, `city`, and a combined `regionstate` from the `location` column. [file:1]  
   - Handle edge cases like “Greater Bengaluru Area” using a custom parsing function to avoid `NaN` values. [file:1]

4. **Feature Refinement**
   - Extract numeric values from `noofapplication` using regex and cast to numeric. [file:1]  
   - Export the final tidy dataset to `linkedinjobsfinal.csv` for further use. [file:1]

---

## Key Findings

From the processed dataset, two headline insights emerge.

### 1. Hiring Hotspot by Region

- The top hiring region is **Bengaluru, Karnataka**, with **1,324** job postings, making it the dominant hub in this dataset. [file:1]  
- A bar chart of the top 10 regions shows Bengaluru far ahead of other cities and states. [file:1]

> Interpretation: Bengaluru acts as a central engine for tech employment, especially in data and software roles. [file:1]

### 2. Competition for Data Analyst Roles

Focusing on roles containing “Data Analyst” in the job title: [file:1]

- Total Data Analyst postings: **224**. [file:1]  
- Total applications for these roles: **24,283**. [file:1]  
- Average applications per posting: **≈108** applications per job. [file:1]

> Interpretation: Demand for Data Analyst roles is strong, but candidate volume is even stronger, creating a highly competitive entry point into data careers. [file:1]

---

## How to Run

You can run the analysis either in Colab or locally.

### Option 1 – Run in Google Colab (Recommended)

1. Open the notebook in Colab using the link in the header. [file:1]  
2. Ensure your Kaggle API credentials are set up in the environment.  
3. Run all cells in order; the dataset will be downloaded automatically using `opendatasets`. [file:1]

### Option 2 – Run Locally

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name

