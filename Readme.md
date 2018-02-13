The increasing importance of the web as a medium for electronic and business
transactions has served as a driving force for the development of recommender
systems technology. An important catalyst in this regard is the ease with which
the web enables users to provide feedback about their likes or dislikes. The basic
idea of recommender systems is to utilize these user data to infer customer
interests. The entity to which the recommendation is provided is referred to as
the user, and the product being recommended is referred to as an item.
The basic models for recommender systems works with two kinds of data:
1. User-Item interactions such as ratings
2. Attribute information about the users and items such as textual profiles
or relevant keywords
Models that use type 1 data are referred to as collaborative filtering methods,
whereas models that use type 2 data are referred to as content based methods. In
this project, we will build recommendation system using collaborative filtering
methods.

Collaborative filtering models use the collaborative power of the ratings provided
by multiple users to make recommendations. The main challenge in designing
collaborative filtering methods is that the underlying ratings matrices
are sparse. Consider an example of a movie application in which users specify
ratings indicating their like or dislike of specific movies. Most users would have
viewed only a small fraction of the large universe of available movies and as a
result most of the ratings are unspecified.
The basic idea of collaborative filtering methods is that these unspecified ratings
can be imputed because the observed ratings are often highly correlated
across various users and items. For example, consider two users named John
and Molly, who have very similar tastes. If the ratings, which both have specified,
are very similar, then their similarity can be identified by the filtering
algorithm. In such cases, it is very likely that the ratings in which only one of them has specified a value, are also likely to be similar. This similarity can be
used to make inferences about incompletely specified values. Most of the collaborative
filtering methods focuses on leveraging either inter-item correlations
or inter-user correlations for the prediction process.
In this project, we will implement and analyze the performance of two types of
collaborative filtering methods:
1. Neighborhood-based collaborative filtering
2. Model-based collaborative filtering

In this project, we will build a recommendation system to predict the ratings
of the movies in the MovieLens dataset. The dataset can be downloaded using
the following link:
http://files.grouplens.org/datasets/movielens/ml-latest-small.zip
Although the dataset contains movie genre information, but we will only use
the movie rating information in this project. For the subsequent discussion,
we assume that the ratings matrix is denoted by R, and it is an m × n matrix
containing m users (rows) and n movies (columns). The (i, j) entry of the matrix
is the rating of user i for movie j and is denoted by rij . Before moving on
to the collaborative filter implementation, we will analyze and visualize some
properties of this dataset.

