# U.S. Hospital Quality Analysis

## Project Overview

This project analyzes publicly available hospital quality data from the Centers for Medicare & Medicaid Services (CMS) to examine how overall hospital quality varies across the United States. Using Python, SQL, and data visualization techniques, the project retrieves live data through the CMS Provider Data Catalog API, performs data cleaning and validation, and compares hospital quality ratings across states to identify meaningful patterns.

---

## Business Question

**How does CMS overall hospital quality vary across U.S. hospitals and states?**

---

## Data Source

**Centers for Medicare & Medicaid Services (CMS)**  
Provider Data Catalog – Hospital General Information  
Dataset ID: **xubh-q36u**

- Access Method: CMS Provider Data Catalog API
- Data retrieved programmatically using Python
- Source updates periodically as CMS releases new information

---

## Tools

- Python
- Pandas
- Requests
- CMS Provider Data Catalog API
- SQLite / SQL
- Matplotlib
- Jupyter Notebook
- GitHub Codespaces
- Git / GitHub

---

## Data Cleaning

The dataset was cleaned and validated before analysis by:

- Removing duplicate hospital records.
- Converting Overall Hospital Rating to a numeric variable where appropriate.
- Separating rated hospitals from hospitals with missing ratings.
- Excluding missing ratings from average-rating calculations.
- Verifying unique hospital identifiers.
- Validating row counts and summary statistics.
- Cross-checking Python results with equivalent SQL queries.

---

## Key Findings

1. CMS Overall Hospital Ratings vary considerably across U.S. hospitals.
2. Average hospital quality differs by state, with some states consistently reporting higher average ratings than others.
3. Excluding hospitals without CMS ratings provides more accurate state-level comparisons.

---

## Visualizations

The complete visualizations and analysis are available in:

```
notebooks/01_hospital_quality_analysis.ipynb
```

Visualizations include:

- Overall Hospital Rating distribution
- Average hospital rating by state
- Rated hospitals by state

---

## SQL Analysis

SQL queries used for validation and comparison are located in:

```
sql/analysis_queries.sql
```

These queries reproduce the primary Python analyses to verify:

- Rated hospital counts
- State average ratings
- Missing rating exclusions
- Consistent filtering logic

---

## Limitations

- CMS updates the dataset periodically, so results may change over time.
- Some hospitals do not have an Overall Hospital Rating and are excluded from rating analyses.
- The analysis is descriptive and does not establish causal relationships.
- Differences in hospital size, patient population, and case complexity are not adjusted for in this project.

---

## How to Reproduce

1. Open this repository in GitHub Codespaces.
2. Open the Jupyter Notebook.
3. Run each notebook cell from top to bottom.
4. The notebook automatically retrieves the latest CMS data through the API.
5. Run the SQL queries in the `sql` folder to validate the Python results.

---

## Repository Structure

```text
US-Hospital-Quality-Analysis/
│
├── notebooks/
│   └── 01_hospital_quality_analysis.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── data/
│   └── (optional cached datasets)
│
├── images/
│   └── (charts and figures)
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Future Improvements

- Integrate HCAHPS patient experience data.
- Incorporate selected outcome and timely/effective care measures.
- Develop an interactive dashboard using Plotly or Tableau.
- Apply statistical modeling to identify predictors of hospital quality.
- Perform longitudinal analyses using multiple CMS reporting periods.

---

## Author

**Richard Torres Romero**  
M.S. Data Analytics (Data Science) Student, Western Governors University  
B.S. Computer Science, University of the People
