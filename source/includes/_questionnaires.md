# Questionnaires

## Get All Questionnaires

```shell
curl "https://questionr.com/api/v1/questionnaires" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/questionnaires HTTP/1.1
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
    "id": 1002,
    "name": "Thing to answer",
    "param": "1002-thing-to-answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "question_ids": [],
    "response_list_ids": [],
    "share_id": null,
    "public_settings_id": null,
    "user_id": 1001
  },
  {
    "id": 1004,
    "name": "Thing to answer",
    "param": "1004-thing-to-answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "question_ids": [],
    "response_list_ids": [],
    "share_id": null,
    "public_settings_id": null,
    "user_id": 1003
  }
]
```

This endpoint retrieves all questionnaires.


Parameter | Description
--------- | -----------
ids | The ids of the questionnaires to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/questionnaires?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/questionnaires?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Questionnaire

```shell
curl "https://questionr.com/api/v1/questionnaires/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/questionnaires/<ID> HTTP/1.1
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
  "questionnaire": {
    "id": 1006,
    "name": "Thing to answer",
    "param": "1006-thing-to-answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "question_ids": [],
    "response_list_ids": [],
    "share_id": null,
    "public_settings_id": null,
    "user_id": 1005
  }
}
```

This endpoint retrieves a specific questionnaire.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the questionnaire to retrieve



## Create a Questionnaire



```shell
curl "https://questionr.com/api/v1/questionnaires" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/questionnaires HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "questionnaire": {
    "name": "Thing to answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "user_id": 1007
  }
}
```

> The above command returns JSON of the newly created questionnaire

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "questionnaire": {
    "id": 1010,
    "name": "Thing to answer",
    "param": "1010-thing-to-answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "question_ids": [],
    "response_list_ids": [],
    "share_id": null,
    "public_settings_id": null,
    "user_id": 1009
  }
}
```

## Update a Specific Questionnaire



```shell
curl "https:questionr.com/api/v1/questionnaires/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/questionnaires/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "questionnaire": {
    "name": "Thing to answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "user_id": 1011
  }
}
```

> The above command returns JSON of the updated questionnaire

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "questionnaire": {
    "id": 1014,
    "name": "Thing to answer",
    "param": "1014-thing-to-answer",
    "release_selection": null,
    "custom_release_text": null,
    "public": false,
    "question_ids": [],
    "response_list_ids": [],
    "share_id": null,
    "public_settings_id": null,
    "user_id": 1013
  }
}
```


## Delete a Specific Questionnaire

Deleting a questionnaire deletes the associated questions and responses.


```shell
curl "https:questionr.com/api/v1/questionnaires/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/questionnaires/<ID> HTTP/1.1
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

