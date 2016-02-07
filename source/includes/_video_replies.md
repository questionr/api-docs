# Video Replies

## Get All Video Replies

```shell
curl "https://questionr.com/api/video_replies" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/video_replies HTTP/1.1
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
    "id": 1371,
    "response_id": 1370,
    "key": null,
    "video_encoding_id": null
  },
  {
    "id": 1378,
    "response_id": 1377,
    "key": null,
    "video_encoding_id": null
  }
]
```

This endpoint retrieves all video_replies.


Parameter | Description
--------- | -----------
ids | The ids of the video_replies to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/video_replies?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/video_replies?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Video Reply

```shell
curl "https://questionr.com/api/video_replies/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/video_replies/<ID> HTTP/1.1
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
  "video_reply": {
    "id": 1385,
    "response_id": 1384,
    "key": null,
    "video_encoding_id": null
  }
}
```

This endpoint retrieves a specific video_reply.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the video_reply to retrieve



## Create a Video Reply



```shell
curl "https://questionr.com/api/video_replies" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/video_replies HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "video_reply": {
    "response_id": 1391,
    "key": null,
    "video_encoding_id": null
  }
}
```

> The above command returns JSON of the newly created video_reply

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "video_reply": {
    "id": 1399,
    "response_id": 1398,
    "key": null,
    "video_encoding_id": null
  }
}
```

## Update a Specific Video Reply



```shell
curl "https:questionr.com/api/video_replies/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/video_replies/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "video_reply": {
    "response_id": 1405,
    "key": null,
    "video_encoding_id": null
  }
}
```

> The above command returns JSON of the updated video_reply

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "video_reply": {
    "id": 1413,
    "response_id": 1412,
    "key": null,
    "video_encoding_id": null
  }
}
```


## Delete a Specific Video Reply



```shell
curl "https:questionr.com/api/video_replies/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/video_replies/<ID> HTTP/1.1
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

