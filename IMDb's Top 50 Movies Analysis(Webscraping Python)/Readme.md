# IMDb's Top 50 Movies Analysis

The world of cinema holds an irresistible allure. They're captivated by the intricate tapestry woven behind the scenes – the years of planning, the mounting expenses, 
and the relentless creativity. All this effort condensed into a mere 1.5-hour movie.Yet, the audience's verdict is swift. In just a few moments, a movie's 
fate is sealed – whether it's captivating or mundane, authentic or fantastical, a source of inspiration or a letdown. The magic of cinema unfolds in a matter of minutes.

## Problem Statement 1
You have been tasked with creating a powerful movie analysis and review aggregator for a media company. The application should allow users to retrieve and display IMDb's Top 50 Movies. 
You will implement web scraping using Python's requests and BeautifulSoup libraries to gather information about the top 50 rated movies on IMDb and then perform additional operations on 
this data. And now, Sort the movie data by IMDb ratings in descending order. Create a list containing the top 5 movies with the highest IMDb ratings. Iterate through the top 5 movies and 
print their details, including movie name, IMDb rating, release year, votes, and genre.
                                      By following this, you will build a movie analysis and review aggregator that retrieves IMDb's top-rated movies and presents the top 5 movies 
with their key information. This application will help users discover highly-rated films quickly and efficiently.

We will also be using the concepts like:

- HTTP Requests
- Web Scraping using Beautiful Soup
- Data Extraction
- String Manipulation
- String Search and Matching
- Data Analysis and Classification

## Code Snippets:
 For extracting data from IMDB website using BeautifulSoup
~~~
    import requests
from bs4 import BeautifulSoup

url = "https://www.imdb.com/search/title/?groups=top_250&sort=user_rating"

response = requests.get(url)
print(response.status_code)

soup = BeautifulSoup(response.content,"html.parser")

movies_list = soup.findAll("div",("class_","lister-item mode-advanced"))

movie_list= {}

for i in movies_list:
  movie_data = {}
  movie_data["ranking"]=i.h3.span.text.strip(".")
  movie_data["name"]=i.h3.a.text
  movie_data["year"]=i.h3.find("span", class_="lister-item-year").text.strip("()")
  movie_data["imdb_rating"]=float(i.find("strong").text)
  movie_data["votes"]=i.find("span", attrs = {"name":"nv"}).text
  movie_data["genre"]=i.find("span", class_="genre").text.strip(" \n ")
  movie_list[i.h3.a.text]=movie_data
print(len(movie_list))
print(movie_list)
~~~

For Sorting Movies according to the ratings
~~~
sorted_list = sorted(movie_list.items(), key=lambda x: x[1]['imdb_rating'], reverse=True)
print(sorted_list)
top_5movies = sorted_list[:5]
print(top_5movies)
for movie_name, movie_info in top_5movies:
    print(f"Movie: {movie_name}")
    print(f"IMDb Rating: {movie_info['imdb_rating']}")
    print(f"Year: {movie_info['year']}")
    print(f"Votes: {movie_info['votes']}")
    print(f"Genre: {movie_info['genre']}")
    print("=" * 30)
~~~

