# Movie-Recommender

Movie Recommender is a simple recommender system that seeks to generate top recommendations for each user based on their past references.

## Datasets:
* [MovieLens 20M Dataset](https://grouplens.org/datasets/movielens/20m/)

## Requirement
- Python 3.6
- Pandas 0.24
- Pyspark 2.4

## Notebooks
### 1: [Movie_recommender](https://github.com/Jingxixi/Movie-Recommender/blob/master/Data_Processing.ipynb)
Explored movies.csv, ratings.csv and tags.csv. Removed unnecessary columns and calculated weighted average rating of each user and movie based on IMDB's formula. Analysed tag frequency, top movie within each genre and other data visualization. Implemented baseline, collaborative filtering and content based approaches.
### 2: [Scalable Version Using PySpark](https://github.com/Jingxixi/Movie-Recommender/blob/master/Recommender-spark.ipynb)
Scaling up the pipeline using pyspark. For matrix factorization, [ALS](https://spark.apache.org/docs/latest/mllib-collaborative-filtering.html) is used. The best RMSE is 0.880.
