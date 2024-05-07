---
method: GET
---

# Get user report stats

**Endpoint:** {{apiRoute}}/user-trackers/:userTrackerId/stats?startDate={{startDate}}&endDate={{endDate}}

**What it does:** This endpoint shows the stats of any give user report. 

There are three main parameters when checking tracker stats. By filtering a tracker by date, you can see how many followers it grew in that period. These parameters are:

- startDate:
-- Unix time (seconds).
-- Reference date as start to get first stats doc
- endDate
-- Unix time (seconds).
-- Reference date to get last stats doc
- isTimeline
-- Optional, boolean
-- If it's false or undefined you will receive a response with two items. Account stats at startDate and accountStats at endDate
-- If it’s true you will receive a response with all the account snapshots between startDate and endDate.
