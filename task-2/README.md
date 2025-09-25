# Task 2: Vehicle Repair Data Analysis

## Overview

This task involves a comprehensive analysis of a vehicle repair dataset. The goal is to clean the data, identify key insights, generate visualizations, and create tags from free-text fields to summarize the information.

## Files

*   `task2_dataset.xlsx`: The main dataset containing the vehicle repair data.
*   `task2.ipynb`: A Jupyter notebook used for initial data exploration and analysis.
*   `cleaned_tagged_task2_dataset.csv`: The final output file with the cleaned and tagged data.
*   `visualizations.png`: A file containing the visualizations generated during the analysis.
*   `task2_report.md`: A detailed report covering the column analysis, data cleaning summary, visualizations, and key takeaways.
*   `README.md`: This file.

## Solution Approach

1.  **Column-Wise Analysis:** A detailed analysis of each of the 52 columns was performed to understand their data type, number of unique values, and potential significance.

2.  **Data Cleaning:**
    *   The `CAMPAIGN_NBR` column was dropped due to 100% missing values.
    *   Missing values in other columns were handled through imputation (using the mean for numerical columns and "Unknown" for categorical columns).
    *   All categorical columns were converted to lowercase to ensure consistency.

3.  **Critical Columns and Visualization:**
    *   The top 5 critical columns were identified as `CAUSAL_PART_NM`, `PLATFORM`, `BODY_STYLE`, `TOTALCOST`, and the verbatim columns.
    *   Visualizations were generated for the top 10 causal parts, platform distribution, and total cost distribution to provide a clear visual representation of the key insights.

4.  **Tag Generation:**
    *   Meaningful tags were generated from the `CUSTOMER_VERBATIM` and `CORRECTION_VERBATIM` columns to summarize the complaints and corrections. These tags include `peeling`, `inoperative`, `noise`, `warning_light`, `replacement`, `reprogram`, and `other`.

5.  **Output Generation:**
    *   The cleaned and tagged DataFrame was saved to `cleaned_tagged_task2_dataset.csv`.
    *   A detailed summary report (`task2_report.md`) was created to document the entire analysis process, including the column analysis, data cleaning steps, visualizations, and actionable insights.

## How to Run

The analysis was performed using a Python script.

1.  **Prerequisites:**
    *   Python 3
    *   pandas
    *   numpy
    *   matplotlib
    *   seaborn
    *   openpyxl

2.  **Execution:**
    The analysis can be replicated by running a Python script with the logic described in the `task2_report.md` file. The script reads the `task2_dataset.xlsx` file, performs the analysis, and generates the output files.

## Dependencies

The solution requires the following Python libraries:

*   `pandas`
*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `openpyxl`

These dependencies are listed in the `requirements.txt` file.
