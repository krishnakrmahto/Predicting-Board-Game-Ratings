Predictive model to predict the rating of board game.

Dataset taken from: https://github.com/ThaWeatherman/scrapers/tree/master/boardgamegeek

*Data preprocessing*:
  1. After investigating the dataset for skewness (average_rating = 0 was sceptically higher than other ratings), it was
    found that such ratings were actually not useful as those examples lacked values for other features as well. Such examles were hence, dropped, i.e, examples with average_rating = 0 were removed from the dataset.
  2. Although null values mostly were in the "Name" feature (which does not contribute to the average_rating), all such
    examples were dropped as well.
  3. The useful features were then extracted and transformed into numpy arrays (matrices for linear regression, for
    Random Forest the y-values were to be taken as vectors).

After data preprocessing was done, Linear Regression and Random Forest algorithms were trained. Random Forest outperformed
Linear Regression (metric used for comparison: mean square error).
