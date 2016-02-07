# Mailing List Contacts

## Get All Mailing List Contacts

```shell
curl "https://questionr.com/api/mailing_list_contacts" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/mailing_list_contacts HTTP/1.1
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
    "id": 1566,
    "mailing_list_id": 1564,
    "contact_id": 1565
  },
  {
    "id": 1569,
    "mailing_list_id": 1567,
    "contact_id": 1568
  }
]
```

This endpoint retrieves all mailing_list_contacts.


Parameter | Description
--------- | -----------
ids | The ids of the mailing_list_contacts to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/mailing_list_contacts?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/mailing_list_contacts?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Mailing List Contact

```shell
curl "https://questionr.com/api/mailing_list_contacts/2" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/mailing_list_contacts/<ID> HTTP/1.1
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
  "mailing_list_contact": {
    "id": 1572,
    "mailing_list_id": 1570,
    "contact_id": 1571
  }
}
```

This endpoint retrieves a specific mailing_list_contact.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the mailing_list_contact to retrieve



## Create a Mailing List Contact



```shell
curl "https://questionr.com/api/mailing_list_contacts" \
  --request POST \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/mailing_list_contacts HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "mailing_list_contact": {
    "mailing_list_id": 1573,
    "contact_id": 1574
  }
}
```

> The above command returns JSON of the newly created mailing_list_contact

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "mailing_list_contact": {
    "id": 1578,
    "mailing_list_id": 1576,
    "contact_id": 1577
  }
}
```

## Update a Specific Mailing List Contact



```shell
curl "https:questionr.com/api/mailing_list_contacts/2" \
  --request PATCH \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/mailing_list_contacts/<ID> HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "mailing_list_contact": {
    "mailing_list_id": 1579,
    "contact_id": 1580
  }
}
```

> The above command returns JSON of the updated mailing_list_contact

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "mailing_list_contact": {
    "id": 1584,
    "mailing_list_id": 1582,
    "contact_id": 1583
  }
}
```


## Delete a Specific Mailing List Contact



```shell
curl "https:questionr.com/api/mailing_list_contacts/2" \
  --request DELETE \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/mailing_list_contacts/<ID> HTTP/1.1
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

