# HHS-Dataset: COVID-19 Hospital Impact and Capacity Analysis

## Overview
This notebook performs an exploratory data analysis on COVID-19 reported patient impact and hospital capacity data across various states. The primary goal is to analyze and visualize key metrics related to hospital resource utilization and patient admissions, aggregated at the state level.

## Data Source
The data is sourced from the `COVID-19_Reported_Patient_Impact_and_Hospital_Capacity_by_Facility` dataset. It contains information on:
- Inpatient bed usage
- Adult and pediatric hospital bed occupancy
- ICU bed usage
- COVID-19 patient admissions (adult and pediatric, broken down by age groups for adults)
- Influenza patient admissions

## Analysis Steps
1.  **Data Loading**: Reads the specified columns from the CSV file into a pandas DataFrame.
2.  **Statistical Aggregation**: Calculates the mean, median, minimum, and maximum values for all selected numeric columns, grouped by state. This provides a summary of reporting frequencies for each metric per state.
3.  **Visualization**: 
    -   **Box Plot**: Displays the overall distribution of these aggregated averages across all states, helping to identify general trends and outliers.
    -   **Bar Graphs**: Generates individual bar charts for each metric, showing the average reporting frequency per state, sorted in descending order for easy comparison.

## Key Metrics Analyzed
The analysis focuses on the following key metrics:
-   `inpatient_beds_used_7_day_coverage`
-   `all_adult_hospital_inpatient_bed_occupied_7_day_coverage`
-   `all_pediatric_inpatient_bed_occupied_7_day_coverage`
-   `total_icu_beds_7_day_coverage`
-   `inpatient_beds_used_covid_7_day_coverage`
-   `total_pediatric_patients_hospitalized_confirmed_covid_7_day_coverage`
-   `total_adult_patients_hospitalized_confirmed_covid_7_day_coverage`
-   `total_patients_hospitalized_confirmed_influenza_7_day_coverage`
-   Various `previous_day_admission` metrics for pediatric and adult COVID-19 patients across different age groups.

## How to Use
To run this notebook, ensure you have the required `COVID-19_Reported_Patient_Impact_and_Hospital_Capacity_by_Facility_20250210.csv` file in the `/content/` directory.

The notebook will:
-   Load the data.
-   Compute state-wise statistics.
-   Generate visualizations to illustrate trends in hospital capacity and patient impact.

*Note: An 'Extraneous' section exists which includes code for detailed summary statistics for Michigan (`df_mi`), thoug
