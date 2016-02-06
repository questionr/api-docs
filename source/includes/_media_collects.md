# Media Collects

## Get All Media Collects

```shell
curl "https://questionr.com/api/v1/media_collects" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/media_collects HTTP/1.1
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
    "id": 1228,
    "question_id": 1227,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  },
  {
    "id": 1232,
    "question_id": 1231,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  }
]
```

This endpoint retrieves all media_collects.


Parameter | Description
--------- | -----------
ids | The ids of the media_collects to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/media_collects?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/media_collects?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Media Collect

```shell
curl "https://questionr.com/api/v1/media_collects/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/media_collects/<ID> HTTP/1.1
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
  "media_collect": {
    "id": 1236,
    "question_id": 1235,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  }
}
```

This endpoint retrieves a specific media_collect.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the media_collect to retrieve



## Create a Media Collect



```shell
curl "https://questionr.com/api/v1/media_collects" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/media_collects HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "media_collect": {
    "question_id": 1239,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  }
}
```

> The above command returns JSON of the newly created media_collect

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "media_collect": {
    "id": 1244,
    "question_id": 1243,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  }
}
```

## Update a Specific Media Collect



```shell
curl "https:questionr.com/api/v1/media_collects/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/media_collects/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "media_collect": {
    "question_id": 1247,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  }
}
```

> The above command returns JSON of the updated media_collect

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "media_collect": {
    "id": 1252,
    "question_id": 1251,
    "allow_video": true,
    "allow_audio": true,
    "allow_picture": true,
    "allow_file": true,
    "max_duration": 30,
    "max_file_size": 4
  }
}
```


## Delete a Specific Media Collect



```shell
curl "https:questionr.com/api/v1/media_collects/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/media_collects/<ID> HTTP/1.1
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

