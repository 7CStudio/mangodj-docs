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
            "description": null,
            "id": 1,
            "title": "user 2 band"
        },
        {
            "description": null,
            "id": 2,
            "title": "user 3 band"
        },
        {
            "description": "some desc",
            "id": 3,
            "title": "my supa act"
        }
    ]
}
```

This endpoint returns all the Acts

### HTTP Request

`GET api/acts`

### Get Parameters

Parameter | Description | Required | Parameter Type
--------- | ----------- | -------- | --------------
musician | Musician ID to filter | No | query
page | pagination ID | No | query

## Create a new Act

```shell
http POST /api/acts/ "Authorization: Token my_auth_token" title='Band of Pythons' description='Some Super Cool Band!'
```

> The above command returns JSON structured like this:

```json
{
    "description": "Some Super Cool Band!",
    "id": 4,
    "title": "Band of Pythons"
}
```

This endpoint creates an Act

### HTTP Request

`POST api/acts`

### Post Parameters

Parameter | Description | Required
--------- | ----------- | --------
title | Name of the Act | Yes
description | Description of the band | No

## Get an Act

```shell
http GET /api/acts/1/ "Authorization: Token my_auth_token"
```

> The above command returns JSON structured like this:

```json
{
    "description": "Some Super Cool Band!",
    "id": 1,
    "title": "Band of Pythons"
}
```

Returns a specific Act

### HTTP Request

`GET api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type
--------- | ----------- | -------- | --------------
id | ID of the Act | Yes | path

## Edit an Act, Multiple Fields

```shell
http PUT api/acts/4/ "Authorization: Token my_auth_token" title='Some Band' description='Some Band Desc'
```

> The above command returns JSON structured like this:

```json
{
    "description": "Some Band Desc",
    "id": 4,
    "title": "Some Band"
}
```

Edits a specific Act

### HTTP Request

`PUT api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type
--------- | ----------- | -------- | --------------
id | ID of the Act | Yes | path
title | New title of the Act | No | form
description | New description of the Act | No | form

## Edit an Act, Single Field

```shell
http PATCH api/acts/4/ "Authorization: Token my_auth_token" title='Some Band PATCHED'
```

> The above command returns JSON structured like this:

```json
{
    "description": "Some Band Desc",
    "id": 4,
    "title": "Some Band PATCHED"
}
```

Edits a specific Act

### HTTP Request

`PATCH api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type
--------- | ----------- | -------- | --------------
id | ID of the Act | Yes | path
title | New title of the Act | No | form
description | New description of the Act | No | form

## Delete an Act

```shell
http DELETE api/acts/4/ "Authorization: Token my_auth_token"
```

> The above command returns HTTP 204 status

Deletes an Act

### HTTP Request

`DELETE api/acts/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type
--------- | ----------- | -------- | --------------
id | ID of the Act | Yes | path
