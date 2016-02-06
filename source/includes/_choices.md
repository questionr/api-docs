# Choices

## Get All Choices

```shell
curl "https://questionr.com/api/v1/choices" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/choices HTTP/1.1
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
    "id": 1257,
    "text": "1 Apples",
    "order": 1,
    "multi_choice_collect_id": 1256
  },
  {
    "id": 1262,
    "text": "2 Apples",
    "order": 2,
    "multi_choice_collect_id": 1261
  }
]
```

This endpoint retrieves all choices.


Parameter | Description
--------- | -----------
ids | The ids of the choices to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/choices?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/choices?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Choice

```shell
curl "https://questionr.com/api/v1/choices/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/choices/<ID> HTTP/1.1
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
  "choice": {
    "id": 1267,
    "text": "3 Apples",
    "order": 3,
    "multi_choice_collect_id": 1266
  }
}
```

This endpoint retrieves a specific choice.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the choice to retrieve



## Create a Choice



```shell
curl "https://questionr.com/api/v1/choices" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/choices HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "choice": {
    "text": "4 Apples",
    "order": 4,
    "multi_choice_collect_id": 1271
  }
}
```

> The above command returns JSON of the newly created choice

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "choice": {
    "id": 1277,
    "text": "5 Apples",
    "order": 5,
    "multi_choice_collect_id": 1276
  }
}
```

## Update a Specific Choice



```shell
curl "https:questionr.com/api/v1/choices/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/choices/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "choice": {
    "text": "6 Apples",
    "order": 6,
    "multi_choice_collect_id": 1281
  }
}
```

> The above command returns JSON of the updated choice

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "choice": {
    "id": 1287,
    "text": "7 Apples",
    "order": 7,
    "multi_choice_collect_id": 1286
  }
}
```


## Delete a Specific Choice



```shell
curl "https:questionr.com/api/v1/choices/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/choices/<ID> HTTP/1.1
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
