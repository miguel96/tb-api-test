# Results navigation

Use these queries to navigate the results you will get from Tweet Binder's API.

**Types of navigation**: The results of Tweet Binder's API can be:

- Paginated
- Filtered
- Ordered

**Pagination**: The response to complex queries will always have the following format:

```
{
  “pagination”: {
    “offset”: 0,
    “limit”: 20,
    “total”: 100,
    “nextResults”: “?offset=1&limit=20”
  },
  “data”: [ … ]
}
```

- limit: integer; number of results per page, defaults to 20.
- total: integer; total number of results with the current query filters.
- nextResults: string; querystring needed to obtain the next page of results with the current query. 
- filters. If there are no results or more pages it will be null.
- data: array; Set of documents with the current query filters.

# Filtering results

**Pagination filters**:

- offset: page number, ie. “?offset=1”
- limit: resultset size limit, ie. “?limit=1”

**Field filters**: Other than the pagination filters, you can filter by any of the document's fields, although some of them might slow down the response. For instance:

- “?status=generated” would filter those reports that have stats.
- “?user.name=tweetbinder” would filter those publications (tweets) whose author is “tweetbinder”

The API is case sensitive, meaning that if we filter by “Tweetbinder” but the field contains “tweetbinder” it will yield zero results.

There are some modifiers that can speed up the filtering:

- lt: field value is less than, ie. “?total=lt|100”
- gt: field value is greater than, ie. “?total=gt|100”
- in: list of values, equivalent to a logical OR, ie. “?status=in|deleted,removed”
- nin: opposite of in, ie. “?status=nin|waiting,generated”
- size: applies only to array fields and refers to their size, ie. “?hashtags=size|1”
- regex: regular expression, ie. “?user.alias=/^celia/”
- exist: field exists, ie. “?user.location=exists|true”

**Ordering results:** To sort the results, the following filter can be applied: order: <field name>|<direction>

- field  name: it can be (almost) any document field.
- direction: -1 (descending order) or 1 (ascending order), if not present defaults to 1.

For instance, “?order=createdAt|-1” would return the results by creation date in a descending order.
