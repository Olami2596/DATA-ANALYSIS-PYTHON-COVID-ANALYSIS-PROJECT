# COVID-19 Data Exploration and Visualization

## Overview
This project involves the exploration and visualization of COVID-19 data, specifically focusing on confirmed cases, confirmed deaths, and stringency index measures. The data has been sourced and processed to understand the trends and patterns during the global health crisis.

## Data Extraction
- The data was extracted from 'https://covidtrackerapi.bsg.ox.ac.uk/api/v2/stringency/date-range/2020-01-22/2020-05-10' using Requests libraries.
- Information below was collected:
- Confirmed Cases: The cumulative number of confirmed COVID-19 cases recorded daily.
- Stringency Index: A measure reflecting the strictness of government policies.
- Confirmed Deaths: The cumulative number of confirmed deaths due to COVID-19 recorded daily.

## Data Wrangling
- The extracted data was cleaned and formatted for analysis.
- The missing data for each measure was identified using the code `df_confirmed_cases.eq(0).sum()`, `df_confirmed_deaths.eq(0).sum()`, and `df_stringency_index.eq(0).sum()`.
- Given that the confirmed cases and deaths are cumulative records, manipulating the data by dropping or replacing them with statistical measures such as mean, mode, or median would lead to inaccurate representations. Therefore, no such manipulations were performed to maintain the integrity of the data.

## Data Visualization – Reproduction & Discussion
1. **Analysis of Log-Scale Graph:**
  - A Log-Scale Graph was used because using log-scale graphs is beneficial for analyzing growth rates, especially in the context of a global health crisis:
  - Relative Change: The slope indicates relative changes, aiding in assessing growth rates accurately.
  - Distribution of Extreme Values: Extreme values are distributed towards the middle, which is useful for significant changes.
  - Modeling Exponential Processes: Suitable for representing exponential growth processes.

2. **Analysis of Line Plots:**
  - A line plot was used to display time series data effectively and the following observations were made:
  - United States: Experienced a steady rise in confirmed cases, maintaining this trend over time.
  - France: Experienced a significant drop followed by a sharp increase in a short period.
  - United Kingdom and Italy: Saw a slight and consistent increase in confirmed cases.
  - Spain: Experienced a slight increase, followed by a significant decrease, which was later corrected.
