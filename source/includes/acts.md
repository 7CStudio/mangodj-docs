# Acts

## Get all the Acts

```shell
http GET /api/acts/ "Authorization: Token my_auth_token"
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
      "description": null,
      "title": "user 2 band",
      "users": []
    },
    {
      "id": 2,
      "description": null,
      "title": "user 3 band",
      "users": []
    },
    {
      "id": 3,
      "description": null,
      "title": "my supa act",
      "users": [
        "http://127.0.0.1:8000/api/musicians/3/"
      ]
    }
  ]
}
```

This endpoint returns all the Acts

### HTTP Request

`GET api/acts`

### Get Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
musician | Musician ID to filter | No | query | integer
page | pagination ID | No | query | integer

## Create a new Act

```shell
http POST /api/acts/ "Authorization: Token my_auth_token" title='Band of Pythons' description='Some Super Cool Band!'
```

> The above command returns JSON structured like this:

```json
{
    "description": "Some Super Cool Band!",
    "id": 5,
    "title": "Band of Pythons",
    "users": []
}
```

This endpoint creates an Act

### HTTP Request

`POST api/acts`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
title | Name of the Act | Yes | form | string
description | Description of the band | No | form | string

## Get an Act

```shell
http GET /api/acts/1/ "Authorization: Token my_auth_token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 5,
  "description": "Some Super Cool Band!",
  "title": "Band of Pythons",
  "users": [
    "http://127.0.0.1:8000/api/musicians/3/"
  ]
}
```

Returns a specific Act

### HTTP Request

`GET api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
id | ID of the Act | Yes | path | integer

## Edit an Act, Multiple Fields

```shell
http PUT api/acts/4/ "Authorization: Token my_auth_token" title='Some Band' description='Some Band Desc'
```

> The above command returns JSON structured like this:

```json
{
    "description": "Edited Description",
    "id": 4,
    "title": "Band of Pythons",
    "users": [
        "http://localhost:8000/api/musicians/3/"
    ]
}
```

Edits a specific Act

### HTTP Request

`PUT api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type 
--------- | ----------- | -------- | -------------- | ---------
id | ID of the Act | Yes | path | integer
title | New title of the Act | No | form | string
description | New description of the Act | No | form | string

## Edit an Act, Single Field

```shell
http PATCH api/acts/4/ "Authorization: Token my_auth_token" title='Some Band PATCHED'
```

> The above command returns JSON structured like this:

```json
{
    "description": "Some Band Desc",
    "id": 4,
    "title": "Some Band PATCHED",
    "users": []
}
```

Edits a specific Act

### HTTP Request

`PATCH api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | -----------
id | ID of the Act | Yes | path | integer
title | New title of the Act | No | form | string
description | New description of the Act | No | form | string

## Delete an Act

```shell
http DELETE api/acts/4/ "Authorization: Token my_auth_token"
```

> The above command returns HTTP 204 status

Deletes an Act

### HTTP Request

`DELETE api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
id | ID of the Act | Yes | path | integer
