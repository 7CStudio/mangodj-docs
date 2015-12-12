# Insights

## Create a User Insight Object

```shell
http POST /api/user_insights/ "Authorization: Token my_auth_token" with body

{
    "number_of_roles": 2,
    "works": [{
        "item_id": "stuff gggg",
        "source_type": 1,
        "in_app_plays": 0,
        "is_individual_work": true
    }]
}
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "has_about": false,
  "number_of_roles": 0,
  "number_of_acts": 0,
  "profile_views": 0,
  "profile_searches": 0,
  "connects": 0,
  "facebook_page_id": null,
  "twitter_handle": null,
  "instagram_handle": null,
  "insight_score": "0.00",
  "twitter_followers_count": null,
  "works": [
    {
      "item_id": "stuff gggg",
      "source_type": 1,
      "is_individual_work": true,
      "in_app_plays": 0
    }
  ],
  "facebook_page_followers_count": null,
  "instagram_followers_count": null
}
```

This endpoint creates a new User Insight object

### HTTP Request

`POST api/user_insights/`

### Post Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
has_about | Whether a user has about field | No | form | boolean
number_of_roles | Number of roles | No | form | int
number_of_acts | Number of act | No | form | int
profile_views | Profile views | No | form | int
profile_searches | Profile searches | No | form | int
connects | Total friends | No | form | int
facebook_page_id | Facebook page ID | No | form | int
twitter_handle | Twitter Handle | No | form | string
instagram_handle | Instagram handle | No | form | string
works | See details below | No | form | JSON

`works` should be a list of dictionaries:

Field | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
item_id | Youtube video ID or Sound Cloud Track ID | Yes | form | string
source_type | Use `1` if YouTube and `2` if soundcloud | Yes | form | int
is_individual_work | Yes, if it's a individual work | Yes | form | boolean
in_app_plays | In app play count | Yes | form | int

# Get Insights data

```shell
http GET /api/user_insights/{user_id} "Authorization: Token my_auth_token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 7,
  "has_about": false,
  "number_of_roles": 1,
  "number_of_acts": 8,
  "profile_views": 8,
  "profile_searches": 7,
  "connects": 2,
  "facebook_page_id": 4546477,
  "twitter_handle": "gigpro",
  "instagram_handle": "gigpro",
  "insight_score": "7.00",
  "twitter_followers_count": 4546,
  "works": [
    {
      "item_id": "l4WNrvVjiTw",
      "source_type": 1,
      "is_individual_work": true,
      "in_app_plays": 7,
      "non_app_plays": 30
    },
    {
      "item_id": "l4WNrvVjiTw",
      "source_type": 2,
      "is_individual_work": false,
      "in_app_plays": 30,
      "non_app_plays": 230
    }
  ],
  "facebook_page_followers_count": 4546,
  "instagram_followers_count": 4564
}
```

This endpoint returns Insights Data

### HTTP Request

`GET api/user_insights/{user_id}`

### Get Parameters

Parameter | Description | Required | Parameter Type | Data Type
--------- | ----------- | -------- | -------------- | ---------
user id | User ID | Yes | path | integer

**Note**:

- Following fields are read only:

    - `insight_score`
    - `twitter_followers_count`
    - `facebook_page_followers_count`
    - `instagram_followers_count`
    - `non_app_plays` in `work`
