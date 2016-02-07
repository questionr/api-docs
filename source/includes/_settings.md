# Settings

## Get All Settings

```shell
curl "https://questionr.com/api/settings" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/settings HTTP/1.1
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
    "id": 1627,
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  },
  {
    "id": 1628,
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  }
]
```

This endpoint retrieves all settings.


Parameter | Description
--------- | -----------
ids | The ids of the settings to retrieve e.g. add a query string urlencoded `?ids[]=711&ids[]=712`

> Below is a similar request with ids in a query string

```shell
curl "https://questionr.com/api/settings?ids%5B%5D=711&ids%5B%5D=712" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```
```http
GET /api/settings?ids%5B%5D=711&ids%5B%5D=712 HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

## Get a Specific Settings

```shell
curl "https://questionr.com/api/settings/2" \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /api/settings/<ID> HTTP/1.1
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
  "settings": {
    "id": 1629,
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  }
}
```

This endpoint retrieves a specific settings.

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the settings to retrieve



## Create a Settings



```shell
curl "https://questionr.com/api/settings" \
  --request POST \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```

```http
POST /api/settings HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "settings": {
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  }
}
```

> The above command returns JSON of the newly created settings

```http
HTTP/1.1 201 Created
Content-Type: application/json
```
```json
{
  "settings": {
    "id": 1631,
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  }
}
```

## Update a Specific Settings



```shell
curl "https:questionr.com/api/settings/2" \
  --request PATCH \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json" \
  --data "$JSON"
```
```http
PATCH /api/settings/<ID> HTTP/1.1
Authorization: Questionr secret_id secret
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```
```json
{
  "settings": {
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  }
}
```

> The above command returns JSON of the updated settings

```http
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "settings": {
    "id": 1633,
    "questionnaires_help_visible": true,
    "questionnaire_edit_help_visible": true,
    "questionnaire_share_help_visible": true,
    "playlists_help_visible": true,
    "playlist_edit_help_visible": true,
    "mailing_list_edit_help_visible": true,
    "media_collect_help_visible": true,
    "user_id": null
  }
}
```


## Delete a Specific Settings



```shell
curl "https:questionr.com/api/settings/2" \
  --request DELETE \
  -H "Authorization: Questionr secret_id secret" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
DELETE /api/settings/<ID> HTTP/1.1
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

