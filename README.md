# Movies-ETL
ETL with Pandas and SQL

## Tools
- PostgreSQL version 12.9
- pgAdmin 4 version 6.1
- Jupyter Notebook version 6.4.6

## Overview
Movies-ETL creates a function that takes in three files (in .csv and .json formats), extracts, transforms and loads the data into a PostgreSQL database.  Wikipedia, and MovieLens Kaggle are the source of data. 

The three data files are loaded into dataFrames. Using regex and python, unnecessary columns are dropped, IDs are extracted out of urls, and date fields are converted to standard formats, monetary fields are normalized, and additional data fields are cleaned.

The dataFrames are then merged and duplicate columns are removed.

Finally the merged dataFrame is loaded into a postgres "movie_data" database using SQLAlchemy.  The raw ratings .csv file containing 26,024,289 is loaded into postgres as well. 


