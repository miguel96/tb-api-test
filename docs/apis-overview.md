---
description: Little intro to our three APIs
---

# APIS Overview

## Types of APIs

There are three types of API within Tweet Binder's API

* Reports API
* Profiles API
* User trackers API

### Reports API

This API is in charge of generating the STATS on hashtags, etc by first collecting the tweets (posts or publications) and then generating the statistics from those. You will perform **SEARCHES** in the API to get the stats and you will always work against a monthly tweet balance, this means that your reports won't be able to overpass that balance of posts during the month. If your balance is 2,500,000 posts (publications) per month, you will be able to create reports until you consume that balance.

When you collect the info after a search, you will receive a **REPORT**.

#### Types of searches

1. 7-day search: Stats from the last 7-days
2. Historical search: Stats from at any date in the past (until 2006)
3. Live search: Stats from now into the future

#### Report features

* Get report state: this checks report status, creation date, query, etc:

```json
{
    "_id": "f952405b-06eb-4a91-bfbc-c2228ac46d06",
    "version": 2,
    "createdAt": 1699436448,
    "updatedAt": 1700041275,
    "generatedTimes": 1,
    "createdFrom": "search/twitter/7-day",
    "type": "7-day",
    "source": "twitter",
    "status": "archived",
    "userId": "ef68cbf9-6107-4f28-af0b-0b8681be7033",
    "query": {
        "or": [
            "Osasuna",
            "#Osasuna"
        ],
        "must": [
            "#Football"
        ],
        "nor": [
            "@RealMadrid"
        ],
        "lang": "en",
        "isRetweet": "included"
    },
    "settings": {
        "stream": {
            "or": [
                "Osasuna",
                "#Osasuna"
            ],
            "must": [
                "#Football"
            ],
            "nor": [
                "@RealMadrid"
            ],
            "lang": "en",
            "isRetweet": "included"
        },
        "name": "#Football (Osasuna OR #Osasuna) -(@RealMadrid) lang:en"
    },
    "affiliate": {
        "id": "9c4d6d6b-d389-40e9-bd90-a79bf1837b37",
        "createdAt": 1604491722,
        "expirationDate": null
    },
    "feedId": "7adf4d5f-ac04-4d58-9b77-58c32bd37ec7",
    "economicValue": 1816.1599999999999,
    "generatedAt": 1699436459,
    "total": 91,
    "excelGeneratedAt": 1699436461
}
```

* Get report stats: after report is generated this will contain the stats. Example of part of the stats:&#x20;

```json
    "stats": {
        "general": {
            "since": 1698925501,
            "until": 1699290958,
            "total": 91,
            "images": 2,
            "links": 20,
            "linksAndImages": 12,
            "impact": 812280,
            "reach": 808667,
            "contributorsValue": 1643.75,
            "economicValue": 1816.1599999999999,
            "clears": 0,
            "replies": 1,
            "retweets": 78,
            "receivedRetweets": 76,
            "favorites": 83,
            "impressions": 60007,
            "quotes": 1,
            "totalReplies": 1,
            "bookmarks": 0,
            "contributors": 19,
            "originalContributors": 6,
            "originals": 13,
            "tweetValueMean": 19.957802197802195,
            "influence": 42561.42,
            "engagement": 4.79,
            "contributorValueMean": 86.51
```

* List reports: this will list all your reports.
* Get publications: this contains the post ids of the report, you will have to rehydrate later.
* Export report to json


[Profile's API Endpoints](documentation/endpoints/reports-endpoints/README.md){ .md-button .md-button--primary }

### Profiles API

This API contains a subset of endpoints that allows you to check an account information and get its followers/friends:

* Get profile info
* Get profile followers/friends list and optionally add profile information

This is the profile info:&#x20;

```json
[
    {
        "id": "1133456036",
        "name": "Tweet Binder",
        "alias": "TweetBinder",
        "picture": "http://pbs.twimg.com/profile_images/1719967396448931840/MmGRpyWf_normal.png",
        "followers": 38737,
        "following": 2577,
        "verified": false,
        "bio": "Twitter Analytics Tool by @AudienseCo:\n\n📈 Twitter Advanced Analytics\n⏳ Twitter Historical Data\n👥 Twitter Followers and Hashtag Tracking\n💙 Sentiment Analytics",
        "age": 1359536324,
        "counts": {
            "lists": 403,
            "statuses": 5645
        },
        "location": "Global",
        "gender": "undefined",
        "value": 85.76
    }
]
```

{% content-ref url="documentation/endpoints/profiles-api-endpoints.md" %}
[profiles-api-endpoints.md](documentation/endpoints/profiles-api-endpoints.md)
{% endcontent-ref %}

### User Trackers API

Automatically takes Twitter Profiles snapshots of their info and stats every hour. Allows to query this snapshots in order to get relevant information.

The info provided is:

* Tweets sent
* Followers
* Following
* List
* Ratio Followers/Following

```json
[
    {
        "_id": 1703732400,
        "tweets": 7968,
        "followers": 1080,
        "following": 1135,
        "lists": 153,
        "followersFollowing": 0.95,
        "createdAt": 1703732627,
        "updatedAt": 1703732627
    },
    {
        "_id": 1704333600,
        "tweets": 7972,
        "followers": 1083,
        "following": 1144,
        "lists": 153,
        "followersFollowing": 0.95,
        "createdAt": 1704333870,
        "updatedAt": 1704333870
    }
]
```

{% content-ref url="documentation/endpoints/user-trackers-api-endpoints.md" %}
[user-trackers-api-endpoints.md](documentation/endpoints/user-trackers-api-endpoints.md)
{% endcontent-ref %}
