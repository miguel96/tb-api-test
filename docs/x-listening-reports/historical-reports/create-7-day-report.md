---
method: POST
---

# Create 7-day report

**Endpoint:** {{apiRoute}}/search/twitter/7-day

**What it does:** This endpoint will give you the statistics of any given query in the last 7 days.

**Limit of posts:** 50,000 per report.

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

The parameter "limit" will establish a limit in the number of posts the report will get in case you want to get less than 50,000. 

After you run the query and the report status is **generated** you will get a **"resourceId"**, to get the stats you will need to execute the action "Get report stats" (check "Report Actions"). If you run the action too early, when the report is not generated yet, you will get an error. To check the status of the report execute the action "Get report state" (check "Report Actions").
