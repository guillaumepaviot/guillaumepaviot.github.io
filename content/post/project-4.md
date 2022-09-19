---
date: 2021-01-17T10:58:08-04:00
description: "Analyzing and forecasting electricity consumption in France"
featured_image: "/images/project-4/production_electricite.jpg"
title: "Forecasting electric consumption"
---

With this project, I wanted to learn about time series and how to forecast them. For the data, I downloaded a JSON file from [ENEDIS open data](https://data.enedis.fr/pages/accueil/?id=init), the french electrical distributor, which reprensents the volumes of energy injected, extracted, produced or consumed in the Enedis mesh over a period of time given to the step of half an hour.  
From all the features, I only kept the timestamp and total consumption. I chose the JSON format because the ENEDIS API sends the data in JSON and my goal at the time was to train the model on the 5 years historical data and then move to online learning to keep it up to date. It's not online yet but it's one of my projects.  
Before trainning the model, I wanted to analyse the data looking for trends. To do that I used the statsmodel module from Python. It can only extract trends from a dataset sampled every months but we can already learn a lot from this   

{{< figure src="/images/project-4/data.png" >}}
*The whole dataset plotted*
{{< figure src="/images/project-4/trend.png" >}}
*The trend over the years*
{{< figure src="/images/project-4/season.png" >}}
*The seasonnality of the data*  

The first trend we can observe is that electricity consumption decreases. We can also see that the comsumption is very seasonnal: peaking in winter and low in the summer. RTE estimates that French consumption increases by 2400MW for each degree less in winter. This is mainly due to the heating of buildings (a third of French households are heated with electricity) as well as the production of hot water.  

For the forecast model, I use the [Prophet](https://facebook.github.io/prophet/) procedure developed by Facebook, because it allows to have rigorous forecasts while integrating the trend effects that exist in the data as well as the dates (days of the week).  
I wanted to also use a recurring neural network but it needed more data preprocessing and they are not necessarily more accurate than the Prophet models.  

After training on the data, the model is able to make predictions but also to give different decompositions of the data it was trained on.

For example, we find the annual, weekly and daily decomposition.  
{{< figure src="/images/project-4/yearly.png" >}}
*The yearly decomposition*
{{< figure src="/images/project-4/weekly.png" >}}
*The weekly decomposition*
{{< figure src="/images/project-4/daily.png" >}}
*The daily decomposition*  

The decomposition we get aligns with the seasonnality announced by ENEDIS. Also, since the model analyzes the data on time and not on months, it allows a finer decomposition than before. We then obtain a weekly decomposition with a minimum in the night from Saturday to Sunday, as well as a daily decomposition with a hollow after midnight and peaks at noon and dinner time.  

Now that the model is trained, we can use it to forecast the consumption.  
{{< figure src="/images/project-4/forecast.png" >}}
*Forecasting a week ahead, balck dots are ENEDIS data, the blue line is the model's forecast and the light blue represents the model's uncertainty*   

The data range from December 12 to 19, 2020, and the forecast extends until December 26. We find the weekly trend with a low on Sundays (13th and 20th), as well as the different peaks and lows during the days.  

Visual examination is not enough to evaluate a model. To do this, I intend to update the data and evaluate the model's error on its forecasts.

[Link to GitHub Repository](https://github.com/guillaumepaviot/energy-forecast)