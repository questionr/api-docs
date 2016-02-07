# Contacts

## Get All Contacts

```shell
curl "https://questionr.com/api/contacts" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/contacts HTTP/1.1
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
    "id": 1557,
    "email": "Ward_1@questionr.com",
    "first_name": "Ward",
    "last_name": "Auer",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  {
    "id": 1558,
    "email": "Orville_2@questionr.com",
    "first_name": "Orville",
    "last_name": "Harber",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  }
]
```

This endpoint retrieves all contacts.


Parameter | Description
--------- | -----------
ids | The ids of the contacts to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/contacts?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/contacts?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Contact

```shell
curl "https://questionr.com/api/contacts/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/contacts/<ID> HTTP/1.1
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
  "contact": {
    "id": 1559,
    "email": "Ludie_3@questionr.com",
    "first_name": "Ludie",
    "last_name": "Bayer",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  "mailing_list_contacts": []
}
```

This endpoint retrieves a specific contact.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve



## Create a Contact



```shell
curl "https://questionr.com/api/contacts" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/contacts HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "contact": {
    "email": "Vicente_4@questionr.com",
    "first_name": "Vicente",
    "last_name": "Feeney",
    "user_id": null,
    "editable": true
  }
}
```

> The above command returns JSON of the newly created contact

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "contact": {
    "id": 1561,
    "email": "Adolfo_5@questionr.com",
    "first_name": "Adolfo",
    "last_name": "Gulgowski",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  "mailing_list_contacts": []
}
```

## Update a Specific Contact



```shell
curl "https:questionr.com/api/contacts/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/contacts/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "contact": {
    "email": "Wanda_6@questionr.com",
    "first_name": "Wanda",
    "last_name": "McKenzie",
    "user_id": null,
    "editable": true
  }
}
```

> The above command returns JSON of the updated contact

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "contact": {
    "id": 1563,
    "email": "Alessandra_7@questionr.com",
    "first_name": "Alessandra",
    "last_name": "Crist",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  "mailing_list_contacts": []
}
```


## Delete a Specific Contact



```shell
curl "https:questionr.com/api/contacts/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/contacts/<ID> HTTP/1.1
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

