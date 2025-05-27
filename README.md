# Neighborhood Safety Index

## Overview
We use external data sources, including [EJScreen](https://www.epa.gov/ejscreen/download-ejscreen-data), [EPA Smart Location](https://www.epa.gov/smartgrowth/smart-location-mapping), [SVI](https://www.atsdr.cdc.gov/place-health/php/svi/svi-data-documentation-download.html), and [ACS datasets](https://www.census.gov/programs-surveys/acs). These sources provide tract-level and block-level variables that contribute to the final creation of the Neighborhood Safety Index. We selected variables that would be relevant, and we cleaned and transformed the data to ensure its quality.

## Data Dictionary

This document provides detailed information about the variables in the `NSI_0424.csv` dataset, including their names, descriptions, data sources, scales, and missing values. The dataset includes **92** unique Census tract IDs. We excluded 9801 since there are no residences in that tract.

| Variable Name                   | Description                                                   | Data Source          | Category               |
|---------------------------------|---------------------------------------------------------------|----------------------|------------------------|
| total_population                   | Total Population                       | ACS                  | Demographics           |
| DISABILITYPCT                   | Percentage of persons with disabilities                       | ACS                  | Demographics           |
| UNDER5PCT                       | Percentage of population under age 5                          | ACS                  | Demographics           |
| OVER64PCT                       | Percentage of population over age 64                          | ACS                  | Demographics           |
| E_SNGPNT_P                      | Percentage of single-parent households with children under 18 | ACS                  | Demographics           |
| E_GROUPQ_P                      | Percentage of persons living in group quarters                | ACS                  | Demographics           |
| Total_Population                | Total Population                                              | ACS                  | Demographics           |
| Median_Age                      | Median Age                                                    | ACS                  | Demographics           |
| Age_Dependency_Ratio            | Ratio of dependents (under 18 or over 64) to working-age pop. | ACS                  | Demographics           |
| Old-age_Dependency_Ratio        | Ratio of persons over 64 to working-age pop.                  | ACS                  | Demographics           |
| Child_Dependency_Ratio          | Ratio of persons under 18 to working-age pop.                 | ACS                  | Demographics           |
| Prop_Race_Color                 | Percentage of people of color (non-white)                     | ACS                  | Demographics           |
| Sex_Ratio(males per 100 females)| Ratio of males per 100 females                                | ACS                  | Demographics           |
| percent_food_insecure                       | Percentage of people with food insecurity                         | ACS                  | Socioeconomic          |
| LOWINCPCT                       | Percentage of people with low income                          | ACS                  | Socioeconomic          |
| UNEMPPCT                        | Percentage of unemployed people                               | ACS                  | Socioeconomic          |
| LINGISOPCT                      | Percentage of population with limited English proficiency   | ACS                  | Socioeconomic          |
| LESSHSPCT                       | Percentage of population with less than high school education | ACS                  | Socioeconomic          |
| E_POV150_P                      | Percentage of population below 150% of poverty level        | ACS                  | Socioeconomic          |
| With_PublicAssIncome_P          | Percentage of households with public assistance income        | ACS                  | Socioeconomic          |
| With_SSI_P                      | Percentage of households with Supplemental Security Income    | ACS                  | Socioeconomic          |
| E_UNINSUR_P                     | Percentage of uninsured population                            | ACS                  | Socioeconomic          |
| With_Medicaid_P                 | Percentage of population with Medicaid coverage               | ACS                  | Socioeconomic          |
| percent_homeowners                       | Percentage of homeowners                         | ACS                  | Housing          |
| PRE1960PCT                      | Percentage of housing built before 1960                       | ACS                  | Housing                |
| E_HBURD_P                       | Percentage of households with a housing cost burden         | ACS                  | Housing                |
| House_Vacant_P                  | Percentage of vacant housing units                            | ACS                  | Housing                |
| E_MUNIT_P                       | Percentage of multi-unit housing structures                   | ACS                  | Housing                |
| E_MOBILE_P                      | Percentage of mobile homes                                    | ACS                  | Housing                |
| E_CROWD_P                       | Percentage of crowded housing units                           | ACS                  | Housing                |
| Owner_occupied_P                | Percentage of owner-occupied housing units                    | ACS                  | Housing                |
| Mean_Proportion_HHIncome        | Housing cost as a percentage of household income (Mean)       | ACS                  | Housing                |
| PTRAF                           | Traffic Volume                                                | EJScreen         | Mobility         |
| E_NOVEH_P                       | Percentage of households with no vehicle available            | ACS                  | Mobility         |
| Mean_Transportation_time(min)   | Average transportation time in minutes                        | ACS                  | Mobility         |
| Work_Drivealone_P               | Percentage of workers who drive alone                         | ACS                  | Mobility         |
| Work_Carpooled_P                | Percentage of workers who carpooled                           | ACS                  | Mobility         |
| Work_PublicTransportation_P     | Percentage of workers using public transportation           | ACS                  | Mobility         |
| Work_Walk_P                     | Percentage of workers who walk                                | ACS                  | Mobility         |
| Work_Taximotorbike_P            | Percentage of workers using taxi or motorbike                 | ACS                  | Mobility         |
| Work_Fromhome_P                 | Percentage of workers who work from home                      | ACS                  | Mobility         |
| Percent_Fatal_Injury            | Percentage of crashes with fatal injuries                     | VDOT Data           | Transportation Risk  |
| Percent_Severe_Injury           | Percentage of crashes with severe injuries                    | VDOT Data           | Transportation Risk  |
| Percent_Visible_Injury          | Percentage of crashes with visible injuries                   | VDOT Data           | Transportation Risk  |
| Percent_Nonvisible_Injury       | Percentage of crashes with non-visible injuries               | VDOT Data           | Transportation Risk  |
| Avg_Kill_Person                 | Average number of persons killed per crash                    | VDOT Data           | Transportation Risk  |
| Avg_Kill_Pedestrian             | Average number of pedestrians killed per crash                | VDOT Data           | Transportation Risk  |
| Avg_Injured_Person              | Average number of persons injured per crash                   | VDOT Data           | Transportation Risk  |
| Avg_Injured_Pedestrian          | Average number of pedestrians injured per crash               | VDOT Data           | Transportation Risk  |
| Percent_Alcohol_Related         | Percentage of crashes related to alcohol                    | VDOT Data           | Transportation Risk  |
| Percent_Distracted_Related      | Percentage of crashes related to distracted driving         | VDOT Data           | Transportation Risk  |
| Percent_Drowsy_Related          | Percentage of crashes related to drowsy driving             | VDOT Data           | Transportation Risk  |
| Percent_Drug_Related            | Percentage of crashes related to drug use                     | VDOT Data           | Transportation Risk  |
| Percent_Speed_Related           | Percentage of crashes related to speeding                     | VDOT Data           | Transportation Risk  |
| Percent_Hitrun_Related          | Percentage of hit and run crashes                             | VDOT Data           | Transportation Risk  |
| Percent_Pedestrian_Related      | Percentage of crashes involving pedestrians                   | VDOT Data           | Transportation Risk  |
| Percent_Schoolzone_Related      | Percentage of crashes in school zones                         | VDOT Data           | Transportation Risk  |
| Percent_Lgtruck_Related         | Percentage of crashes involving large trucks                  | VDOT Data           | Transportation Risk  |
| Percent_Young_Related           | Percentage of crashes involving young drivers                 | VDOT Data           | Transportation Risk  |
| Percent_Senior_Related          | Percentage of crashes involving senior drivers                | VDOT Data           | Transportation Risk  |
| Percent_Bike_Related            | Percentage of crashes involving bicycles                      | VDOT Data           | Transportation Risk  |
| Percent_Night_Related           | Percentage of crashes occurring at night                      | VDOT Data           | Transportation Risk  |
| Percent_Workzone_Related        | Percentage of crashes in work zones                           | VDOT Data           | Transportation Risk  |
| PM25                            | Fine Particulate Matter (PM2.5) concentration                 | EJScreen Data   | Environmental          |
| OZONE                           | Ozone concentration                                           | EJScreen Data   | Environmental          |
| DSLPM                           | Diesel Particulate Matter concentration                       | EJScreen Data   | Environmental          |
| NO2                             | Nitrogen Dioxide concentration                                | EJScreen Data   | Environmental          |
| RSEI_AIR                        | Risk-Screening Environmental Indicators (RSEI) Air Toxics     | EJScreen Data   | Environmental          |
| PTSDF                           | Number of Treatment, Storage, and Disposal Facilities       | EJScreen Data   | Environmental          |
| UST                             | Number of Underground Storage Tanks                           | EJScreen Data   | Environmental          |
| PWDIS                           | Number of permitted Water Discharge Sites                     | EJScreen Data   | Environmental          |
| PNPL                            | Number of National Priority List (Superfund) Sites            | EJScreen Data   | Environmental          |
| PRMP                            | Number of Risk Management Plan Facilities                     | EJScreen Data   | Environmental          |
| LIFEEXPPCT                      | Life Expectancy                                               | EJScreen Data   | Public Health          |
| EMS_Calls                       | Number of EMS calls                                           | EMS/Fire Data   | Public Health          |
| Fire_Calls                      | Number of Fire calls                                          | EMS/Fire Data   | Public Health          |
| Structure_Fires                 | Number of Structure Fires                                     | EMS/Fire Data   | Public Health          |
| Stroke_Calls                    | Number of Stroke related EMS calls                            | EMS/Fire Data   | Public Health          |
| Cardiac_Calls                   | Number of Cardiac related EMS calls                           | EMS/Fire Data   | Public Health          |
| Diabetic_Calls                  | Number of Diabetic related EMS calls                          | EMS/Fire Data   | Public Health          |
| CPR_Calls                       | Number of CPR related EMS calls                               | EMS/Fire Data   | Public Health          |
| Shootings                       | Number of Shooting incidents                                  | EMS/Fire Data   | Public Health          |
| Stabbings                       | Number of Stabbing incidents                                  | EMS/Fire Data   | Public Health          |
| Opioid_Calls                    | Number of Opioid related calls                                | EMS/Fire Data   | Public Health          |
| Auto_Accidents                  | Number of Auto Accident related calls                         | EMS/Fire Data   | Public Health          |
| High_Volume_Utilizer_Calls      | Number of calls from High-Volume 911 Utilizers              | EMS/Fire Data   | Public Health          |
| Unique_HVU_Callers              | Number of Unique High-Volume 911 Utilizers                  | EMS/Fire Data   | Public Health          |
| Calls_Per_HVU_Caller            | Average calls per High-Volume 911 Utilizer                    | EMS/Fire Data   | Public Health          |
| Domestic    | Number of Domestic Calls  | EMS/Fire Data  | Public Health          |
| Homeless    | Number of Calls related to Homelessness | EMS/Fire Data  | Public Health          |
| SFPC       | Number of Code Violations related to State Fire Protection Code | Internal Agency  | Public Health          |
| VMC    | Number of Code Violations related to Virginia Maintenance Code | Internal Agency  | Public Health          |
| Vegetation Ordinance    | Number of Code Violations related to Vegetation Ordinance  | Internal Agency  | Public Health          |
| Num_School                      | Number of Schools                                             | Local/GIS Data       | Protective Infrastructure       |
| Num_Fire_Station                | Number of Fire Stations                                       | Local/GIS Data       | Protective Infrastructure       |
| Num_Library                     | Number of Libraries                                           | Local/GIS Data       | Protective Infrastructure       |
| Num_Hospital                    | Number of Hospitals                                           | Local/GIS Data       | Protective Infrastructure       |
| Num_UrgentCare                  | Number of Urgent Care centers                                 | Local/GIS Data       | Protective Infrastructure       |
| Num_Worship                     | Number of Places of Worship                                   | Local/GIS Data       | Protective Infrastructure       |
| Num_Shopping_Center             | Number of Shopping Centers                                    | Local/GIS Data       | Protective Infrastructure       |  
|1st Due | 1st Due is the location of each individual fire station and where their apparatus is housed | Local/GIS Data |  Location  | 
|District | District | Local/GIS Data |  Location  | 
|City | City | Local/GIS Data |  Location  | 
|Neighborhood | Neighborhood | Local/GIS Data |  Location  | 


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
