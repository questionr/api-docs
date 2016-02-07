# File Replies

## Get All File Replies

```shell
curl "https://questionr.com/api/file_replies" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/file_replies HTTP/1.1
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
    "id": 1322,
    "response_id": 1321,
    "url": null,
    "uploaded": false,
    "name": null
  },
  {
    "id": 1329,
    "response_id": 1328,
    "url": null,
    "uploaded": false,
    "name": null
  }
]
```

This endpoint retrieves all file_replies.


Parameter | Description
--------- | -----------
ids | The ids of the file_replies to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/file_replies?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/file_replies?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific File Reply

```shell
curl "https://questionr.com/api/file_replies/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/file_replies/<ID> HTTP/1.1
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
  "file_reply": {
    "id": 1336,
    "response_id": 1335,
    "url": null,
    "uploaded": false,
    "name": null
  }
}
```

This endpoint retrieves a specific file_reply.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the file_reply to retrieve



## Create a File Reply



```shell
curl "https://questionr.com/api/file_replies" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/file_replies HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "file_reply": {
    "response_id": 1342,
    "url": null,
    "uploaded": false,
    "name": null
  }
}
```

> The above command returns JSON of the newly created file_reply

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "file_reply": {
    "id": 1350,
    "response_id": 1349,
    "url": null,
    "uploaded": false,
    "name": null
  }
}
```

## Update a Specific File Reply



```shell
curl "https:questionr.com/api/file_replies/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/file_replies/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "file_reply": {
    "response_id": 1356,
    "url": null,
    "uploaded": false,
    "name": null
  }
}
```

> The above command returns JSON of the updated file_reply

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "file_reply": {
    "id": 1364,
    "response_id": 1363,
    "url": null,
    "uploaded": false,
    "name": null
  }
}
```


## Delete a Specific File Reply



```shell
curl "https:questionr.com/api/file_replies/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/file_replies/<ID> HTTP/1.1
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

