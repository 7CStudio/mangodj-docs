# Genre

## Get all the Genres

```shell
http GET /api/genre/ "Authorization: Token my_auth_token"
```

> The above command returns JSON structured like this:

```json
{
  "count": 3,
  "next": null,
  "previous": null,
  "results": [
    {
      "id": 1,
      "name": "rock"
    },
    {
      "id": 2,
      "name": "jazz"
    },
    {
      "id": 3,
      "name": "pop"
    }
  ]
}
```

This endpoint returns all the Genres and their ids.

### HTTP Request

`GET api/genre`

### Get Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
page | pagination ID | No | query | integer
