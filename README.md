# U.S. Hospital Quality Analysis

## Project Overview

This project analyzes hospital quality across the United States using publicly available data from the Centers for Medicare & Medicaid Services (CMS). The analysis retrieves the latest hospital information directly from the CMS Provider Data Catalog API, cleans and validates the data using Python and Pandas, performs exploratory analyses, validates key results with SQL using SQLite, and visualizes patterns in hospital quality across states, hospital types, and ownership categories.

---

## Business Question

**How does CMS overall hospital quality vary across U.S. hospitals, states, hospital types, and ownership categories?**

---

## Data Source

**Centers for Medicare & Medicaid Services (CMS)**  
Provider Data Catalog – Hospital General Information

- **Dataset ID:** `xubh-q36u`
- Accessed through the CMS Provider Data Catalog API
- Data retrieved programmatically during notebook execution
- Analysis date recorded within the notebook

---

## Tools

- Python
- Pandas
- Requests
- CMS Provider Data Catalog API
- SQLite
- SQL
- Matplotlib
- Jupyter Notebook
- GitHub Codespaces
- Git & GitHub

---

## Analysis Performed

The notebook includes analyses of:

- National CMS hospital quality ratings
- State-level hospital quality statistics
- Average hospital ratings by state
- Hospital quality by hospital type
- Hospital quality by ownership
- Comparison of individual hospitals to their state averages
- SQL validation of Python analyses
- Cross-validation between Python and SQLite

---

## Data Cleaning & Validation

The dataset was prepared by:

- Retrieving the latest CMS data directly through the API
- Converting Overall Hospital Rating to numeric values
- Handling missing hospital ratings
- Checking duplicate hospital records
- Validating unique facility identifiers
- Confirming appropriate data types
- Excluding missing ratings from statistical analyses
- Applying a minimum threshold of **20 rated hospitals** for state ranking comparisons
- Verifying results using equivalent SQL queries in SQLite

---

## Key Findings

- Colorado had the highest average CMS hospital rating (**3.41**) among states with at least 20 rated hospitals.
- Maryland had the lowest average hospital rating (**2.83**) under the same inclusion criteria.
- Veterans Administration acute-care hospitals achieved substantially higher average ratings than Critical Access and other Acute Care hospitals.
- Most U.S. hospitals clustered below an overall CMS rating of **3.0**, indicating generally moderate performance.
- SQL and Python produced matching results after applying identical filtering and aggregation logic.

---

## Visualizations

The notebook contains visualizations including:

- Distribution of CMS Overall Hospital Ratings
- Average Hospital Rating by State
- Hospital Ratings by Hospital Type
- Hospital Ratings by Ownership
- Additional summary tables supporting the analysis

---

## SQL Validation

SQLite was used to independently validate the Python analysis.

Validation included:

- National hospital rating distribution
- Average hospital ratings by state
- Rated hospital counts
- Cross-check of SQL and Python outputs
- Verification that missing ratings were excluded consistently
- Confirmation that the same minimum sample threshold was applied in both workflows

---

## Limitations

- CMS data are updated periodically, so results may change over time.
- Hospital ratings are unavailable for some facilities and were excluded from rating analyses.
- State averages represent facility-level averages rather than official statewide quality scores.
- Differences may reflect hospital mix, ownership structure, and other factors not modeled in this project.
- States with fewer than 20 rated hospitals were excluded from state ranking comparisons.

---

## How to Reproduce

1. Clone this repository.
2. Open the project in GitHub Codespaces.
3. Install the required Python packages.
4. Open `notebooks/01_hospital_quality_analysis.ipynb`.
5. Run all notebook cells from top to bottom.
6. The notebook automatically downloads the current CMS dataset through the API.
7. Execute the SQL queries to validate the Python results.

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
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Future Improvements

- Incorporate HCAHPS patient experience measures.
- Analyze CMS outcome and timely/effective care metrics.
- Develop an interactive dashboard using Plotly or Tableau.
- Build predictive models to identify factors associated with higher hospital quality ratings.
- Expand the analysis to evaluate trends across multiple CMS reporting periods.

---

## Author

**Richard Torres Romero**

- M.S. Data Analytics (Data Science) Student, Western Governors University
- B.S. Computer Science, University of the People

---

## License

This project is intended for educational and portfolio purposes using publicly available CMS data.
