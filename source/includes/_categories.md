# Categories

## Get a list of all user categories

```ruby
```

```shell
curl "https://www.example.com/api/v14/categories"
  -H "SECRET_TOKEN: xxx-yyy-zzz,CLIENT_ID: xxx-yyy-zzz, CLIENT_SECRET: xxx-yyy-zzz"
```

> The above command returns JSON structured like this:

```json
[  
   {  
      "id":2283796,
      "name":"Advertising",
      "code":"advertising",
      "parent_id":2283795,
      "is_system":true,
      "enabled":true,
      "guid":"254fcc1f-943d-4d53-9f56-42fe1d219b70",
      "mode":"other"
   },
   {  
      "id":2283811,
      "name":"Alcohol \u0026 Bars",
      "code":"alcohol_and_bars",
      "parent_id":2283810,
      "is_system":true,
      "enabled":true,
      "guid":"93568413-2e8f-41e0-85fd-387f1348269b",
      "mode":"spendable"
   }
]
```

This endpoint retrieves all user categories.

### HTTP Request

`GET http://www.example.com/api/v14/categories`

### Query Parameters

Parameter | Description
--------- | ------- 
CLIENT_ID | It is used to authenticate a User & It should be present in every request to server.
CLIENT_SECRET | It is used to authenticate a User & It should be present in every request to server.

## Get a Specific Category

```ruby

```

```shell
curl "http://www.example.com/api/v11/categories/2283811"
  -H "SECRET_TOKEN: xxx-yyy-zzz, CLIENT_ID: xxx-yyy-zzz, CLIENT_SECRET: xxx-yyy-zzz"
```



> The above command returns JSON structured like this:

```json
{  
      "id":2283811,
      "name":"Alcohol \u0026 Bars",
      "code":"alcohol_and_bars",
      "parent_id":2283810,
      "is_system":true,
      "enabled":true,
      "guid":"93568413-2e8f-41e0-85fd-387f1348269b",
      "mode":"spendable"
   }

```

This endpoint retrieves a specific category.

### HTTP Request

`GET http://www.example.com/api/v14/categories/:id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the category to retrieve

## Delete a Specific Category

```ruby
```

```shell
curl "http://www.example.com/api/v14/categories/2283811"
    -X DELETE
  -H "SECRET_TOKEN: xxx-yyy-zzz, CLIENT_ID: xxx-yyy-zzz, CLIENT_SECRET: xxx-yyy-zzz"
```
> The above command returns JSON structured like this:

```json
{
  "id": 2283811,
  "deleted" : ":("
}
```

This endpoint deletes a specific category.

### HTTP Request

`DELETE https://www.example.com/api/v14/categories/:id`

### URL Parameters

Parameter | Description
--------- | -----------
:id | The ID of the category to delete
