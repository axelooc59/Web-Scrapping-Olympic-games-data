# Web-Scrapping-Olympic-games-data

### Topic: How I scpraped data for the Tokyo 2020 Olympic Games?

For my job at ACSSI, we wanted to create a Qlik Sense app showcasing Olympic games data. Unfortunately, we only had data since 2016. So, I had the idea to scrape the data from the official Olympic games website, https://olympics.com/fr/olympic-games, for which I used Python with mainly two libraries: requests_html and Selenium.

I had two main cases to get all the data from every event. The first one could be handled more efficiently than the second one. The first case was the individual event, while the second one was the team event.

The difference between these two cases is that in the second one, we had to extend every item of the list to generate the HTML source for athletes' names; otherwise, it wouldn't be in the source. I could not do that using requests_html, so I switched to Selenium to extend their items by clicking on them.

Before scraping, we obviously needed URLs. I figured out the pattern of their URLs and generated them. Eventually, I categorized them automatically based on team/individual events.

For the individual case event, the scraping process was as follows:

* Request the current link
* Parse the HTML source using BeautifulSoup
* Search nodes of interest (name, country, result) and iterate through them
* Calculate the position in the event
* Add each item to the lists
* Convert the lists to a CSV file

For the team case event, the difference was that I had to extend the items. For that, I used an automated browser called Selenium and clicked automatically on the items that needed to be extended to reveal the source of athletes' names. After all items were extended, the process was the same as above.


You can see the result in dataInd2.csv and dataTeam2.csv
Don't forget to leave a start if you liked my project !





