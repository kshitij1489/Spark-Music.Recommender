# Spark-Music.Recommender

Collaborative filtering is one of the most popular recommender system techniques and is being extensively
used in many applications such as in music and movies streaming applications, in ecommerce industry for product recommendations,
used in restaurant and place recommendations etc. 

In this this application, we have used spark and the collaborative filtering technique to build a artist recommender system,
which suggests users, artists based on his/her and other's listening history. We have used the Spark mllib's Alternating least square
algorithm library to build our model.

This dataset used here for demonstration is from the publicly available song data from audioscrobbler[1]. The dataset included here is a 
trimmed version of the original dataset containing information about the 50 most active users. 
The original dataset contains information about 141K users, and 1.6 million artists.

The flow of our implementation is as follows:

1. Read all the three dataset files in RDDs
2. Filter, manipulate and tranform the RDD's to extract information about users like: artist play counts, user - mean playcount etc.
3. Split these tranformed RDDs into training, validation and test RDDs
4. Train Model: Create three models with different number of latent factors using the trainingRDD.
5. Model Evaluation: Choose the best model of the three by testing on the validationRDD.
6. Make predictions on the testRDD using the best model.
7. Recommend top 5 artist names for a user.
  

References
---
[1] http://www-etud.iro.umontreal.ca/~bergstrj/audioscrobbler_data.html
