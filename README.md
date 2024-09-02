# Recommendation-Systems
Compares performance of Surprise models: SVD, NMF, KNNBasic, SlopeOne, CoClustering
This project compares Surprise package’s recommendation system models: 
SVD
KNNBasic
NMF
SlopeOne
CoClustering

Dataset:
MovieLens’s ml-latest-small.zip consisting of each movie ratings and tiles last updated 9/2018 was used.  The dataset uses a 1-5 star rating system and contains over 100K ratings over  9,700 movies. Tags.csv contains the free-text tagging for each movie.
Ratings.csv contains the user ratings for each movie based on the movie ID, and movies.csv maps the movieID to a specific movie title.

Process Flow:
Load “ratings.csv” as data frame 
Created common function with “recommendation algorithm” as parameter to go thru the this common steps:
Create Surprise object reader, load data from Pandas data frame with ratings from 1 to 5
Split data into train/test sets
Perform cross-validation with cv=5
     3. Display RSME, MSE, Fit and Test Times
     4. Display Movie Recommendations


Observation:

Top 10 and ‘Middle 10’ movie recommendations are printed based on their estimated score.  Interesting observation is that beyond the top 3 - 5 recommendations there seemed to be not much similarity between the different methods. This suggest to use only the up to the top 5 recommendations from any of the models.
