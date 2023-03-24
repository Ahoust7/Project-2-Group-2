# IMDB Scraping Project 
![1_f-bF79_zFHGXEhJvx2WPLg](https://user-images.githubusercontent.com/119638430/226774336-e070b73d-d4d3-4b6c-b489-f57fcc7a417a.jpg)

## Project 2 Information
  
  ### Resources We Used
  This project consisted of utilizing Beautiful Soup from the Python library to web scrape and pull data from IMDB.com. 
Data was uploaded to Mongo database. Pymongo via Python Library was used to create queries on our findings. 

   Data Scraped: ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt) and ["Top 1000 TV Shows"](https://www.imdb.com/search/title/?count=100&languages=en&num_votes=1000,&sort=num_votes,desc&title_type=tv_series)

  ### Our Process 
Beautiful Soup was used to pull details -- show title, year, rating, votes per show, stars from each show, and tv show genres -- from ["Top 1000 Movies"](https://www.imdb.com/search/title/?groups=top_1000&sort=user_rating,desc&count=100&start=108&ref_=adv_nxt) which can be denoted below.
![Screenshot 2023-03-23 211756](https://user-images.githubusercontent.com/118394753/227401596-50b3fd4a-4f28-4702-8057-d0769cf00964.png, width="48")

