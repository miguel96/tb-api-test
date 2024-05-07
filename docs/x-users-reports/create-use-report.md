---
method: POST
---

# Create user report

**Endpoint:** {{apiRoute}}/user-trackers/multi

**What it does:** this endpoint create user reports. Each user report will track the performance of one X (Twitter) user starting since the day it was activated. These reports are also known as "trackers". 

**Payload example:**

```
[
{"alias":"tweetbinder"},
{"alias":"audienseco"},
{"alias":"elonmusk"}
]

```
If the user was already being tracked you will receive this error message: "active tracker with alias already exists".

If the user does not exist, you will receive a error 400 "Bad request".
