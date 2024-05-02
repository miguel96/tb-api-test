---
method: GET
---

# Check report errors

**Endpoint:** {{apiRoute}}/reports?status=generated&generatedAt=gt|1684485526

**What it does:** This endpoint is used to check what live reports have errors since a given date. The date must be in unix time, the number "1684485526" of the endpoint is just an example. Sometimes, if you pass an invalid rule your report will be flagged as stream error, this means that the rule (query) you inserted is not valid because it might have a special character or something. It's your responsibility to check the stream and fix it. Until you don't fix the rule, your report will not get new publications. 

You can check if you have failing reports with this request and use the Update report stream endpoint to fix it. You can check the field errorStreams to get some info about error.
