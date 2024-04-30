---
method: GET
---

# Check balance

**Endpoint:*** {{apiRoute}}/users/me

Depending on your subscription, you will have different balances to create reports, etc.

The balances are renewed each month and are not cumulative.

The main variables of the balance sheets are:

- Posts (tweets): the number of posts (tweets) limits the number of reports you can make. For example, if you have 10,000 posts in your balance, you could create 2 reports of 5,000 or 4 of 2,5000, etc.

- Reports: generally the number of reports is unlimited and is only limited by the number of posts, but sometimes certain subscriptions may have a limited number of reports that can be created. Reports can be historical, 7-day or live ones.

- Clones: number of times a user can clone a report. This feature is widely used when the user wants to save a backup copy of their report before modifying it.

- Twitter parallel streams: number of live reports one user can have running at the same time.

- Twitter parallel user tracker: number of uses reports one user can have running at the same time.


``{
    "user": {
        "_id": "ef68cbf9-6107-4f28-af0b-0b8681be7033",
        "migration": {
            "id": 13442
        },
        "name": "tweetbinderpro",
        "lang": "en",
        "lastLogin": 1712331738,
        "createdAt": 1385368653,
        "profiles": {
            "twitter": {
                "id": "2161686082",
                "account": {
                    "id_str": "2161686082",
                    "name": "Tweet Binder PRO by Audiense",
                    "screen_name": "TweetBinderPRO",
                    "profile_image_url": "http://pbs.twimg.com/profile_images/1687154068425228291/PZ4maSvt_normal.jpg",
                    "profile_image_url_https": "https://pbs.twimg.com/profile_images/1687154068425228291/PZ4maSvt_normal.jpg",
                    "location": "Global",
                    "followers_count": 1132,
                    "email": "tweetbi.nder@gmail.com"
                }
            }
        },
        "flags": [
            "admin"
        ],
        "scopes": [
            "admin",
            "instagram",
            "manager",
            "events",
            "graphext-export",
            "twitter-v2",
            "audiense-export"
        ],
        "email": "javier@tweetbinder.com",
        "password": "XXXXXXX",
        "payments": {
            "country": "ES"
        },
        "ninja": {
            "clientId": "2719"
        },
        "intercom": {
            "userHash": "f9a4dd8c3508de1756bb9197fcfcec86b9ceee41ecf0e6037823b493b8112715"
        },
        "currency": "USD",
        "updatedAt": 1712331738
    },
    "balances": {
        "publications": {
            "balance": 875000038816,
            "total": 875000166111
        },
        "twitter:7-day": {
            "balance": "unlimited",
            "total": "unlimited"
        },
        "twitter:live": {
            "balance": "unlimited",
            "total": "unlimited"
        },
        "clones": {
            "balance": 100,
            "total": 100
        },
        "twitter:parallel-streams": {
            "balance": "unlimited",
            "total": 0
        },
        "twitter:parallel:user-trackers": {
            "balance": 242,
            "total": 234
        },
        "profiles": {
            "balance": 30000,
            "total": 30000
        },
        "twitter-count:historical": {
            "balance": 12330,
            "total": 12345
        },
        "twitter:enterprise": {
            "balance": 3024,
            "total": 3033
        },
        "twitter-count:7-day": {
            "balance": "unlimited",
            "total": "unlimited"
        },
        "tiktok:historical": {
            "balance": "unlimited",
            "total": "unlimited"
        },
        "twitter:parallel:user-trackers-tags": {
            "balance": 2,
            "total": 0
        },
    },
    "plans": [
        {
            "_id": "0becc8f9-da28-422e-97cd-3192907692c9",
            "createdAt": 1570190429,
            "updatedAt": 1712160318,
            "balanceId": "44dd99ff-89bc-4f71-844f-27e89a23f291",
            "renewDate": 1714749082,
            "type": "advanced",
            "renewCycle": "month",
            "userId": "ef68cbf9-6107-4f28-af0b-0b8681be7033",
            "status": "active",
            "productPrices": [
                {
                    "_id": "publications",
                    "prices": {
                        "EUR": 0.00067
                    }
                }
            ]
        },
            "updatedAt": 1712138720
        }
    ]
}``
