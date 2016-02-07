# Playlists

## Get All Playlists

```shell
curl "https://questionr.com/api/playlists" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/playlists HTTP/1.1
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
    "id": 1516,
    "name": "Great playlist 1",
    "user_id": 1515,
    "width": null,
    "height": null,
    "public": null,
    "editable": true,
    "ordered_video_encodable_ids": []
  },
  {
    "id": 1518,
    "name": "Great playlist 2",
    "user_id": 1517,
    "width": null,
    "height": null,
    "public": null,
    "editable": true,
    "ordered_video_encodable_ids": []
  }
]
```

This endpoint retrieves all playlists.


Parameter | Description
--------- | -----------
ids | The ids of the playlists to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/playlists?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/playlists?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Playlist

```shell
curl "https://questionr.com/api/playlists/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/playlists/<ID> HTTP/1.1
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
  "playlist": {
    "id": 1520,
    "name": "Great playlist 3",
    "user_id": 1519,
    "width": null,
    "height": null,
    "public": null,
    "editable": true,
    "ordered_video_encodable_ids": []
  }
}
```

This endpoint retrieves a specific playlist.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the playlist to retrieve



## Create a Playlist



```shell
curl "https://questionr.com/api/playlists" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/playlists HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "playlist": {
    "name": "Great playlist 4",
    "user_id": 1521,
    "width": null,
    "height": null,
    "public": null
  }
}
```

> The above command returns JSON of the newly created playlist

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "playlist": {
    "id": 1524,
    "name": "Great playlist 5",
    "user_id": 1523,
    "width": null,
    "height": null,
    "public": null,
    "editable": true,
    "ordered_video_encodable_ids": []
  }
}
```

## Update a Specific Playlist



```shell
curl "https:questionr.com/api/playlists/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/playlists/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "playlist": {
    "name": "Great playlist 6",
    "user_id": 1525,
    "width": null,
    "height": null,
    "public": null
  }
}
```

> The above command returns JSON of the updated playlist

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "playlist": {
    "id": 1528,
    "name": "Great playlist 7",
    "user_id": 1527,
    "width": null,
    "height": null,
    "public": null,
    "editable": true,
    "ordered_video_encodable_ids": []
  }
}
```


## Delete a Specific Playlist



```shell
curl "https:questionr.com/api/playlists/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/playlists/<ID> HTTP/1.1
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

