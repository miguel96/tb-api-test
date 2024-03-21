---
description: >-
  This API covers how to access to Twitter Profiles info like profile info and
  profile followers
---

# Profiles' API endpoints

## Profile info example

This is the profile's information you will receive:&#x20;

```json
        "id": "2161686082", // Twitter profile id
        "name": "Tweet Binder PRO", // User name
        "alias": "TweetBinderPRO", // User alias (@)
        "picture": "http://pbs.twimg.com/profile_images/1243598978425462796/sk_I23NT_normal.jpg", // Profile picture
        "followers": 1070, // Followers count
        "following": 1050,// Following count
        "verified": false, // True if account is verified
        "bio": "📊 Visit https://t.co/LkVmNmjxod and get free tweet counts\n📲 Stay tuned https://t.co/CfNP0dBrCV\n📧  marketing (@) https://t.co/LkVmNmjxod\n➕Follow: @TweetBinder", // Profile bio
        "age": 1383217118, // Unix time when account was created
        "counts": {
            "lists": 153, // Numer of public twitter lists which includes this account
            "statuses": 7549 // Published tweets count
        },
        "location": "Global", // Profile location
        "gender": "undefined", // Account estimated gender: male,female,undefined
        "value": 2.92 // Account economic value, calculated by Tweet Binder
```

Fields, as shown in the previous example, are:

* id&#x20;
* name&#x20;
* alias
* picture&#x20;
* followers
* following&#x20;
* verified&#x20;
* bio&#x20;
* age&#x20;
* counts&#x20;
  * lists
  * statuses&#x20;
* location&#x20;
* gender&#x20;
* value

## Get profiles by alias

Given a list of account @usernames returns their profiles info. Allows to pass up to 100 usernames by request.

## Get profiles by id

Given a list of account ids returns their profiles info. Allows to pass up to 100 ids by request.

## Get profile followers

Given a Twitter account, it allows to list their followers.

Use the **getUsersInfo** parameter to retrieve only account ids (getUsersInfo=false) or full accounts information (getUsersInfo=true). Keep in mind that getUsersInfo=true will discount one profile from your profiles balance for each result and will be slower.

Use the next parameter to iterate results by getting the value from the latest request next\_srt\_token response

## Get profile friends

Similar to Get profile followers but with followings, it works identically.
