---
method: PUT
---

# Update report stream

**Endpoint:** {{apiRoute}}/reports/:reportId/settings

**What it does:** This endpoint is used to edit or update the query of a report.

**Limit of posts:** 50,000 per report.

**Payload Example:** 

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

