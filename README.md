# Gemini CLI Tasks

## Overview

This repository contains the solutions for two data analysis tasks performed using the Gemini CLI.

## Folder Structure

*   `task-1/`: Contains the solution for the Complaint Data Tagging task.
*   `task-2/`: Contains the solution for the Vehicle Repair Data Analysis task.
*   `requirements.txt`: A file listing the Python dependencies for both tasks.

---

## Task 1: Complaint Data Tagging

### Overview

This task involves tagging free-text complaint data based on a predefined taxonomy. The goal is to categorize the `Complaint`, `Cause`, and `Correction` fields into `Root Cause`, `Symptom Condition`, `Symptom Component`, `Fix Condition`, and `Fix Component`.

### Solution Approach

1.  **Data Exploration:** The `task_dataset.xlsx` file was analyzed to identify the `Task` and `Taxonomy` sheets.
2.  **Data Cleaning:** The `Taxonomy` sheet was cleaned to correct inconsistencies in column names.
3.  **Tagging:** A Python script was used to read the `Task` and `Taxonomy` sheets, create mapping dictionaries, and apply tags to the free-text data based on keyword matching.
4.  **Output:** The tagged dataset was saved as `tagged_dataset.csv`, and a summary report was generated.

### Files

*   `task-1/task_dataset.xlsx`: The main dataset.
*   `task-1/tagged_dataset.csv`: The final tagged dataset.
*   `task-1/summary_report.txt`: A report explaining the tagging approach and insights.
*   `task-1/README.md`: A detailed README for Task 1.

---

## Task 2: Vehicle Repair Data Analysis

### Overview

This task involves a comprehensive analysis of a vehicle repair dataset. The goal is to clean the data, identify key insights, generate visualizations, and create tags from free-text fields to summarize the information.

### Solution Approach

1.  **Column-Wise Analysis:** A detailed analysis of each of the 52 columns was performed to understand their data type, unique values, and significance.
2.  **Data Cleaning:** The `CAMPAIGN_NBR` column was dropped, missing values were imputed, and categorical columns were standardized.
3.  **Visualization:** Visualizations were generated for the top 10 causal parts, platform distribution, and total cost distribution.
4.  **Tag Generation:** Tags were generated from the `CUSTOMER_VERBATIM` and `CORRECTION_VERBATIM` columns to summarize complaints and corrections.
5.  **Output:** The cleaned and tagged dataset was saved as `cleaned_tagged_task2_dataset.csv`, and a detailed report was generated.

### Files

*   `task-2/task2_dataset.xlsx`: The main dataset.
*   `task-2/cleaned_tagged_task2_dataset.csv`: The final cleaned and tagged dataset.
*   `task-2/visualizations.png`: Visualizations of the key insights.
*   `task-2/task2_report.md`: A detailed report of the analysis.
*   `task-2/README.md`: A detailed README for Task 2.

---

## How to Run

Each task folder contains a detailed `README.md` file with instructions on how to replicate the analysis.

## Dependencies

The solution requires the following Python libraries:

*   `pandas`
*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `openpyxl`
*   `nbformat`
*   `nbconvert`

These dependencies are listed in the `requirements.txt` file.
