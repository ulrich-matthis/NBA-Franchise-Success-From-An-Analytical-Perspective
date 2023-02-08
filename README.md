# NBA Franchise Success Analysis
  
## Motivation
In the United States there are few things more engrained within our nation’s culture than professional sports. To go along with that, is endless debates within the media of which players and teams have had the most success. This could be seen from number of championships, to longevity, to the phrase, “What have you done for me lately?” and everything in between. This project intends to approach the question of what makes a team successful from a more numerical perspective.

## Goals
The aim of this project was to examine how much success franchises in the NBA are having from a perspective that looks past the league’s stars and instead examines other intangibles such as team profits, franchise attendance totals over seasons, geographic location and the relative average ages of each team in the league, using win percentage as a constant for these comparisons. 

## Tools
Our work was done in a jupyter notebook using python. Libraries used include Pandas, matplotlib, seaborn, numpy, scipy.stats and bokeh. Multiple visiualizations were done for each question to illustrate our findings. Graphs are shown in notebook and saved in the 'Outputs' folder.

## Data
Data compilation was completed using the website basketball-reference to help compile season to season data for all NBA franchises. runrepeat.com was used to provide 
income data for each team over the timeframe of our study and hoopshype was also used for salary data which will be a focal point of team financials versus wins.

## Analysis

### Fan Engagement versus Wins
First point of comparison was the teams win percentage and how much of an effect that had on yearly attendance for that team. The primary question for this comparison was if team performance for the season, had any effect on the amount of people attending games. 
	
### Player Age versus Wins
This portion of the analysis was to see if there were any consistent trends that existed between the average age of a team and the teams win rate. The main reason we asked this was to see if a teams performance could be tied to the age of a team.

### Team Financials versus Wins
To analyse the financial influence over the performance, we will create two graphs:
- A scatter plot to analyse the correlation between the payroll and the number of wins of each team.
- A bar plot and a line plot overlayed to compare the average income, payroll and wins.

### Location versus Wins
Additional data used to answer this question includes
- the main data compiled by our team
- media market data obtained from hoop-social.com
- name and geocoordinates of each team's arena via Geoapify API
- calculated five-year means and total counts

Two maps were made showing metro population versus win count and metro population versus franchise income. From an initial glance at the first map, the number of wins does not seem to be correlated with the market size of a franchise. In the second map, it does appear that the mean income of a franchise does seem to be correlated with the market size. 

The variables "Metro Population" "mean Income" and "Total Wins" were discretized into categories using the pd.cut method, and chi-square analysis was run to test our initial observations. Looking at the results of chi square analysis, market size and total wins are independent. This means that the size of a market does not have an impact on a team's ability to win. However, the variables of market size and mean income are dependent. This means that cities with larger media markets tend to be more profitable.

## Summary of Findings
Our correlation matrix displays how all variables of interest are related to each other.

- Attendance at games does not seem to impact a team's ability to win.
 - r = 0.25

- Player age actually has a positive, moderate relationship with a team's ability to win. More aggregate experience among players seems to lead to success.
 - r = 0.56

- A positive, moderate relationship exists for payroll and team wins. Better players will cost a premium.
 - r = 0.52
 
- A team's income, however, has little to do with a winning record.
 - r = 0.017
 
- A team's market size also has little to do with a team's ability to win. In fact, many teams in smaller metro areas have top-tier records. The relationship is negative but weak.
 - r = -0.2
 
- The market size of a team does impact a franchise's ability to generate income. Teams in larger metropolital areas are more successful from a financial standpoint.
 - r = 0.52

## Conclusion

Experience seems to be an important factor in an NBA team's ability to succeed as the relationship between wins and mean age was the strongest in our study. This experience, though, will come with a cost since high player payrolls are also correlated with wins.

From a financial perspective, a winning team does not necessarily translate large profits. The factors of market size and average attendance do more to predict a larger income than a team's win record. For an owner, the ability to generate income depends more on marketability.
