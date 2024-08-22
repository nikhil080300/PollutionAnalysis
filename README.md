# Pollution Analysis

## Overview
This project explores the US Air Pollution dataset for fine particulate matter (PM) at 332 locations. The main focus is on two pollutants: sulfate and nitrate. The analysis includes calculating pollutant means, identifying complete cases, and determining correlations between pollutants.

## Data
The dataset used in this analysis can be downloaded from the following link:

[specdata.zip (2.4MB)](https://d396qusza40orc.cloudfront.net/rprog%2Fdata%2Fspecdata.zip)

The zip file contains 332 CSV files, each corresponding to a specific monitoring location in the United States. Each file contains data on the levels of sulfate and nitrate in the air, as well as the date of observation.

### Relevant Variables
- **Date**: The date of observation in YYYY-MM-DD format.
- **Sulfate**: The level of sulfate PM in the air (measured in micrograms per cubic meter).
- **Nitrate**: The level of nitrate PM in the air (measured in micrograms per cubic meter).

## Functions

### 1. `pollutantmean(directory, pollutant, id = 1:332)`
This function calculates the mean of a specified pollutant (sulfate or nitrate) across a list of monitors. Missing values (coded as `NA`) are ignored.

**Arguments**:
- `directory`: The directory where the CSV files are stored.
- `pollutant`: The pollutant to calculate the mean for (either `"sulfate"` or `"nitrate"`).
- `id`: A vector of monitor ID numbers to include in the analysis (default is `1:332`).

**Example Usage**:
```r
pollutantmean("specdata", "sulfate", 1:10)
