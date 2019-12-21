<p align="center">
  <img src="https://github.com/alextrambley/alex_trambley_oscars_capstone/blob/master/oscars_logo.jpg">
</p>

# Alex Trambley's Oscars Capstone
This is my Capstone project for the Data Analytics Cohort 1. I decided to focus on films that were nominated for the Best Picture Academy Award, and look at what makes a winner!

-----
# Sourcing the Data
![Oscars-DB-logo](https://github.com/alextrambley/alex_trambley_oscars_capstone/blob/master/oscars_database_logo.png)

## Academy Award Films - Gotta Get Em' All
> I first needed to find a list of all of the films that have been nominated by the Academy for any category during its history. 
> I sourced this search via a table I found on [another Github sourcing all of the Oscar winners from 1927 - 2017](https://datahub.io/rufuspollock/oscars-nominees-and-winners) that scraped the [Academy Awards Database website](http://awardsdatabase.oscars.org/).

-----

# Pairing The Awards Data With More Info
![omdb_logo](https://github.com/alextrambley/alex_trambley_oscars_capstone/blob/master/omdb_api_logo.png)

## OMDb API Is Where It's At
> From here I found the [OMDb API Database](http://www.omdbapi.com/) as a location that I could use to get information about each film > > including Genre, Release Data, Country of Origin, Language, Director, Actors, etc.

> This API is sourced using information found from [the IMDB official site](https://www.imdb.com/). 

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
> Then, I filtered out the categories associated with acting (any categories that included the letters "ACT" in the title) so that I could use this table as a source of nominations in categories other than Best Picture. I also did this same filtering for all of the other categories __NOT__ associated with acting as their own dataframe so that their values could be referenced against the Best Picture values in a separate table.
