---
method: PUT
---

# Add or remove tags

**Endpoint:** {{apiRoute}}/user-trackers/tags

**What it does:** This endpoint inserts and groups one or more user reports (trackers) in a tag.

**Payload:**

```
{
  "add": [{{tagId}}],
  "delete": [],
  "trackers": [
    "{{userTrackerId}}"
  ]
}
```

