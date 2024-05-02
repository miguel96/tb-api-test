---
method: GET
---

# Get report state

**Endpoint:** {{apiRoute}}/reports/:reportId

**What it does:** This endpoint is used to check the state of a report. 

There are several states in a report:

- Generated: the report stats have been generated correctly
- Waiting: the report is waiting to be generated because the posts (tweets) are still entering or because they will enter
- Outdated: the report is being updated and the stats will be generated correctly. After being outdated the report will be generated norally
- Deleted: the report has been deleted
- Archived: this is the state old report go to before the are deleted

