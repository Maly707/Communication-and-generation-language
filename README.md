# Communication-and-generation-language
Language one of the main tools we used as human beings to communicate, without language we will not be able to explain our needs feeling or even ours though. There are many languages in this world, but we still be able to communicate, English is ranked as first language in the world over 1.268 billion speak English, 369.7 million people speaks English as a first language while 898.4 million English speakers English is their second language. It doesn’t mean we speak the same language we will be able to understand each other well, there is some difficulty you will face like if this different generation or different education or where you come from. This study will focus in different generations, we will deep be looking at what is the difference between different generation by analyze the words each generation say and try to guess the age from the language or finding the best words we can use when we try to communicate with the other generation.


# Data collection
First part of the project was data collection, I did chose twitter over facebook or other social media for flexibility, the only issue I found in twitter API that they don’t share anything about the age or even the date of birth so I used Google to collect some celebrities profile with them twitter account and them date of birth, also I found more details it might be useful in other project or if decide to expand in this project like relative, place of birth, position, career …
<div><h4>Google search biography bar</h4></div>
<img src='https://github.com/Maly707/Communication-and-generation-language/blob/master/images/Capture.PNG' title='google search people bar'/>

<div style='style="text-align: center;"'>
<h4>Google search biography information card</h4>
<img src='https://github.com/Maly707/Communication-and-generation-language/blob/master/images/bio%20bar.PNG' title='google search people bar' height="400"/>
<br>
</div>
For getting random profile I was just search by jobs or key word famous people.
After that from the list in the top I loop in each person to extract the information from his/her card.
And store all the data in csv file after the data scraping.

Also create twitter API to call twitter profile I found in them bio, I did filter after word the users without Twitter account or when I found his/her account not work or not been use or private.

<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/scrapingGoogleSearch.ipynb'>Code for data scraping the bio information from google search.</a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/Celebrities%20bio.csv'>bio data after scrapping and formatted </a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/TwitterAPI.ipynb'>Twitter API</a></li>
<li><a href='https://developer.twitter.com/en'>Twitter Developer Portal</a></li>
<hr><br>

# Link data
In this stage I linked the user profile using his google bio to twitter account by looping over google profiling collected from scraping and use the twitter account in the bio information to get most his tweets from his/her account, the only challenge here I takes long time since twitter strict them API call with number of calls before go sleep for 15 min. to be able to place any new call.

The data been stored in csv file to save time from calling the API my account authentication is included in the code to be able to use it for testing.
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/extractUserProfileAndTweets.ipynb'>Code to extract the data from the profiling and link it with twitter account. Repeating the code to catch any network failed records</a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/data.csv'>The profiling data after added generation column with excel</a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/tweetsData.csv'>All the tweets for all users with generation column </a>this file will save a lot of time for you since generate this file may take over 5 h estimated</li>
<hr><br>

# Data analysis and discover:
Start to discover the data and group the data with generation groups which was:

<li>30s	People who born from 1930 to 1939</li>
<li>40s	People who born from 1940 to 1949</li>
<li>50s	People who born from 1950 to 1959</li>
<li>60s	People who born from 1960 to 1969</li>
<li>70s	People who born from 1970 to 1979</li>
<li>80s	People who born from 1980 to 1989</li>
<li>90s	People who born from 1990 to 1999</li>
<li>00s	People who born from 2000 and after</li>

These groups been generated from date of birth it is not in the code because I did use excel to generate this column

The column been added to the csv file to save the time for later
Also generate graph to compare between percentage of the user per generation and tweets per generation.


<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/DataDiscovery.ipynb'>Comparison between user percentage and tweets per generation</a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/data.csv'>The profiling data after added generation column with excel</a></li>
<hr><br>

# Data cleansing:
It was one of the important process where deleted the duplicate profiles duplicate tweets for same user also clean the text from image, links, emojis, mentions, spaces and punctuations

Also delete the empty tweets after the cleanup. 

<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/dataCleansing.ipynb'>Comparison between user percentage and tweets per generation</a></li>
<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/wordMatrix.csv'>The profiling data after added generation column with excel</a></li>
<hr><br>


# Data preparation, model and testing:
One of the long processors is break sentences to words where take each sentence and break it to word and classify it in which generation if it new word will be added if it was before it will add to the number.

<div style='style="text-align: center;"'>
<h4>Word matrix example</h4>
<img src='https://github.com/Maly707/Communication-and-generation-language/blob/master/images/wordMatrix.PNG' title='Word matrix example' height="400"/>
<br>
</div>
After words create the model based on this table and train and test the model.

<li><a href='https://github.com/Maly707/Communication-and-generation-language/blob/master/dataModeling.ipynb'>The code for prepare the data for the model and create train and test the model</a></li>
<hr><br>

# Reference:<br>
<li>https://pypi.org/project/tweepy/</li>
<li>https://www.geeksforgeeks.org/python-api-get_status-in-tweepy/?ref=rp</li>
<li>http://gettwitterid.com/?user_name=ddlovato&submit=GET+USER+ID</li>
<li>https://groups.google.com/forum/#!topic/twitter4j/Nibyf30jIBs</li>
<li>https://stackoverflow.com/questions/753052/strip-html-from-strings-in-python</li>
<li>https://www.geeksforgeeks.org/python-string-replace/<br>
<li>https://hackernoon.com/how-to-scrape-google-with-python-bo7d2tal</li>
<li>https://developers.google.com/people</li>
<li>https://realpython.com/beautiful-soup-web-scraper-python/</li>
<li>https://towardsdatascience.com/solving-a-simple-classification-problem-with-python-fruits-lovers-edition-d20ab6b071d2</li>

