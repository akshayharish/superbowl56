# Predicting the outcome of Superbowl LVI

Data was gathered from freely available sources for the 2021-22 season.

The approach was to build an ensemble model that would capture almost all uncertainties of the game.

A four-step strategy was built-
1) Comparision framework: Since The Rams and Bengals had never played each other, there was no head-to-head statistics available. <br/>
To generate these match-up statistics, we clustered the games that LA Rams played using an unsupervised model. We then used the statistics
of the opposition teams that the Bengals had played and matched them in these clusters. This way, we would have a scenario based match-up for the two teams. <br/>

2) Team Statistics: Using the team's offense and defense statistics, a linear regression model was built to predict the outcome (score) of the game. 
The output from the comparison framework was used as the input for the regression to a prediction.

3) Quarterback Statistics: The quarterback's performance is key to how well a team performs. So a regression model was built using the Quarterback statistics of the two players.
The avaerage season performance was used as an input for the regression and another prediction was made.

4) External factors: Betting statistics, weather, home advantage was factored in to build a probability measure of success for these predictions.

Finally, the predictions from the Team Statistics and Quarterback statistics were used in a simple Ensemble model to get the final prediction - LA Rams to win the Superbowl
29 to 23.

