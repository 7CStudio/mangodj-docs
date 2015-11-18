# Musicians

## Get All Musicians

```shell
http GET /api/musicians/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
  "count": 4,
  "next": null,
  "previous": null,
  "results": [
    {
      "id": 2,
      "email": "hi@avi.im",
      "name": "some name",
      "profile_picture": "http://avi-from-console.com",
      "works": [
        19,
        20,
        21,
      ],
      "acts": [
        3,
        9
      ],
      "roles": [
        1
      ]
    },
    {
      "id": 3,
      "email": "newguy2@hi.com",
      "name": null,
      "profile_picture": null,
      "works": [],
      "acts": [],
      "roles": []
    },
    {
      "id": 4,
      "email": "3rduser@hi.com",
      "name": null,
      "profile_picture": null,
      "works": [
        5
      ],
      "acts": [],
      "roles": []
    },
    {
      "id": 5,
      "email": "user@email.com",
      "name": "Hans Zimmer",
      "profile_picture": "http://facebook/profile/pic.png",
      "works": [],
      "acts": [],
      "roles": []
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
  "id": 3,
  "email": "hi@avi.im",
  "name": "some name",
  "profile_picture": "http://avi-from-console.com",
  "works": [
    19,
    20,
    21,
  ],
  "acts": [
    3,
    9
  ],
  "roles": [
    1
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
