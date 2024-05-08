# X Users Reports

X User reports are used to track the evolution of X (Twitter) Accounts. This feature allows you to automatically take a snapshot of a X (Twitter) account stats periodically and to make queries against those snapshots.

**Payload Exmaple:**

```
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
