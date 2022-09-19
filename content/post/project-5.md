---
date: 2022-09-04T10:58:08-04:00
description: "Scrapping and visualising data from League of Legend pro players"
featured_image: "/images/project-5/LOL_worlds.jpg"
title: "Ranking a video game's players"
---

At the end of every year, the best League of Legend teams from all regions gather on one server to train before the World Championships. And this is the best time to scrape data from the API to answer the question: who is the strongest player ? Who is the strongest team ?  

I will reuse the code I used last year to scrape data and then explore the dataset with some visualisation. I will use a similar ranking as [IBM Watson's power ranking on Overwatch players](https://overwatchleague.com/en-us/news/introducing-power-rankings-with-ibm-watson). It will be done over win correlated features, probably egineered ones, assigne a weight to each of them, normalise the features and the grade will be the weighted sum of those features.  

After this, the end goal would be to make a model to predict which team is going to win a game, but League of Legends depends on a lot of features that are difficult to capture with the data that we have.  

[Link to the Github Repository](https://github.com/guillaumepaviot/lol_scraping)