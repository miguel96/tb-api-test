---
description: >-
  Using Tweet Binder's API you can also track conversations happening in real
  time. New publications will be added into your report right after they get
  published.
---

# Live reports

## Create Live Report

Route: \{{apiRoute\}}/search/twitter/live/

Use this endpoint to create a live report. You can pass some fields:

* query: standard query, check reference in [.](./README.md)
  * limit: important parameter. Your stream will stop tracking after it reaches this limit of publications. It is 35,000 by default.
* stream
  * startDate: unix time (in seconds) indicated when the stream will start tracking
  * endDate: (optional) unix time (in seconds) indicated when the stream will stop tracking

## Get reports updated since timestamp

Route: \{{apiRoute\}}/reports?status=generated\&generatedAt=gt|_1684485526_

This endpoint will let you check which ones of your reports got new publication since a given date.

## Get report new tweets

Route: \{{apiRoute\}}/reports/:reportId/transcript/tweets?updatedAt=gt|_1679558988_

This endpoint allows you to get only the tweets inserted into a report since a given date.

## Check report errors

Route: \{{apiRoute\}}/reports?status=generated\&generatedAt=gt|_1684485526_

Sometimes, if you pass an invalid rule your report will be flagged as stream error, this means that the rule (query) you inserted is not valid because it might have a special character or something. It's your responsibility to check the stream and fix it. Until you don't fix the rule, your report will not get new publications.&#x20;

You can check if you have failing reports with this request and use the [#update-report-stream](live-reports.md#update-report-stream "mention") endpoint to fix it. You can check the field errorStreams to get some info about error.

## Get tracking reports

\{{apiRoute\}}/reports?streamActive=true

This endpoint lists all your report that has an active stream.

## Update report stream

Use this endpoint to change your report rule. Parameters are the same ones you can pass when creating a live report:

* Every query operator like or, must, not
* limit
* startDate
* endDate

## Stop report stream&#x20;

Use this endpoint to stop a live report.

## Restart report stream

Endpoint to restart a stopped report.

