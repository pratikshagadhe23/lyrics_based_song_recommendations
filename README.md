# Lyrics Analysis and Song Recommendation System

## Overview
This project involves analyzing song lyrics and generating recommendations based on textual similarities. Utilizing Natural Language Processing (NLP) and Word Embeddings, the system performs exploratory data analysis (EDA), cleans and processes lyrics, and provides song recommendations based on user input. The key components of this project include data processing, sentiment analysis, and visualization using word clouds and t-SNE plots.

* DATASET Source: https://www.kaggle.com/datasets/deepshah16/song-lyrics-dataset/data*

- **Data Collection**: Aggregating song lyrics from multiple CSV files.
- **Text Processing**: Cleaning and preprocessing the lyrics for analysis.
- **Word2Vec Model**: Training a Word2Vec model to generate word embeddings.
- **Recommendation System**: Using the trained model to recommend songs based on input lyrics.
- **Visualization**: Creating visualizations to understand the distribution of song lengths, popular artists, and word embeddings.

## Table of Contents

1. [Getting Started](#getting-started)
2. [Data Preparation](#data-preparation)
3. [Word2Vec Model](#word2vec-model)
4. [Song Recommendation](#song-recommendation)
5. [Visualization](#visualization)
6. [Dependencies](#dependencies)

## Project Structure 
1. Data Loading and Preparation
- Mount Google Drive
- Load CSV files containing song data
- Combine multiple CSV files into a single DataFrame
- Filter and clean the data
- The project uses CSV files containing song lyrics. These files should be placed in the sample_data/csv directory. The CSV files are expected to have the following columns:
       * Artist: The name of the artist.
       * Title: The title of the song.
       * Lyric: The lyrics of the song.
- The data is loaded from the CSV files and combined into a single DataFrame. The lyrics are then cleaned to remove stop words and punctuation.
  
2. Data Processing
- Word2Vec Model Training
- Train a Word2Vec model using song lyrics
- Lyric Cleaning
- Remove stopwords and punctuation from lyrics
- Perform custom cleaning for common lyrics terms

3. Recommendation System
- Compute similarities between input lyrics and stored lyrics using Word2Vec embeddings
- Generate and display the top 5 recommended songs
- The recommendation system uses the trained Word2Vec model to provide song recommendations based on user-input lyrics. It calculates the similarity between the input lyrics and the lyrics of songs in the dataset and returns the top 5 most similar songs.

4. Exploratory Data Analysis (EDA)
- Visualize song length distributions
- Show the distribution of top artists
- Create a word cloud of the cleaned lyrics

5. Visualizations

- Word Cloud: Display the most common words in the lyrics
- t-SNE Plot: Visualize the Word2Vec embeddings in 2D space
- The project includes various visualizations to understand the data better:
     * Word Cloud: A word cloud of the most common words in the lyrics.
     * Distribution of Song Lengths: A histogram showing the distribution of song lengths.
     * Top Artists: A bar plot showing the top 10 artists by the number of songs.
     * Word Embeddings Scatter Plot: A t-SNE scatter plot of word embeddings for selected words.


## Word2Vec Model 
- A Word2Vec model is trained using the cleaned lyrics. This model generates word embeddings that capture the semantic meaning of words in the context of the lyrics.
- Training the Model
- The Word2Vec model is trained with the following parameters:
     * vector_size: 100
     * window: 5
     * min_count: 1
     * workers: 4

## Dependencies 
This project requires the following Python libraries:

- pandas
- numpy
- matplotlib
- seaborn
- gensim
- nltk
- wordcloud
- sklearn

## Results 
- Word Cloud: Shows the most frequently occurring words in the lyrics.
- t-SNE Plot: Visualizes the distribution of word embeddings in a 2D space.
- Recommendations: Provides a list of top 5 recommended songs based on the input lyrics.

## Future Work 
- Enhance Recommendations: Implement more advanced recommendation algorithms.
- Expand Dataset: Incorporate additional datasets for more comprehensive analysis.
- Improve Visualizations: Add more interactive visualizations for deeper insights.
