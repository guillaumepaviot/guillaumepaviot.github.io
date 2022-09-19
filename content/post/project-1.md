---
date: 2022-07-25T10:58:08-04:00
description: "A network of Twitter accounts that took part in an event"
featured_image: "/images/project-1/full_graph.png"
title: "A network of Twitter accounts"
---

The goal of this project was to learn more about networks and use the Twitter API.  
During a trending topic on Twitter and Twitch involving a lot of reactions from different communities, I scrapped almost 29 000 tweets from the API.  
To be used in Gephi, I had to clean the data and scrape the missing values from other endpoints.
Then, I separated the cleaned data into an edges CSV file and a nodes CSV file.  
I loaded 24 000 nodes and 40 000 edges in Gephi and analysed the network using clustering and ranking algorithms.
I also posted the final visualisation on Twitter with some findings and explainations about the graph.

[Link to Network in full resolution](https://www.easyzoom.com/imageaccess/2ea1991c24ce43359b4feb22297d3c0c)  
[Link to GitHub Repository](https://github.com/guillaumepaviot/twitter_graph)

{{< figure src="/images/project-1/closeup.png" >}}
*A close up picture of the center of the network with the biggest accounts*

{{< figure src="/images/project-1/pattern.png" >}}
*Without the edges, we can observe some interesting patterns in the postions of the edges*