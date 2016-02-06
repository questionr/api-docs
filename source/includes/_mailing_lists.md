# Mailing Lists

## Get All Mailing Lists

```shell
curl "https://questionr.com/api/v1/mailing_lists" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/mailing_lists HTTP/1.1
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
    "id": 1550,
    "name": "An Awesom Mailing List",
    "user_id": null,
    "mailing_list_contact_ids": [],
    "share_ids": []
  },
  {
    "id": 1551,
    "name": "An Awesom Mailing List",
    "user_id": null,
    "mailing_list_contact_ids": [],
    "share_ids": []
  }
]
```

This endpoint retrieves all mailing_lists.


Parameter | Description
--------- | -----------
ids | The ids of the mailing_lists to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/v1/mailing_lists?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/mailing_lists?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Mailing List

```shell
curl "https://questionr.com/api/v1/mailing_lists/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/mailing_lists/<ID> HTTP/1.1
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
  "mailing_list": {
    "id": 1552,
    "name": "An Awesom Mailing List",
    "user_id": null,
    "mailing_list_contact_ids": [],
    "share_ids": []
  },
  "mailing_list_contacts": []
}
```

This endpoint retrieves a specific mailing_list.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the mailing_list to retrieve



## Create a Mailing List



```shell
curl "https://questionr.com/api/v1/mailing_lists" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/mailing_lists HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "mailing_list": {
    "name": "An Awesom Mailing List",
    "user_id": null
  }
}
```

> The above command returns JSON of the newly created mailing_list

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "mailing_list": {
    "id": 1554,
    "name": "An Awesom Mailing List",
    "user_id": null,
    "mailing_list_contact_ids": [],
    "share_ids": []
  },
  "mailing_list_contacts": []
}
```

## Update a Specific Mailing List



```shell
curl "https:questionr.com/api/v1/mailing_lists/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/mailing_lists/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "mailing_list": {
    "name": "An Awesom Mailing List",
    "user_id": null
  }
}
```

> The above command returns JSON of the updated mailing_list

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "mailing_list": {
    "id": 1556,
    "name": "An Awesom Mailing List",
    "user_id": null,
    "mailing_list_contact_ids": [],
    "share_ids": []
  },
  "mailing_list_contacts": []
}
```


## Delete a Specific Mailing List



```shell
curl "https:questionr.com/api/v1/mailing_lists/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/mailing_lists/<ID> HTTP/1.1
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

