<!-- PROJECT HEADER - DARK THEME -->
<div align="center">
  
  [![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
  [![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
  [![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)](https://matplotlib.org/)
  [![Seaborn](https://img.shields.io/badge/Seaborn-FF9999?style=for-the-badge&logo=seaborn&logoColor=white)](https://seaborn.pydata.org/)
  [![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
  [![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/)
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
  [![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

</div>

<h1 align="center">
  🔍 LinkedIn Jobs Analysis – India Tech Market Insights
</h1>

<p align="center">
  <em>Data cleaning • EDA • Job market competition analysis</em>
  <br><br>
  <a href="https://colab.research.google.com/drive/your-notebook-link">
    <b>🧪 Open in Colab</b>
  </a>
  ·
  <a href="#key-insights">
    <b>📊 Key Insights</b>
  </a>
  ·
  <a href="#data-pipeline">
    <b>🔄 Data Pipeline</b>
  </a>
  ·
  <a href="#run-locally">
    <b>🚀 Run Locally</b>
  </a>
</p>

---

## ✨ Key Insights

<div align="center">

| Insight | Metric | Value |
|---------|--------|-------|
| 🏆 **Top Hiring Region** | Bengaluru, Karnataka | **1,324** jobs [file:1] |
| 📈 **Data Analyst Postings** | Total roles | **224** [file:1] |
| 🔥 **Applications Received** | Total for Data Analyst | **24,283** [file:1] |
| ⚔️ **Competition Ratio** | Apps per Data Analyst posting | **~108** applicants/job [file:1] |

</div>

> **Takeaway**: Bengaluru dominates hiring, but Data Analyst roles see **108 applicants per opening** – highly competitive![file:1]

---

## 📊 Data Pipeline

```mermaid
graph TD
    A[📥 Raw CSV<br/>7,927 jobs] --> B[🧹 Data Cleaning]
    B --> C[✂️ Remove duplicates<br/>7,848 unique]
    B --> D[📝 Standardize titles<br/>Title case]
    C --> E[🌍 Location parsing<br/>city, region, state]
    D --> F[🔢 Extract applications<br/>Regex → numeric]
    E --> G[📈 Analysis & Viz]
    F --> G
    G --> H[💾 linkedinjobsfinal.csv]
