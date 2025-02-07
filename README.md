# Neighborhood Safety Index

## Overview
We use external data sources, including [EJScreen](https://www.epa.gov/ejscreen/download-ejscreen-data), [EPA Smart Location](https://www.epa.gov/smartgrowth/smart-location-mapping), [SVI](https://www.atsdr.cdc.gov/place-health/php/svi/svi-data-documentation-download.html), and [ACS datasets](https://www.census.gov/programs-surveys/acs). These sources provide tract-level and block-level variables that contribute to the final creation of the Neighborhood Safety Index. We selected variables that would be relevant, and we cleaned and transformed the data to ensure its quality.

## Data Dictionary

This document provides detailed information about the variables in the `Clean_df_safetyindex.csv` dataset, including their names, descriptions, data sources, scales, and missing values. The dataset includes **93** unique tract IDs.

| Variable Name   | Description                          | Data Source  | Scale | Missing Values |
|----------------|----------------------------------|-------------|-------------|-------------|
| ID            | Tract ID for different tracts in PWC | Common key ID | 93 individual IDs | 0 |
| PEOPCOLORPCT  | Percentage of people of color      | EJScreen | 0-1, 1:100% | 0 |
| LOWINCPCT     | Percentage of low-income population | EJScreen | 0-1, 1:100% | 0 |
| UNEMPPCT      | Percentage of unemployed individuals | EJScreen | 0-1, 1:100% | 0 |
| DISABILITYPCT | Percentage of persons with disabilities | EJScreen | 0-1, 1:100% | 0 |
| LINGISOPCT    | Percentage of persons in limited English-speaking households | EJScreen | 0-1, 1:100% | 0 |
| LESSHSPCT     | Percentage of population with less than a high school education | EJScreen | 0-1, 1:100% | 0 |
| UNDER5PCT     | Percentage of population under age 5 | EJScreen | 0-1, 1:100% | 0 |
| OVER64PCT     | Percentage of population over age 64 | EJScreen | 0-1, 1:100% | 0 |
| LIFEEXPPCT    | Percentage of low life expectancy | EJScreen | 0-1, 1:100% | 16 |
| PRE1960PCT    | Percentage of housing units built before 1960 | EJScreen | 0-1, 1:100% | 0 |
| PM25          | Particulate Matter 2.5 | EJScreen | 6.94-7.34 | 0 |
| OZONE         | Ozone levels | EJScreen | 53.01-56.03 | 0 |
| DSLPM         | Diesel particulate matter | EJScreen | 0.09-0.25 | 0 |
| RSEI_AIR      | Toxic releases to air | EJScreen | 4.43-614 | 0 |
| PTRAF         | Traffic proximity | EJScreen | 10000-100000 | 0 |
| PTSDF         | Hazardous waste proximity | EJScreen | 0-1.76 | 0 |
| UST           | Underground storage tanks | EJScreen | 0-7.35 | 0 |
| PWDIS         | Wastewater discharge | EJScreen | 22-27419 | 0 |
| NO2           | Nitrogen Dioxide (NO2) levels | EJScreen | 2.25-8.39 | 0 |
| DWATER        | Drinking water non-compliance | EJScreen | All the same, 0 | 3 |
| PNPL          | Superfund site proximity | EJScreen | 0-11.2 | 0 |
| PRMP          | RMP facility proximity | EJScreen | 0-1.21 | 0 |
| E_TOTPOP                 | Population estimate (2018-2022)                                                                | SVI                      | 0-9046            | 0                   |
| E_HU                     | Housing unit estimate (2018-2022)                                                              | SVI                      | 0-3015            | 0                   |
| E_HH                     | Household estimate (2018-2022)                                                               | SVI                      | 0-2931            | 0                   |
| E_POV150_P               | Percentage of population below 150% of the poverty line                                         | SVI (ACS Poverty)        | 0-1, 1:100%       | 1 (tract 9801)      |
| E_UNINSUR_P              | Percentage of uninsured population in total civilian non-institutionalized population (2018-2022) | SVI (ACS Uninsured)      | 0-1, 1:100%       | 1 (tract 9801)      |
| E_HBURD_P                | Percentage of housing cost-burdened households with income <$75,000                              | SVI (ACS Housing Cost)   | 0-1, 1:100%       | 1 (tract 9801)      |
| E_SNGPNT_P               | Percentage of single-parent households with children under 18                                     | SVI                      | 0-1, 1:100%       | 1 (tract 9801)      |
| E_MUNIT_P                | Percentage of housing in structures with 10+ units                                               | SVI                      | 0-1, 1:100%       | 1 (tract 9801)      |
| E_MOBILE_P               | Percentage of mobile homes                                                                        | SVI                      | 0-1, 1:100%       | 1 (tract 9801)      |
| E_CROWD_P                | Percentage of overcrowded households                                                             | SVI                      | 0-1, 1:100%       | 1 (tract 9801)      |
| E_NOVEH_P                | Percentage of households with no vehicle available                                               | SVI                      | 0-1, 1:100%       | 1 (tract 9801)      |
| E_GROUPQ_P               | Percentage of persons living in group quarters                                                   | SVI                      | 0-1, 1:100%       | 1 (tract 9801)      |
| SVI_statewide            | Statewide SVI score                                                                              | SVI                      | 0-1, 1:Most vulnerable | 1 (tract 9801)   |
| House_Vacant_P           | Percentage of vacant housing units                                                               | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| With_Medicaid_P          | Percentage of population covered by Medicaid                                                     | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Work_Drivealone_P        | Percentage of people driving alone to work                                                       | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Work_Carpooled_P         | Percentage of people carpooling to work                                                          | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Work_PublicTransportation_P | Percentage of people using public transportation to work                                       | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Work_Walk_P              | Percentage of people walking to work                                                             | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Work_Taximotorbike_P     | Percentage of people using taxi, motorbike, or bicycle to work                                   | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Work_Fromhome_P          | Percentage of people working from home                                                          | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| With_PublicAssIncome_P   | Percentage of population receiving public assistance or SNAP                                     | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| With_SSI_P               | Percentage of population receiving Supplemental Security Income (SSI)                            | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Mean_Transportation_time(min) | Average time to commute to work (in minutes)                                               | ACS                      | 0-100 (max: 100)  | 1 (tract 9801)      |
| Mean_Proportion_HHIncome | Average proportion of household income spent on housing costs                                    | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |
| Owner_occupied_P         | Percentage of population in owner-occupied housing units                                         | ACS                      | 0-1, 1:100%       | 1 (tract 9801)      |


This document provides detailed information about the variables in the `df_EPA_TBD.csv` dataset, including their names, descriptions, data source, scale and missing values. There are all from block-level dataset (EPA Smart Location) and contains **83** unique tract id finally.

Ac_Total	Total geometric area (acres) of the CBG	Sum from block level	224-21000	0
Ac_Water	Total water area (acres)	Sum from block level	0-1882	0
Ac_Land	Total land area (acres)	Sum from block level	224-21000	0
Ac_Unpr	Total land area (acres) that is not protected from development (i.e., not a park, natural area or conservation area)	Sum from block level	224-19400	0
D1A	Gross residential density (HU/acre) on unprotected land	Sum from block level	0-28	0
D1B	Gross population density (people/acre) on unprotected land	Sum from block level	0-79	0
D1C	Gross employment density (jobs/acre) on unprotected land	Sum from block level	0-22	0
D1D	Gross activity density (employment + Hus) on unprotected land	Sum from block level	0-44	0
D2A_JPHH	Jobs per household	Average from block level	0-9	0
D3A	Total road network density	Sum from block level	2-105	0
D3B	Street intersection density (weighted, auto-oriented intersections eliminated)	Sum from block level	2-397	0
D4A	Distance from the population-weighted centroid to nearest transit stop (meters)	Average from block level	84-1136	34
D4C	Aggregate frequency of transit service within 0.25 miles of CBG boundary per hour during evening peak period	Average from block level	0-18	15
D4D	Aggregate frequency of transit service [D4C] per square mile	Average from block level	0-51	15
D4E	Aggregate frequency of transit service [D4C] per capita	Average from block level	0.0001-0.007	15
NatWalkInd	Walkability Index	Average from block level	4-17;	0

## Data Transformation Methods

1) PEOPCOLORPCT


