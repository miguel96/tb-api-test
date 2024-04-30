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

After you run the query and the count is **generated** you will get a **"resourceId"**, to get the stats you will need to execute the action "Get report stats" (check "Report Actions"). If you run the action too early, when the count is not generated yet, you will get ane error.
