# Role

## Get all the Roles

```shell
http GET /api/role/ "Authorization: Token my_auth_token"
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
      "name": "singer"
    },
    {
      "id": 2,
      "name": "guitarist"
    },
    {
      "id": 3,
      "name": "drummer"
    }
  ]
}
```

This endpoint returns all the Roles and their ids.

### HTTP Request

`GET api/role`

### Get Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
page | pagination ID | No | query | integer
