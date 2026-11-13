# Week4
I am learning how to upload changes from RStudio to GitHub.
This change was made on GitHub.


CASA0005 - Week 4 Homework
Author : Natig Hasanli
Purpose : This project examines the change in Gender Inequality Index(GII) between 2010 and 2019. 
It joined UNDP data to world country boundaries using the three letter ISO country codes.

Data Sources

- UNDP Human Development Reports : All Composite indices and component time series (1990 - 2023)
- World Countries Generalized : country boundaries generalized as GeoJSON.

Files
- Week 4 homework.Rmd : analysis code and explanation

- week4data/gender_inequality.csv: UNDP time-series data.

- week4data/world.geojson: world country boundaries.

- casa0005-week4.Rproj: RStudio project file.

How to reproduce the analysis

1. Ib duiaDownload or clone this repository.

2. Open casa0005-week4.Rproj in RStudio.

3. Install the required packages if necessary: sf, tidyverse, janitor, countrycode and rmarkdown.

4. Check that the two input datasets are in the week4data folder. If they are not included, download them from the links above and rename them to match the filenames listed here.

5. Open Week 4 homework.Rmd.

5. Click Knit to run the analysis and generate an HTML report.

Method

The analysis imports and cleans the datasets, converts country names to ISO codes, joins the inequality data to the country boundaries, and calculates:

gii_change = gii_2019 - gii_2010

A negative value indicates a reduction in gender inequality. A positive value indicates an increase. Zero indicates no change.

Missing data and limitations

Some country or territory names were not matched automatically to ISO codes. These remain on the map with missing inequality values pending further checks.

A change cannot be calculated when either year's GII value is missing. Missing values are retained as NA, rather than replaced with zero.

