---
method: POST
---

# Create user report

**Endpoint:** {{apiRoute}}/user-trackers/multi

**What it does:** this endpoint create user reports. Each user report will track the performance of one X (Twitter) user starting since the day it was activated. 

**Payload example:**

```
[
{"alias":"tweetbinder"},
{"alias":"audienseco"},
{"alias":"elonmusk"}
]

```
