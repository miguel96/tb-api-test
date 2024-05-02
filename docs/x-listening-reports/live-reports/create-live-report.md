---
method: POST
---

# Create live report

**Endpoint:** {{apiRoute}}/search/twitter/live/

**What it does:** This endpoint will give you the statistics of any given query starting in the moment the report is created.

**Limit of posts:** 50,000 per report.

**Payload Example:** 

```
{
	"query":{
        "or":["from:audienseco","from:tweetbinder","#FOABCN"],
        "must": [""],
        "nor":["is:retweet"],
        "limit": 100
	},
	"stream":{
	"startDate":{{startDate}},
	"endDate": {{endDate}}
	}
}
```
The **stream** parameter is used to establish in unix time the start and the end of the tracking. The report will collect information to generate stats within that timeframe. The endDate is optional.
