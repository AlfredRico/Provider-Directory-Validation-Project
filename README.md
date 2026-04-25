# Provider Directory Data Validation & Quality Analysis

---

## Overview

This project focuses on validating and cleaning provider directory data to improve reliability before analysis. The goal is to identify issues like missing values, duplicate records, inconsistent formatting, invalid entries, and outliers that can create problems in provider operations and claims processing. Once the data is cleaned and structured, the analysis can be used to support clearer reporting, stronger provider records, and better decision making across credentialing and claims readiness.

---
## Business Problems

* Provider records contain missing and incomplete fields, making it difficult to verify credentials and increasing the likelihood of delays in claims processing and referrals.
* Duplicate providers and inconsistent identifiers create conflicting records, reducing trust in reporting and making provider tracking unreliable.
* Key identifiers such as NPIs and dates are not consistently formatted or validated, introducing avoidable errors into credentialing and claims workflows.
* Variability in claims outcomes and processing times suggests gaps in either operational efficiency or underlying data quality that need to be addressed.
* Inconsistent categorical fields such as specialty, state, and network status make it harder to group providers accurately and produce reliable summaries.
* Without structured validation, provider data cannot be confidently used for reporting, decision making, or claims readiness assessments.

---

## Key Insights

* Missing values were not evenly distributed and appeared more frequently in credentialing related fields, indicating that the areas most critical for claims readiness were also the least reliable.
* Duplicate records often shared similar names but differed in identifiers or formatting, showing that simple matching is not enough to resolve provider duplication issues.
* Invalid NPIs and mixed date formats required standardization before any analysis, reinforcing that validation must come before reporting.
* Providers with higher claim denials also tended to have inconsistent or incomplete records, suggesting a link between data quality and operational outcomes.
* Cleaning and standardizing categorical fields significantly improved grouping accuracy, making provider segmentation more consistent across specialties and locations.
* After validation, it became easier to isolate providers contributing to delays and errors, allowing the data to be used more reliably for operational review and reporting. 

---

## Reproducibility

This project uses **UV** for fast, deterministic environment management.

### 🔧 Prerequisites

Install UV (official guide):  
https://docs.astral.sh/uv/getting-started/

---

### ▶️ Run Locally (Step-by-Step)

```bash
# 1. Clone the repository
git clone https://github.com/AlfredRico/Provider-Directory-Validation-Project.git
cd Provider-Directory-Validation-Project

# 2. Sync environment (installs Python + dependencies)
uv sync

# 3. Launch Jupyter Lab
uv run jupyter lab
```

---

### 📂 Open the Project

Once Jupyter Lab opens in your browser:

1. Navigate to the project root directory  
2. Open the notebook:

   ```
   provider_directory_validation.ipynb
   ```

3. Run all cells from top to bottom  

---

### 🧠 Notes

- The environment is fully defined by:
  - `pyproject.toml`
  - `uv.lock`
- No manual package installation is required  
- Results are fully reproducible across systems  

---

## Project Structure

```
provider_directory_validation_project/
├── data/provider_validation_dataset.csv   # sample dataset (tracked)
├── provider_directory_validation.ipynb
├── pyproject.toml
├── uv.lock
└── README.md
```

---

## Data Source

This project uses a synthetic provider operations dataset created to simulate real provider directory and claims readiness challenges. The dataset was designed to reflect common operational issues such as missing values, duplicate records, invalid NPIs, inconsistent formatting, incorrect dates, and outliers across provider records.

The goal was to create a realistic environment for data cleaning, validation, and exploratory analysis focused on provider directory reliability and claims processing readiness.

```
---

## Ecosystem

* Portfolio webpage → Project hub and navigation: https://alfredrico.github.io/  
* GitHub → Project repositories featuring UV management for reproducibility: https://github.com/AlfredRico  