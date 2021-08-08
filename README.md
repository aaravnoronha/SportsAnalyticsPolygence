# Predicting NBA win probability using machine learning methods

## Summary

The aim of this project is to harness historical NBA data in order to gain insights into what statistical factors make a team successful in a given season. The team of focus for this project is the Golden State Warriors, and the box score data for each game within the span of the most recent NBA season is accessed via the Sports Reference API. The concepts and algorithms used range from Bayesian probability to more advanced ML models such as logistic regression and decision trees. With sports fanatics, NBA analysts, and players / coaches in mind, the final deliverable will be a data-driven report with an emphasis on strategic actionability. That is, the results of the model should ideally shed light on how to maximize wins for the GSW in the future.

***Author**: Aarav Noronha*  
***Polygence Mentor**: Sejal Dua*

----------------------------------

## Introduction 

I am interested in this domain because I am an NBA fan (specifically, a Warriors fan) and I wanted to have a better insight into what factors would make it more likely for the Warriors to win a given game.  I figured the best way to do this would be through a Machine Learning model, because it would be able to identify patterns or correlations within the data and make informed predictions. This data could be utilized by sports analysts, coaches, players, etc. who want a better understanding of what statistical elements of a game are impactful, and to what extent, as well as what combinations of stats within a game would give a team the best chance of winning.

## Exploratory Data Analysis

<img src="efg_histplot.png" width="300"/> <img src="tov_histplot.png" width="300"/> <img src="trb_histplot.png" width="300"/> 

<img src="corr_matrx.png" width="450"/> <img src="pairplot.png" width="450"/> 

I found that a team’s offensive rating is very highly correlated to its true shooting percentage as well as its effective field goal percentage, and that those 2 were also highly correlated, which was expected. Additionally, I found that turnover percentage was highly correlated with steals, which was also expected. The total rebound percentage was also highly correlated with both the offensive and defensive rebound percentage, and they were also correlated. The usage percentage data was not as useful because it takes into account many other different variables. Using the heatmap, the highest correlation occurred between the TS% and EFG%, followed by TRB%, ORB% and DRB%, as stated above. The lowest correlation was between STL% and TOV%.

## Features

- `MP`: Minutes Played
- `TS%`: True Shooting Percentage - 2pts, 3pts, FT combined
- `eFG%`: Effective Field Goal Percentage - Values 3pt shot more than 2
- `3PAr`: 3-point Attempt Rate - Percentage of FG from 3
- `ORB%`: Offensive Rebound Percentage - estimated % of available off rbd a player grabbed
- `DRB%`: Defensive Rebound Percentage - estimated % of available def rbd a player grabbed
- `TRB%`: Total Rebound Percentage - estimated % of available rbd a player grabbed
- `AST%`: Assist Percentage - estimated % of FG a player assisted
- `STL%`: Steal Percentage - estimated % of opp poss ending with steal by player
- `BLK%`: Block Percentage - estimated % of opp 2pt FG blocked by player
- `TOV%`: Turnover Percentage - estimated % of turnovers committed per 100 plays
- `USG%`: Usage Percentage - estimated % of team plays used by player
    *NOTE: This feature is not useful for team data, only individual players stats
- `ORtg`: Offensive Rating - estimate of pts produced (player) or scored (teams) per 100 poss
- `DRtg`: Defensive Rating - estimate of pts allowed per 100 poss
- `BPM`: Box Plus/Minus - box score estimate of pts per 100 poss a player contributed above an avg player, translated to an avg team

