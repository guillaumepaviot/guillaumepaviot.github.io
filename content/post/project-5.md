---
date: 2022-09-04T10:58:08-04:00
description: "Scrapping and visualising data from League of Legend pro players"
featured_image: "/images/project-5/LOL_worlds.jpg"
title: "Ranking a video game's players"
---
As a League of Legend fan, I always wondered who is the best team, and the best player ? And how do they compare to each other across the years and leagues. To answer those questions, I tried different methods.

**1. Power Ranking**  
I first started with a power ranking as they did in [Overwatch League by IBM](https://overwatchleague.com/en-us/news/introducing-power-rankings-with-ibm-watson). It was done by engineering features that correlated to winning, and then assigning a weight to each of them, proportional to their correlation. The features are then normalised over the league and summed up with their respective to get a grade for each player or team.  
The problem is that it was not possible to predict which team would win a game with only the grades. It was also hard to compare teams that were in different leagues, as their grades don't reflect the differences in terms of level between different leagues. And normalising the features over the whole dataset would only favours the small teams that dominate their local leagues comapred to major leagues that are usually competitives with tensed games.

**2. Elo and derivatives**
I then tried to use a more traditional approach, using the [ELO rating system](https://en.wikipedia.org/wiki/Elo_rating_system). It is a method that was used in chess to rank players. The idea is that each player has an initial score of 1500 points. Then, for each game played by two teams, the winner scores points and the loser loses the same amount of points. The number of points won or lost is determined by the difference of score between the teams and the result of the game.
I then switched to [Glicko2](https://en.wikipedia.org/wiki/Glicko_rating_system) system and applied it to the players individually, the score for the team becoming the average of its 5 players. This gave better results than using the power ranking. The problem is that it was hard to compare teams that were in different leagues but their scores don't reflect the differences between different leagues.
To do this, I then gave each team a new score for the whole region and add it during  international events. This lead to better results but since there's not much international events, the score isn't updated often enough to really reflect the differeces in level between the region.
I also used another ranking systems : [TrueSkill](https://trueskill.org), but the results weren't more convincing than the other systems.

The Glicko2 approach still gave some interesting results : 
{{< figure src="/images/project-5/lplranking.png" >}}
*The LPL 2023 Spring season gives the correct first four teams*
{{< figure src="/images/project-5/regionscore.png" >}}
*After only one international event, we can already see the first three major regions, even if their score don't reflect their differences. Also, we can observe that for the regions with the least games played, the variability is quite high.*

To go further, since it needs more historical data, I would need to switch to an SQL database to store the games, since it's currently on excel and difficult to handle.

[Link to the Github Repository](https://github.com/guillaumepaviot/lol_scraping)