# Neighborhood Safety Index

## Overview
We use external data sources, including [EJScreen](https://www.epa.gov/ejscreen/download-ejscreen-data), [EPA Smart Location](https://www.epa.gov/smartgrowth/smart-location-mapping), [SVI](https://www.atsdr.cdc.gov/place-health/php/svi/svi-data-documentation-download.html), and [ACS datasets](https://www.census.gov/programs-surveys/acs). These sources provide tract-level variables that contribute to the final creation of the Neighborhood Safety Index.

## Data Dictionary

This document provides detailed information about the variables in the dataset, including their names, descriptions, and data sources.

| Variable Name   | Description                          | Data Source  |
|----------------|----------------------------------|-------------|
| ID            | Tract ID for different tracts in PWC | Common key ID |
| PEOPCOLORPCT  | Percentage of people of color      | EJScreen |
| LOWINCPCT     | Percentage of low-income population | EJScreen |
| UNEMPPCT      | Percentage of unemployed individuals | EJScreen |
| DISABILITYPCT | Percentage of persons with disabilities | EJScreen |

## Data Transformation Methods

1) PEOPCOLORPCT


