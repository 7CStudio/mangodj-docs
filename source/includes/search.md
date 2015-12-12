# Search

## Auto Suggestion

```shell
http GET /api/autosuggest?query=u "Authorization: Token my_auth_token"
```

> The above command returns JSON structured like this:

```json
[
  {
    "text": "user 2 band",
    "score": 75,
    "payload": {
      "users": [],
      "title": "user 2 band",
      "id": 1,
      "description": null
    }
  },
  {
    "text": "user 3 band",
    "score": 75,
    "payload": {
      "users": [],
      "title": "user 3 band",
      "id": 2,
      "description": null
    }
  }
]
```

This endpoint returns auto search suggestions for a given query string

### HTTP Request

`GET api/autosuggest?query=<query_param here>`

### Get Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
query | Search query parameter | Yes | query | string
