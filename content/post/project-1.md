---
date: 2022-07-25T10:58:08-04:00
description: "A network of Twitter accounts that took part in an event"
featured_image: "/images/project-1/full_graph.png"
title: "A network of Twitter accounts"
---

During the announcement of an event on Twitch that sparked significant reactions from various communities on Twitter, I scraped approximately 29,000 tweets using the API to learn more about network analysis and using an API.

Key Steps and Achievements:

**1.** **Data Cleaning and Enrichment**: I cleaned the data and retrieved missing values from additional endpoints to ensure data integrity for analysis in Gephi.
**2.** **Data Preparation**: The cleaned data was organized into two CSV files: one for edges and one for nodes, resulting in 24,000 nodes (Twitter users) and 40,000 edges (interactions between Tweets through by someone).
**3.** **Network Analysis**: I loaded the data into Gephi and conducted a comprehensive analysis using clustering and ranking algorithms to uncover patterns and insights.
**4.** **Visualization and Communication**: I created a final visualization of the network, which I shared on Twitter along with key findings and explanations of the graph

This project was really interesting and I learned a lot about managing a large dataset and communicating complex results to an audience that doesn't have a technical background.

[Link to Network in full resolution](https://www.easyzoom.com/imageaccess/2ea1991c24ce43359b4feb22297d3c0c)  
[Link to GitHub Repository](https://github.com/guillaumepaviot/twitter_graph)

{{< figure src="/images/project-1/closeup.png" >}}
*A close up picture of the center of the network with the biggest accounts*

{{< figure src="/images/project-1/pattern.png" >}}
*Without the edges, we can observe some interesting patterns in the postions of the edges*