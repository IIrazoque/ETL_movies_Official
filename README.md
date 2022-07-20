# ETL_movies_Official

## Deliverable 1:
Assist Amazing Prime with extracting, transforming, and loading 3 datasets then adding the clean dataset into PostgresSQL database.
Deliverable 1: Write an ETL Function to Read Three Data Files 
We created a function to read and retrieve datasets to convert them into DataFrames.  
		 def extract_transform_load (wiki, kaggle, ratings):

We used pd.read_csv(file_name, low_memory=False) function to convert the Kaggle metadata file to a Pandas DataFrame. The same function was applicable to ratings csv file. Our wiki JSON file was also converted.

*Figure1. Defining ETL function to read three files*

![This is an image]()

Showing all three dataframes wiki, Kaggle and ratings in Figures; 2, 3, 4.

*Figure 2 - wiki_movies_df*
![This is an image]()

*Figure 3 - Kaggle_metadata_df*
![This is an image]()

*Figure 4 - ratings_df*
![This is an image]()

## Deliverable 2: Extract and Transform the Wikipedia Data

In the first few steps we cleaned the wiki data by cleaning up the movie titles. Created a non-destructive copy and changed the movie titles into a new alternative tittles dictionary without changing the original data. We also cleaned up the columns names. Using the extract_transform_load function we were able to filter out for TV shows “Television series” and clean the “Box office”, “Budget”, “Release date”, “Running time” columns.  The cleaned wiki dataframe showin in figure 5. Figure 6 showing new column names.

*Figure 5 – Cleaned wiki_movies_df*
![This is an image]()

*Figure 6 – cleaned columns names in wiki_movies_df*
![This is an image]()

## Deliverable 3: Extract and Transform the Kaggle data

The same cleaning functions in wiki was used for the Kaggle dataset, but for Kaggle we dropped unnecessary columns such (e.g “adult”), set column values to numeric and converted dates to standard times. 
Wiki and Kaggle dataframes were merged (figure 7) to create and new dataframe called movies_df (figure 8). The combined columns were re-names, added missing values, dropped unnecessary columns to then merged with the ratings dataset.  

*Figure 7 – Merged wiki and Kaggle dataframes*
![This is an image]()

*Figure 8 – Merged dataframe movies_df*
![This is an image]()

*Figure 9 – Newest dataframe movie_with_ratings_df*
![This is an image]()

## Deliverable 4: Create the Movie Database
Lastly we added our new movies_df and rating dataframes into SQL database. Figure 10 & 11

*Figure 10 – movies_query.png*
![This is an image]()

*Figure 11 – ratings_query.png*
![This is an image]()


