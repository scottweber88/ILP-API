---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - json

includes:
  - activity_types
  - activity_reading
  - activity_writing
  - activity_hotspot
  - activity_conversation
  - activity_song
  - activity_video
  - activity_word_to_picture_matching
  - activity_picture_to_word_matching
  - activity_word_matching


search: true
---

# Introduction

Welcome to the ILP API! 



# Register


> On success the API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
    "token": "f4kJs(Hmzys3G9)%sObCZXEkz-7IpVNZ",
    "name": "Jason"
  }
}
```


> On error the API returns JSON structured like this:

```json
{
  "status": "failure",
  "errors": {
    "name": [
      "The name field is required."
    ],
    "email": [
      "The email field is required."
    ],
    "password": [
      "The password field is required."
    ],
    "gender": [
      "The gender field is required."
    ],
    "dob": [
      "The dob field is required."
    ],
    "indigenous": [
      "The indigenous field is required."
    ],
    "postcode": [
      "The postcode field is required."
    ]
  }
}
```
This endpoint retrieves the authentication token and users name.

### HTTP Request

`POST [API URL]/api/v2/register`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
name      | string     | True    | `Verna` | 
email  | string     | True     | `Verna@email.com` |
password  | string     | True     | `Ve73lxU90rZx` | 
gender  | string     | True     | `female` |
dob  | date     | True     | `1972-06-29` |
postcode  | int     | True     | `5001` | 
indigenous  | bool     | True     | `True`| 
attributes  | array     | False     | See [attributes](#attributes)  | 




# Login


> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
    "token": "f4kJs(Hmzys3G9)%sObCZXEkz-7IpVNZ",
    "name": "Jason"
  }
}
```

This endpoint retrieves the authentication token and users name.

### HTTP Request

`POST [API URL]/api/v2/auth`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 






















# Languages

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 

# Core 

## Phrases

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Classrooms

> The API returns JSON structured like this:

```json
{
    "data": [
        {
            "id": 38,
            "name": "Adrians Classroom - Year 2",
            "year_level": "Foundation to Year 2",
            "topic": {
                "data": []
            },
            "teacher": {
                "data": {
                    "id": 130,
                    "name": "Adrian Barr",
                    "email": "ABarr@musicaviva.com.au"
                }
            },
            "school": {
                "data": {
                    "id": 3,
                    "name": "Murray Bridge - South School",
                    "language": {
                        "data": {
                            "id": 1,
                            "language": "Ngarrindjeri",
                            "shortcode": "nga",
                            "timezone": "Australia/Adelaide",
                            "greeting": "Nguldi arndu"
                        }
                    }
                }
            }
        },
        ...
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Dictionary

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Dreaming stories

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Language primer

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 
AKA: basics, welcome, 101

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 

# Games

## Get the game leaderboard

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Check for a game

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 



## Get game activities

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 



## Submit a score

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`POST [API URL]/api/v2/auth`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


# Get a resource

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 

# Password reset 

## Request password reset

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Reset password

> The API returns JSON structured like this:

```json
{
  "status": "success",
  "data": {
  }
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/auth`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


