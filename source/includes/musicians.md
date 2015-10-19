# Musicians

## Get All Musicians

```shell
http GET /api/musicians/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
    "count": 3,
    "next": null,
    "previous": null,
    "results": [
        {
            "email": "ar_rahman@gmail.com",
            "id": 1,
            "name": "A R Rahman",
            "profile_picture": "http://ar-rahman.com",
            "works": []
        },
        {
            "email": "mobi@musics.com",
            "id": 2,
            "name": "Mobi",
            "profile_picture": null,
            "works": []
        },
        {
            "email": "hanszimmerman@musics.com",
            "id": 3,
            "name": "Hans Zimmerman",
            "profile_picture": null,
            "works": [
                {
                    "description": "Dark Knight Opening Video",
                    "id": 3,
                    "item_id": "youtube.com/mywork",
                    "source_type": 1,
                    "thumbnail": "youtube.com/thumbnail",
                    "title": "Dark Knight Opening Video"
                }
            ]
        }
    ]
}
```

This endpoint retrieves all the musicians.

### HTTP Request

`GET api/musicians`

### Query Parameters

Parameter | Description | Required
--------- | ----------- | --------
act | filter by `act` | No
page | pagination parameter | No

## Get A Specific Musician

```shell
http GET /api/musicians/3/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
    "email": "hanszimmerman@musics.com",
    "id": 3,
    "name": "Hans Zimmerman",
    "profile_picture": null,
    "works": [
        {
            "description": "Dark Knight Opening Video",
            "id": 3,
            "item_id": "youtube.com/mywork",
            "source_type": 1,
            "thumbnail": "youtube.com/thumbnail",
            "title": "Dark Knight Opening Video"
        }
    ]
}
```

This endpoint retrieves a specific musician.

### HTTP Request

`GET api/musicians/{id}`

### Query Parameters

Parameter | Description | Required
--------- | ----------- | --------
id | ID of the musician | Yes
act | filter by `act` | No
