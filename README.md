# Web-Scrapping-Olympic-games-data

For my job at ACSSI, we wanted to create a Qlik Sense app showing Olympic games data. Unfortunatelly, we  just have found data since 2016... 
So I had the idea to scrap them from this website (official Olympic games website I think) : https://olympics.com/fr/olympic-games.

For that I used Python with mainly two librarys : requests_html and selenium.



I had two main cases, to get all the data from every event . 

The first one could be handle more efficiently than the second one.
The first case was the individual event.The second one, team event.


The difference between this two cases is that in the second one we had to extend every item of the list to generate the html source for Athletes otherwise it won't be in source.I could not do that using resquests_html so I switch using Selenium in order to extend their items by clicking on them.

Before scrapping, we obviously need urls. I figure it out the pattern of theirs urls and generated them. Eventually I categorize them automatically in function of Team/Individual event.

For the indivdual case event the scrapping process was this one :
* Request the current link
* parse html source using BeautifulSoup
* search nodes of interest (name,country,result) and iterate them
* calculate position in the event
* adding each items in list
* Convert list in csv file







