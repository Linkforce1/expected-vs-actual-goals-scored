# Expected vs Actual Goals Scored: Finishing Efficiency
Scoring goals in soccer is difficult — but some players make it look effortless. This project analyzes which players at the 2022 FIFA World Cup most significantly overperformed or underperformed their expected goals using data visualization and finishing efficiency metrics. Lucky for us, that we have a metric that can judge the quality of a shot called “xG”, or expected goal. This metric represents how promising the opportunity to score was before the shot was taken. Over performing relative to the xG metric would indicate that the specific player would beat the “average” shooter on identical chances. On the other hand, under performing would indicate either slightly below par finishing or perhaps some other contextual factors. Anyone can technically create their own xG model with their own features but for the purposes of this exploration, I used the shot_statsbomb_xg metric from the Hudl Statsbomb dataset. 

We computed each player’s expected goals by multiplying each players average xG with the number of shots they took during the tournament. We compare this to the actual goals scored, and finishing ratio (Goals / Expected Goals) to evaluate who converted their chances best — and who left goals on the table. Visualizations were created using Plotly in Python and exported as static images for presentation.

📈 **Key Visuals**

This distribution shows the overall shot quality of all the shots taken during the 2022 World Cup. There weren’t a lot of high quality shots taken in this tournament. The slight bump at the tail of the distribution would be the penalties taken. The poor shot quality might not be the fault of the strikers/forwards themselves but rather an indication of how tough the defenses are playing and not providing a lot of opportunities for clean looks at goal. I kind of equate it to someone batting .300 in baseball and being an all-star. Which is why it’s impressive that Lionel Messi had an average xG of 0.22 through the tournament placing him in the 85th percentile. Now, how he got those opportunities is certainly interesting and a topic that we will certainly explore for another day. 

https://linkforce1.github.io/expected-vs-actual-goals-scored/Distribution%20of%20Shot%20Quality.html
<img src="docs/Distribution of Shot Quality.png" alt="Distribution of Shot Quality (xG) in 2022 World Cup" width="600"/>

https://linkforce1.github.io/expected-vs-actual-goals-scored/Top%20Players%20by%20Shot%20Quality%20Opportunity.html
<img src="docs/Top Players by xG.png" alt="Top Players by Shot Quality in 2022 World Cup" width="600"/>

The scatterplot below highlights the finishing efficiency of the players in the tournament based on their shot quality. Anyone above the diagonal would be classified as someone who overperformed realtive to expecations and anyone below would be someone who underperformed. 

https://linkforce1.github.io/expected-vs-actual-goals-scored/Goals%20vs%20Expected%20Goals.html
<img src="docs/Goals vs Expected Goals.png" alt="Goals vs Expected Goals Scatterplot" width="600"/>

The bar chart highlights the top 10 overperformers in terms of finishing differential in the World Cup. The finishing differential is defined as the difference between the expected and actual number of goals scored.

https://linkforce1.github.io/expected-vs-actual-goals-scored/Top%20Overperformers%20in%20World%20Cup.html
<img src="docs/Top Overperformers in 2022 World Cup.png" alt="Top Overperformers Bar Chart" width="600"/>

The scatterplot below shows player's finishing ratio which indicates a level of efficiency. Anyone with a ratio above 1, indicates that they are scoring more goals than is expected of them. 

https://linkforce1.github.io/expected-vs-actual-goals-scored/Finishing%20Ratio%20vs%20Expected%20Goals.html
<img src="docs/Finishing Ratio vs Expected Goals.png" alt="Finishing Ratio vs Expected Goals" width="600"/>

# Takeaway

It’s tempting to crown every overachiever a clinical finisher and every underachiever a flop. Context matters and the World Cup is not the biggest sample size. But when a player consistently beats their expected target across multiple tournaments, or seasons, you start to suspect this player might be the real deal. Smart movement, elite shot placement, composure under pressure — those things don’t show up in a metric like a finishing differential. The gap between expected and actual goals helps us spot special players or special circumstances which warrant further investigation. This only drums up more questions regarding players such as how involved are they in setting up high xG possessions. How often do they beat the expected target? Are they getting unlucky this tournament? While this analysis might provide some insight into key players, this is only a stepping stone to help us analyze which players have real influence is during the game.




