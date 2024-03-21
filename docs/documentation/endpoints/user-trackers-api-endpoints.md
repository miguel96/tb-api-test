---
description: >-
  Tweet Binder’s User Trackers feature allows you to automatically take a
  snapshot of a twitter account stats periodically and to make queries against
  these snapshots.
---

# User Trackers' API endpoints

## Stats Payload

This is the tracker's information you will receive:&#x20;

```json
[
    {
        "_id": 1703732400, 
        "tweets": 7968, // Total tweets sent by the account
        "followers": 1080, // Number of followers of the account
        "following": 1135, // Number of accounts the account follows
        "lists": 153, // Number of list the account is in
        "followersFollowing": 0.95, // Ratio between followers and following of the account
        "createdAt": 1703732627, // 
        "updatedAt": 1703732627
    },
]

```

Fields, as shown in the previous example, are:

* \_id&#x20;
* tweets &#x20;
* followers&#x20;
* following&#x20;
* lists&#x20;
* followersFollowing&#x20;

## Create user trackers

It allows to create one or more trackers. You just need to pass user screen name (@username in twitter).&#x20;

Endpoint: \{{apiRoute\}}/user-trackers/multi

```postman_json
[{
	"alias": "osasuna"
}]
```

When creating a tracker, the message will be

```json
{
    "errors": [],
    "ok": [
        {
            "alias": "osasuna",
            "resourceId": "37ca9cf9-369c-4857-8bd4-40116b7bf820"
        }
    ]
}
```

## List user trackers

It returns a list of user trackers documents.

Endpoint: \{{apiRoute\}}/user-trackers/me

## Stop User Trackers

It stops selected trackers. After stopping a tracker your trackers balance will be restored. Know that when stopping a tracker, it will stop collecting information and that "uncollected" information cannot be recovered later.

## Get User Tracker stats

It checks a tracker stats

### Query

There are three main parameters when checking tracker stats. By filtering a tracker by date, you can see how many followers it grew in that period. These parameters are:

* startDate:
  * Unix time (seconds).
  * Reference date as start to get first stats doc
* endDate
  * Unix time (seconds).
  * Reference date to get last stats doc
* isTimeline
  * Optional, boolean
  * If it's false or undefined you will receive a response with two items. Account stats at startDate and accountStats at endDate
  * If it’s true you will receive a response with all the account snapshots between startDate and endDate.
