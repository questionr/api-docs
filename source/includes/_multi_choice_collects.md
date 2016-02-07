# Multi Choice Collects

## Get All Multi Choice Collects

```shell
curl "https://questionr.com/api/multi_choice_collects" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/multi_choice_collects HTTP/1.1
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
    "id": 1200,
    "question_id": 1199,
    "min_choices": 1,
    "max_choices": 3,
    "choice_ids": []
  },
  {
    "id": 1204,
    "question_id": 1203,
    "min_choices": 1,
    "max_choices": 3,
    "choice_ids": []
  }
]
```

This endpoint retrieves all multi_choice_collects.


Parameter | Description
--------- | -----------
ids | The ids of the multi_choice_collects to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/multi_choice_collects?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/multi_choice_collects?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Multi Choice Collect

```shell
curl "https://questionr.com/api/multi_choice_collects/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/multi_choice_collects/<ID> HTTP/1.1
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
  "multi_choice_collect": {
    "id": 1208,
    "question_id": 1207,
    "min_choices": 1,
    "max_choices": 3,
    "choice_ids": []
  },
  "choices": []
}
```

This endpoint retrieves a specific multi_choice_collect.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the multi_choice_collect to retrieve



## Create a Multi Choice Collect



```shell
curl "https://questionr.com/api/multi_choice_collects" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/multi_choice_collects HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "multi_choice_collect": {
    "question_id": 1211,
    "min_choices": 1,
    "max_choices": 3
  }
}
```

> The above command returns JSON of the newly created multi_choice_collect

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "multi_choice_collect": {
    "id": 1216,
    "question_id": 1215,
    "min_choices": 1,
    "max_choices": 3,
    "choice_ids": []
  },
  "choices": []
}
```

## Update a Specific Multi Choice Collect



```shell
curl "https:questionr.com/api/multi_choice_collects/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/multi_choice_collects/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "multi_choice_collect": {
    "question_id": 1219,
    "min_choices": 1,
    "max_choices": 3
  }
}
```

> The above command returns JSON of the updated multi_choice_collect

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "multi_choice_collect": {
    "id": 1224,
    "question_id": 1223,
    "min_choices": 1,
    "max_choices": 3,
    "choice_ids": []
  },
  "choices": []
}
```


## Delete a Specific Multi Choice Collect



```shell
curl "https:questionr.com/api/multi_choice_collects/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/multi_choice_collects/<ID> HTTP/1.1
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

