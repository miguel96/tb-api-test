# X Listening Reports

With our API you can create reports that analyze X (Twitter) content. This content is basically post (tweets). In this section we must differentiate "counts" from "reports". A count will only give us the number of posts (tweets) of a query, however, the "report" offers all the complete statistics. Counts are very useful when we want to quickly see how many posts (tweets) a particular event has obtained, which is also why counts are much faster than reports.

There are several types of reports/counts:

- Historical reports: Analyze information from the past

  - 7-day count
  - Historical count
  - 7-day report
  - Historical report
 
- Live reports: They analyze information in real time from the moment they are activated. There are no counts in live reports.

Live reports do not include engagement data (likes, reposts, impressions, etc.) because the posts are collected so quickly that there is no time for any engagement to enter. They can be updated later.

These are some parameters/operators you can use:

|Operator |Example|
|-----|--------|
|keyword|Paris       |
|OR  |Paris OR Pamplona OR "New York"      |	
|emoji|	(😃 OR 😡) 😬
|"exact phrase match"|	"Tweet Binder is great"
|#|	#Osasuna
|@tweetbinder| 	@ElonMusk
|$|	$BTC
|from:|	from:tweetbinder
|to:|	to:tweetbinder
|url:|	url:https://www.tweetbinder.com
|list:|	lists:1492601169428025349
|has:media|	"Tweet Binder" has:media
|lang:|	"Tweet Binder" lang:en
|retweets_of:|	retweets_of:tweetbinder
|in_reply_to_tweet_id:|	in_reply_to_tweet_id:1518703397020577793
|retweets_of_tweet_id:|	retweets_of_tweet_id:1518703397020577793
|quotes_of_tweet_id:|	quotes_of_tweet_id:1518703397020577793
|place:|	place:chicago
|place_country:|	place_contry:US
|is:retweet|	"Tweet Binder" is:retweet
|is:reply|	"Tweet Binder" is:reply
|is:quote|	"Tweet Binder" is:quote
|is:verified|	"Tweet Binder" is:verified
|has:images|	"Tweet Binder" has:images
|has:video_link|	"Tweet Binder" has:video_link
|has:geo|	"Tweet Binder" has:geo
|has:hashtags|	"Tweet Binder" has:hashtags
|has:cashtags|	"Tweet Binder" has:cashtags
|has:links|	"Tweet Binder" has:links
|has:mentions|	"Tweet Binder" has:mention
