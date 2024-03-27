# Data Preparation for a Recommendation System
## Access the New York Times API
Constructed the query_url correctly to access The New York Times API.

Created an empty list called reviews_list to store the extracted data.

Implemented a for loop to iterate 20 times, with a 12-second interval between queries.

Handled exceptions using a try-except clause to continue the loop and print page numbers with no results.

Successfully retrieved and stored JSON data from The New York Times API. Converted the extracted data into a Pandas DataFrame, extracted the title and converted the "keywords" column to string data.

Created a list of titles extracted from the DataFrame.

## Access The Movie Database API
Prepared an empty list called tmdb_movies_list and a variable request_counter for API requests.

Implemented a for loop to iterate through the titles list, sending GET requests to The Movie Database API and retrieving JSON results.

Handled exceptions to print statements when a movie is not found and continued processing for successful results.

Extracted movie details including genre names, spoken languages, production countries, and created a dictionary for each movie.

Appended the results to the tmdb_movies_list list and previewed the first five results in JSON format.

Converted the results into a Pandas DataFrame named tmdb_df.

## Merge and Clean the Data for Export
Merged The New York Times reviews and TMDB DataFrames on the "title" column. Created lists to store columns requiring data type conversion and characters to remove.

Converted columns to string data type and removed unwanted characters using Pandas str.replace() method.

Dropped the "byline.person" column, removed duplicate rows, and reset the DataFrame index.
Exported the cleaned DataFrame to a CSV file without the index.
## Findings
Overall, the data preparation process involved accessing and extracting data from The New York Times API and The Movie Database API, merging the data, cleaning it by converting data types, removing unwanted characters, and exporting the final cleaned data to a CSV file for use in a recommendation system.
