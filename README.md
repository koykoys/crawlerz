## SCRAPING PROCESS

1. The crawler will require user to input username, password and search phrase that will be used on searching profiles on m.ok.ru
2. Login will be initiated using POST method on the website.
3. After a successful login, crawler will automatically use the search phrase that has been supplied by the user.
4. Search process will be executed using GET method on the website.
5. On the results page, only the first 2 profiles will be scraped(as per request of Oren) and basic information will be parsed.
6. The 5 basic information that will be parsed will be profile name, age, birhtday, city and country.
7. After scraping information, the data will be automatically stored on MongoDB using the pipeline class of scrapy.

## RUNNING THE CRAWLER W/ PARAMETERS
* python file = "OKru_Crawler.py"
* crawler name = "spidey"
* username variable = "uname"
* password variable = "passwrd"
* search phrase variable = "keyphrase"

1. Open Terminal
2. Navigate to "spiders" directory using "cd" command
3. To pass the username, password and search phrase parameters, after the comand "scrapy crawl spidey", we will need to add the syntax "-a" following the prameter name and its value.

2. This will be the format of the whole command line:
	
	scrapy crawl spidey -a uname=your_username -a passwrd=your_password -a keyphrase=keyword_for_searching
