---
title: AION Fentury API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby

toc_footers:
  - <a href='https://aiondigital.com/'>Documentation Powered by Aion Digital</a>

includes:
  - categories
  - errors

search: true
---

# Introduction
Welcome to the AION Digital World! Future of Fintech.

Personal finance manager which connects to your bank accounts automatically, allows you to keep track of your bills, set financial goals and get advice.


We have language bindings in Shell, Ruby. You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, set your API key in your header:

This uses an `CLIENT ID` and `CLIENT SECRET` to allow access to the API. The API expects the 
`CLIENT ID` and `CLIENT SECRET` to be included in all API requests to the server in the header of the request.

The `CLIENT ID` and `CLIENT SECRET` is set in the header. You will get a 401 if the `CLIENT ID` is missing in header, is invalid or has been changed by the UI.


You can regenerate your API KEY using the UI above whenever you like. Please
note that when the API KEY is regenerated the old key will continue to work
until you explicitly deactivate it.

```ruby

```
