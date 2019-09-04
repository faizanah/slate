---
title: AION Fentury API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby

toc_footers:
  - <a href='https://aiondigital.com/'>Documentation Powered by Aion Digital</a>

includes:
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

# Attachments
In order to send create credentials using API, You need to send in cloud URLs of the file. If cloud URLs are not present, Use this API to get a pre-signed URL from MaiaExchange. The URL is valid for 10 minutes, And during that you can upload the document directly onto it without any auth required. (Note this does not scan for virus, Your creation may fail on later steps if virus or any other error may be found)

> Get a pre signed AWS-S3 to upload your file directly onto S3 and then use this uploaded file url to create credentials.

```shell
curl -X GET --header 'Accept: application/json' 'https://maiaexchange.com/api/v1.1/attachments/request_upload_url?api_key=dfd45a161ea941ce0030f420f61b91bd&'
```

```shell
uri = URI.parse('https://maiaexchange.com/api/v1.1/attachments/request_upload_url')
http = Net::HTTP.new(uri.host, uri.port)
request = Net::HTTP::Post.new(uri.request_uri, {'Content-Type' => 'text/json', 'X-Api-Key' => API_KEY })
http.request(request)
```

# Categories

## Get a list of all user categories

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

