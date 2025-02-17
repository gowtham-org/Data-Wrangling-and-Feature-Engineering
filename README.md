# Data Wrangling and Analysis

This document outlines the steps taken during data wrangling and analysis, including the removal of incomplete samples, outlier detection, feature engineering, and correlation analysis.

## 1. Removal of Incomplete Samples
As part of the data wrangling process, all samples with incomplete measurements across the four categories (a, b, c, d) were removed.

- **Action**: Removed samples with missing values.
- **Result**: 4 samples were removed due to missing values.

## 2. Removal of Outlier Samples
Samples with outlier permeability values were identified and removed. The outliers were determined using appropriate statistical methods.

- **Action**: Removed samples with outlier permeability values.
- **Result**: 26 outlier samples in Insitu Klinkenberg Permeability (mD) were removed.

## 3. Feature Engineering
Feature engineering methods were applied to better analyze the data. The following method was found to be effective:

- **Method**: Log transformation
- **Reason**: The data was skewed, and log transformation helped in normalizing the distribution.

## 4. Cross Plots of the First Three Properties
Cross plots were generated for the first three properties to visualize their relationships.

- **Properties**: Sample Depth, Log Permeability, Log Porosity
- **Plot Type**: Scatter Plot

## 5. Correlation Coefficients Before and After Feature Engineering
The correlation coefficients of the first three properties were determined before and after feature engineering to assess the impact of the transformations.

### Before Feature Engineering:
- In situ Klinkenberg Permeability and Routine Porosity: 0.50508
- In situ Klinkenberg Permeability and Sample Depth: -0.12158
- Routine Porosity and Sample Depth: -0.025141

### After Feature Engineering:
- Log Permeability and Log Porosity: 0.762848 (increase from 0.50508)
- Log Permeability and Sample Depth: 0.225107 (increase from -0.12158)
- Log Porosity and Sample Depth: 0.331675 (increase from -0.025141)

## 6. Discussion on Correlation Coefficients
The correlation coefficients were analyzed to determine if they capture the dependencies in the data.

- **Observation**: The feature engineering (log transformation) increased the strength of the correlations among the properties, particularly between Log Permeability and Log Porosity. The negative or weak correlations between Sample Depth and other properties became positive or stronger in magnitude after feature engineering.
- **Conclusion**: Feature engineering, specifically log transformations, had significant effects on the data. It made the relationships between variables more linear and improved the interpretability of the data.

---

This report summarizes the key steps and findings from the data wrangling and analysis process. The feature engineering methods applied have proven to be effective in enhancing the data's quality and interpretability.
