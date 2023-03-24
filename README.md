# IMDB Scraping Project 
![1_f-bF79_zFHGXEhJvx2WPLg](https://user-images.githubusercontent.com/119638430/226774336-e070b73d-d4d3-4b6c-b489-f57fcc7a417a.jpg)

## Project 2 Information
  
  ### Resources We Used
  This project consisted of utilizing Beautiful Soup from the Python library to web scrape and pull data from IMDB.com. 
Data was uploaded to Mongo database. Pymongo via Python Library was used to create queries on our findings. 

   Data Scraped: ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt) and ["Top 1000 TV Shows"](https://www.imdb.com/search/title/?count=100&languages=en&num_votes=1000,&sort=num_votes,desc&title_type=tv_series)

  ### Our Process 
  #### TV Shows
Beautiful Soup was used to pull details -- show title, year, rating, votes per show, stars from each show, and tv show genres -- from ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt)
  Our code can be denoted here:
  ![Screenshot 2023-03-23 211756](https://user-images.githubusercontent.com/118394753/227401596-50b3fd4a-4f28-4702-8057-d0769cf00964.png)
  Following, we cleaned up our data by (a) separating year range into two columns, (b) dropping the year range, (c) and removing extra characters (roman numerals and spaces)
  (a) ![Screenshot 2023-03-23 213934](https://user-images.githubusercontent.com/118394753/227402738-29c0a6fe-ef6e-449e-a2be-d5520e8a0f74.png)
  (b) ![Screenshot 2023-03-23 213924](https://user-images.githubusercontent.com/118394753/227402665-ea4bcdd1-19cc-4325-8ce0-bb428ce90f90.png)
  (c) ![Screenshot 2023-03-23 213948](https://user-images.githubusercontent.com/118394753/227402863-fc1306a2-d21a-4771-b532-007e57633563.png)


