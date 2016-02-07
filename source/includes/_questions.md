# Questions

## Get All Questions

```shell
curl "https://questionr.com/api/questions" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/questions HTTP/1.1
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
    "id": 1150,
    "order": 22,
    "required": false,
    "questionnaire_id": 1149,
    "response_ids": [],
    "text_cue_ids": [],
    "video_cue_ids": [],
    "multi_choice_collect_id": null,
    "media_collect_id": null,
    "text_collect_id": null
  },
  {
    "id": 1153,
    "order": 23,
    "required": false,
    "questionnaire_id": 1152,
    "response_ids": [],
    "text_cue_ids": [],
    "video_cue_ids": [],
    "multi_choice_collect_id": null,
    "media_collect_id": null,
    "text_collect_id": null
  }
]
```

This endpoint retrieves all questions.


Parameter | Description
--------- | -----------
ids | The ids of the questions to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/questions?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/questions?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Question

```shell
curl "https://questionr.com/api/questions/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/questions/<ID> HTTP/1.1
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
  "question": {
    "id": 1156,
    "order": 24,
    "required": false,
    "questionnaire_id": 1155,
    "response_ids": [],
    "text_cue_ids": [],
    "video_cue_ids": [],
    "multi_choice_collect_id": null,
    "media_collect_id": null,
    "text_collect_id": null
  },
  "text_cues": [],
  "video_cues": [],
  "multi_choice_collects": [],
  "media_collects": [],
  "text_collects": []
}
```

This endpoint retrieves a specific question.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the question to retrieve



## Create a Question



```shell
curl "https://questionr.com/api/questions" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/questions HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "question": {
    "order": 25,
    "required": false,
    "questionnaire_id": 1158
  }
}
```

> The above command returns JSON of the newly created question

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "question": {
    "id": 1162,
    "order": 26,
    "required": false,
    "questionnaire_id": 1161,
    "response_ids": [],
    "text_cue_ids": [],
    "video_cue_ids": [],
    "multi_choice_collect_id": null,
    "media_collect_id": null,
    "text_collect_id": null
  },
  "text_cues": [],
  "video_cues": [],
  "multi_choice_collects": [],
  "media_collects": [],
  "text_collects": []
}
```

## Update a Specific Question



```shell
curl "https:questionr.com/api/questions/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/questions/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "question": {
    "order": 27,
    "required": false,
    "questionnaire_id": 1164
  }
}
```

> The above command returns JSON of the updated question

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "question": {
    "id": 1168,
    "order": 28,
    "required": false,
    "questionnaire_id": 1167,
    "response_ids": [],
    "text_cue_ids": [],
    "video_cue_ids": [],
    "multi_choice_collect_id": null,
    "media_collect_id": null,
    "text_collect_id": null
  },
  "text_cues": [],
  "video_cues": [],
  "multi_choice_collects": [],
  "media_collects": [],
  "text_collects": []
}
```


## Delete a Specific Question



```shell
curl "https:questionr.com/api/questions/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/questions/<ID> HTTP/1.1
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

