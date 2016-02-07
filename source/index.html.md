---
title: Questionr API Reference

language_tabs:
  - http
  - shell

toc_footers:
  - <a href='https://questionr.com/sign_up'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - questionnaires
  - shares
  - video_cues
  - text_cues
  - response_lists
  - responses
  - questions
  - cues
  - multi_choice_collects
  - media_collects
  - choices
  - text_collects

  - file_replies
  - video_replies
  - audio_replies
  - picture_replies
  - video_encodings
  - plans
  - quotas

  - playlists
  - ordered_video_encodables

  - mailing_lists
  - contacts
  - mailing_list_contacts
  - invites

  - public_settings
  - settings
  - searches
  - api_tokens

  - errors
search: true
---

# Introduction

Welcome to the Questionr API! You can use our API to access Questionr API endpoints, which can get information on questionnaires.

We have language bindings in Shell! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: Questionr $SECRET_ID $SECRET" \
  -H "Accept: application/vnd.questionr.com; version=1,application/json"
```

```http
GET /endpoint HTTP/1.1
Authorization: Questionr $SECRET_ID $SECRET
Accept: application/vnd.questionr.com; version=1,application/json
Host: questionr.com
```

> Make sure to replace `$SECRET_ID` and `$SECRET` with your API $SECRET_ID and $SECRET.

Questionr uses API keys to allow access to the API. You can generate a new API key in your [Questionr Dashboard](https://questionr.com/dashboard/settings/tokens).

Questionr expects the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Questionr $SECRET_ID $SECRET`

<aside class="notice">
You must replace <code>$SECRET_ID</code> and <code>$SECRET</code> with your API $SECRET_ID and $SECRET.
</aside>

