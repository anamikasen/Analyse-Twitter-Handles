# Analyse-Twitter-Handles
A jupyter notebook implementation of analysing Barack Obama's tweets.
##### In this project, I have tried analysing the tweets by Barack Obama. 
The project uses Tweepy API for fetching the tweets.
###### The project is divided into 6 different parts as follows. Most of the explanation is done in the jupyter notebook. This section gives an overview of each.
____

##### Part 1: Setting up Twitter API
The Twitter API is set here using Tweepy. API keys can be obtained by going to  https://apps.twitter.com/. It is necessary to have a Twitter account in order to obtain keys. 
Store the API keys in the credentials.py. It is a good practice to keep the keys in a separate file.
____

##### Part 2: Exploring Tweepy built-in methods
The Tweepy API contains many built-in methods which can be used effectively. The project tries getting the number of tweets done by a handle using 'statuses_count()'

Interestingly, as of today (06/03/2018) Kanye West has tweeted 407 times. For more information, refer to Tweepy documentation: http://docs.tweepy.org/en/v3.5.0/api.html
____

##### Part 3: Get Tweets
A method is defined to receive tweets by passing the Twitter handle as the argument. This method gathers the most recent 400 tweets of Barack Obama.

A dataframe with attributes I found relevant for some analysis was created.
____

##### Part 4: Exploratory Analysis:
Basic statistics was done on the dataframe. Obama's most-liked and most RTed tweet were coincidentally the same.
The count is: Most-liked = 4573005 likes, Most-RTed: 1701391.

And the tweet is:
![obamatweet](https://user-images.githubusercontent.com/31828834/40893913-8cb55378-6773-11e8-9b54-8ba26f759feb.png)

I also did an analysis on the sources which tweeted Obama's tweets. 
The 3 different sources are: ['Twitter for iPhone' 'Twitter Web Client' 'Media Studio']. 
The distribution can be seen as follows:
![image](https://user-images.githubusercontent.com/31828834/40893984-2c8b6248-6774-11e8-8912-4efeb778d267.png)

Only one tweet was schedule by the Media Studio. It is used to manage videos on Twitter. (https://business.twitter.com/en/help/troubleshooting/media-studio-faqs.html) Following is the tweet:
![mediastudio](https://user-images.githubusercontent.com/31828834/40893897-76c56c4c-6773-11e8-9947-c41aae76cc3d.png)
____

##### Part 5: Time Series Analysis:
I did a time-series evaluation on likes, RTs and lengths of the tweets by Obama.
###### Evaluation of density of his tweets
![lenTS](https://user-images.githubusercontent.com/31828834/40894058-d0f6e9b0-6774-11e8-9eb8-3d6bca3bbcf4.png)
Barack Obama served as the President of the United States from January 20, 2009, to January 20, 2017. From the Time Series graph above, we can see that the amount of tweets were dense from September 2016 to December 2016 towards the end of his tenure. He does not tweet much these days. His tweets dropped around March of 2017. Maybe that's just a bit of relaxation he needed! ;)

##### Likes vs RT evaluation:
![likesvsrt](https://user-images.githubusercontent.com/31828834/40894093-1cbcb33e-6775-11e8-8c6f-7a3e002746b4.png)
From the graph of Likes vs RTs above, it is evident that he Likes more than he retweets. Maybe he considers his RTs to be endorsements?
____

##### Part 6: Sentimental Analysis:
The final part of this project was to do a sentimental analysis of Barack Obama's tweets. I have used textblob library. For documentation, please refer: http://textblob.readthedocs.io/en/dev/
![sentanalysis](https://user-images.githubusercontent.com/31828834/40894268-6fbedcb4-6776-11e8-9089-f047ea8256e2.png)

Here, 1, 0 and -1 resemble positive, neutral and negative sentiments respectively. We can see over 45% of his tweets are considered to be positive while less than 10% are negative.
***

Please note that this analysis was done on his most recent 400 tweets as of 06/03/2018.
***

#### References: 
1) https://apps.twitter.com/
2) http://docs.tweepy.org/en/v3.5.0/api.html
3) http://textblob.readthedocs.io/en/dev/
4) https://dev.to/bhaskar_vk/how-to-use-twitters-search-rest-api-most-effectively














