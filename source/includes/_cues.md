# Cues

## Get All Cues

```shell
curl "https://questionr.com/api/v1/cues" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/cues HTTP/1.1
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
    "id": 1172,
    "text": null,
    "question_id": 1171,
    "type": "Cue"
  },
  {
    "id": 1176,
    "text": null,
    "question_id": 1175,
    "type": "Cue"
  }
]
```

This endpoint retrieves all cues.


Parameter | Description
--------- | -----------
ids | The ids of the cues to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/cues?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/cues?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Cue

```shell
curl "https://questionr.com/api/v1/cues/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/cues/<ID> HTTP/1.1
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
  "cue": {
    "id": 1180,
    "text": null,
    "question_id": 1179,
    "type": "Cue"
  }
}
```

This endpoint retrieves a specific cue.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the cue to retrieve



## Create a Cue



```shell
curl "https://questionr.com/api/v1/cues" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/cues HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "cue": {
    "text": null,
    "question_id": 1183,
    "type": "Cue"
  }
}
```

> The above command returns JSON of the newly created cue

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "cue": {
    "id": 1188,
    "text": null,
    "question_id": 1187,
    "type": "Cue"
  }
}
```

## Update a Specific Cue



```shell
curl "https:questionr.com/api/v1/cues/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/cues/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "cue": {
    "text": null,
    "question_id": 1191,
    "type": "Cue"
  }
}
```

> The above command returns JSON of the updated cue

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "cue": {
    "id": 1196,
    "text": null,
    "question_id": 1195,
    "type": "Cue"
  }
}
```


## Delete a Specific Cue



```shell
curl "https:questionr.com/api/v1/cues/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/cues/<ID> HTTP/1.1
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

