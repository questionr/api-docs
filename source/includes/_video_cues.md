# Video Cues

## Get All Video Cues

```shell
curl "https://questionr.com/api/video_cues" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/video_cues HTTP/1.1
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
    "id": 1039,
    "key": "asdf234asdf",
    "question_id": 1038,
    "video_encoding_id": null
  },
  {
    "id": 1043,
    "key": "asdf234asdf",
    "question_id": 1042,
    "video_encoding_id": null
  }
]
```

This endpoint retrieves all video_cues.


Parameter | Description
--------- | -----------
ids | The ids of the video_cues to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/video_cues?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/video_cues?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Video Cue

```shell
curl "https://questionr.com/api/video_cues/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/video_cues/<ID> HTTP/1.1
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
  "video_cue": {
    "id": 1047,
    "key": "asdf234asdf",
    "question_id": 1046,
    "video_encoding_id": null
  }
}
```

This endpoint retrieves a specific video_cue.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the video_cue to retrieve



## Create a Video Cue



```shell
curl "https://questionr.com/api/video_cues" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/video_cues HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "video_cue": {
    "key": "asdf234asdf",
    "question_id": 1050
  }
}
```

> The above command returns JSON of the newly created video_cue

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "video_cue": {
    "id": 1055,
    "key": "asdf234asdf",
    "question_id": 1054,
    "video_encoding_id": null
  }
}
```

## Update a Specific Video Cue



```shell
curl "https:questionr.com/api/video_cues/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/video_cues/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "video_cue": {
    "key": "asdf234asdf",
    "question_id": 1058
  }
}
```

> The above command returns JSON of the updated video_cue

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "video_cue": {
    "id": 1063,
    "key": "asdf234asdf",
    "question_id": 1062,
    "video_encoding_id": null
  }
}
```


## Delete a Specific Video Cue



```shell
curl "https:questionr.com/api/video_cues/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/video_cues/<ID> HTTP/1.1
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

