# Contacts

## Get All Contacts

```shell
curl "https://questionr.com/api/v1/contacts" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/contacts HTTP/1.1
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
    "id": 1557,
    "email": "Fausto_1@questionr.com",
    "first_name": "Fausto",
    "last_name": "Dibbert",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  {
    "id": 1558,
    "email": "Tate_2@questionr.com",
    "first_name": "Tate",
    "last_name": "Windler",
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
curl "https://questionr.com/api/v1/contacts?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret"
```
```http
GET /api/v1/contacts?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Contact

```shell
curl "https://questionr.com/api/v1/contacts/2" \
  -H "Authorization: Questionr secret_id secret"
```

```http
GET /api/v1/contacts/<ID> HTTP/1.1
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
  "contact": {
    "id": 1559,
    "email": "Elmo_3@questionr.com",
    "first_name": "Elmo",
    "last_name": "Ebert",
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
curl "https://questionr.com/api/v1/contacts" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```

```http
POST /api/v1/contacts HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "contact": {
    "email": "Jane_4@questionr.com",
    "first_name": "Jane",
    "last_name": "Pagac",
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
    "email": "Kian_5@questionr.com",
    "first_name": "Kian",
    "last_name": "Fritsch",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  "mailing_list_contacts": []
}
```

## Update a Specific Contact



```shell
curl "https:questionr.com/api/v1/contacts/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  --data "$JSON"
```
```http
PATCH /api/v1/contacts/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "contact": {
    "email": "Weldon_6@questionr.com",
    "first_name": "Weldon",
    "last_name": "Ryan",
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
    "email": "Leonora_7@questionr.com",
    "first_name": "Leonora",
    "last_name": "O'Reilly",
    "user_id": null,
    "editable": true,
    "mailing_list_contact_ids": []
  },
  "mailing_list_contacts": []
}
```


## Delete a Specific Contact



```shell
curl "https:questionr.com/api/v1/contacts/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret"
```

```http
DELETE /api/v1/contacts/<ID> HTTP/1.1
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

