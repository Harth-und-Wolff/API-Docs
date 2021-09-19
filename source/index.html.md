---
title: HuW-API-Reference

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

Herzlich Willkomen in den Docs der API der Harth & Wolff.

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
    },
    "ip": {
      "4": 0.90,
      "6": 0.00
    }
  }
]
```

Über diesen Endpoint bekommst du eine Preisliste für die KVM-Server.

### HTTP Request

`GET https://api.harth-und-wolff.de/v1/kvm/getPrices`

## Order a Server

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
{
  "id": 2,
  "config": {
    "rescourcen": {
      "ram": 4,
      "core": 1,
      "storage": 20,
      "traffic": 1,
      "bandwith": 250,
      "ip": {
        "4": 1,
        "6": 1
      }
    },
    "price": 5.60,
    "template": "Ubuntu 21.04"
  }
}
```

This endpoint retrieves a specific kitten.

### HTTP Request

`POST https://api.harth-und-wolff.de/v1/kvm/order`

### Body Parameters

Parameter | Required | Description
--------- | ----------- | -----------
ram | Ja | Die Ram-Anzahl die du haben möchtest
cores | Ja | Die Core-Anzahl die du haben möchtest
storage | Ja | Der Speicher, den du haben möchtest
traffic | Ja | The ID of the kitten to retrieve
bandwith | Ja | The ID of the kitten to retrieve
ipv4 | Ja | The ID of the kitten to retrieve
ipv6 | Ja | The ID of the kitten to retrieve

## Delete a Server

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
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE https://api.wolff-und-harth.de/v1/kvm/<id>/delete

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the KVM to delete

