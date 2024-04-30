---
method: POST
---

# Create 7-day count

**Endpoint:** {{apiRoute}}/search/twitter-count/7-day

**Payload Example:** 

```
{
	"query":
        {
        "or":["Osasuna","#Osasuna"],
    	"must": [""],
        "nor":["@RealMadrid"],
        "lang":"en",
        "isRetweet":"included"
	}
}
```

After you run the query you will get a **"resourceId"**, to get the stats you will need to execute the action "Get report stats" (check "Report Actions") and the result will be:

```
{
    "stats": {
        "general": {
            "since": 1713860544,
            "until": 1714465344,
            "total": 2229
        },
        "timeline": [
            {
                "count": 7,
                "max": 1713880704,
                "min": 1713860544
            },
            {
                "count": 26,
                "max": 1713900864,
                "min": 1713880704
            },
            {
                "count": 18,
                "max": 1713921024,
                "min": 1713900864
            },
            {
                "count": 10,
                "max": 1713941184,
                "min": 1713921024
            },
            {
                "count": 11,
                "max": 1713961344,
                "min": 1713941184
            },
            {
                "count": 83,
                "max": 1713981504,
                "min": 1713961344
            },
            {
                "count": 39,
                "max": 1714001664,
                "min": 1713981504
            },
            {
                "count": 18,
                "max": 1714021824,
                "min": 1714001664
            },
            {
                "count": 8,
                "max": 1714041984,
                "min": 1714021824
            },
            {
                "count": 22,
                "max": 1714062144,
                "min": 1714041984
            },
            {
                "count": 6,
                "max": 1714082304,
                "min": 1714062144
            },
            {
                "count": 53,
                "max": 1714102464,
                "min": 1714082304
            },
            {
                "count": 246,
                "max": 1714122624,
                "min": 1714102464
            },
            {
                "count": 279,
                "max": 1714142784,
                "min": 1714122624
            },
            {
                "count": 230,
                "max": 1714162944,
                "min": 1714142784
            },
            {
                "count": 266,
                "max": 1714183104,
                "min": 1714162944
            },
            {
                "count": 97,
                "max": 1714203264,
                "min": 1714183104
            },
            {
                "count": 72,
                "max": 1714223424,
                "min": 1714203264
            },
            {
                "count": 101,
                "max": 1714243584,
                "min": 1714223424
            },
            {
                "count": 65,
                "max": 1714263744,
                "min": 1714243584
            },
            {
                "count": 41,
                "max": 1714283904,
                "min": 1714263744
            },
            {
                "count": 136,
                "max": 1714304064,
                "min": 1714283904
            },
            {
                "count": 287,
                "max": 1714324224,
                "min": 1714304064
            },
            {
                "count": 32,
                "max": 1714344384,
                "min": 1714324224
            },
            {
                "count": 6,
                "max": 1714364544,
                "min": 1714344384
            },
            {
                "count": 12,
                "max": 1714384704,
                "min": 1714364544
            },
            {
                "count": 18,
                "max": 1714404864,
                "min": 1714384704
            },
            {
                "count": 21,
                "max": 1714425024,
                "min": 1714404864
            },
            {
                "count": 5,
                "max": 1714445184,
                "min": 1714425024
            },
            {
                "count": 14,
                "max": 1714465344,
                "min": 1714445184
            }
        ]
    },
    "meta": {
        "updatedAt": 1714465364,
        "id": "bade995e-097e-42d1-a5e3-a5501170e0c7",
        "name": " (Osasuna OR #Osasuna) -(@RealMadrid) lang:en",
        "source": "twitter-count",
        "type": "7-day",
        "version": 2
    }
}
```
