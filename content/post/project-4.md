---
date: 2021-01-17T10:58:08-04:00
description: "Analyzing and forecasting electricity consumption in France"
featured_image: "/images/project-4/production_electricite.jpg"
title: "Forecasting electric consumption"
---
This project aimed to explore time series analysis and forecasting using energy consumption data from [ENEDIS open data](https://data.enedis.fr/pages/accueil/?id=init), the French electrical distributor. The dataset includes energy volumes injected, extracted, produced, or consumed in the Enedis network, recorded every half hour.

**Key Steps and Achievements:**

**1. Data Preparation:**

-Downloaded JSON data from the ENEDIS API.
-Focused on timestamps and total consumption.
-Chose JSON for compatibility with the ENEDIS API and future online learning updates.

**2. Data Analysis:**

-Used Python's *statsmodel* module to identify trends and seasonal patterns.
-Observed a decrease in overall electricity consumption.
-Identified strong seasonality: peaks in winter, lows in summer, with a 2400MW increase per degree drop in temperature during winter.

**3. Forecast Model:**

-Utilized Facebook’s [Prophet](https://facebook.github.io/prophet/) model for rigorous forecasts, integrating trends and weekly patterns.
-Initially considered a recurrent neural network but chose Prophet for its ease and accuracy with less preprocessing.

**4. Model Training and Results:**

-Trained the model on five years of historical data.
-The model provided detailed decompositions, aligning with ENEDIS’s seasonality reports.
-Identified weekly patterns with lows on Sundays and daily patterns with lows after midnight and peaks at noon and dinner time.

**5. Forecasting:**

-Forecasted energy consumption from December 12 to 26, 2020.
-Identified weekly trends and daily peaks/lows accurately.
-Planned to update data and evaluate the model's error for continuous improvement.

Some trends identified by Prophet:
{{< figure src="/images/project-4/yearly.png" >}}
*The yearly decomposition*
{{< figure src="/images/project-4/weekly.png" >}}
*The weekly decomposition*
{{< figure src="/images/project-4/daily.png" >}}
*The daily decomposition*  

And the projected energy consumption :
{{< figure src="/images/project-4/forecast.png" >}}
*Forecasting a week ahead, balck dots are ENEDIS data, the blue line is the model's forecast and the light blue represents the model's uncertainty*   

This project was my first introduction to time series analysis, data preprocessing, and forecasting using advanced models and even if it's imperfect, I'm really happy with the results I obtained.

[Link to GitHub Repository](https://github.com/guillaumepaviot/energy-forecast)