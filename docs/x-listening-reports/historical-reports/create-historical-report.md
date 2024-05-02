---
method: POST
---

# Create historical report

**Endpoint:** {{apiRoute}}/search/twitter/enterprise

**What it does:** This endpoint will give you the statistics of any given query without time limit.

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
        "startDate":1142981988,
        "endDate":1699434351,
        "isRetweet":"included"
	}
}
```

The parameter "limit" will establish a limit in the number of posts the report will get in case you want to get less than 50,000. 

The dates parameters **startDate** and **endDate** indicates when the reports starts and finishes. The report will not get tweets of the end date.

After you run the query and the report status is **generated** you will get a **"resourceId"**, to get the stats you will need to execute the action "Get report stats" (check "Report Actions"). If you run the action too early, when the report is not generated yet, you will get an error. To check the status of the report execute the action "Get report state" (check "Report Actions").
