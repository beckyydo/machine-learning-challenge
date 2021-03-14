# Exo-Planet Machine Learning

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.
For 9 years the NASA Kepler space teleschope has helped collected data on potential exoplanets.To help predict the classify candidate exoplanets for the raw data, machine learning models were used. Data was pulled from the link below.

Data: https://www.kaggle.com/nasa/kepler-exoplanet-search-results

In the notebook, the following data processes implemented:

1. Preprocess the raw data <br>
2. Tune the models <br>
3. Compare two or more models <br>

### Model 1 (KNN)
The first model created was the k-nearest neighbors (KNN), for the initial n neighbour 10 was used. The initial score training dataset was 85.61% and the testing dataset was 81.75%, the drop in score in the testing set suggests a bit of overfitting in the training dataset. Using the GridSearch testing various n values, it produced that 18 was the best n neighbour with a score of 81.79% which is slightly better than the initial model. This model is still less than 85% which suggests this model is not good at predicting exoplanets and should not be used. To increase the score, the model can we adjusted removing other features or testing a large range of n values.

### Model 2 (Logistic Regression)
The second model created was the logistic regression, the initial model was implemented with the default parameters. The intial score training dataset was 84.64% while the testing score was 86.38%. Using the GridSearch testing the c and solver parameter. Using the GridSearch, it printed that parameter c of 10 and solver with 'saga' were the best parameters with a score of 86.59%. This score is over 85% which means it's decent enough to help predict candidates for exoplanets. To improve the model we can adjust by removing more features that may not be necessary or add more parameters to test in the GridSearch to find the optimal parameter combinations.
