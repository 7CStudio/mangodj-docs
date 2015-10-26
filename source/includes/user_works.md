# User Works

## Get All Works Of A User

```shell
http GET /api/user_works/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
  "count": 1,
  "next": null,
  "previous": null,
  "results": [
    {
      "id": 5,
      "description": "My new youtube video",
      "thumbnail": "https://www.youtube.com/watch?v=7JmhK6MHS40",
      "title": "Penny Dreadful - Soundtrack",
      "item_id": "https://www.youtube.com/watch?v=7JmhK6MHS40",
      "source_type": 1,
      "acts": null,
      "users": [
        "http://127.0.0.1:8000/api/musicians/4/"
      ]
    }
  ]
}
```

This endpoint retrieves all the works of current user.

### HTTP Request

`GET api/user_works`

### Query Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
page | pagination parameter | No | query | integer


## Get a specific User Work

```shell
http GET /api/user_works/2/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "description": "Some Amazing Description",
  "thumbnail": "https://www.youtube.com/watch?v=7JmhK6MHS40",
  "title": "Penny Dreadful - Soundtrack",
  "item_id": "https://www.youtube.com/watch?v=7JmhK6MHS40",
  "source_type": 1,
  "acts": null,
  "users": [
    "http://127.0.0.1:8000/api/musicians/4/"
  ]
}
```

This endpoint retrieves a specific User Work.


### HTTP Request

`GET api/user_works/{id}`

### URL Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
ID | The ID of the User Work to retrieve | Yes | path | integer

## Delete a User Work

```shell
http DELETE /api/user_works/2/ "Authorization: Token my_token_here"
```

> The above command returns HTTP Status 204


This endpoint deletes a specific User Work.


### HTTP Request

`DELETE api/user_works/{id}`

### URL Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
ID | The ID of the User Work to delete | Yes | path | integer

## Create a new User Work

```shell
http POST /api/user_works/ "Authorization: Token my_auth_token" item_id='https://www.youtube.com/watch?v=7JmhK6MHS40' source_type=1 thumbnail="https://www.youtube.com/watch?v=7JmhK6MHS40" title="Penny Dreadful - Soundtrack" description="Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London."
```

> The above command returns JSON structured like this:

```json
{
    "acts": null,
    "description": "Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London.",
    "id": 7,
    "item_id": "https://www.youtube.com/watch?v=7JmhK6MHS40",
    "source_type": 1,
    "thumbnail": "https://www.youtube.com/watch?v=7JmhK6MHS40",
    "title": "Penny Dreadful - Soundtrack",
    "users": []
}
```

This endpoint creates a new User Work

### HTTP Request

`POST api/user_works`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
item_id | URL to the work | Yes | form | string
source_type | Type of source | Yes | form | string
description | Description of the work | No | form | string
thumbnail | URL to the thumbnail | No | form | string
title | Title of the work | No | form | string

## Edit a Work, Multiple Fields

```shell
http PUT /api/user_works/6/ "Authorization: Token my_auth_token" item_id='https://www.googletube.com/watch?v=7JmhK6MHS40' source_type=1 thumbnail="https://www.googletube.com/watch?v=7JmhK6MHS40" title="Penny Dreadful - Soundtrack But From Google"
```

> The above command returns JSON structured like this:

```json
{
    "acts": null,
    "description": null,
    "id": 6,
    "item_id": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "source_type": 1,
    "thumbnail": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "title": "Penny Dreadful - Soundtrack But From Google",
    "users": [
      "http://127.0.0.1:8000/api/musicians/4/"
    ]
}
```

This endpoint edits a Work

### HTTP Request

`PUT api/user_works/{id}`

### Put Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
id | ID of the Work | Yes | path | integer
item_id | URL to the work | No | form | string
source_type | Type of source | No | form | string
description | Description of the work | No | form | string
thumbnail | URL to the thumbnail | No | form | string
title | Title of the work | No | form | string


## Edit a Work, Single Field

```shell
http PATCH /api/user_works/6/ "Authorization: Token my_auth_token" item_id='https://www.googletube.com/watch?v=7JmhK6MHS40' source_type=1 thumbnail="https://www.googletube.com/watch?v=7JmhK6MHS40" title="Penny Dreadful - Soundtrack But From Google"
```

> The above command returns JSON structured like this:

```json
{
    "acts": null,
    "description": null,
    "id": 5,
    "item_id": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "source_type": 1,
    "thumbnail": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "title": "Penny Dreadful - Soundtrack But From Google",
    "users": [
      "http://127.0.0.1:8000/api/musicians/4/"
    ]
}
```

This endpoint edits a Work

### HTTP Request

`PUT api/user_works/{id}`

### Patch Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
id | ID of the Work | Yes | path | integer
item_id | URL to the work | No | form | string
source_type | Type of source | No | form | string
description | Description of the work | No | form | string
thumbnail | URL to the thumbnail | No | form | string
title | Title of the work | No | form | string
