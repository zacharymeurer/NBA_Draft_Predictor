# NBA Draft Predictor

## Overview: 

This project utilizes an NBA prospect’s college basketball stats to predict what pick the player will be drafted. 

## Data Sources: 

- NCAA season stats for each player from Aditya Kumar's [College Basketball 2009-2021 + NBA Advanced Stats](https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021?resource=download)

  https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021?resource=download

- RPI Ratings for [conferences](https://www.teamrankings.com/ncaa-basketball/rpi-ranking/rpi-rating-by-conf/) and [teams](https://www.teamrankings.com/ncb/rpi/) from [TeamRankings.com](https://www.teamrankings.com/)

  https://www.teamrankings.com/ncaa-basketball/rpi-ranking/rpi-rating-by-conf/ & https://www.teamrankings.com/ncb/rpi/

## Methods: 

### Data Preparation:

- Scraped RPI ratings for teams and conferences.
- Merged ratings data with NCAA data after making join key consistent between datasets (i.e. reformatting conference and team names to match in each dataset).
- Cleaned Data (e.g. Drop Null values, verified data consistency, changed data types, etc.).
- Grouped the records of CollegeBasketballPlayers2009-2021.csv on player by taking a weighted average of each attribute dependent on a players’ minutes played.
- Normalized Data.

### Machine Learning:

- Trained a random forest regressor on a prospect's college basketball stats to predict draft pick. 
- Tuned the hyperparameters through Bayesian optimization before visualizing the model and its performance.
- Measured and Plotted model accuracy.

## Considerations:

Ideas to implement in the future to improve accuracy: 

- Adding additional auxiliary data from the [nba draft combine](https://github.com/wyattowalsh/nba-db/tree/main) (e.g. draft combine data like vertical leap, wingspan, etc.)
- Weighting the weighted average on multiple variables (e.g. minutes played, conference strength, and team strength)
- Trying a different machine learning model (e.g. neural network regressor).
