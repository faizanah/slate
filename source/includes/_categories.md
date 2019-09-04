# Categories

## Get a list of all user categories

```ruby
```

```shell
curl "http://api.aiondigital.com/api/categories"
  -H "client_id: xxx-yyy-zzz, client_secret: xxx-yyy-zzz"
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

`GET http://api.aiondigital.com/v1/categories`

### Query Parameters

Parameter | Description
--------- | ------- 
client_id | It is used to authenticate a User & It should be present in every request to server.
client_secret | It is used to authenticate a User & It should be present in every request to server.

## Get a Specific Category

```ruby

```

```shell
curl "http://api.aiondigital.com/v1/categories/2283811"
  -H "client_id: xxx-yyy-zzz, client_secret: xxx-yyy-zzz"
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

`GET http://api.aiondigital.com/v1/categories/:id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the category to retrieve

## Delete a Specific Category

```ruby
```

```shell
curl "http://api.aiondigital.com/v1/categories/2283811"
    -X DELETE
  -H "client_id: xxx-yyy-zzz, client_secret: xxx-yyy-zzz"
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

`DELETE https://api.aiondigital.com/v1/categories/:id`

### URL Parameters

Parameter | Description
--------- | -----------
:id | The ID of the category to delete

