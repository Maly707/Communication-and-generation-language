# Communication-and-generation-language
Language one of the main tools we used as human beings to communicate, without language we will not be able to explain our needs feeling or even ours though. There are many languages in this world, but we still be able to communicate, English is ranked as first language in the world over 1.268 billion speak English, 369.7 million people speaks English as a first language while 898.4 million English speakers English is their second language. It doesn’t mean we speak the same language we will be able to understand each other well, there is some difficulty you will face like if this different generation or different education or where you come from. This study will focus in different generations, we will deep be looking at what is the difference between different generation by analyze the words each generation say and try to guess the age from the language or finding the best words we can use when we try to communicate with the other generation.


# Data collection
First part of the project was data collection, I did chose twitter over facebook or other social media for flexibility, the only issue I found in twitter API that they don’t share anything about the age or even the date of birth so I used Google to collect some celebrities profile with them twitter account and them date of birth, also I found more details it might be useful in other project or if decide to expand in this project like relative, place of birth, position, career …
<div><h4>Biography bar</h4></div>
<img src='https://github.com/Maly707/Communication-and-generation-language/blob/master/images/Capture.PNG' title='google search people bar'/>

For getting random profile I was just search by jobs or key word famous people.
After that from the list in the top I loop in each person to extract the information from his/her card.
And store all the data in csv file after the data scraping.

Also create twitter API to call twitter profile I found in them bio, I did filter after word the users without Twitter account or when I found his/her account not work or not been use or private.

<li><a href='https://developer.twitter.com/en'>Twitter Developer Portal</a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/TwitterAPI.ipynb'>Twitter API</a></li>


# week 4 Celebrities bio
In Week 4 we solve the issue we faced in week 3 twitter API does not retrieve birthdate or age, the going around by data scraping all the famous celebrity’s bios from google which provide date of birth and all the social media accounts the strong point of this solution is data is more trusted, the technology been used python Beautiful Soup.
Profiles been created for each celebrity with the data needed (birth date, social media links)
The data from week 3 been linked with the profiling record from week 4.
<a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/week%204%20Celebrities%20bio%20.ipynb'>week 4 Celebrities bio</a>

# Reference:<br>
•	https://pypi.org/project/tweepy/<br>
•	https://www.geeksforgeeks.org/python-api-get_status-in-tweepy/?ref=rp<br>
•	http://gettwitterid.com/?user_name=ddlovato&submit=GET+USER+ID<br>
•	https://groups.google.com/forum/#!topic/twitter4j/Nibyf30jIBs<br>
•	https://stackoverflow.com/questions/753052/strip-html-from-strings-in-python<br>
•	https://www.geeksforgeeks.org/python-string-replace/<br>
•	https://hackernoon.com/how-to-scrape-google-with-python-bo7d2tal<br>
•	https://developers.google.com/people<br>
•	https://realpython.com/beautiful-soup-web-scraper-python/<br>
