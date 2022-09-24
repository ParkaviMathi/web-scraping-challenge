# web-scraping-challenge
In this assignment, I'll be scrapping information from Mars-related websites and analyse it with Pandas.

This assignment is divided into two parts:
1.Scrapping Mars News
2.Scrapping and Analysing Mars Weather Data

## Part  1: Scrapping Mars News
The initial scraping is completed using Jupyter Notebook, Splinter, and BeautifulSoup.

.A Jupyter Notebook file called mars_data_challenge_part_1.ipynb. has been created.This file is used to complete all the scraping and analysis tasks. 

.The Mars News Site is scraped using the automated browser and BeautifulSoup.

.Specifically, the title and preview of each article is scrapped. Chrome DevTools was used to inspect the page to identify which elements to scrape.

.The results are stored using Python data structures. Each pair of an article's title and preview has been stored in a Python dictionary, e.g. {'title': "Mars Rover Begins Mission!", 'preview': "NASA's Mars Rover begins a multi-year mission to collect data about the little-explored planet."}. Note that each dictionary has two keys: title and preview. The title and preview text of each article are stored in a dictionary. The dictionaries, in turn, are stored inside a Python list. The list is printed in the Jupyter notebook.


## Part 2: Scrapping and Analysing Mars Weather Data
Using the scraping skills, an HTML table of Mars weather data has been extracted.Pandas and Matplotlib was used to clean, visualise, and analyse the data.


A Jupyter notebook was created and named as mars_data_challenge_part_2.ipynb.The relevant dependencies for web scraping was imported. 


Automated browser was used to visit the Mars weather site. The URL is https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html


The data in the HTML tablewas scrapped using Pandas's read_html method. 


The scraped data was assembled into a Pandas DataFrame. Here is an explanation of the column headers.

id: The identification number of a single transmission from Curiosity.
terrestrial_date: The date on Earth.
sol: The number of elapsed sols (Martian days) since Curiosity landed on Mars.
ls: The solar longitude.
month: The Martian month.
min_temp: The minimum temperature, in Celsius, of a single Martian day (sol).
pressure: The atmospheric pressure in Curiosity's location.



The data types of all DataFrame columns was examined and cast (convert) to appropriate datetime, int or float data types. Pandas's astype and to_datetime methods were used to accomplish this task.

The follwing questins were answered by analysing the Scrapped data.
1.How many months are there on Mars?


2.How many Martian (not Earth) days' worth of data are there in the scraped dataset?


3.What are the coldest and warmest months on Mars (at the location of Curiosity)? The answer was obtained by averaging the minimum daily temperature of each month and the results were plotted as a bar plot.


4.Which months have the lowest and highest atmospheric pressure on Mars? The answer was obtained by averaging the daily atmospheric pressure of each month and the results were plotted as a bar plot.


5.Approximately how many terrestrial (earth) days are there in a Martian year? In other words, in the time that Mars circles the Sun once, how many days elapse on the Earth? The result was estimated visually by plotting the daily minimum temperature.


The DataFrame was exported to a CSV file.
