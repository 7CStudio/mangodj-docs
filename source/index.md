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

search: true
---

# Introduction

Welcome! Here you can find docs for Mango API.

# Authentication

All authenticated requests will have a HTTP header `Authorization` containing `Token my_token_here`.

To get a new authorization token, send `POST` request to `/api/user_works/`
