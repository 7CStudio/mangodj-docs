---
title: API Reference

language_tabs:
  - python
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - user_profile
  - user_works
  - musicians
  - acts
  - search
  - insights
  - role
  - genre

search: true
---

# Introduction

Welcome! Here you can find docs for Mango API.

# Authentication

```shell
http GET /api/protected_resource "Authorization: Token 89b87375895304da7dccff753bf0e38dd177254c"
```

All requests, except for signup, needs to be authenticated. Hence all requests need to have a HTTP header `Authorization` containing string `Token my_token_here`.

To get a new authorization token, send `POST` request to `/api/user_works/`