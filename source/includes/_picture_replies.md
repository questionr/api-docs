# Picture Replies

## Get All Picture Replies

```shell
curl "https://questionr.com/api/picture_replies" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/picture_replies HTTP/1.1
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
    "id": 1469,
    "response_id": 1468,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  },
  {
    "id": 1476,
    "response_id": 1475,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  }
]
```

This endpoint retrieves all picture_replies.


Parameter | Description
--------- | -----------
ids | The ids of the picture_replies to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/picture_replies?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/picture_replies?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Picture Reply

```shell
curl "https://questionr.com/api/picture_replies/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/picture_replies/<ID> HTTP/1.1
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
  "picture_reply": {
    "id": 1483,
    "response_id": 1482,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  }
}
```

This endpoint retrieves a specific picture_reply.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the picture_reply to retrieve



## Create a Picture Reply



```shell
curl "https://questionr.com/api/picture_replies" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/picture_replies HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "picture_reply": {
    "response_id": 1489,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  }
}
```

> The above command returns JSON of the newly created picture_reply

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "picture_reply": {
    "id": 1497,
    "response_id": 1496,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  }
}
```

## Update a Specific Picture Reply



```shell
curl "https:questionr.com/api/picture_replies/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/picture_replies/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "picture_reply": {
    "response_id": 1503,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  }
}
```

> The above command returns JSON of the updated picture_reply

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "picture_reply": {
    "id": 1511,
    "response_id": 1510,
    "url": null,
    "uploaded": false,
    "thumbnail_url": null
  }
}
```


## Delete a Specific Picture Reply



```shell
curl "https:questionr.com/api/picture_replies/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/picture_replies/<ID> HTTP/1.1
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

