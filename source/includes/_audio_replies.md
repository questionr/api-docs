# Audio Replies

## Get All Audio Replies

```shell
curl "https://questionr.com/api/v1/audio_replies" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/audio_replies HTTP/1.1
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
    "id": 1420,
    "response_id": 1419
  },
  {
    "id": 1427,
    "response_id": 1426
  }
]
```

This endpoint retrieves all audio_replies.


Parameter | Description
--------- | -----------
ids | The ids of the audio_replies to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/audio_replies?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/audio_replies?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Audio Reply

```shell
curl "https://questionr.com/api/v1/audio_replies/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/audio_replies/<ID> HTTP/1.1
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
  "audio_reply": {
    "id": 1434,
    "response_id": 1433
  }
}
```

This endpoint retrieves a specific audio_reply.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the audio_reply to retrieve



## Create an Audio Reply



```shell
curl "https://questionr.com/api/v1/audio_replies" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/audio_replies HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "audio_reply": {
    "response_id": 1440
  }
}
```

> The above command returns JSON of the newly created audio_reply

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "audio_reply": {
    "id": 1448,
    "response_id": 1447
  }
}
```

## Update a Specific Audio Reply



```shell
curl "https:questionr.com/api/v1/audio_replies/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/audio_replies/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "audio_reply": {
    "response_id": 1454
  }
}
```

> The above command returns JSON of the updated audio_reply

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "audio_reply": {
    "id": 1462,
    "response_id": 1461
  }
}
```


## Delete a Specific Audio Reply



```shell
curl "https:questionr.com/api/v1/audio_replies/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/audio_replies/<ID> HTTP/1.1
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

