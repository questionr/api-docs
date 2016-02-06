# Text Cues

## Get All Text Cues

```shell
curl "https://questionr.com/api/v1/text_cues" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/text_cues HTTP/1.1
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
    "id": 1067,
    "text": "This is a text cue",
    "question_id": 1066,
    "type": "TextCue"
  },
  {
    "id": 1071,
    "text": "This is a text cue",
    "question_id": 1070,
    "type": "TextCue"
  }
]
```

This endpoint retrieves all text_cues.


Parameter | Description
--------- | -----------
ids | The ids of the text_cues to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/text_cues?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/text_cues?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Text Cue

```shell
curl "https://questionr.com/api/v1/text_cues/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/text_cues/<ID> HTTP/1.1
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
  "text_cue": {
    "id": 1075,
    "text": "This is a text cue",
    "question_id": 1074,
    "type": "TextCue"
  }
}
```

This endpoint retrieves a specific text_cue.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the text_cue to retrieve



## Create a Text Cue



```shell
curl "https://questionr.com/api/v1/text_cues" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/text_cues HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "text_cue": {
    "text": "This is a text cue",
    "question_id": 1078,
    "type": "TextCue"
  }
}
```

> The above command returns JSON of the newly created text_cue

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "text_cue": {
    "id": 1083,
    "text": "This is a text cue",
    "question_id": 1082,
    "type": "TextCue"
  }
}
```

## Update a Specific Text Cue



```shell
curl "https:questionr.com/api/v1/text_cues/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/text_cues/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "text_cue": {
    "text": "This is a text cue",
    "question_id": 1086,
    "type": "TextCue"
  }
}
```

> The above command returns JSON of the updated text_cue

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "text_cue": {
    "id": 1091,
    "text": "This is a text cue",
    "question_id": 1090,
    "type": "TextCue"
  }
}
```


## Delete a Specific Text Cue



```shell
curl "https:questionr.com/api/v1/text_cues/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/text_cues/<ID> HTTP/1.1
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

