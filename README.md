# Movie-Recommender

Movie Recommender is a simple recommender system that seeks to generate top recommendations for each user based on their past references.

## Datasets:
* [MovieLens 20M Dataset](https://grouplens.org/datasets/movielens/20m/)

## Requirement
- Python 3.6
- Pandas 0.24
- Pyspark 2.4

## Approach
### 1: [Data Preprocessing](https://github.com/Jingxixi/Movie-Recommender/blob/master/Data_Processing.ipynb)
Explored movies.csv, ratings.csv and tags.csv. Removed unnecessary columns and calculated weighted average rating of each user and movie based on IMDB's formula. Analysed tag frequency, top movie within each genre and other data visualization. 
### 2: [Baseline](https://github.com/Jingxixi/Movie-Recommender/blob/master/Baseline_Method.ipynb)
Used basic linear regression model as baseline method. Cross Validation is use to evaluate the baseline model. Result average RMSE is 1.042.
### 3: [Collaborative Filtering](https://github.com/Jingxixi/Movie-Recommender/blob/master/Collaborative_Filtering.ipynb)
Used [Surprise](http://surpriselib.com/) implemented SVD method to do the matrix factorization. The result RMSE is 0.888.
### 4: [Scalable Version Using PySpark](https://github.com/Jingxixi/Movie-Recommender/blob/master/Recommender-spark.ipynb)
Scaling up the pipeline using pyspark. For matrix factorization, [ALS](https://spark.apache.org/docs/latest/mllib-collaborative-filtering.html) is used. The best RMSE is 0.880.
