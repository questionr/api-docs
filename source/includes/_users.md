# Users

## Get All Users

```shell
curl "https://questionr.com/api/v1/users"
  -H "Authorization: Token secret_id secret"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1001,
    "guest": null,
    "subscription_cancelled": null,
    "email": "Shane_1@questionr.com",
    "param": "1001-shane-1",
    "first_name": "Shane",
    "last_name": "Dach",
    "receive_updates": "Not in use",
    "questionnaire_ids": [],
    "question_ids": [],
    "response_list_ids": [],
    "api_token_ids": [],
    "subscription_id": null,
    "public_settings_id": null,
    "settings_id": null
  },
  {
    "id": 1002,
    "guest": null,
    "subscription_cancelled": null,
    "email": "Estella_2@questionr.com",
    "param": "1002-estella-2",
    "first_name": "Estella",
    "last_name": "Rodriguez",
    "receive_updates": "Not in use",
    "questionnaire_ids": [],
    "question_ids": [],
    "response_list_ids": [],
    "api_token_ids": [],
    "subscription_id": null,
    "public_settings_id": null,
    "settings_id": null
  }
]
```

This endpoint retrieves all users.

### HTTP Request

`GET https://questionr.com/api/v1/users`

### URL Parameters

Parameter | Description
--------- | -----------
ids | The ids of the users to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

### HTTP Request

`GET https://questionr.com/api/v1/users?ids%5B%5D=711&ids%5B%5D=712`

## Get a Specific User

```shell
curl "https://questionr.com/api/v1/users/2"
  -H "Authorization: Token secret_id secret"
```

> The above command returns JSON structured like this:

```json
{
  "user": {
    "id": 1003,
    "guest": null,
    "subscription_cancelled": null,
    "email": "Sandra_3@questionr.com",
    "param": "1003-sandra-3",
    "first_name": "Sandra",
    "last_name": "Dach",
    "receive_updates": "Not in use",
    "questionnaire_ids": [],
    "question_ids": [],
    "response_list_ids": [],
    "api_token_ids": [],
    "subscription_id": null,
    "public_settings_id": null,
    "settings_id": null
  },
  "settings": []
}
```

This endpoint retrieves a specific user.

### HTTP Request

`GET https://questionr.com/api/v1/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user to retrieve



## Create an User

```shell
curl --request POST "https:questionr.com/api/v1/user"
  -H "Authorization: Token secret_id secret"
  --data ''
```

> The above command returns JSON of the newly created user

### HTTP Request

`POST https://questionr.com/api/v1/users`



## Update a Specific User

```shell
curl --request PATCH "https:questionr.com/api/v1/user/2"
  -H "Authorization: Token secret_id secret"
  --data ''
```

> The above command returns JSON of the updated user

### HTTP Request

`PATCH https://questionr.com/api/v1/users/<ID>`



## Delete a Specific User

```shell
curl --request DELETE "https:questionr.com/api/v1/user/2"
  -H "Authorization: Token secret_id secret"
```

> The above command returns a empty JSON hash:

```json
  {}
```

### HTTP Request

`DELETE https://questionr.com/api/v1/users/<ID>`


