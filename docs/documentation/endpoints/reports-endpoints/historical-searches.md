---
description: >-
  Get stats for ant query in the past. “Wait A Minute, Doc. Are You Telling Me
  You Built A Time Machine... Out Of A DeLorean?”
---

# Historical Searches

## Search: 7 day and historical search

It queues a Twitter query in our system to be processed. The request returns a **resourceId** that is stored in the Postman environment as **reportId** and a short version of it as **reportCode**. These variables are later used by the endpoints. Internally, this creates a report document as well.

The search can be:

* 7-day search: generates a report from the last 7 days \{{apiRoute\}}/search/twitter/7-day
* Full Historical search: generates a report from any date in the past (since 2006) \{{apiRoute\}}/search/twitter/enterprise

### **Payload example**

```
{
	"query":{
        "or":["Osasuna","#Osasuna"],
    	"must": ["#Football"],
        "nor":["@RealMadrid"],
        "lang":"en",
	"limit": 100,
        "startDate":1142981988,
        "endDate":1699434351,
        "isRetweet":"excluded"
	}
}
```

That complex query would search for publications that contain the word “Osasuna” or the hashtag “#Osasuna” and also containing the hashtag #Football in English but not @RealMadrid, limiting the _resultset_ to 100 publications in the indicated dates and excluding retweets. That limit of publications can be increased.

When creating a search you will get as "tweets" original tweets and retweets.

### **Parameters**

These parameters are very important when creating queries that retrieve tweets and stats:

* or: string array; At least one of the terms must be present.
* must: string array; All terms must be present. It’s equivalent to a logic AND. If&#x20;
* nor: string array; None of the terms must be present.
* lang: string; Publications language.
* limit: integer; limits the number of publications below the theoretical maximum. It’s quite useful for testing.
* startDate: unix time; Date at which the search will stop as long as the limit (either manual or by default) hasn’t been reached.
* endDate: unix time; Date from which the search will dismiss publications.
* isRetweet:&#x20;
  * "excluded": You will get only original tweets
  * "only": You will get only retweets
  * "included": You will get both, retweets and original tweets (default)

NOTE: At least one of the following parameters must be present in the payload: _must_ or _or_. The rest are optional.

### Creating Queries using the advanced operators

Queries can contain Twitter's advanced search commands (aka operators) in order to further refine the results. You can combine the basic parameters that we just showed in the last paragraph to filter by date, language, etc. But there are more.

We have created a list [here](https://docs.google.com/spreadsheets/d/1gsKTVdDl\_9gHjvkSFF6pmZnOovxHMTkDwej9KtSzfNg/edit#gid=903868805), but you can see examples below:

* "Exact phrase match". When creating a query you&#x20;
*   **FROM.** Tweets sent by one user: for example, tweets from @TweetBinder \


    ```
    {
    	"query":{
        	"must": ["from:tweetbinder"]
    	}
    }
    ```
*   **FROM + Keyword.** Tweets sent by one user mentioning that mention a specific keyword: for example, tweets from @TweetBinder that mention the keyword Twitter\


    ```
    {
    	"query":{
        	"must": ["from:tweetbinder","twitter"]
    	}
    }
    ```
*   **TO.** Tweets that are replies to one particular user:\


    ```
    {
    	"query":{
        	"must": ["to:tweetbinder"]
    	}
    }
    ```


*   **LIST.** Tweets sent by a list of users:\


    ```
    {
    	"query":{
        	"must": ["list:183090433"]
    	}
    }
    ```
*   **VERIFIED.** Tweets sent by only verified account. Combine this operator with a keyword or hashtag or other ones:\


    ```
    {
    	"query":{
        	"must": ["Tweet Binder", "is:verified"]
    	}
    }
    ```
*   **RETWEETS OF.** Get a list of people who retweets one particular user. For example, to get people who retweets Elon Musk\


    ```
    {
    	"query":{
        	"must": ["retweets_of:elonmusk"]
    	}
    }
    ```

    You can also get retweets of a particular tweet using the retweets\_of\_tweet\_id: operator:

    ```
    {
    	"query":{
        	"must": ["retweets_of_tweet_id:1718557264074641818"]
    	}
    }
    ```

We highly recommend to combine operators to refine your search. Please study[ this document](https://docs.google.com/spreadsheets/d/1gsKTVdDl\_9gHjvkSFF6pmZnOovxHMTkDwej9KtSzfNg/edit#gid=903868805) to know more.
