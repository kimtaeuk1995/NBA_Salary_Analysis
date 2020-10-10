# Predicting NBA Salary 

With the rise in superstars and their salary, it has become even more vital for teams and managers to allocate resources wisely when it comes to signing or trading players. It is in the best interest of the team to pay right amount based on player's performance and reduce risk of overpaying a player. It is also in the best interest of players to be paid adequately based on his performance. 

# Methodology

1. Scrape Player Salary and Contract information data Basketball Reference
2. Feature Engineering to create new variables 
3. Discard irrelevant features using recursive feature elimination
4. Build linear regression model using current scraped data to predict salaries of players
5. Optimize model using regularization

# Data
 - Here is link to Baksetball-referece website [Basketball Reference](https://www.basketball-reference.com/players/)
 - Here is link to Espn Player Salary Page [ESPN Salary](http://www.espn.com/nba/salaries/_/page/1/seasontype/3)
 
# Features Target Variables
 - Target: Salary
 - Features: 
    - Individual Stats: Season, Age, Tm,	Lg,	Pos,	G,	GS,	MP,	FG,	FGA,	FG%,	3P,	3PA,	3P%,	2P,	2PA,	2P%,	eFG%,	FT,	FTA,	FT%,	ORB,	DRB,	TRB,	AST,	STL,	BLK,	TOV,	PF,	PTS
     - Advanced Stats: PER,	TS%, ORB%,	DRB%,	TRB%,	AST%,	STL%,	BLK%,	TOV%,	USG%, OWS,	DWS,	WS,	WS/48, OBPM,	DBPM,	BPM,	VORP

# Model
In my initial analysis, I attempted to use a Linear Regression model with a wide variety of features to compute an average RMSE for the data set with cross validation considered. I decided that this wasn't the best way for me to predict a player's salary data as each player have different roles on the court. For example, for a player of position center, his number of rebounds and blocks would matter more as opposed to the number of 3 points he makes. Therefore, to account for that, I added interaction terms. The model was then optimized using Lasso and Ridge regularization. 

# Usage
 
 
