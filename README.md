# Coursera_Capstone
## Problem and Background
This repository contains my coursera_capstone project from the Applied Data Science course offered by IBM. As my project I chose to predict the 2019/2020 season standing of the NBA, the National Basketball Association. The NBA is the best basketball league in the world and it is a huge business. Being able to predict the season standing before the season starts can help the team, the media and the bet companies to plan better. I especially want to choose a model which will give some insight into what features are the most defining for predicting the season standing. These are the features the team need to look out for. 

## Data
I will get my data from the NBA Api (https://github.com/swar/nba_api). It contains data about every team and player running back to the old days. I can use it to fid the stats of a previous year of a team and players to predict the next years performance. As the feature to predict I chose the winning percentage, which leads to a direct season standing. 

## Methodology
The final goal is to predict the winning percentage of each team, thus it is a regression problem. Since I especially want to know the contribution of the individual features to the final result I chose a Multiple Linear Regression approach and the Regularized Versions Ridge and Lasso Regression. In a first exploratiry analysis I looked at the correlation of the individual features and found that the main rellevant feature is the previous years winning percentage which makes sense. All the other features were not helpful in improving the RMSE score. So I gathered additional data about the individual players that joined a team before a new season, which helped in improve the predcition. I used 5-fold CV for the parameter tuning. 
For more details, take a look at the jupyter notebook in this repository.

## Results & Discussion
Left are my predicted season stanings according to the individual Winning Percentage and on the right side is the current season standing. The season winner was predicted correctly and all in all the prediction are quite good. The Warriors, even though last's year first place, were predicted to not be in the playoff (but not to be on the last position, injuries not inculded). But nevertheless the model sometimes still makes bad predictions, like with the Lakers where everybody would have guesses that they would land in the first places. Further analysis has to be done to find the reason for this. The model especially does not include injuries and the effect of indiviaul players like Lebron can have on a whole team. Also coaches and stuff were not included in the calculation. The most important features for predicting the winning percentage are the previous years percentage and the summed assists all current players of a team have done in the previous year. 
Bucks 	Bucks
Clippers 	Raptors
Nuggets 	Lakers
Raptors 	Clippers
76ers 	Celtics
Rockets 	Nuggets
Magic 	Pacers
Jazz 	Rockets
Trail Blazers 
Kings 	Thunder
Nets 	Jazz
Spurs 	Heat
Mavericks 	76ers
Pacers 	Mavericks
Warriors 	Nets
Lakers 	Blazers
Celtics 	Grizzlies
Thunder 	Suns
Hawks 	Spurs
Bulls Kings
Heat 	Pelicans
Pelicans 	Hornets
Pistons 	Wizards
Timberwolves Bulls
Hornets 	Knicks
Suns Pistons
Cavaliers 	Hawks
Grizzlies Timberwolves
Wizards Cavaliers
Knicks  Warriors

## Conclusion
The model made a good final prediction for this year's season standing. But nevertheless, compare to a baseline model which only used the previous year's winning percentage the advanced model only improved the RMSE form 0.112 to 0.102. Advanced informations like injurie probability, individual players importance and the improvement of single players from one year to net could be included as well as the coaching stuff.
