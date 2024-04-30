---
method: POST
---

# Create 7-day count

**Endpoint:** {{apiRoute}}/search/twitter-count/7-day

**Payload Example:** 

{
	"query":{
        "or":["Osasuna","#Osasuna"],
    	"must": [""],
        "nor":["@RealMadrid"],
        "lang":"en",
		"limit": 100,
        "isRetweet":"included"
	}
}
