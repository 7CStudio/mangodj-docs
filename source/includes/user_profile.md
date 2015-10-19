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

Parameter | Description | Type | Required
--------- | ----------- | ---- | --------
name | name of the user | string | yes
profile_picture | URL to the profile picture | string | yes
access_token | Facebook access token | string | yes
email | email address | string | yes

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
            "email": "3rduser@hi.com",
            "id": 4,
            "name": null,
            "profile_picture": null,
            "works": [
                {
                    "description": "My new youtube video",
                    "id": 3,
                    "item_id": "youtube.com/mywork",
                    "source_type": 1,
                    "thumbnail": "youtube.com/thumbnail",
                    "title": "my video"
                },
                {
                    "description": "Explorer Sir Malcolm Murray, American gunslinger Ethan Chandler and medium Vanessa Ives unite to combat supernatural threats in Victorian London.",
                    "id": 6,
                    "item_id": "https://www.googletube.com/watch?v=7JmhK6MHS40",
                    "source_type": 1,
                    "thumbnail": "https://www.googletube.com/watch?v=7JmhK6MHS40",
                    "title": "Penny Dreadful - PATCHED"
                }
            ]
        }
    ]
}
```

Retrieve User Profile.

### HTTP Request

`GET /api/user_profiles/`
