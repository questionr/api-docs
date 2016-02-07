# Public Settings

## Get All Public Settings

```shell
curl "https://questionr.com/api/public_settings" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/public_settings HTTP/1.1
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
    "id": 1620,
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  },
  {
    "id": 1621,
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  }
]
```

This endpoint retrieves all public_settings.


Parameter | Description
--------- | -----------
ids | The ids of the public_settings to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/public_settings?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/public_settings?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Public Settings

```shell
curl "https://questionr.com/api/public_settings/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/public_settings/<ID> HTTP/1.1
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
  "public_settings": {
    "id": 1622,
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  }
}
```

This endpoint retrieves a specific public_settings.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the public_settings to retrieve



## Create a Public Settings



```shell
curl "https://questionr.com/api/public_settings" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/public_settings HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "public_settings": {
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  }
}
```

> The above command returns JSON of the newly created public_settings

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "public_settings": {
    "id": 1624,
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  }
}
```

## Update a Specific Public Settings



```shell
curl "https:questionr.com/api/public_settings/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/public_settings/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "public_settings": {
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  }
}
```

> The above command returns JSON of the updated public_settings

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "public_settings": {
    "id": 1626,
    "custom_default_release": null,
    "use_custom_default_release": false,
    "rights_owner": null,
    "user_id": null
  }
}
```


## Delete a Specific Public Settings



```shell
curl "https:questionr.com/api/public_settings/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/public_settings/<ID> HTTP/1.1
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

