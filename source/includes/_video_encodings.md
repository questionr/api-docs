# Video Encodings

## Get All Video Encodings

```shell
curl "https://questionr.com/api/video_encodings" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/video_encodings HTTP/1.1
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
    "id": 1512,
    "status": "pending",
    "url": null,
    "thumbnail_url": null,
    "thumbnail_head_url": null,
    "video_encodable_id": null
  },
  {
    "id": 1513,
    "status": "pending",
    "url": null,
    "thumbnail_url": null,
    "thumbnail_head_url": null,
    "video_encodable_id": null
  }
]
```

This endpoint retrieves all video_encodings.


Parameter | Description
--------- | -----------
ids | The ids of the video_encodings to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/video_encodings?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/video_encodings?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Video Encoding

```shell
curl "https://questionr.com/api/video_encodings/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/video_encodings/<ID> HTTP/1.1
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
  "video_encoding": {
    "id": 1514,
    "status": "pending",
    "url": null,
    "thumbnail_url": null,
    "thumbnail_head_url": null,
    "video_encodable_id": null
  }
}
```

This endpoint retrieves a specific video_encoding.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the video_encoding to retrieve


