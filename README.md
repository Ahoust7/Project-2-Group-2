# IMDB Scraping Project 
![1_f-bF79_zFHGXEhJvx2WPLg](https://user-images.githubusercontent.com/119638430/226774336-e070b73d-d4d3-4b6c-b489-f57fcc7a417a.jpg)

## Project 2 Information
  
  ### Resources We Used
  This project consisted of utilizing Beautiful Soup from the Python library to web scrape and pull data from IMDB.com. 
Data was uploaded to Mongo database. Pymongo via Python Library was used to create queries on our findings. 

   Data Scraped: ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt) and ["Top 1000 TV Shows"](https://www.imdb.com/search/title/?count=100&languages=en&num_votes=1000,&sort=num_votes,desc&title_type=tv_series)

  ### Our Process 
  #### TV Shows
Beautiful Soup was used and a loop was used to pull details -- show title, year, rating, votes per show, stars from each show, and tv show genres -- from ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt)
  Our code can be denoted here:
  ![Screenshot 2023-03-23 211756](https://user-images.githubusercontent.com/118394753/227401596-50b3fd4a-4f28-4702-8057-d0769cf00964.png)
  
  Following, we cleaned up our data by (a) separating year range into two columns, (b) dropping the year range, (c) and removing extra characters (roman numerals and spaces)
  
  (a) ![Screenshot 2023-03-23 213934](https://user-images.githubusercontent.com/118394753/227402738-29c0a6fe-ef6e-449e-a2be-d5520e8a0f74.png)
  (b) ![Screenshot 2023-03-23 213924](https://user-images.githubusercontent.com/118394753/227402665-ea4bcdd1-19cc-4325-8ce0-bb428ce90f90.png)
  (c) ![Screenshot 2023-03-23 213948](https://user-images.githubusercontent.com/118394753/227402863-fc1306a2-d21a-4771-b532-007e57633563.png)

  Data was re-formatted where some of the data types were changed to fit our interest - differentiating between start and end dates of how long tv series ran
  
  (a) ![Screenshot 2023-03-23 224232](https://user-images.githubusercontent.com/118394753/227411187-1dbbcea2-0750-47d8-9281-11af34750b14.png)
  
  (b) ![Screenshot 2023-03-23 224248](https://user-images.githubusercontent.com/118394753/227411210-27e94492-bdee-49a4-ba84-39bd0e1bddb8.png)

  
  After the rest of the data was cleaned, the DataFrame was converted to a ["CSV file"](imdb_top_1000_TV_Final.csv). ![Screenshot 2023-03-23 214702](https://user-images.githubusercontent.com/118394753/227403554-f05939c1-7543-4114-9e20-92aca9e7f068.png)

  For our queries in MongoDB, the CSV file was then brought back into Python library to spit out a ["JSON file"](imdb_top_1000_TV_final.json).
    ![Screenshot 2023-03-23 214656](https://user-images.githubusercontent.com/118394753/227403528-e836edc1-710d-43e2-8907-baaa0b1ce7de.png)
    
 #### Movies
The same process was done to [clean up](imdb_top_1000_movies_final.ipynb) and spit out the data from a CSV file into a JSON for ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt) 

In addition to the same clean up and reformatting process, a drop of the 'Gross' column was made. 
![Screenshot 2023-03-23 225710](https://user-images.githubusercontent.com/118394753/227412852-e2b35767-6d5b-44bd-bdb4-06eb24795929.png)

### [Data Analysis](imdb_MongoDB.ipynb)
Data was converted from CSV to JSON to be consistent with our use of MongoDB for further data analysis. Queries were made to display our analyses.
