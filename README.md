<p align="center">
  <img src="https://github.com/alextrambley/alex_trambley_oscars_capstone/blob/master/oscars_logo.jpg">
</p>

# Alex Trambley's Oscars Capstone

### Project Summary
This project will look at the historical data of all films that have been nominated for an Academy Award (Oscar), and attempt to determine if there are any trends or patterns that may drive a film toward being more likely to win the Best Picture award. Looking at different associated factors of each film, and pairing with outside data, I plan to pitch a “sweet spot” film that has the best theoretical chance to be nominated, and win, a Best Picture Oscar. Given my knowledge of the recent history of this category, I expect that there will be some genres and categories that are often ignored by the Academy when choosing a winner, while other factors like release date (time of the year) and film/title length may have less of an effect.

### Motivation
I chose this project as I have recently gained a love for film and appreciation all of the different aspects associated with films and film creation. The Academy Awards, or Oscars, as they are frequently called, are considered by some to be the quintessential award showcasing the quality and achievement within a year of film. One of the more interesting aspects of the Oscars is not only examination of the films nominated, but why specific films win over others. Could you have an absolute masterpiece film loved by all, but because it is a certain genre that it may have less of a chance to win Best Picture? These are the questions that I want to answer!

### Data Question
Are there factors that can be used to determine the likelihood (or lack thereof) of a film winning an Oscar? Things like category/genre, film length, title length, country of origin, release date, etc. Are there trends with the winners that could inform a film maker or a film production company on how they could craft a winner? Also, does being nominated in other categories increase the likelihood of winning?

### Data Struggles
Some sources of difficulty within this project were contained within the data sourced and compared between multiple sources. I often had to change formatting like dates and titles so that the separate sources could be linked to one another via table joins, etc.. Much of the time of this project was spent trying to format the data correctly so that tidy versions of the data could effectively be visualized in the final product.

## Tools Used
* Excel
* Python
* Tableau

-----
# Sourcing the Data
![Oscars-DB-logo](https://github.com/alextrambley/alex_trambley_oscars_capstone/blob/master/oscars_database_logo.png)

## Academy Award Films - Gotta Get Em' All
I first needed to find a list of all of the films that have been nominated by the Academy for any category during its history. 
I sourced this search via a table I found on [another Github sourcing all of the Oscar winners from 1927 - 2017](https://datahub.io/rufuspollock/oscars-nominees-and-winners) that scraped the [Academy Awards Database website](http://awardsdatabase.oscars.org/).


# Pairing The Awards Data With More Info
![omdb_logo](https://github.com/alextrambley/alex_trambley_oscars_capstone/blob/master/omdb_api_logo.png)

## OMDb API Is Where It's At
From here I found the [OMDb API Database](http://www.omdbapi.com/) as a location that I could use to get information about each film including Genre, Release Data, Country of Origin, Language, Director, Actors, etc.

This API is sourced using information found from [the IMDB official site](https://www.imdb.com/). 

-----
# Working With The Data

To start working with the data, I imported my complete films table into a Jupyter Notebook using Python. I then filtered out the films by category, searching by the categories associated with "Best Picture". This included:
<b>
* BEST PICTURE
* OUTSTANDING PICTURE
* OUTSTANDING PRODUCTION
* OUTSTANDING MOTION PICTURE
* BEST MOTION PICTURE
</b>
This was necessary as the names of the categories changed over time. 

-----
Then, I filtered out the categories associated with acting (any categories that included the letters "ACT" in the title) so that I could use the remaining categories for comparison within the final Tableau project.

After obtaining the list of films nominated for the Best Picture (or associated name) award, I then created a function within Python to pull all of the information for each film from the OMDb API. During this process, I discovered that there were some films that either had naming or release year issues when referencing the OMDb API. To remedy this, as part of the function I created, an "error" list was generated so that I could manually address any film titles that did not work with a normal pull.

With the error list I had to manually check the film release year against IMDb and make sure that I had the correct film and IMDb ID. This was done with about 45 films.

Now that the error list was completed and fixed, I was able to start cleaning up the data frames within Python to include a new piece of information, release month, as well as trimming down categorical variables like Language, Country, Genre, and more. These changes were completed by going back and forth between Python and Excel with the Python generated CSVs.

# Working in Tableau

To visualize and present the findings of the data, I chose to use Tableau. I felt that Tableau was a great tool to showcase the data in an interactive format (instead of a Powerpoint) that could also be easily shared and accessible to anyone.

## [Click here to see the findings of my project, and what a great "Best Picture" contender looks like!](https://public.tableau.com/profile/alex.trambley#!/vizhome/alex_trambley_oscars_capstone/Dashboard1?publish=yes)
