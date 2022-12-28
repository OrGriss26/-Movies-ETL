# Movies-ETL

This project was an introduction ot the EXTRACT, TRANSFORM, and LOAD process. Movie data from Wikipedia, Kaggle, and aggregated ratings was used to assemble a movie database from a clean dataset for a fictional hackathon.

As mentioned, the ETL process was used to extract the Wikipedia and Kaggle data from their respective files, transform the datasets by cleaning rows and formating datatypes, preforming joins, and loading the cleaned dataset into a SQL database.

## Overview

The goal of this analysis is to create automated pipeline that extracts, transform and loads data. This analysis consists of four parts, where each step is building up from beginning of extracting data and function testing, through transformation and cleaning process to its final step connect and load to the database. The entire process of ETL can be executed with a single call of the function extract_transform_load in the final step ETL_create_database.ipynb. The ETL process is broken down into four jupyter notebook files:

## Purpose

Create an ETL pipeline from raw data to a SQL database.
Extract data from disparate sources using Python.
Clean and transform data using Pandas.
Use regular expressions (Regex) to parse data and to transform text into numbers.
Load data with PostgreSQL and verify in PgAdmin.
The project included extracting a large data set from Kaggle, then transforming the data into a usable dataset for a "hacking competition." Once the data was transformed and narrowed in scope for the hack-a-thon, the DataFrames were loaded into PostgresSQL.


### ETL_function_test

Data is extracted from the website in JSON and CSV formats.
Data is transformed into Pandas data frames.
JSON file requires extra step – loading file first and then transforming into data frame.
ETL_clean_wiki_movies.ipynb
Function clean_movie combines scattered data of alternative languages into one column alt_titles.

Its subfunction change_column_name organizes column names into consistent pattern.

In the function extract_transform_load the transformation process of wiki movies data begins and includes:
- Python list comprehensions.
- apply() and map() methods in combination with lambda functions.
- regular expressions or RegEx.

### ETL_clean_kaggle_data

Function extract_transform_load gets new tasks for cleaning Kaggle data and includes:
- Changing datatypes, using methods pd.to_numeric, astype() and python comparison operators for Boolean types.
- Filling missing values and filtering unwanted columns.
- Merging data frames using pd_merge method.

### ETL_create_database

The function in its final step connects to the database by sqlalchemy library and to_sql method.
Complete ETL process can be executed with a single function extract_transform_load call.
