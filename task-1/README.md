# Task 1: Complaint Data Tagging

## Overview

This task involves tagging free-text complaint data based on a predefined taxonomy. The goal is to categorize the `Complaint`, `Cause`, and `Correction` fields into `Root Cause`, `Symptom Condition`, `Symptom Component`, `Fix Condition`, and `Fix Component`.

## Files

*   `task_dataset.xlsx`: The main dataset containing the complaint data and the taxonomy.
    *   `Task` sheet: Contains the raw complaint data.
    *   `Taxonomy` sheet: Contains the predefined categories for tagging.
*   `task1.ipynb`: A Jupyter notebook used for initial data exploration.
*   `tagged_dataset.csv`: The final output file with the tagged data.
*   `summary_report.txt`: A report explaining the tagging approach and potential insights.
*   `README.md`: This file.

## Solution Approach

1.  **Initial Analysis:** The `task1.ipynb` notebook was used to perform an initial analysis of the dataset. This involved loading the data, examining its structure, and identifying the presence of the `Taxonomy` sheet within the `task_dataset.xlsx` file.

2.  **Data Loading and Cleaning:** The `Task` and `Taxonomy` sheets were loaded into separate pandas DataFrames. A data quality issue was identified in the `Taxonomy` sheet where the 'Symptom Condition' column had a trailing space. This was corrected before proceeding.

3.  **Taxonomy Mapping:** To facilitate the tagging process, dictionaries were created from the `Taxonomy` DataFrame. These dictionaries mapped the predefined categories for each of the five target fields.

4.  **Tagging Logic:** A Python script was developed to implement the tagging logic. This script defines a set of functions, one for each target field. These functions iterate through the free-text columns (`Complaint`, `Cause`, `Correction`), search for keywords from the taxonomy dictionaries, and apply the corresponding tags.

5.  **Output Generation:** The tagging script was executed to process the entire dataset. The resulting DataFrame, with the newly added tags, was saved as `tagged_dataset.csv`. A summary report (`summary_report.txt`) was also generated to document the process and potential insights.

## How to Run

The solution is implemented as a Python script that can be executed from the command line.

1.  **Prerequisites:**
    *   Python 3
    *   pandas
    *   openpyxl

2.  **Execution:**
    The tagging process can be replicated by running a Python script with the logic described above. The script reads the `task_dataset.xlsx` file, performs the tagging, and generates the `tagged_dataset.csv` file.

## Dependencies

The solution requires the following Python libraries:

*   `pandas`
*   `numpy`
*   `openpyxl`

These dependencies are listed in the `requirements.txt` file.
