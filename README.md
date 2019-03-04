# twitter-dataset
# twitter dataset
- This data set is collected for a PhD thesis work named "User Modeling On Microblogging Websites"
- Twitter  Streaming  API  has  been  used  to  collect  live  tweets  of  users  between November, 4th 2015 and January 12, 2016
- I contains 177K users and 37M tweets. 
- This data is used for research on identifying topical authorities on Twitter [1, 2]
- Each tweet is assigned with zero, one or many topics (See example below).  
- Data is dumped from MongoDB 
- Uset and Twitter Ids are anonymized in the data to comply with the Twitter privacy Policy
- For same reason tweet texts are also removed.
- There are three collections. users, tweets and network.
- tweets collection is split into chunks of 4M tweets to avoid size complaints of GitHub
- below is a sample document from user_anonymized collection
> db.users_anonymized.findOne()
{
        "_id" : 701838,
        "statusCount" : 289,
        "friendsCount" : 859,
        "followersCount" : 556,
        "tweet_count" : 61
}


 - below is a sample document from user_anonymized collection

 > db.tweets_anonymized.findOne()
{
        "_id" : 1,
        "date" : ISODate("2015-11-04T05:53:57Z"),
        "retweetCount" : 50,
        "favCount" : 0,
        "isRetweet" : true,
        "reTweetedTweetId" : 29802569,
        "reTweetedUserId" : 704944,
        "hashtags" : [ ],
        "urls" : [
                "https://t.co/TigZ0wfOMd"
        ],
        "userid" : 556176,
        "topics" : [
                "politics/breakingNews"
        ]
}

-below is a sample document from network_anonymized collection
db.network_anonymized.findOne()
{
        "_id" : "3639",
        "followers" : [
                "121983",
                "114361",
                "133932",
                "593498",
                "107879",
                "343785",
                "12375",
                "118293",
                "313674"
        ]
}



- Consumers of this data should cite below paper(s)

[1] Alp, Z. Z., & Öğüdücü, Ş. G. (2018). Identifying topical influencers on twitter based on user behavior and network topology. Knowledge-Based Systems, 141, 211-221. https://www.sciencedirect.com/science/article/abs/pii/S0950705117305439

[2] Alp, Z. Z., & Öğüdücü, Ş. G. (2019). Influence Factorization for identifying authorities in Twitter. Knowledge-Based Systems, 163, 944-954. https://www.sciencedirect.com/science/article/pii/S0950705118305069


