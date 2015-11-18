# User Profile

## Create a New User / Signup

```shell
http POST api/user_profiles/ access_token="facebook access token" email="user@email.com" name="Hans Zimmer" profile_picture="http://facebook/profile/pic.png"
```

> The above command returns JSON structured like this:

```json
{
    "auth_token": "89b87375895304da7dccff753bf0e38dd177254c",
    "user_profile_id": 5
}
```

Creates a new User.

### HTTP Request

`POST /api/user_profiles/`

### POST Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- |--------- | -------------- | ---------
access_token | Facebook access token | yes | form | string
email | email address | yes | form | string
name | name of the user | no | form | string
profile_picture | URL to the profile picture | no | form | string

## Get current User Profile

```shell
http GET api/user_profiles/ "Authorization: Token my_token_here"
```

> The above command returns JSON structured like this:

```json
{
  "count": 1,
  "next": null,
  "previous": null,
  "results": [
    {
      "id": 4,
      "email": "3rduser@hi.com",
      "name": null,
      "profile_picture": null,
      "works": [
        19,
        20,
        21,
        23
      ],
      "acts": [
        3,
        9
      ],
      "roles": [
        1,
        3
      ]
    }
  ]
}
```

Retrieve User Profile.

### HTTP Request

`GET /api/user_profiles/`
