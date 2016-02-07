# Api Tokens

## Get All Api Tokens

```shell
curl "https://questionr.com/api/api_tokens" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/api_tokens HTTP/1.1
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
    "id": 1635,
    "name": "Api Token Description",
    "secret_id": null,
    "secret": null,
    "last_used_at": null,
    "user_id": 1634
  },
  {
    "id": 1637,
    "name": "Api Token Description",
    "secret_id": null,
    "secret": null,
    "last_used_at": null,
    "user_id": 1636
  }
]
```

This endpoint retrieves all api_tokens.


Parameter | Description
--------- | -----------
ids | The ids of the api_tokens to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/api_tokens?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/api_tokens?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Api Token

```shell
curl "https://questionr.com/api/api_tokens/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/api_tokens/<ID> HTTP/1.1
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
  "api_token": {
    "id": 1639,
    "name": "Api Token Description",
    "secret_id": null,
    "secret": null,
    "last_used_at": null,
    "user_id": 1638
  }
}
```

This endpoint retrieves a specific api_token.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the api_token to retrieve



## Create an Api Token



```shell
curl "https://questionr.com/api/api_tokens" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/api_tokens HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "api_token": {
    "name": "Api Token Description",
    "user_id": 1640
  }
}
```

> The above command returns JSON of the newly created api_token

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "api_token": {
    "id": 1643,
    "name": "Api Token Description",
    "secret_id": null,
    "secret": null,
    "last_used_at": null,
    "user_id": 1642
  }
}
```

## Update a Specific Api Token



```shell
curl "https:questionr.com/api/api_tokens/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/api_tokens/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "api_token": {
    "name": "Api Token Description",
    "user_id": 1644
  }
}
```

> The above command returns JSON of the updated api_token

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "api_token": {
    "id": 1647,
    "name": "Api Token Description",
    "secret_id": null,
    "secret": null,
    "last_used_at": null,
    "user_id": 1646
  }
}
```


## Delete a Specific Api Token



```shell
curl "https:questionr.com/api/api_tokens/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/api_tokens/<ID> HTTP/1.1
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

