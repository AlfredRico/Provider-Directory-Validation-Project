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

* Exact duplicate rows were removed, while repeated names such as `Maria Lopez` were confirmed to be separate providers with different `Provider_ID` and `NPI_Number` values. This shows why provider matching should rely on true identifiers rather than provider names alone.
* Fields such as `Specialty`, `License_State`, and `Insurance_Network_Status` contained formatting issues, spelling errors, and mixed naming conventions. Standardizing these fields improves grouped analysis and reporting accuracy.
* ZIP code validation standardized valid records into 5-digit text format, but 434 records still contain missing ZIP values. These should remain flagged for review rather than being filled with assumptions.
* `Last_Credentialing_Review_Date` contained mixed date formats that affected time-based reporting. Most valid dates were standardized, whil e 370 invalid values remain flagged for manual review.
* Final NPI validation showed that 526 records still do not meet the required 10-digit structure. Since NPI numbers are critical for credentialing and payer matching, these remain a high priority issue.

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


---
## Ecosystem

* Portfolio webpage → Project hub and navigation: https://alfredrico.github.io/  
* GitHub → Project repositories featuring UV management for reproducibility: https://github.com/AlfredRico  