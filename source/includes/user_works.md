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
            "description": "My new youtube video",
            "id": 2,
            "item_id": "youtube.com/mywork",
            "source_type": 1,
            "thumbnail": "youtube.com/thumbnail",
            "title": "my video"
        }
    ]
}
```

This endpoint retrieves all the works of a user.

### HTTP Request

`GET api/user_works`

### Query Parameters

Parameter | Description | Required
--------- | ----------- | --------
page | pagination parameter | No


## Get a specific User Work

```shell
http GET /api/user_works/2/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
    "description": "My new youtube video",
    "id": 2,
    "item_id": "youtube.com/mywork",
    "source_type": 1,
    "thumbnail": "youtube.com/thumbnail",
    "title": "my video"
}
```

This endpoint retrieves a specific User Work.


### HTTP Request

`GET api/user_works/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the User Work to retrieve

## Delete a User Work

```shell
http DELETE /api/user_works/2/ "Authorization: Token my_token_here"
```

> The above command returns HTTP Status 204


This endpoint deletes a specific User Work.


### HTTP Request

`DELETE api/user_works/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the User Work to delete

## Create a new User Work

```shell
http POST /api/user_works/ "Authorization: Token my_auth_token" item_id='https://www.youtube.com/watch?v=7JmhK6MHS40' source_type=1 thumbnail="https://www.youtube.com/watch?v=7JmhK6MHS40" title="Penny Dreadful - Soundtrack" description="Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London."
```

> The above command returns JSON structured like this:

```json
{
    "description": "Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London.",
    "id": 6,
    "item_id": "https://www.youtube.com/watch?v=7JmhK6MHS40",
    "source_type": 1,
    "thumbnail": "https://www.youtube.com/watch?v=7JmhK6MHS40",
    "title": "Penny Dreadful - Soundtrack"
}
```

This endpoint creates a new User Work

### HTTP Request

`POST api/user_works`

### Post Parameters

Parameter | Description | Required
--------- | ----------- | --------
item_id | URL to the work | Yes
source_type | Type of source | Yes
description | Description of the work | No
thumbnail | URL to the thumbnail | No
title | Title of the work | No

## Edit a Work, Multiple Fields

```shell
http PUT /api/user_works/6/ "Authorization: Token my_auth_token" item_id='https://www.googletube.com/watch?v=7JmhK6MHS40' source_type=1 thumbnail="https://www.googletube.com/watch?v=7JmhK6MHS40" title="Penny Dreadful - Soundtrack But From Google"
```

> The above command returns JSON structured like this:

```json
{
    "description": "Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London.",
    "id": 6,
    "item_id": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "source_type": 1,
    "thumbnail": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "title": "Penny Dreadful - Soundtrack But From Google"
}
```

This endpoint edits a Work

### HTTP Request

`PUT api/user_works/{id}`

### Post Parameters

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
    "description": "Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London.",
    "id": 6,
    "item_id": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "source_type": 1,
    "thumbnail": "https://www.googletube.com/watch?v=7JmhK6MHS40",
    "title": "Penny Dreadful - PATCHED"
}
```

This endpoint edits a Work

### HTTP Request

`PUT api/user_works/{id}`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
id | ID of the Work | Yes | path | integer
item_id | URL to the work | No | form | string
source_type | Type of source | No | form | string
description | Description of the work | No | form | string
thumbnail | URL to the thumbnail | No | form | string
title | Title of the work | No | form | string
