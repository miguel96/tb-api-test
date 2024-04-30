---
method: POST
---

# Create 7-day count

**Endpoint:** {{apiRoute}}/search/twitter-count/7-day

**Payload Example:** 

```
{
	"query":{
        "or":["Osasuna","#Osasuna"],
    	"must": [""],
        "nor":["@RealMadrid"],
        "lang":"en",
	"isRetweet":"included"
	}
}
```

After you run this query you will get a "resourceId", to get the stats you will need to execute the action "Get rpeort stats" and you will get something  
