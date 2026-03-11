# BUS32120-Final-Project
Group Members: Wanjia Gao; Xueqi Bai; Tian Zhou
# YouTube Content Strategy Analysis

This project analyzes a category-balanced sample of YouTube videos using both **Python** and **SQL**. The target audience is a **content strategy manager** who wants practical insight into how video category, timing, format, and audience response relate to performance and engagement.

## Project Goal

The main goal of this project is to answer the following question:

**What can a category-balanced YouTube sample tell us about video performance, engagement, and content strategy?**

To support fair cross-category comparison, the final analytical sample was built using **stratified sampling by category** rather than relying only on the naturally imbalanced raw uploads pool.

## Data Sources

This project uses multiple connected datasets collected through the **YouTube Data API**:

- **Video-level dataset** built from public channel uploads playlists
- **Official YouTube category lookup table**
- **Sampled comment-level dataset**, later aggregated to the video level

These data were cleaned, transformed, and stored in both **CSV** and **SQLite** formats so that the Python and SQL sections use the same final analytical tables.

## Methods

The project combines **Python** and **SQL** as required by the course rubric.

### Python work includes:
- data collection and cleaning
- data-quality checks
- exploratory data analysis (EDA)
- feature engineering
- two simple models:
  - linear regression
  - logistic regression

### SQL work includes:
- grouped summaries
- joins
- window functions
- subqueries
- validation and comparison queries relevant to the analysis

## Repository Contents

- `BUS32120_FINAL_Python_SQL_YouTube_SUBMIT.ipynb`  
  Final polished Python notebook with introduction, data preparation, data-quality checks, EDA, modeling, and conclusion.

- `BUS32120_FINAL_SQL_Queries_ONLY_SUBMIT.ipynb`  
  Separate SQL-only notebook containing the required SQL queries with comments explaining what each query does, why it is included, and what the results show in general.

## Main Analytical Features

Some of the key engineered variables include:
- title length
- title word count
- question mark in title
- number in title
- publish hour
- weekday / weekend indicator
- duration bins
- comment-based summary features
- transformed and standardized variables for modeling

## Key Checks Performed

Before EDA and modeling, the project checks:
- missingness
- duplicate video IDs
- impossible negative counts
- missing key fields
- category balance in the final sample

These checks help confirm that the cleaned dataset is suitable for analysis.

## Notes on Reproducibility

The notebook is designed to:
- read the API key securely
- reuse cached CSV files when available
- rebuild project tables from the API when needed

Because API-based collection can vary slightly across reruns, final interpretation should be based on the outputs saved in the submitted notebook.

## Summary

This project is primarily **explanatory and decision-oriented**. It does not claim causal effects, but it uses a structured, category-balanced design to produce practical insights about YouTube content performance.
