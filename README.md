# COVID-19 Data Analysis

This project looks at how COVID-19 spread around the world between 22 January and 27 July 2020. I wanted to understand how cases, deaths and recoveries changed over time, which countries were hit hardest and how the WHO regions compared.

## Data

I used two files from the COVID-19 dataset on Kaggle:

**day_wise.csv** has global totals for each day (188 rows).

**full_grouped.csv** has daily numbers for each country (35,156 rows, 187 countries).

## Data cleaning

The data was already in good shape, so I kept the cleaning light and printed every change it made. I checked for blank text, bad dates and numbers, missing values and exact duplicates, and found none.

One row for Liechtenstein had more recoveries than confirmed cases. I filled it with the previous day's value and capped it so active cases could not go below zero. Negative daily values were left in because they are reporting corrections. No rows were removed.

## What I looked at

1. Global totals and the latest death and recovery rates
2. Peak days for new cases, deaths and recoveries
3. Daily case trend with a 7 day average
4. Top 10 countries by confirmed cases and by deaths
5. Confirmed cases and deaths by WHO region

## Key findings

By 27 July 2020 there were about 16.5 million confirmed cases and 654,036 deaths worldwide. The death rate was 3.97% and the recovery rate was 57.45%.

Daily cases were still rising at the end of the period, with the highest day on 23 July (282,756 new cases).

The US, Brazil and India had the most confirmed cases. Italy, France and Spain were in the top 10 for deaths but not for cases.

The Americas had more confirmed cases than any other WHO region, with about 8.84 million.

## Tools

Python, pandas, NumPy and Matplotlib, run in a Kaggle notebook.

## How to run

Open the notebook on Kaggle with the dataset attached and run all cells. To run it locally, download the two CSV files and change the `path` variable in the first code cell to point to their folder.
