# Shares

## Get All Shares

```shell
curl "https://questionr.com/api/shares" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/shares HTTP/1.1
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
    "id": 1017,
    "message": null,
    "questionnaire_id": 1016,
    "mailing_list_ids": [],
    "invite_ids": []
  },
  {
    "id": 1020,
    "message": null,
    "questionnaire_id": 1019,
    "mailing_list_ids": [],
    "invite_ids": []
  }
]
```

This endpoint retrieves all shares.


Parameter | Description
--------- | -----------
ids | The ids of the shares to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/shares?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/shares?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Share

```shell
curl "https://questionr.com/api/shares/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/shares/<ID> HTTP/1.1
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
  "share": {
    "id": 1023,
    "message": null,
    "questionnaire_id": 1022,
    "mailing_list_ids": [],
    "invite_ids": []
  }
}
```

This endpoint retrieves a specific share.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the share to retrieve



## Create a Share

Updating a share automatically emails an unique invite email to previously unemailed contacts in associated mailing lists.

<aside class="notice">
mailing_list_ids can be sent as part of the JSON payload.
</aside>



```shell
curl "https://questionr.com/api/shares" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/shares HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "share": {
    "message": null,
    "questionnaire_id": 1025,
    "mailing_list_ids": []
  }
}
```

> The above command returns JSON of the newly created share

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "share": {
    "id": 1029,
    "message": null,
    "questionnaire_id": 1028,
    "mailing_list_ids": [],
    "invite_ids": []
  }
}
```

## Update a Specific Share

Updating a share automatically emails an unique invite email to previously unemailed contacts in associated mailing lists.

<aside class="notice">
mailing_list_ids can be sent as part of the JSON payload.
</aside>



```shell
curl "https:questionr.com/api/shares/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/shares/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "share": {
    "message": null,
    "questionnaire_id": 1031,
    "mailing_list_ids": []
  }
}
```

> The above command returns JSON of the updated share

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "share": {
    "id": 1035,
    "message": null,
    "questionnaire_id": 1034,
    "mailing_list_ids": [],
    "invite_ids": []
  }
}
```


## Delete a Specific Share



```shell
curl "https:questionr.com/api/shares/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/shares/<ID> HTTP/1.1
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

