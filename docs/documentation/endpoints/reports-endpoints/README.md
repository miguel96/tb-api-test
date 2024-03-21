---
description: >-
  Use this API to generate Twitter impact reports and to get stats for hashtags,
  keywords, users and lists.
---

# Reports Endpoints

## Types of reports

There are two types of reports:

* [Historical search](historical-searches.md): with two sub-types of reports
  * 7 day search: **covers the last** 7 days.
  * Full Historical: covers any date since 2006 (when Twitter was born).
* [Live report](live-reports.md): collects the information in real time. Live reports do not contain engagement information.

## Get report state

This endpoint returns a search document (AKA report) from our platform.&#x20;

For example, if you just created a report and ran this endpoint you will get this:

```json
{
    "_id": "f952405b-06eb-4a91-bfbc-c2228ac46d06",
    "version": 2,
    "createdAt": 1699436448,
    "updatedAt": 1699436448,
    "generatedTimes": 0,
    "createdFrom": "search/twitter/7-day",
    "type": "7-day",
    "source": "twitter",
    "status": "waiting",
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
    "feedId": "7adf4d5f-ac04-4d58-9b77-58c32bd37ec7"
}
```

Notice the status field says "waiting", it means that the report is still being generated. This field can have several values:

* waiting : the search hasn’t finished yet
* generated: the search has finished and stats have been generated
* outdated: some new publications are pending for processing, this will only happen with streams (live reports).

Once it is generated, it looks like this:

```json
{
    "_id": "f952405b-06eb-4a91-bfbc-c2228ac46d06",
    "version": 2,
    "createdAt": 1699436448,
    "updatedAt": 1699436461,
    "generatedTimes": 1,
    "createdFrom": "search/twitter/7-day",
    "type": "7-day",
    "source": "twitter",
    "status": "generated",
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

* total: integer; Total number of publications processed so far. In general if the status is generated this will be the total number of publications.

## Get report stats

This endpoint returns statistics of one report. If the status is waiting it will return an error, so wait until it is generated.

Tweet Binder provides numerous statistics for each search, here **some of them**:

* Total number of tweets (retweets included)
* Types of tweets
* Real impressions
* Potential Impressions
* Potential Reach
* Likes / Retweets / Replies / Quotes / Bookmarks
* Several User rankings: active, engager, etc.
* Sentiment
* Economic study
* Engagement study
* Users' age on Twitter
* Length of the tweets
* Top languages
* Top sources
* Top hashtags
* Rankings of images by:
  * Retweets
  * Likes
* Ranking of tweets by:
  * Retweets
  * Likes

## Delete report

It deletes a report document.

## List reports

It returns a list of report documents.

## Export report to json

It exports to a json which will contain all the tweets in report. Steps are:

1. Export report: Pass report id to request report json export&#x20;
2. Await until report has jsonGeneratedAt>generatedAt: Request report status until json is generated. It may take from some minutes to several hours depending on report size
3. Get report json url: After report is generated use this request to get URL to download JSON file
