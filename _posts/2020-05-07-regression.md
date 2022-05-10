---
layout: post
title: Ridership Regression Model
subtitle: The combined influence of crime on transit ridership at the stop level
cover-img: /assets/img/bart_station_photo.jpg
thumbnail-img: /assets/img/bart_station_photo_b.jpg
<!-- share-img: /assets/img/path.jpg -->
tags: [books, test]
---

Using ridership data collected from BART stations (2018-2021) we used a negative binomial regression model to understand the influence of crime on transit ridership at the stop level. We used the number of entries from 8 stations as a dependent variable for the regression analysis. Independent variables included: number of crime incidents around stations, rate of new COVID-19 cases and socio-demographics (race, gender, income). 

### Data Collection
* Police Department Incident reports were gathered from San Francisco Open Data portal, from 2018 to 2021, the dataset included incident reports filed to the San Francisco Police Department online report system. 
* Monthly ridership reports were collected from the BART official portal. Only entries from 2018 to 2021 to each station were taken into account for the modeling
*  Datasets for income, gender, race and ethnicity were taken from the US Census Bureau official site at census tract neighborhood level
* Impacts of the COVID-19 pandemic were included through number of new cases reported on San Francisco’s Open Data portal

### Spatial Resolution
An area division of San Francisco using Voronoi diagrams (Thiessen polygons) was used to determine the area of influence of BART stations. An additional buffer area of 800m around stations was created as direct catchment area. Crime, income and demographic data were attachet to a station if they fell within it's buffer. For overlapping buffers, the Voronoi polygons were used as delimitants. (_Thiessen polygons were made with QGIS but the buffers and the data join in Python_)

<p align="center">
  <img src="../assets/img/Buffer_Thiessen.png" width="550"/>
</p>
<!-- ![Buffers](../assets/img/Buffer_Thiessen.png) -->

### Exploratory Data Analysis
A correlation matrix between all available variables collected allows shows there is a strong positive correlation between number of crimes and entries to BART stations. 

<!-- ![Buffers](../assets/img/Correlation matrix.png) -->
<p align="center">
  <img src="../assets/img/Correlation matrix.png" align="center" width="550"/>
</p>

Another finding of the exploration relates to the trend of number of entries and number of crime incidents over the years 2018 to 2021. Crimes around stations from 2020 to 2021 showed a significant increase opposed to the number of entries for that same period. Although there is a positive correlation between entry and crime around BART stations, further exploration of the possible causes for this increase in crime is necessary.

<p align="center">
  <img src="../assets/img/Entries&Crimes.png" align="center" width="550"/>
</p>

### Model & Results
Time associated dummy variables were created for important events that could impact the number of passengers riding BART (holiday months, the 2020 California wildfires, pre-COVID months, peak waves of the COVID pandemic, etc.) 

<p align="center">
  <img src="../assets/img/RegressionModel.png" align="center" width="450"/>
</p>

The regression indicates a positive correlation between number of passengers and: percentage of female population, percentage of population over 18 years, percentage of hispanic population, number of crimes and the dummy variables for the second dose of the COVID-19 vaccine and the Omicron variant. Negative correlation between ridership and: population density, number of new COVID-19 cases, November and December months. 

* Pre-pandemic, crimes and ridership had a negative correlation with a very high significance.
* After the pandemic there is a positive correlation between crimes and ridership, but lower significance. Before the pandemic, increased crime rates did negatively impact ridership. Post pandemic, we see that as there is more crime there is more ridership. This is likely because they both dropped significantly at the start of the pandemic, and independently they both started growing as restrictions decreased and people returned to some of their normal routines. It is important that this was much less significant than pre-covid, which is most likely because we are looking at a smaller data set of ridership and crime rates. 

### Conclusions
In San Francisco, the COVID-19 pandemic has affected the relationship between crime and ridership around BART stations, and as crime has increased, so has ridership. The most important takeaway from our model is finding that before the pandemic, the negative binomial regression showed that crime had a negative correlation with ridership and was highly significant. This initial finding could implicate stations that had more crimes and saw less ridership. Post-pandemic, we believe there was not enough ridership to get a significant relationship between crime and ridership to draw conclusions. However, we these findings highlight the need for BART to take actions to address crime and safety perception to increase ridership. 
