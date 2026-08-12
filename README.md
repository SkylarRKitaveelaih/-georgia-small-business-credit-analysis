Small Business Credit Access and Business Formation in Georgia

OVERVIEW

In this project, the research question focuses on the correlation between small-business lending from the SBA and entrepreneurship in Georgia counties.

Data from the U.S. Small Business Administration 7(a) Loans and U.S. Census Business Dynamics Statistics (BDS) have been used to create a county-level data panel for the years 2020-2023 and determine whether counties that receive greater amounts of SBA loans relative to their number of businesses enter establishments at a greater rate.

In addition, geographic credit gaps in counties are determined.

RESEARCH QUESTION

Does better access to SBA 7(a) loans result in more new business creation in counties throughout Georgia?

DATA

Analysis uses two public data sets:

* 7(a) Loan Data from U.S. Small Business Administration – Loan size, year of approval, county of borrower, and job creation.
* U.S. Census Bureau Business Dynamics Statistics (BDS) – Number of firms, number of establishments, establishment creation, and entry rate by counties.

Overlapping period for analysis is 2020-2023.

METHODOLOGY

The analyses were conducted using Python with packages such as pandas, NumPy, SciPy, statsmodels, and Matplotlib.

This process included:

1. Data cleaning and filtering of SBA and Census data.
2. Standardization of Georgia counties via five-digit FIPS codes.
3. Aggregation of individual SBA loans to county-year data.
4. Merging SBA loan lending with Census business formation.
5. Creation of normalized credit access variables, which includes number of SBA loans per 1,000 businesses.
6. Pearson correlation test between credit access and establishments.
7. Ordinary Least Squares regression with controls for the year.
8. Robustness tests where extremely small economies and county years with no SBA loans are excluded.
9. Standardization of the credit gap to detect possible geographic mismatch between entrepreneurship and SBA lending.

The main sample size is 620 county-year observations from Georgia.

KEY FINDINGS

Intensities of SBA lending had a positive correlation with firm creation in the main model.

Controlling for the year, an increase in 10 more SBA loans for every 1,000 establishments had an approximate 0.73 percentage point higher probability of firm creation.

The result was statistically significant:

* Coefficient: 0.0731
* p-value: 0.0013
* Observations: 620

The effect did not change much by excluding the county-years that had fewer than 100 firms:

* Coefficient: 0.0719
* p-value: 0.0027
* Observations: 539

On the other hand, the effect was weaker when the sample was narrowed down to only the county-years where there were some SBA loans:

* Coefficient: 0.0473
* p-value: 0.0762
* Observations: 457

It seems that the observed correlation can be partly explained by a different characteristic between those counties that received SBA loans and those that did not.

CREDIT-GAP ANALYSIS

To analyze geographic differences between entrepreneurial activity and SBA lending, I first standardized both establishment entry rates and SBA loan intensity by year and then contrasted the two statistics.

Credit gaps with positive values indicate counties and years in which there was greater establishment creation relative to SBA lending.

This study aims to point out research issues but does not suggest that firms in those counties could not access capital.

LIMITATIONS

These findings are indicative of associations rather than causations. In addition, SBA lending itself might be influenced by the local economic environment, whereas variables like growth in population, income levels, industrial makeup, banking, interest rates, and local policies might affect both lending and entrepreneurship.

SBA 7(a) lending is just one type of small business funding and thus does not represent a comprehensive picture of credit availability.

There are also peculiarities of the economic environment during the 2020-2023 period that should be taken into account.

TOOLS

Python · pandas · NumPy · SciPy · statsmodels · Matplotlib · Google Colab

REPOSITORY CONTENTS

* Georgia_Small_Business_Credit_Analysis.ipynb — complete reproducible data-cleaning, analysis, regression, robustness, and visualization workflow.
* README.md — project methodology, findings, and limitations.
