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
      "id": 1,
      "email": "newguy2@hi.com",
      "name": null,
      "profile_picture": null,
      "works": [
        "http://127.0.0.1:8000/api/user_works/2/"
      ],
      "acts": []
    },
    {
      "id": 2,
      "email": "3rduser@hi.com",
      "name": null,
      "profile_picture": null,
      "works": [
        "http://127.0.0.1:8000/api/user_works/5/"
      ],
      "acts": [
        "http://127.0.0.1:8000/api/acts/3/"
      ]
    },
    {
      "id": 3,
      "email": "user@email.com",
      "name": "Hans Zimmer",
      "profile_picture": "http://facebook/profile/pic.png",
      "works": [],
      "acts": []
    }
  ]
}
```

This endpoint retrieves all the musicians.

### HTTP Request

`GET api/musicians`

### GET Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
act | filter by `act` | No | query | integer
page | pagination parameter | No | query | integer

## Get A Specific Musician

```shell
http GET /api/musicians/3/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
    "email": "hanszimmer@musics.com",
    "id": 3,
    "name": "Hans Zimmer",
    "profile_picture": null,
    "works": [
        "http://127.0.0.1:8000/api/user_works/7/"
    ]
}
```

This endpoint retrieves a specific musician.

### HTTP Request

`GET api/musicians/{id}`

### Query Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
id | ID of the musician | Yes | path | integer
act | filter by `act` | No | query | integer
