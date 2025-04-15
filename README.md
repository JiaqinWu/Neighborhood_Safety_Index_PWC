# Neighborhood Safety Index

## Overview
We use external data sources, including [EJScreen](https://www.epa.gov/ejscreen/download-ejscreen-data), [EPA Smart Location](https://www.epa.gov/smartgrowth/smart-location-mapping), [SVI](https://www.atsdr.cdc.gov/place-health/php/svi/svi-data-documentation-download.html), and [ACS datasets](https://www.census.gov/programs-surveys/acs). These sources provide tract-level and block-level variables that contribute to the final creation of the Neighborhood Safety Index. We selected variables that would be relevant, and we cleaned and transformed the data to ensure its quality.

## Data Dictionary

This document provides detailed information about the variables in the `Final_df_NSI.csv` dataset, including their names, descriptions, data sources, scales, and missing values. The dataset includes **93** unique tract IDs.

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
| EMS_Calls        | Number of EMS Calls from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Fire_Calls        | Number of Fire Calls from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Structure_Fires     | Number of Calls about Structure Fire from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Stroke_Calls        | Number of Calls about Strokes from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Cardiac_Calls        | Number of Calls about Cardiac Illnesses from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Diabetic_Calls        | Number of Calls about Diabetes from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| CPR_Calls        | Number of Calls about CPR (cardiopulmonary resuscitation) from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Shootings        | Number of Calls about Shootings from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Stabbings        | Number of Calls about Stabbings from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Opioid_Calls        | Number of Calls about Opioid from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Auto_Accidents        | Number of Calls about Auto Accidents from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Total_Calls        | Number of total Calls from 2022 to 2024                                        | Fire&EMS Department                      |        |     |
| Percent_Fatal_Injury        | Percentage of Fatal Injury Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Severe_Injury        | Percentage of Severe Injury Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Visible_Injury        | Percentage of Visible Injury Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Nonvisible_Injury        | Percentage of Nonvisible Injury Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Avg_Kill_Person        | Average Number of Killed Person by Crash Number Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Avg_Kill_Pedestrian        | Average Number of Killed Pedestrian by Crash Number from 2021 to 2024                                        | VDOT                      |        |     |
| Avg_Injured_Person        | Average Number of Injured Person by Crash Number Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Avg_Injured_Pedestrian        | Average Number of Injured Pedestrian by Crash Number Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Workzone_Related        | Percentage of Work Zone-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Schoolzone_Related        | Percentage of School Zone-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Alcohol_Related        | Percentage of Alcohol-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Animal_Related        | Percentage of Animal-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Unrestrained_Related        | Percentage of Unrestrained-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Bike_Related        | Percentage of Bike-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Distracted_Related        | Percentage of Distracted-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Drowsy_Related        | Percentage of Drowsy-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Drug_Related        | Percentage of Drug-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Guardrail_Related        | Percentage of Guardrail-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Hitrun_Related        | Percentage of Hitrun-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Lgtruck_Related        | Percentage of Large Truck-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Motorcycle_Related        | Percentage of Motorcycle-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Pedestrian_Related        | Percentage of Pedestrian-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Speed_Related        | Percentage of Speed-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Senior_Related        | Percentage of Senior People-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Young_Related        | Percentage of Young People-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Mainline_Related        | Percentage of Main Line-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Night_Related        | Percentage of Night-related Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Percent_Urban_Crash        | Percentage of Urban Crashs Happened from 2021 to 2024                                        | VDOT                      |        |     |
| Total_Population        | Total Population                        | ACS                      |        |     |
| Median_Age        | Median Age                        | ACS                      |        |     |
| Sex_Ratio(males per 100 females)        | Sex Ratio(males per 100 females)                        | ACS                      |        |     |
| Age_Dependency_Ratio        | Age Dependency Ratio                        | ACS                      |        |     |
| Old-age_Dependency_Ratio        | Old-age Dependency Ratio                        | ACS                      |        |     |
| Child_Dependency_Ratio        | Child Dependency Ratio                        | ACS                      |        |     |
| Num_School        | Number of Schools                        | Virginia Open Data Portal                      |        |     |
| Num_Fire_Station        | Number of Fire Stations                  | Virginia Open Data Portal                        |        |     |
| Num_Library        | Number of Libraries                        | Virginia Open Data Portal                      |        |     |
| Num_Hospital        | Number of Hospitals                        | Virginia Open Data Portal                      |        |     |
| Num_Worship        | Number of Places of Worship                        | Virginia Open Data Portal                      |        |     |
| Num_Shopping_Center        | Number of Shopping Centers                        | Virginia Open Data Portal                      |        |     |
| Prop_Hisp        | Proportion of Hispanic or Latino                        | ACS                      |        |     |
| Prop_White        | Proportion of White Alone                        | ACS                      |        |     |
| Prop_Black        | Proportion of Black or African American alone                        | ACS                      |        |     |
| Prop_American_Native        | Proportion of American Indian and Alaska Native alone                       | ACS                      |        |     |
| Prop_Asian        | Proportion of Asian alone                       | ACS                      |        |     |
| Prop_Hawaiian        | Proportion of Native Hawaiian and Other Pacific Islander alone                      | ACS                      |        |     |
| Prop_Onemorerace        | Proportion of People with More than One Race                        | ACS                      |        |     |


This document provides detailed information about the variables in the `df_EPA_TBD.csv` dataset, including their names, descriptions, data sources, scales, and missing values. These variables are derived from block-level datasets (EPA Smart Location) and include **83** unique tract IDs.

| **Variable Name** | **Description**                                                                                     | **Data Source**            | **Scale**         | **Missing Values** |
|-------------------|-----------------------------------------------------------------------------------------------------|----------------------------|-------------------|---------------------|
| Ac_Total          | Total geometric area (acres) of the CBG                                                            | Sum from block level (EPA Smart Location) | 224-21000       | 0                   |
| Ac_Water          | Total water area (acres)                                                                           | Sum from block level (EPA Smart Location) | 0-1882          | 0                   |
| Ac_Land           | Total land area (acres)                                                                            | Sum from block level (EPA Smart Location) | 224-21000       | 0                   |
| Ac_Unpr           | Total land area (acres) not protected from development (e.g., parks, natural areas)                | Sum from block level (EPA Smart Location) | 224-19400       | 0                   |
| D1A               | Gross residential density (housing units/acre) on unprotected land                                 | Sum from block level (EPA Smart Location) | 0-28            | 0                   |
| D1B               | Gross population density (people/acre) on unprotected land                                         | Sum from block level (EPA Smart Location) | 0-79            | 0                   |
| D1C               | Gross employment density (jobs/acre) on unprotected land                                           | Sum from block level (EPA Smart Location) | 0-22            | 0                   |
| D1D               | Gross activity density (employment + housing units/acre) on unprotected land                       | Sum from block level (EPA Smart Location) | 0-44            | 0                   |
| D2A_JPHH          | Jobs per household                                                                                 | Average from block level (EPA Smart Location) | 0-9         | 0                   |
| D3A               | Total road network density                                                                         | Sum from block level (EPA Smart Location) | 2-105           | 0                   |
| D3B               | Street intersection density (weighted, excluding auto-oriented intersections)                      | Sum from block level (EPA Smart Location) | 2-397           | 0                   |
| D4A               | Distance from population-weighted centroid to nearest transit stop (meters)                        | Average from block level (EPA Smart Location) | 84-1136      | 34                  |
| D4C               | Aggregate frequency of transit service within 0.25 miles of CBG boundary per hour during peak time | Average from block level (EPA Smart Location) | 0-18         | 15                  |
| D4D               | Aggregate frequency of transit service per square mile                                             | Average from block level (EPA Smart Location) | 0-51         | 15                  |
| D4E               | Aggregate frequency of transit service per capita                                                  | Average from block level (EPA Smart Location) | 0.0001-0.007  | 15                  |
| NatWalkInd        | Walkability Index                                                                                  | Average from block level (EPA Smart Location) | 4-17          | 0                   |


## Data Transformation Methods

1. **E_UNINSUR_P**

   The SVI dataset contains two variables: `E_UNINSUR` (total number of uninsured individuals) and `E_TOTPOP` (total civilian noninstitutionalized population). To calculate the percentage of uninsured individuals, the formula **E_UNINSUR / E_TOTPOP** is applied.

2. **E_HBURD_P**

   The SVI dataset contains two variables: `E_HBURD` (housing cost-burdened occupied housing units with annual income less than $75,000) and `E_HH` (total number of households). The percentage of housing cost-burdened units is calculated using the formula **E_HBURD / E_HH**.

3. **E_SNGPNT_P**

   To calculate the percentage of single-parent households with children under 18, the formula **E_SNGPNT / E_HH** is used. Here, `E_SNGPNT` represents the number of single-parent households, and `E_HH` is the total number of households.

4. **E_MUNIT_P**

   The percentage of housing in structures with 10 or more units is derived using **E_MUNIT / E_HU**, where `E_MUNIT` represents the number of multi-unit housing structures, and `E_HU` is the total number of housing units.

5. **E_MOBILE_P**

   To compute the percentage of mobile homes, the formula **E_MOBILE / E_HU** is applied. Here, `E_MOBILE` is the number of mobile homes, and `E_HU` is the total number of housing units.

6. **E_CROWD_P**

   The percentage of overcrowded households is calculated as **E_CROWD / E_HH**, where `E_CROWD` represents households with more people than rooms, and `E_HH` is the total number of households.

7. **E_NOVEH_P**

   The percentage of households without vehicle availability is determined using **E_NOVEH / E_HH**, where `E_NOVEH` is the number of households without vehicles, and `E_HH` is the total number of households.

8. **E_GROUPQ_P**

   The percentage of individuals living in group quarters is computed as **E_GROUPQ / E_TOTPOP**, where `E_GROUPQ` represents the number of individuals in group quarters, and `E_TOTPOP` is the total population.

9. **With_Medicaid_P**

   The percentage of individuals covered by Medicaid is calculated as **Medicaid / Total Population**, using data from ACS datasets.

10. **Work_Drivealone_P**

    The percentage of individuals driving alone to work is derived as **Drive Alone / Total Workers**, using data from ACS "Mode of Transportation to Work".

11. **Work_Carpooled_P**

    The percentage of individuals carpooling to work is computed as **Carpooled / Total Workers**, using data from ACS "Mode of Transportation to Work".

12. **Work_PublicTransportation_P**

    To determine the percentage of individuals taking public transportation to work, the formula **Public Transportation / Total Workers** is used, sourced from ACS datasets.

13. **Work_Walk_P**

    The percentage of individuals walking to work is derived as **Walk / Total Workers**, sourced from ACS "Mode of Transportation to Work".

14. **Work_Taximotorbike_P**

    The percentage of individuals using taxi, motorbike, or bicycle to work is calculated as **Taxi, Motorbike, or Bicycle / Total Workers**, using ACS datasets.

15. **Work_Fromhome_P**

    The percentage of individuals working from home is computed as **Work from Home / Total Workers**, sourced from ACS datasets.

16. **With_PublicAssIncome_P**

    The percentage of individuals receiving public assistance or SNAP benefits is derived as **Public Assistance Income / Total Population**, sourced from ACS "SNAP".

17. **With_SSI_P**

    The percentage of individuals receiving Supplemental Security Income (SSI) is calculated as **SSI / Total Population**, using data from ACS datasets.

18. **Mean_Transportation_time(min)**

    The average commute time is calculated using the mean values for each time period band in ACS "Travel Time to Work". For example, a band of 20-24 minutes is approximated as **(20 + 24) / 2 = 22.5** minutes. For the maximum band (>90 minutes), a value of 100 is used for estimation.

19. **Mean_Proportion_HHIncome**

    The average proportion of household income spent on housing costs is derived by calculating the midpoint for each percentage band in ACS "Housing Costs". For example, a band of 10-14.9% is approximated as **(10 + 14.9) / 2 = 12.45%**. For the highest band (>50%), 60% is used for estimation.

20. **Owner_occupied_P**

    The percentage of housing units that are owner-occupied is calculated as **Owner-Occupied / Total Housing Units**, sourced from ACS "B25008".

21. **Ac_Total**

    The total geometric area of the CBG is obtained by summing block-level data.

22. **Ac_Water**

    The total water area of the CBG is calculated by summing block-level data.

23. **Ac_Land**

    The total land area of the CBG is computed by summing block-level data.

24. **Ac_Unpr**

    The total land area of the CBG not protected from development is determined by summing block-level data.

25. **D1A**

    Gross residential density (housing units per acre) on unprotected land is calculated by summing block-level data.

26. **D1B**

    Gross population density (people per acre) on unprotected land is calculated by summing block-level data.

27. **D1C**

    Gross employment density (jobs per acre) on unprotected land is calculated by summing block-level data.

28. **D1D**

    Gross activity density (employment plus housing units per acre) on unprotected land is calculated by summing block-level data.

29. **D2A_JPHH**

    Jobs per household is calculated as the average from block-level data.

30. **D3A**

    Total road network density is computed by summing block-level data.

31. **D3B**

    Street intersection density (weighted, excluding auto-oriented intersections) is calculated by summing block-level data.

32. **D4A**

    The distance from the population-weighted centroid to the nearest transit stop is averaged from block-level data.

33. **D4C**

    Aggregate frequency of transit service within 0.25 miles of the CBG boundary per hour during peak time is averaged from block-level data.

34. **D4D**

    Aggregate frequency of transit service per square mile is averaged from block-level data.

35. **D4E**

    Aggregate frequency of transit service per capita is averaged from block-level data.

36. **NatWalkInd**

    Walkability Index is calculated as the average from block-level data.
