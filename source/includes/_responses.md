# Responses

## Get All Responses

```shell
curl "https://questionr.com/api/responses" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/responses HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
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
    "id": 1111,
    "text": "my response",
    "question_id": 1110,
    "response_list_id": 1107,
    "selected_choice_ids": [],
    "video_reply_id": null,
    "audio_reply_id": null,
    "picture_reply_id": null,
    "file_reply_id": null
  },
  {
    "id": 1117,
    "text": "my response",
    "question_id": 1116,
    "response_list_id": 1113,
    "selected_choice_ids": [],
    "video_reply_id": null,
    "audio_reply_id": null,
    "picture_reply_id": null,
    "file_reply_id": null
  }
]
```

This endpoint retrieves all responses.


Parameter | Description
--------- | -----------
ids | The ids of the responses to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/responses?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/responses?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Response

```shell
curl "https://questionr.com/api/responses/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/responses/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
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
  "response": {
    "id": 1123,
    "text": "my response",
    "question_id": 1122,
    "response_list_id": 1119,
    "selected_choice_ids": [],
    "video_reply_id": null,
    "audio_reply_id": null,
    "picture_reply_id": null,
    "file_reply_id": null
  },
  "video_replies": [],
  "audio_replies": [],
  "picture_replies": [],
  "file_replies": []
}
```

This endpoint retrieves a specific response.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the response to retrieve



## Create a Response



```shell
curl "https://questionr.com/api/responses" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/responses HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "response": {
    "text": "my response",
    "question_id": 1128,
    "response_list_id": 1125,
    "selected_choice_ids": []
  }
}
```

> The above command returns JSON of the newly created response

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "response": {
    "id": 1135,
    "text": "my response",
    "question_id": 1134,
    "response_list_id": 1131,
    "selected_choice_ids": [],
    "video_reply_id": null,
    "audio_reply_id": null,
    "picture_reply_id": null,
    "file_reply_id": null
  },
  "video_replies": [],
  "audio_replies": [],
  "picture_replies": [],
  "file_replies": []
}
```

## Update a Specific Response



```shell
curl "https:questionr.com/api/responses/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/responses/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "response": {
    "text": "my response",
    "question_id": 1140,
    "response_list_id": 1137,
    "selected_choice_ids": []
  }
}
```

> The above command returns JSON of the updated response

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "response": {
    "id": 1147,
    "text": "my response",
    "question_id": 1146,
    "response_list_id": 1143,
    "selected_choice_ids": [],
    "video_reply_id": null,
    "audio_reply_id": null,
    "picture_reply_id": null,
    "file_reply_id": null
  },
  "video_replies": [],
  "audio_replies": [],
  "picture_replies": [],
  "file_replies": []
}
```


## Delete a Specific Response



```shell
curl "https:questionr.com/api/responses/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/responses/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
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

