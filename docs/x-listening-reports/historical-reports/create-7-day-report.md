---
method: POST
---

# Create 7-day report

**Endpoint:** {{apiRoute}}/search/twitter/7-day

**Payload Example:** 

```
{
	"query":{
        "or":["Osasuna","#Osasuna"],
    	"must": ["#Football"],
        "nor":["@RealMadrid"],
        "lang":"en",
		    "limit": 100,
        "isRetweet":"included"
	}
}
```

The parameter "limit" will establish a limit in the number of posts the report will get. 

After you run the query you will get a **"resourceId"**, to get the stats you will need to execute the action "Get report stats" (check "Report Actions") and the result will be:

```
{
    "stats": {
        "general": {
            "since": 1714100336,
            "until": 1714309201,
            "total": 3,
            "images": 0,
            "links": 2,
            "linksAndImages": 2,
            "impact": 182966,
            "reach": 182966,
            "contributorsValue": 354.54,
            "economicValue": 389.94,
            "clears": 1,
            "replies": 0,
            "retweets": 0,
            "receivedRetweets": 0,
            "favorites": 3,
            "impressions": 2599,
            "quotes": 0,
            "totalReplies": 0,
            "bookmarks": 0,
            "contributors": 3,
            "originalContributors": 3,
            "originals": 3,
            "tweetValueMean": 129.98,
            "influence": 60988.67,
            "engagement": 1,
            "contributorValueMean": 118.18
        },
        "sentiment": {
            "general": {
                "negative": {
                    "_id": "negative",
                    "total": 0,
                    "images": 0,
                    "links": 0,
                    "linksAndImages": 0,
                    "impact": 0,
                    "reach": 0,
                    "contributorsValue": 0,
                    "economicValue": 0,
                    "clears": 0,
                    "replies": 0,
                    "retweets": 0,
                    "totalReplies": 0,
                    "quotes": 0,
                    "impressions": 0,
                    "bookmarks": 0,
                    "originalContributors": 0,
                    "contributors": 0,
                    "influence": 0,
                    "engagement": 0,
                    "originals": 0,
                    "tweetValueMean": 0,
                    "contributorValueMean": 0
                },
                "positive": {
                    "_id": "positive",
                    "total": 1,
                    "images": 0,
                    "links": 0,
                    "linksAndImages": 0,
                    "impact": 107,
                    "reach": 107,
                    "contributorsValue": 0.46,
                    "economicValue": 0.46,
                    "clears": 1,
                    "replies": 0,
                    "retweets": 0,
                    "totalReplies": 0,
                    "quotes": 0,
                    "impressions": 108,
                    "bookmarks": 0,
                    "originalContributors": 1,
                    "contributors": 1,
                    "influence": 107,
                    "engagement": 1,
                    "originals": 1,
                    "tweetValueMean": 0.46,
                    "contributorValueMean": 0.46
                },
                "neutral": {
                    "_id": "neutral",
                    "total": 2,
                    "images": 0,
                    "links": 2,
                    "linksAndImages": 2,
                    "impact": 182859,
                    "reach": 182859,
                    "contributorsValue": 354.08000000000004,
                    "economicValue": 389.48,
                    "clears": 0,
                    "replies": 0,
                    "retweets": 0,
                    "totalReplies": 0,
                    "quotes": 0,
                    "impressions": 2491,
                    "bookmarks": 0,
                    "originalContributors": 2,
                    "contributors": 2,
                    "influence": 91429.5,
                    "engagement": 1,
                    "originals": 2,
                    "tweetValueMean": 194.74,
                    "contributorValueMean": 177.04000000000002
                },
                "undefined": {
                    "_id": "undefined",
                    "total": 0,
                    "images": 0,
                    "links": 0,
                    "linksAndImages": 0,
                    "impact": 0,
                    "reach": 0,
                    "contributorsValue": 0,
                    "economicValue": 0,
                    "clears": 0,
                    "replies": 0,
                    "retweets": 0,
                    "totalReplies": 0,
                    "quotes": 0,
                    "impressions": 0,
                    "bookmarks": 0,
                    "originalContributors": 0,
                    "contributors": 0,
                    "influence": 0,
                    "engagement": 0,
                    "originals": 0,
                    "tweetValueMean": 0,
                    "contributorValueMean": 0
                }
            },
            "score": 85.38
        },
        "contributorRankings": {
            "mostActive": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 1
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 1
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 1
                }
            ],
            "mostFavorites": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 3
                }
            ],
            "mostPopular": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 182851
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 107
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 8
                }
            ],
            "mostRepliers": [],
            "mostBookmarked": [],
            "mostImpressions": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 2432
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 108
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 59
                }
            ],
            "mostTotalReplies": [],
            "mostQuotes": [],
            "mostRetweeted": [],
            "mostViral": [
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 7.375
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 1.0093457943925233
                },
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 0.013300446811885087
                }
            ],
            "highestImpact": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 182851
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 107
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 8
                }
            ],
            "originalTweets": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 1
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 1
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 1
                }
            ],
            "retweeters": [],
            "topPolite": [],
            "topTroll": [],
            "topPhotographers": [],
            "verifiedUsers": [
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 107
                }
            ],
            "topUsersValue": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 354.04
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 0.46
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 0.04
                }
            ],
            "topUserTweetsValue": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 389.44
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 0.46
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 0.04
                }
            ],
            "topImpressionsEngagers": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 2432
                },
                {
                    "_id": "1682706159717822467",
                    "alias": "ml_ufsbt",
                    "name": "Football Soccer Betting Tips",
                    "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                    "verified": true,
                    "value": 108
                },
                {
                    "_id": "1581211127890866176",
                    "alias": "l0linx",
                    "name": "l0l",
                    "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                    "verified": false,
                    "value": 59
                }
            ],
            "topRetweetEngagers": [],
            "topFavoriteEngagers": [
                {
                    "_id": "601993521",
                    "alias": "English_AS",
                    "name": "AS USA",
                    "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                    "verified": false,
                    "value": 3
                }
            ],
            "mostMentioned": [
                {
                    "id": "423384542",
                    "alias": "LaLiga",
                    "name": "LALIGA",
                    "picture": "https://pbs.twimg.com/profile_images/1678328302476337152/v92fpqsq_normal.jpg",
                    "followers": 12436079,
                    "verified": true,
                    "_id": "@laliga",
                    "value": 1
                },
                {
                    "id": "1565681650427731969",
                    "alias": "CAOsasuna",
                    "name": "CAOsasuna",
                    "picture": "https://pbs.twimg.com/profile_images/1565683142085730304/3Nk39z_5_normal.jpg",
                    "followers": 219,
                    "verified": false,
                    "_id": "@caosasuna",
                    "value": 1
                }
            ]
        },
        "mediaRankings": {
            "topPublications": [
                {
                    "_id": "1784550561368490286",
                    "counts": {
                        "favorites": 3,
                        "publicationScore": 3,
                        "userValue": 354.04,
                        "tweetValue": 389.44,
                        "retweets": 0
                    },
                    "createdAt": 1714304983,
                    "images": [],
                    "text": "\"Michael and Souey were like two peas in a pod...\" - remembering Michael Robinson, footballer, TV pundit, producer and 'archetypal English gentleman' https://t.co/CbgalYcPQ1 #ManCity #BHAFC #LFC #Osasuna #LaLiga #MichaelRobinson #Souness #Soccer #Football",
                    "user": {
                        "id": "601993521",
                        "name": "AS USA",
                        "alias": "English_AS",
                        "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                        "followers": 182851,
                        "verified": false
                    },
                    "value": 3
                }
            ],
            "mostValuedTweets": [
                {
                    "_id": "1784550561368490286",
                    "counts": {
                        "favorites": 3,
                        "publicationScore": 3,
                        "userValue": 354.04,
                        "tweetValue": 389.44,
                        "retweets": 0
                    },
                    "createdAt": 1714304983,
                    "images": [],
                    "text": "\"Michael and Souey were like two peas in a pod...\" - remembering Michael Robinson, footballer, TV pundit, producer and 'archetypal English gentleman' https://t.co/CbgalYcPQ1 #ManCity #BHAFC #LFC #Osasuna #LaLiga #MichaelRobinson #Souness #Soccer #Football",
                    "user": {
                        "id": "601993521",
                        "name": "AS USA",
                        "alias": "English_AS",
                        "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                        "followers": 182851,
                        "verified": false
                    },
                    "value": 389.44
                },
                {
                    "_id": "1784568252863328634",
                    "counts": {
                        "favorites": 0,
                        "publicationScore": 0,
                        "userValue": 0.46,
                        "tweetValue": 0.46,
                        "retweets": 0
                    },
                    "createdAt": 1714309201,
                    "images": [],
                    "text": "🇪🇸 #Spain, LaLiga, 2024-04-28, Round 33 ⚽️\nGranada CF vs. CA Osasuna\nTough season for Granada, positioned 19th 📉\nOsasuna better at 11th, but not shining 🌥️\nThe match could end in Osasuna's favor or a draw 🤝\n#GranadaOsasuna #LaLiga #Football #Prediction",
                    "user": {
                        "id": "1682706159717822467",
                        "name": "Football Soccer Betting Tips",
                        "alias": "ml_ufsbt",
                        "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                        "followers": 107,
                        "verified": true
                    },
                    "value": 0.46
                },
                {
                    "_id": "1783692208421683628",
                    "counts": {
                        "favorites": 0,
                        "publicationScore": 0,
                        "userValue": 0.04,
                        "tweetValue": 0.04,
                        "retweets": 0
                    },
                    "createdAt": 1714100336,
                    "images": [],
                    "text": "CA Osasuna Football Team Training on 24thApr⚽🏟️\n@laliga @caosasuna \n#laliga #osasuna #caosasuna #training #practice #football https://t.co/YMXFjnhJMr",
                    "user": {
                        "id": "1581211127890866176",
                        "name": "l0l",
                        "alias": "l0linx",
                        "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                        "followers": 8,
                        "verified": false
                    },
                    "value": 0.04
                }
            ],
            "mostRetweetedTweets": [],
            "mostImpressionsTweets": [
                {
                    "_id": "1784550561368490286",
                    "counts": {
                        "favorites": 3,
                        "publicationScore": 3,
                        "userValue": 354.04,
                        "tweetValue": 389.44,
                        "retweets": 0
                    },
                    "createdAt": 1714304983,
                    "images": [],
                    "text": "\"Michael and Souey were like two peas in a pod...\" - remembering Michael Robinson, footballer, TV pundit, producer and 'archetypal English gentleman' https://t.co/CbgalYcPQ1 #ManCity #BHAFC #LFC #Osasuna #LaLiga #MichaelRobinson #Souness #Soccer #Football",
                    "user": {
                        "id": "601993521",
                        "name": "AS USA",
                        "alias": "English_AS",
                        "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                        "followers": 182851,
                        "verified": false
                    },
                    "value": 2432
                },
                {
                    "_id": "1784568252863328634",
                    "counts": {
                        "favorites": 0,
                        "publicationScore": 0,
                        "userValue": 0.46,
                        "tweetValue": 0.46,
                        "retweets": 0
                    },
                    "createdAt": 1714309201,
                    "images": [],
                    "text": "🇪🇸 #Spain, LaLiga, 2024-04-28, Round 33 ⚽️\nGranada CF vs. CA Osasuna\nTough season for Granada, positioned 19th 📉\nOsasuna better at 11th, but not shining 🌥️\nThe match could end in Osasuna's favor or a draw 🤝\n#GranadaOsasuna #LaLiga #Football #Prediction",
                    "user": {
                        "id": "1682706159717822467",
                        "name": "Football Soccer Betting Tips",
                        "alias": "ml_ufsbt",
                        "picture": "https://pbs.twimg.com/profile_images/1762810286086524928/atba3w5S_normal.jpg",
                        "followers": 107,
                        "verified": true
                    },
                    "value": 108
                },
                {
                    "_id": "1783692208421683628",
                    "counts": {
                        "favorites": 0,
                        "publicationScore": 0,
                        "userValue": 0.04,
                        "tweetValue": 0.04,
                        "retweets": 0
                    },
                    "createdAt": 1714100336,
                    "images": [],
                    "text": "CA Osasuna Football Team Training on 24thApr⚽🏟️\n@laliga @caosasuna \n#laliga #osasuna #caosasuna #training #practice #football https://t.co/YMXFjnhJMr",
                    "user": {
                        "id": "1581211127890866176",
                        "name": "l0l",
                        "alias": "l0linx",
                        "picture": "https://pbs.twimg.com/profile_images/1717622335484624896/yj5VXEWt_normal.jpg",
                        "followers": 8,
                        "verified": false
                    },
                    "value": 59
                }
            ],
            "mostTotalRepliesTweets": [],
            "mostBookmarkTweets": [],
            "mostQuotesTweets": [],
            "mostFavoritedTweets": [
                {
                    "_id": "1784550561368490286",
                    "counts": {
                        "favorites": 3,
                        "publicationScore": 3,
                        "userValue": 354.04,
                        "tweetValue": 389.44,
                        "retweets": 0
                    },
                    "createdAt": 1714304983,
                    "images": [],
                    "text": "\"Michael and Souey were like two peas in a pod...\" - remembering Michael Robinson, footballer, TV pundit, producer and 'archetypal English gentleman' https://t.co/CbgalYcPQ1 #ManCity #BHAFC #LFC #Osasuna #LaLiga #MichaelRobinson #Souness #Soccer #Football",
                    "user": {
                        "id": "601993521",
                        "name": "AS USA",
                        "alias": "English_AS",
                        "picture": "https://pbs.twimg.com/profile_images/1766373116626833408/U2mwRqlc_normal.jpg",
                        "followers": 182851,
                        "verified": false
                    },
                    "value": 3
                }
            ],
            "topHashtags": [
                {
                    "_id": "#laliga",
                    "value": 3
                },
                {
                    "_id": "#football",
                    "value": 3
                },
                {
                    "_id": "#osasuna",
                    "value": 2
                },
                {
                    "_id": "#mancity",
                    "value": 1
                },
                {
                    "_id": "#bhafc",
                    "value": 1
                },
                {
                    "_id": "#granadaosasuna",
                    "value": 1
                },
                {
                    "_id": "#michaelrobinson",
                    "value": 1
                },
                {
                    "_id": "#caosasuna",
                    "value": 1
                },
                {
                    "_id": "#training",
                    "value": 1
                },
                {
                    "_id": "#soccer",
                    "value": 1
                }
            ],
            "topLanguages": [
                {
                    "_id": "en",
                    "value": 3
                }
            ],
            "genderPerContributor": [
                {
                    "_id": "undefined",
                    "value": 3
                }
            ],
            "mostRetweetedImages": [],
            "mostFavoritedImages": []
        },
        "influences": {
            "sentimentInfluence": {
                "intervals": [
                    {
                        "influence": "negative",
                        "tweets": 0,
                        "lowerLimit": -999999,
                        "upperLimit": -2
                    },
                    {
                        "influence": "neutral",
                        "tweets": 3,
                        "lowerLimit": -2,
                        "upperLimit": 2
                    },
                    {
                        "influence": "positive",
                        "tweets": 0,
                        "lowerLimit": 2,
                        "upperLimit": "∞"
                    }
                ],
                "average": 0
            },
            "tweetsPerContributor": {
                "intervals": [
                    {
                        "influence": "1",
                        "contributors": 3,
                        "lowerLimit": 1,
                        "upperLimit": 2
                    },
                    {
                        "influence": "2",
                        "contributors": 0,
                        "lowerLimit": 2,
                        "upperLimit": 3
                    },
                    {
                        "influence": "3",
                        "contributors": 0,
                        "lowerLimit": 3,
                        "upperLimit": 4
                    },
                    {
                        "influence": "4",
                        "contributors": 0,
                        "lowerLimit": 4,
                        "upperLimit": 5
                    },
                    {
                        "influence": "5",
                        "contributors": 0,
                        "lowerLimit": 5,
                        "upperLimit": 6
                    },
                    {
                        "influence": "6",
                        "contributors": 0,
                        "lowerLimit": 6,
                        "upperLimit": 7
                    },
                    {
                        "influence": "6>",
                        "contributors": 0,
                        "lowerLimit": 7,
                        "upperLimit": "∞"
                    }
                ],
                "average": 1
            },
            "contributorInfluence": {
                "intervals": [
                    {
                        "influence": "XXS",
                        "contributors": 1,
                        "lowerLimit": 0,
                        "upperLimit": 10
                    },
                    {
                        "influence": "XS",
                        "contributors": 0,
                        "lowerLimit": 10,
                        "upperLimit": 50
                    },
                    {
                        "influence": "S",
                        "contributors": 1,
                        "lowerLimit": 50,
                        "upperLimit": 200
                    },
                    {
                        "influence": "M",
                        "contributors": 0,
                        "lowerLimit": 200,
                        "upperLimit": 500
                    },
                    {
                        "influence": "L",
                        "contributors": 0,
                        "lowerLimit": 500,
                        "upperLimit": 1000
                    },
                    {
                        "influence": "XL",
                        "contributors": 0,
                        "lowerLimit": 1000,
                        "upperLimit": 5000
                    },
                    {
                        "influence": "XXL",
                        "contributors": 1,
                        "lowerLimit": 5000,
                        "upperLimit": "∞"
                    }
                ],
                "average": 60988.666666666664
            },
            "tweetValueInfluence": {
                "intervals": [
                    {
                        "influence": "XS",
                        "tweets": 2,
                        "lowerLimit": 0,
                        "upperLimit": 1
                    },
                    {
                        "influence": "S",
                        "tweets": 0,
                        "lowerLimit": 1,
                        "upperLimit": 3
                    },
                    {
                        "influence": "M",
                        "tweets": 0,
                        "lowerLimit": 3,
                        "upperLimit": 8
                    },
                    {
                        "influence": "L",
                        "tweets": 0,
                        "lowerLimit": 8,
                        "upperLimit": 15
                    },
                    {
                        "influence": "XL",
                        "tweets": 1,
                        "lowerLimit": 15,
                        "upperLimit": "∞"
                    }
                ],
                "average": 129.98
            },
            "userValueInfluence": {
                "intervals": [
                    {
                        "influence": "XS",
                        "contributors": 2,
                        "lowerLimit": 0,
                        "upperLimit": 1
                    },
                    {
                        "influence": "S",
                        "contributors": 0,
                        "lowerLimit": 1,
                        "upperLimit": 3
                    },
                    {
                        "influence": "M",
                        "contributors": 0,
                        "lowerLimit": 3,
                        "upperLimit": 8
                    },
                    {
                        "influence": "L",
                        "contributors": 0,
                        "lowerLimit": 8,
                        "upperLimit": 15
                    },
                    {
                        "influence": "XL",
                        "contributors": 1,
                        "lowerLimit": 15,
                        "upperLimit": "∞"
                    }
                ],
                "average": 118.18
            },
            "ageInfluence": {
                "intervals": [
                    {
                        "influence": "XXS",
                        "tweets": 1,
                        "lowerLimit": 0,
                        "upperLimit": 31536000
                    },
                    {
                        "influence": "XS",
                        "tweets": 1,
                        "lowerLimit": 31536000,
                        "upperLimit": 63072000
                    },
                    {
                        "influence": "S",
                        "tweets": 0,
                        "lowerLimit": 63072000,
                        "upperLimit": 94608000
                    },
                    {
                        "influence": "M",
                        "tweets": 0,
                        "lowerLimit": 94608000,
                        "upperLimit": 126144000
                    },
                    {
                        "influence": "L",
                        "tweets": 0,
                        "lowerLimit": 126144000,
                        "upperLimit": 157680000
                    },
                    {
                        "influence": "XL",
                        "tweets": 0,
                        "lowerLimit": 157680000,
                        "upperLimit": 189216000
                    },
                    {
                        "influence": "XXL",
                        "tweets": 1,
                        "lowerLimit": 189216000,
                        "upperLimit": "∞"
                    }
                ],
                "average": 149491112.66666666
            },
            "viralUsersInfluence": {
                "intervals": [
                    {
                        "influence": "XS",
                        "contributors": 1,
                        "lowerLimit": 0,
                        "upperLimit": 0.25
                    },
                    {
                        "influence": "S",
                        "contributors": 0,
                        "lowerLimit": 0.25,
                        "upperLimit": 0.5
                    },
                    {
                        "influence": "M",
                        "contributors": 0,
                        "lowerLimit": 0.5,
                        "upperLimit": 0.75
                    },
                    {
                        "influence": "L",
                        "contributors": 0,
                        "lowerLimit": 0.75,
                        "upperLimit": 1
                    },
                    {
                        "influence": "XL",
                        "contributors": 2,
                        "lowerLimit": 1,
                        "upperLimit": "∞"
                    }
                ],
                "average": 2.799215413734803
            },
            "textLengthInfluence": {
                "intervals": [
                    {
                        "influence": "XXS",
                        "tweets": 0,
                        "lowerLimit": 0,
                        "upperLimit": 40
                    },
                    {
                        "influence": "XS",
                        "tweets": 0,
                        "lowerLimit": 40,
                        "upperLimit": 80
                    },
                    {
                        "influence": "S",
                        "tweets": 0,
                        "lowerLimit": 80,
                        "upperLimit": 120
                    },
                    {
                        "influence": "M",
                        "tweets": 1,
                        "lowerLimit": 120,
                        "upperLimit": 160
                    },
                    {
                        "influence": "L",
                        "tweets": 0,
                        "lowerLimit": 160,
                        "upperLimit": 200
                    },
                    {
                        "influence": "XL",
                        "tweets": 1,
                        "lowerLimit": 200,
                        "upperLimit": 240
                    },
                    {
                        "influence": "XXL",
                        "tweets": 1,
                        "lowerLimit": 240,
                        "upperLimit": "∞"
                    }
                ],
                "average": 205.33333333333334
            },
            "oldVsNewInfluence": {
                "intervals": [
                    {
                        "influence": "old",
                        "tweets": 1,
                        "lowerLimit": 0,
                        "upperLimit": 140
                    },
                    {
                        "influence": "new",
                        "tweets": 2,
                        "lowerLimit": 140,
                        "upperLimit": "∞"
                    }
                ],
                "average": 205.33333333333334
            }
        },
        "timeline": [
            {
                "tweets": 1,
                "linksAndImages": 1,
                "retweets": 0,
                "originals": 1,
                "replies": 0,
                "tweetsValue": 0.04,
                "images": 0,
                "links": 1,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 59,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 1,
                "undefined": 0,
                "min": 1714100336,
                "contributors": 1,
                "max": 1714107298
            },
            {
                "min": 1714107298,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714114260
            },
            {
                "min": 1714114260,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714121223
            },
            {
                "min": 1714121223,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714128185
            },
            {
                "min": 1714128185,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714135147
            },
            {
                "min": 1714135147,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714142109
            },
            {
                "min": 1714142109,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714149071
            },
            {
                "min": 1714149071,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714156033
            },
            {
                "min": 1714156033,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714162996
            },
            {
                "min": 1714162996,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714169958
            },
            {
                "min": 1714169958,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714176920
            },
            {
                "min": 1714176920,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714183882
            },
            {
                "min": 1714183882,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714190844
            },
            {
                "min": 1714190844,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714197806
            },
            {
                "min": 1714197806,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714204769
            },
            {
                "min": 1714204769,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714211731
            },
            {
                "min": 1714211731,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714218693
            },
            {
                "min": 1714218693,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714225655
            },
            {
                "min": 1714225655,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714232617
            },
            {
                "min": 1714232617,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714239579
            },
            {
                "min": 1714239579,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714246542
            },
            {
                "min": 1714246542,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714253504
            },
            {
                "min": 1714253504,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714260466
            },
            {
                "min": 1714260466,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714267428
            },
            {
                "min": 1714267428,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714274390
            },
            {
                "min": 1714274390,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714281352
            },
            {
                "min": 1714281352,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714288315
            },
            {
                "min": 1714288315,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714295277
            },
            {
                "min": 1714295277,
                "tweets": 0,
                "linksAndImages": 0,
                "retweets": 0,
                "originals": 0,
                "replies": 0,
                "tweetsValue": 0,
                "contributors": 0,
                "images": 0,
                "links": 0,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 0,
                "bookmarks": 0,
                "positives": 0,
                "negatives": 0,
                "neutrals": 0,
                "undefined": 0,
                "max": 1714302239
            },
            {
                "tweets": 2,
                "linksAndImages": 1,
                "retweets": 0,
                "originals": 2,
                "replies": 0,
                "tweetsValue": 389.9,
                "images": 0,
                "links": 1,
                "totalReplies": 0,
                "quotes": 0,
                "impressions": 2540,
                "bookmarks": 0,
                "positives": 1,
                "negatives": 0,
                "neutrals": 1,
                "undefined": 0,
                "min": 1714302239,
                "contributors": 2,
                "max": 1714309201
            }
        ],
        "binders": []
    },
    "meta": {
        "updatedAt": 1714466926,
        "id": "0bf8efd0-4e11-49bf-8e25-3483932ea74a",
        "name": "#Football (Osasuna OR #Osasuna) -(@RealMadrid) lang:en",
        "source": "twitter",
        "type": "7-day",
        "version": 2
    }
}
```
