# Data_Mining_Project
***

## Web Scraper

### Program description:
***

This program scrapes Metacritic's website for data regarding gaming. There are 182 pages on Metacritics gaming rank, each page contains 100 games from highest to lowest Metacritic ranking. This web_scraper is capable of scraping the following data from each game: Link, Rank, Title, Date (release), Platform, Meta Score, and User Score. Additionally, this program can also return the first result of a query on Youtube of the games trailer using a google data API. The user can choose how many web pages you request to scrape as well as which data to scrape for.

### Usage:
***
To run the Web_Scraper from the command line, the following initial input must be given:
```
python /web_scraper.py --n <numbers of pages to scrap> --cat <categories to scrap>
```
Where 'numbers of pages to scrape' must be an integer from 1 to 182. If no value is passed, it will scrape 1 page by default.

'Numbers of pages to scrape' are not case sensitive and their input order does not affect results. The input categories must be separated by " ".
If no values are passed, it will scrape Title and Rank by default.


See below an example:
```
python /web_scraper.py --n 10 --cat Rank Title Date
```
This command would result in the web_scraper scraping 10 webpages for the categories _Rank_, _Title_ and _Date_.

### Data description:
***

The Entity Relationship Diagram contains four tables, see below the diagram:

![title](ERD.png)

The description of all the categories is below:

| Category | Description |
| ------ | ------ |
| Link | Returns the game's Metacritic website URL |
| Rank| The game's Metacritic ranking score. |
| Title| The game's title. |
| Date | Date of release of the game |
| Platform| The platform in which the game runs on. |
| Meta_Score | Meta_Score is Metacritics score given by professional reviews. |
| User_Score | User_Score is the score given by users on Metacritic. |
| Youtube_Link | The game's trailer as per the first result of a youtube query. * |

*Requires a google API key by the user.

### Installation:
***
Besides installing the requirements file to their virtual enviroment the user must create an API key at https://console.cloud.google.com/apis and add the key to the conf file variable API_KEY (string format) in order to run the 'Youtube_Link' feature.


### Authors:
***

__Andre Gutnik__ & __Brian Troib__