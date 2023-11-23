# Soccer-Game-Prediction-Simulation
## Predict and simulate FIFA World Cup Qatar 2022 group stage/ knock-out stage games
### 1. Collect national football teams' data from fbref.com 
+ Manually download national football teams' matches data in Excel file format from fbref.com 
+ Rename files to align with countries names
### 2. Collect national football teams' elo ratings from eloratings.net
+ Manually retrieve national football teams who are participate in world cup group stage
+ Save them descendingly in Excel file
### 3. Calculate each team's offensive and defensive ratings
+ Bayes Rule: $Posterior = Prior * Likelihood$
+ $Likelihood$: each team's average goal($Goal$) and average goal received($GoalRec$) among most recent year matches data as of world cup group stage
+ $Prior$: $A_{elo} / Average_{elo}$, where $Average_{elo} = \sum elo/32$
+ $Posterior$: national football teams' estimated offensive and defensive ratings, where $off = Goal * Prior$ and $def = GoalRec / Prior$
### 4. Estimate xG for a specific match
+ $Goal_{team_1} = off_{team_1} * def_{team_2}$; $Goal_{team_2} = off_{team_2} * def_{team_1}$
### 5. Simulate a match by discrete multivariate poisson model
+ $xG$ as of parameters
### 6. Simulate the whole tournament
+ Monte Carlo Simulation
