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
The **stream** parameter is used to establish in unix time the start and the end of the tracking. The report will collect information to generate stats within that timeframe. The endDate is optional. The dates parameters **startDate** and **endDate** indicates when the reports starts and finishes. The report will not get tweets of the end date.

The parameter "limit" will establish a limit in the number of posts the report will get in case you want to get less than 50,000. 

After you run the query and the report status is **generated** you will get a **"resourceId"**, to get the stats you will need to execute the action "Get report stats" (check "Report Actions"). If you run the action too early, when the report is not generated yet or when the report has not received any post (tweet) yet, you will get an error. To check the status of the report execute the action "Get report state" (check "Report Actions").

The live report has several states:

- Generated: the report has been generated ok and it shows the stats
- Waiting: the report is waiting to get the first (posts) tweets
- Outdated: the report is being updated at the moment, the duration of this state depends on the number of posts (tweets) of the report, the more tweets the longer it will be.
