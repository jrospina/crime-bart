---
layout: post
title: Ridership Regression Model
subtitle: The combined influence of crime on transit ridership at the stop level
cover-img: /assets/img/bart_station_photo.jpg
thumbnail-img: /assets/img/bart_station_photo.jpg
<!-- share-img: /assets/img/path.jpg -->
tags: [books, test]
---

Using ridership data collected from BART stations we used a negative binomial regression model to understand the influence of crime on transit ridership at the stop level. We used the number of entries from 8 stations as a dependent variable for the regression analysis. Independent variables included: number of crime incidents around stations, rate of new COVID-19 cases and socio-demographics (race, gender, income). 

### Data Collection
* Police Department Incident reports were gathered from San Francisco Open Data portal, from 2018 to 2021, the dataset included incident reports filed to the San Francisco Police Department online report system. 
* Monthly ridership reports were collected from the BART official portal. Only entries from 2018 to 2021 to each station were taken into account for the modeling
*  Datasets for income, gender, race and ethnicity were taken from the US Census Bureau official site at census tract neighborhood level
* Impacts of the COVID-19 pandemic were included through number of new cases reported on San Francisco’s Open Data portal

### Spatial Resolution
A coverage area division of San Francisco using Voronoi diagrams (or Thiessen polygons) was applied to determine the area of influence of BART stations. An additional buffer area of 800m around stations is created as direct catchment area. Crime, income and demographic data were attachet to a station of they fell within it's buffer. For overlapping buffers (stations that fall closer together), the Voronoi polygons were used as delimitants

<img src="/assets/img/Buffer_Thiessen.png" width="5500">












The final model results indicate that the number of crime incidents around stations have a significant effect on transit ridership. Our results also showed that there is a stark difference in assessing crime and ridership in pre vs post pandemic scenarios.  Study findings suggest crime-related safety measures are crucial to addressing ridership declines. 


The truth is that no one else can definitively know the path we are here to walk. It’s tempting to listen—many of us long for the omnipotent other—but unless they are genuine psychic intuitives, they can’t know. All others can know is their own truth, and if they’ve actually done the work to excavate it, they will have the good sense to know that they cannot genuinely know anyone else’s. Only soul knows the path it is here to walk. Since you are the only one living in your temple, only you can know its scriptures and interpretive structure.

At the heart of the struggle are two very different ideas of success—survival-driven and soul-driven. For survivalists, success is security, pragmatism, power over others. Success is the absence of material suffering, the nourishing of the soul be damned. It is an odd and ironic thing that most of the material power in our world often resides in the hands of younger souls. Still working in the egoic and material realms, they love the sensations of power and focus most of their energy on accumulation. Older souls tend not to be as materially driven. They have already played the worldly game in previous lives and they search for more subtle shades of meaning in this one—authentication rather than accumulation. They are often ignored by the culture at large, although they really are the truest warriors.

A soulful notion of success rests on the actualization of our innate image. Success is simply the completion of a soul step, however unsightly it may be. We have finished what we started when the lesson is learned. What a fear-based culture calls a wonderful opportunity may be fruitless and misguided for the soul. Staying in a passionless relationship may satisfy our need for comfort, but it may stifle the soul. Becoming a famous lawyer is only worthwhile if the soul demands it. It is an essential failure if you are called to be a monastic this time around. If you need to explore and abandon ten careers in order to stretch your soul toward its innate image, then so be it. Flake it till you make it.
