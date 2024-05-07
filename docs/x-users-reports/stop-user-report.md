---
method: PUT
---

# Stop user report

**Endpoint:** {{apiRoute}}/user-trackers/delete

**What it does:** This endpoint will stop a user report. Knwo that when you stop a user report, you won't be able to collect data unless you rectivate it.

**Payload:**

```
{
    "userTrackers":["{{userTrackerId}}"]
}
```
