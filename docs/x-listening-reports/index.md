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

These are some parameters you can use
keyword	Standalone	Essential	"Matches a keyword within the body of a Tweet. This is a tokenized match, meaning that your keyword string will be matched against the tokenized text of the Tweet body. Tokenization splits words based on punctuation, symbols, and Unicode basic plane separator characters.

For example, a Tweet with the text “I like coca-cola” would be split into the following tokens: I, like, coca, cola. These tokens would then be compared to the keyword string used in your query. To match strings containing punctuation (for example coca-cola), symbol, or separator characters, you must wrap your keyword in double-quotes.

Example: pepsi OR cola OR ""coca cola"""
emoji	Standalone	Essential	"Matches an emoji within the body of a Tweet. Similar to a keyword, emojis are a tokenized match, meaning that your emoji will be matched against the tokenized text of the Tweet body.

Note that if an emoji has a variant, you must wrap it in double quotes to add to a query.

Example: (😃 OR 😡) 😬"
"exact phrase match"	Standalone	Essential	"Matches the exact phrase within the body of a Tweet.

Example: (""Twitter API"" OR #v2) -""recent search"""
#	Standalone	Essential	"Matches any Tweet containing a recognized hashtag, if the hashtag is a recognized entity in a Tweet.

This operator performs an exact match, NOT a tokenized match, meaning the rule #thanku will match posts with the exact hashtag #thanku, but not those with the hashtag #thankunext.

Example: #thankunext #fanart OR @arianagrande"
@tweetbinder 	Standalone	Essential	"Matches any Tweet that mentions the given username, if the username is a recognized entity (including the @ character).

Example: (@twitterdev OR @twitterapi) -@twitter"
$	Standalone	Elevated	"Matches any Tweet that contains the specified ‘cashtag’ (where the leading character of the token is the ‘$’ character).

Note that the cashtag operator relies on Twitter’s ‘symbols’ entity extraction to match cashtags, rather than trying to extract the cashtag from the body itself.

Example: $twtr OR @twitterdev -$fb"
from:	Standalone	Essential	"Matches any Tweet from a specific user.
The value can be either the username (excluding the @ character) or the user’s numeric user ID.

You can only pass a single username/ID per from: operator.

Example: from:twitterdev OR from:twitterapi -from:twitter"
to:	Standalone	Essential	"Matches any Tweet that is in reply to a particular user.
The value can be either the username (excluding the @ character) or the user’s numeric user ID.

You can only pass a single username/ID per to: operator.

Example: to:twitterdev OR to:twitterapi -to:twitter"
url:	Standalone	Essential	"Performs a tokenized match on any validly-formatted URL of a Tweet.

This operator can matches on the contents of both the url or expanded_url fields. For example, a Tweet containing ""You should check out Twitter Developer Labs: https://t.co/c0A36SWil4"" (with the short URL redirecting to https://developer.twitter.com) will match both the following rules:

from:TwitterDev url:""https://developer.twitter.com""
(because it will match the contents of entities.urls.expanded_url)

from:TwitterDev url:""https://t.co""
(because it will match the contents of entities.urls.url)

