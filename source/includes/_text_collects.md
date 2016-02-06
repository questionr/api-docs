# Text Collects

## Get All Text Collects

```shell
curl "https://questionr.com/api/v1/text_collects" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/text_collects HTTP/1.1
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
    "id": 1291,
    "question_id": 1290,
    "max_characters": 500
  },
  {
    "id": 1295,
    "question_id": 1294,
    "max_characters": 500
  }
]
```

This endpoint retrieves all text_collects.


Parameter | Description
--------- | -----------
ids | The ids of the text_collects to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/text_collects?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/text_collects?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Text Collect

```shell
curl "https://questionr.com/api/v1/text_collects/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/text_collects/<ID> HTTP/1.1
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
  "text_collect": {
    "id": 1299,
    "question_id": 1298,
    "max_characters": 500
  }
}
```

This endpoint retrieves a specific text_collect.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the text_collect to retrieve



## Create a Text Collect



```shell
curl "https://questionr.com/api/v1/text_collects" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/text_collects HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "text_collect": {
    "question_id": 1302,
    "max_characters": 500
  }
}
```

> The above command returns JSON of the newly created text_collect

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "text_collect": {
    "id": 1307,
    "question_id": 1306,
    "max_characters": 500
  }
}
```

## Update a Specific Text Collect



```shell
curl "https:questionr.com/api/v1/text_collects/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/text_collects/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "text_collect": {
    "question_id": 1310,
    "max_characters": 500
  }
}
```

> The above command returns JSON of the updated text_collect

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "text_collect": {
    "id": 1315,
    "question_id": 1314,
    "max_characters": 500
  }
}
```


## Delete a Specific Text Collect



```shell
curl "https:questionr.com/api/v1/text_collects/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/text_collects/<ID> HTTP/1.1
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

