# Response Lists

## Get All Response Lists

```shell
curl "https://questionr.com/api/v1/response_lists" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/response_lists HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

> The above command returns JSON structured like this:

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
[
  {
    "id": 1093,
    "created_at": "2016-02-06T19:54:29.267Z",
    "accepted_release": null,
    "response_ids": [],
    "user_id": 1092,
    "questionnaire_id": null
  },
  {
    "id": 1095,
    "created_at": "2016-02-06T19:54:29.272Z",
    "accepted_release": null,
    "response_ids": [],
    "user_id": 1094,
    "questionnaire_id": null
  }
]
```

This endpoint retrieves all response_lists.


Parameter | Description
--------- | -----------
ids | The ids of the response_lists to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/response_lists?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/response_lists?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Response List

```shell
curl "https://questionr.com/api/v1/response_lists/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/response_lists/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

> The above command returns JSON structured like this:

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "response_list": {
    "id": 1097,
    "created_at": "2016-02-06T19:54:29.320Z",
    "accepted_release": null,
    "response_ids": [],
    "user_id": 1096,
    "questionnaire_id": null
  },
  "responses": []
}
```

This endpoint retrieves a specific response_list.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the response_list to retrieve



## Create a Response List



```shell
curl "https://questionr.com/api/v1/response_lists" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/response_lists HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "response_list": {
    "accepted_release": null,
    "user_id": 1098,
    "questionnaire_id": null
  }
}
```

> The above command returns JSON of the newly created response_list

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "response_list": {
    "id": 1101,
    "created_at": "2016-02-06T19:54:29.414Z",
    "accepted_release": null,
    "response_ids": [],
    "user_id": 1100,
    "questionnaire_id": null
  },
  "responses": []
}
```

## Update a Specific Response List



```shell
curl "https:questionr.com/api/v1/response_lists/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/response_lists/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "response_list": {
    "accepted_release": null,
    "user_id": 1102,
    "questionnaire_id": null
  }
}
```

> The above command returns JSON of the updated response_list

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "response_list": {
    "id": 1105,
    "created_at": "2016-02-06T19:54:29.507Z",
    "accepted_release": null,
    "response_ids": [],
    "user_id": 1104,
    "questionnaire_id": null
  },
  "responses": []
}
```


## Delete a Specific Response List



```shell
curl "https:questionr.com/api/v1/response_lists/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/response_lists/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

> The above command returns a empty JSON hash:

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
  {}
```

