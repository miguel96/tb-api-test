---
method: POST
---

# Create historical count

**Endpoint:** {{apiRoute}}/search/twitter-count/

**What it does:** This endpoint will give you the number of posts (tweets) of any given query without time limit.

**Limit of posts:** no limit.

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

After you run the query and the count is **generated** you will get a **"resourceId"**, to get the number of posts (tweets) you will need to execute the action "Get report stats" (check "Report Actions"). If you run the action too early, when the count is not generated yet, you will get an error.

