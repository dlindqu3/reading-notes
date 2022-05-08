# Code 401 Reading Notes 
### 17. Read: 17 - Web Scraping  

- "Web scrape with python in 4 minutes" is not freely available 

####  source: "Web scraping" [link](https://en.wikipedia.org/wiki/Web_scraping)
- typically refers to a bot or web crawler using automated http requests to scrape online data 
- fetch from a page then extract from it 
- newer forms of scraping grab live data sent from server to the website 
- you can use regex and text pattern matching to find certain data

####  source: "How to scrape websites without getting blocked" [link](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)
- a site might list its policies on /robots.txt
- to avoid detection, scrape via proxies
- rotate user agents and http headers 
- avoid scraping behind a login

####  source: "Build a Python App that Tracks Amazon Prices!" [link](https://www.youtube.com/watch?v=Bg9r_yLk7VY)

```python 
pip install requests bs4
from bs4 import BeautifulSoup
import smtplib #deals with emails

URL ='<url to scrape here>'

headers = {"User-Agent": '<search for and paste your user agent here>'}

page = requests.get(URL, headers=headers)

soup = BeautifulSoup(page.content, 'html.parser')

#this will print tons of data, need to pull out useful stuff
print(soup.prettify())

#search for specific data ex: 
title = soup.find(id="productTitle").get_text().strip()

print(title)


```

#### Things I want to know more about 
- beautiful soup 