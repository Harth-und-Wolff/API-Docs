---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - php
  - python
  - javascript

toc_footers:
  - <a href='https://harth-und-wolff.de/account/api'>Sign Up for a Developer Key</a>
  - <a href='https://harth-und-wolff.de/unternehmen/impressum'>Impressum</a>

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the API
---

# Introduction

Herzlich Willkomen in den Docs der API der Harth und Wolff.

Wir freuen uns, dass Sie sich für unsere API interessieren. 

Bei ungeklärten Fragen, melden Sie sich gerne hier:
Robin Wolff
r.wolff@harth-und-wolff.de

# KVM-Server

## Get Prices

```php
```

```python
```

```shell
```

```javascript
```

> The above command returns JSON structured like this:

```json
[
  {
    "basic": 1.00,
    "ram": 0.80,
    "core": 0.90,
    "storage": 0.50,
    "traffic": 3.00,
    "bandwith": {
      "250": 0.00,
      "500": 5.00,
      "1000": 10.00
    }
  }
]
```

Über diesen Endpoint bekommst du eine Preisliste für die KVM-Server.

### HTTP Request

`GET http://api.harth-und-wolff.de/v1/kvm/getPrices`

## Order a Server

```php
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
curl "http://example.com/api/kittens/2" \
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

## Delete a Server

```php
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
curl "http://example.com/api/kittens/2" \
  -X DELETE \
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

