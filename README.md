# Movie-Recommendation-System
 A Movie Recommendations system Project with Heroku Deployment

    This project will be an end to end development of a content based movie recommender system with cosine similarity.

Project Flow:
    DATASET -> PreProcessing -> Model Development -> Web Interface Development -> Deployment

DATASET :
    TMDB 5000 Movie Dataset
    https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

DATAFRAME AFTER PREPROCESSING:
Movie_id | Title | Tags

the previous columns overview,genres, keywords, cast and crew were merged to form the TAGS column.


TEXT VECTORIZATION

we need to compare the similarity within the 'tags' values to build the model.
In case of a numeric data it can be performed easily by mathematical function. One approach can be to find similar words be wouldn't be as effective. So we take the approach of vectorization.
We will convert the Textual data into vectors or in simpler terms, a coordinate on a 2D graph.
Upon vectorization, we can perform recommendation by comparing and selecting the nearest vector to any particular vector.

The technique we have used is know as BagOfWords where we combine and concatenate all the tags to form a large text.
From this large text we extract the words which appear most frequently.
We form a tabular records of keywords and their frequency for each movie.
These numbers will act as the cordinates for us to build a vector graph for our data.
(We will not include stop words in vectorization - i.e. a,in,as,to,is, etc.)

These graph will be in a 5000 dimensional space with each movie having its own dimensional vector.

