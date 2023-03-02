# i310-assignment7

The goal of the project: To execute ETL (Extract, Transform, and Load) the data and visualize with insights

Links to API: BeautifulSoup(https://pypi.org/project/beautifulsoup4/#:~:text=Beautiful%20Soup%20is%20a%20library,and%20modifying%20the%20parse%20tree.)

Links to Data: 2022 Fantasy Football Data (https://www.pro-football-reference.com/fantasy/index.htm, terms of use: https://www.sports-reference.com/data_use.html)

Data Description:

Top 100 players based on fantasy points
- Player: name of the player, string
- Position: position of the player, string
- Age: age of the player, float
- PassingTD: number of passing touchdown made by the player, float
- rushingTD: number of rushing touchdown made by the player, float
- receivingTD: number of receiving touchdown made by the player, float
- Non-passingTD: number of rushing+receiving touchdowns made by the player, float
- Int: number of interceptions made by the player, float
- Points: fantasy points throughout the year 2022, float 

There was no issues found in the data.

From histograms, I could find points and age have both bell on the left side having tail on the right (skewed right).

Pearson Correlation gives that...

[1] PassingTD and Points have about 0.71. This is very strong linear correlation, which makes sense since TD gives the most points.

[2] RushingTD and Points have about 0.42. This is pretty strong linear correlation.

[3] Age and Points have about 0.15. This is very weak correlation.

[4] Int and Points have about 0.56. This is pretty strong. This is pretty interesting considering that interception takes away your point not give.

I calculated the average score for each position and made the bar plot. This bar plot suggests that average fantasy points for positions are ranked as QB (quarterback), RB (runningback), WR (Wide Receiver), TE (Tight End).

The scatterplot for PassingTD vs. Points had two big patterns to consider. First, there is a straight line going up where passing TD is zero. This happens because there are lots of ways to acquire points without having passing TD. Second, there is a pretty strong linearity which suggests the more passingTD, the higher points were.
