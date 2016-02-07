# Invites

## Get All Invites

```shell
curl "https://questionr.com/api/invites" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/invites HTTP/1.1
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
    "id": 1589,
    "contact_id": 1585,
    "share_id": 1588
  },
  {
    "id": 1594,
    "contact_id": 1590,
    "share_id": 1593
  }
]
```

This endpoint retrieves all invites.


Parameter | Description
--------- | -----------
ids | The ids of the invites to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/invites?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/invites?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Invite

```shell
curl "https://questionr.com/api/invites/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/invites/<ID> HTTP/1.1
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
  "invite": {
    "id": 1599,
    "contact_id": 1595,
    "share_id": 1598
  }
}
```

This endpoint retrieves a specific invite.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the invite to retrieve



## Create an Invite



```shell
curl "https://questionr.com/api/invites" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/invites HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "invite": {
    "contact_id": 1600,
    "share_id": 1603
  }
}
```

> The above command returns JSON of the newly created invite

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "invite": {
    "id": 1609,
    "contact_id": 1605,
    "share_id": 1608
  }
}
```

## Update a Specific Invite



```shell
curl "https:questionr.com/api/invites/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/invites/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "invite": {
    "contact_id": 1610,
    "share_id": 1613
  }
}
```

> The above command returns JSON of the updated invite

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "invite": {
    "id": 1619,
    "contact_id": 1615,
    "share_id": 1618
  }
}
```


## Delete a Specific Invite



```shell
curl "https:questionr.com/api/invites/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/invites/<ID> HTTP/1.1
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