Tokens and phrases containing punctuation or special characters should be double-quoted (for example, url:""/developer""). Similarly, to match on a specific protocol, enclose in double-quotes (for example, url:""https://developer.twitter.com"")."
list:	Standalone	Elevated	"NEW Matches Tweets posted by users who are members of a specified list. 
For example, if @twitterdev and @twitterapi were members of List 123, and you included list:123 in your query, your response will only contain Tweets that have been published by those accounts. You can find List IDs by using the List lookup endpoint.
Please note that you can only use a single list: operator per query, and you can only specify a single List per list: operator.
Example: list:123"
has:media	Conjunction required	Essential	"Available alias: has:media_link
Matches Tweets that contain a media object, such as a photo, GIF, or video, as determined by Twitter. This will not match on media created with Periscope, or Tweets with links to other media hosting sites.

Example: (kittens OR puppies) has:media"
lang:	Conjunction required	Essential	"Matches Tweets that have been classified by Twitter as being of a particular language (if, and only if, the Tweet has been classified). It is important to note that each Tweet is currently only classified as being of one language, so AND’ing together multiple languages will yield no results.

You can only pass a single BCP 47 language identifier per lang: operator.

Note: if no language classification can be made the provided result is ‘und’ (for undefined).

Example: recommend #paris lang:en

The list below represents the currently supported languages and their corresponding BCP 47 language identifier:

Amharic: am German: de Malayalam: ml Slovak: sk Arabic: ar Greek: el Maldivian: dv Slovenian: sl Armenian: hy Gujarati: gu Marathi: mr Sorani Kurdish: ckb
Basque: eu Haitian Creole: ht Nepali: ne Spanish: es Bengali: bn Hebrew: iw Norwegian: no Swedish: sv Bosnian: bs Hindi: hi Oriya: or Tagalog: tl Bulgarian: bg Latinized Hindi: hi-Latn Panjabi: pa Tamil: ta Burmese: my Hungarian: hu Pashto: ps Telugu: te Croatian: hr Icelandic: is Persian: fa Thai: th Catalan: ca Indonesian: id Polish: pl Tibetan: bo Czech: cs Italian: it Portuguese: pt Traditional Chinese: zh-TW Danish: da Japanese: ja Romanian: ro Turkish: tr Dutch: nl Kannada: kn Russian: ru Ukrainian: uk English: en Khmer: km Serbian: sr Urdu: ur Estonian: et Korean: ko Simplified Chinese: zh-CN Uyghur: ug Finnish: fi Lao: lo Sindhi: sd Vietnamese: vi French: fr Latvian: lv Sinhala: si Welsh: cy Georgian: ka Lithuanian: lt"
retweets_of:	Standalone	Essential	"Matches Tweets that are Retweets of the specified user. The value can be either the username (excluding the @ character) or the user’s numeric user ID.

You can only pass a single username/ID per retweets_of: operator.

Example: retweets_of:twitterdev OR retweets_of:twitterapi"
in_reply_to_tweet_id:	Standalone	Essential	"Available alias: in_reply_to_status_id:
Matches on replies to the specified Tweet. 
 
Example: in_reply_to_tweet_id:1539382664746020864"
retweets_of_tweet_id:	Standalone	Essential	"Available alias: retweets_of_status_id:
Matches on explicit (or native) Retweets of the specified Tweet. Note that the Tweet ID used should be the ID of an original Tweet and not a Retweet. 
 
Example: retweets_of_tweet_id:1539382664746020864"
quotes_of_tweet_id:	Standalone	Essential	"Available alias: quotes_of_status_id:
Matches on Quote Tweets of the specified Tweet. Note that the Tweet ID used should be the ID of an original Tweet and not a Quote Tweet. 
 
Example: quotes_of_tweet_id:1739356084190560494"
place:	Standalone	Elevated	"Matches Tweets tagged with the specified location or Twitter place ID. Multi-word place names (“New York City”, “Palo Alto”) should be enclosed in quotes.

You can only pass a single place per place: operator.

Note: See the GET geo/search standard v1.1 endpoint for how to obtain Twitter place IDs.

Note: This operator will not match on Retweets, since Retweet's places are attached to the original Tweet. It will also not match on places attached to the original Tweet of a Quote Tweet.

Example: place:""new york city"" OR place:seattle OR place:fd70c22040963ac7"
place_country:	Standalone	Elevated	"Matches Tweets where the country code associated with a tagged place/location matches the given ISO alpha-2 character code.

You can find a list of valid ISO codes on Wikipedia.

You can only pass a single ISO code per place_country: operator.

Note: This operator will not match on Retweets, since Retweet's places are attached to the original Tweet. It will also not match on places attached to the original Tweet of a Quote Tweet.

Example: place_country:US OR place_country:MX OR place_country:CA"
is:retweet	Conjunction required	Essential	"Matches on Retweets that match the rest of the specified rule. This operator looks only for true Retweets (for example, those generated using the Retweet button). Quote Tweets will not be matched by this operator.

Example: data @twitterdev -is:retweet"
is:reply	Conjunction required	Essential	"Deliver only explicit replies that match a rule. Can also be negated to exclude replies that match a query from delivery.

Note: This operator is also available with the filtered stream endpoint. When used with filtered stream, this operator matches on replies to an original Tweet, replies in quoted Tweets, and replies in Retweets.

Example: from:twitterdev is:reply"
is:quote	Conjunction required	Essential	"Returns all Quote Tweets, also known as Tweets with comments.

Example: ""sentiment analysis"" is:quote"
is:verified	Conjunction required	Essential	"Deliver only Tweets whose authors are verified by Twitter.

Example: #nowplaying is:verified"
has:images	Conjunction required	Essential	"Matches Tweets that contain a recognized URL to an image.

Example: #meme has:images"
has:video_link	Conjunction required	Essential	"Available alias: has:videos
Matches Tweets that contain native Twitter videos, uploaded directly to Twitter. This will not match on videos created with Periscope, or Tweets with links to other video hosting sites.

Example: #icebucketchallenge has:video_link"
has:geo	Conjunction required	Elevated	"Matches Tweets that have Tweet-specific geolocation data provided by the Twitter user. This can be either a location in the form of a Twitter place, with the corresponding display name, geo polygon, and other fields, or in rare cases, a geo lat-long coordinate.

Note: Operators matching on place (Tweet geo) will only include matches from original tweets. Retweets do not contain any place data.

Example: recommend #paris has:geo -bakery"
has:hashtags	Conjunction required	Essential	"Matches Tweets that contain at least one hashtag.

Example: from:twitterdev -has:hashtags"
has:cashtags	Conjunction required	Elevated	"Matches Tweets that contain a cashtag symbol (with a leading ‘$’ character. For example, $tag).

Example: #stonks has:cashtags"
has:links	Conjunction required	Essential	"This operator matches Tweets which contain links and media in the Tweet body.

Example: from:twitterdev announcement has:links"
has:mentions	Conjunction required	Essential	"Matches Tweets that mention another Twitter user.

Example: #nowplaying has:mentions"
