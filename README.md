# Movies-ETL

## Overview
This project involved extracting and transforming movie and rating data from Wikipedia, Kaggle, and MovieLens using Jupyter Notebooks, Pandas, and Python, and then loading a merged dataframe into PostgreSQL. This ETL process was done to develop an algorithm to predict which low-budget movies being released will become popular.

## Analysis
The data for this analysis was extracted through scrapes from Wikipedia and Kaggle. Because the scraped Wikipedia data was saved in the JSON format, it needed to be loaded in as a list of dictionaries. The Kaggle dataset, which contained over 20 million ratings from MovieLens, was saved as a .csv file and was pulled into a Pandas DataFrame directly.
The transformation of the data involved a lot of data cleaning to get the data into a useable format to merge and move to PostgreSQL.
Upon initial inspection of the Wikipedia data, there were many duplicate columns and even TV shows included. List comprehensions were created to filter the data so that it only showed movies. A function was created for clean movies to combine alternative titles and languages and to rename columns. Functions were also created to iterate through the clean movies and clean the data by dropping unnecessary rows and columns, filling in NaNs, and formatting values.
Finally, a connection was created to PostgreSQL to save the combined movies dataframe to a database.

## Summary
Although the initial Wikipedia and Kaggle movie data were in bad shape, the ETL process helped to clean out all of the bad data and transform the rest into a useable merged dataframe to analyze the movies and associated ratings. An automated pipeline was created that takes in new data, performs appropriate transformations, and loads the data into the existing tables on PostgreSQL.
