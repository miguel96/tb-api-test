---
method: PUT
---

# Update report stream

**Endpoint:** {{apiRoute}}/reports/:reportId/settings

**What it does:** This endpoint is used to edit or update the stream of a report. Usually used to edit the query of the report.

**Payload example:**

```
{
    "stream": {
        "raw": "obanos",
        "limit": 5,
        "startDate": 1686056612,
        "endDate": 1688648612
    }
}
```

