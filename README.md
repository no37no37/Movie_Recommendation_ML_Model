# Movie Recommendation Machine Learning Project

## Introduction
The "Movie Recommendation Machine Learning Model" is designed to provide personalized movie recommendations based on user preferences. The model utilizes a dataset obtained from Netflix, containing information about movie titles, directors, cast, genres, and descriptions. By leveraging machine learning techniques, the model aims to enhance user experience by offering tailored suggestions.

## Data Preprocessing
The initial step involves cleaning the dataset by removing duplicate entries and handling null values. The relevant columns, such as 'director,' 'cast,' 'listed_in,' and 'description,' are combined into a new column named 'tags.' This consolidated information serves as the basis for identifying similarities between movies.

## Feature Extraction
To convert textual data into a format suitable for machine learning algorithms, the CountVectorizer from scikit-learn is employed. This process transforms the 'tags' into numerical vectors, allowing for the application of cosine similarity calculations.

## Cosine Similarity
The model utilizes cosine similarity to measure the likeness between movies based on their 'tags' vectors. Cosine similarity calculates the cosine of the angle between two vectors, providing a metric for their similarity. In this context, it helps identify movies with comparable themes, genres, and descriptions.

## Recommendation Function
A recommendation function is implemented to generate movie suggestions for a given title. By inputting a movie name, the function identifies the movie's index, calculates its similarity with others, and outputs a list of recommended titles along with their similarity percentages.

## Usage Example
For instance, calling the function with the movie 'Ganglands' may yield recommendations such as 'Dealer' with a similarity of 55.47%, 'Bangkok Breaking' with 54.13%, and others. Users can explore these suggestions to discover movies closely related to their preferences.

## Model Export
The model, along with the dataset and similarity matrix, can be exported using the pickle library. This enables the creation of a web application that incorporates the recommendation system for an interactive and user-friendly movie exploration experience.

By implementing this Movie Recommendation Machine Learning Model, users can enjoy a more personalized and engaging movie-watching journey based on their unique tastes and preferences.
