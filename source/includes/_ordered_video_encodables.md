# Ordered Video Encodables

## Get All Ordered Video Encodables

```shell
curl "https://questionr.com/api/v1/ordered_video_encodables" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/ordered_video_encodables HTTP/1.1
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
    "id": 1531,
    "order": 1,
    "video_encodable_id": null,
    "playlist_id": 1530
  },
  {
    "id": 1534,
    "order": 2,
    "video_encodable_id": null,
    "playlist_id": 1533
  }
]
```

This endpoint retrieves all ordered_video_encodables.


Parameter | Description
--------- | -----------
ids | The ids of the ordered_video_encodables to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/ordered_video_encodables?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/ordered_video_encodables?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Ordered Video Encodable

```shell
curl "https://questionr.com/api/v1/ordered_video_encodables/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/ordered_video_encodables/<ID> HTTP/1.1
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
  "ordered_video_encodable": {
    "id": 1537,
    "order": 3,
    "video_encodable_id": null,
    "playlist_id": 1536
  }
}
```

This endpoint retrieves a specific ordered_video_encodable.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the ordered_video_encodable to retrieve



## Create an Ordered Video Encodable



```shell
curl "https://questionr.com/api/v1/ordered_video_encodables" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/ordered_video_encodables HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "ordered_video_encodable": {
    "order": 4,
    "video_encodable_id": null,
    "playlist_id": 1539
  }
}
```

> The above command returns JSON of the newly created ordered_video_encodable

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "ordered_video_encodable": {
    "id": 1543,
    "order": 5,
    "video_encodable_id": null,
    "playlist_id": 1542
  }
}
```

## Update a Specific Ordered Video Encodable



```shell
curl "https:questionr.com/api/v1/ordered_video_encodables/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/ordered_video_encodables/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "ordered_video_encodable": {
    "order": 6,
    "video_encodable_id": null,
    "playlist_id": 1545
  }
}
```

> The above command returns JSON of the updated ordered_video_encodable

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "ordered_video_encodable": {
    "id": 1549,
    "order": 7,
    "video_encodable_id": null,
    "playlist_id": 1548
  }
}
```


## Delete a Specific Ordered Video Encodable



```shell
curl "https:questionr.com/api/v1/ordered_video_encodables/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/ordered_video_encodables/<ID> HTTP/1.1
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

