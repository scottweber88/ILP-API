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
  - entity_types


search: true
---

# Introduction

Welcome to the ILP API! 


<aside class="notice">
This documentation is currently under construction. <br><br>
Some parts may be incomplete, outdated or missing entirely but every effort is being made to keep them up-to-date and complete.
</aside>

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

`POST [API URL]/api/v3/register`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
title      | string     | False    | `Aunti` | 
first_name      | string     | True    | `Verna` | 
last_name      | string     | True    | `Creswell` | 
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
    "title": "Tsar",
    "first_name": "Jason",
    "last_name": "Millward"
  }
}
```

This endpoint retrieves the authentication token and users name.

### HTTP Request

`POST [API URL]/api/v3/auth`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 






















# Languages

> The API returns JSON structured like this:

```json
{  
  "data":[  
    {  
      "id":1,
      "language":"Ngarrindjeri",
      "shortcode":"nga",
      "timezone":"Australia\/Adelaide",
      "greeting":"Nguldi arndu"
    },
    {  
      "id":2,
      "language":"Yugambeh",
      "shortcode":"yug",
      "timezone":"Australia\/Brisbane",
      "greeting":"Jingeri"
    },
    {  
      "id":3,
      "language":"Gunggari",
      "shortcode":"gun",
      "timezone":"Australia\/Brisbane",
      "greeting":"Yowala"
    },
    {  
      "id":4,
      "language":"Yalnun An'gabah",
      "shortcode":"yal",
      "timezone":"Australia\/Brisbane",
      "greeting":"Jingeri"
    }
  ]
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v3/language`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 



# Core 


## Classrooms

> The API returns JSON structured like this:

```json
{  
  "data":[  
    {  
      "id":49,
      "name":"Kainggi Thunggari Prap",
      "year_level":"Years 3 to 6",
      "topic":{  
        "data":[  
          {  
            "id":79,
            "sort":1,
            "title":"Greeting people",
            "description":"Greetings",
            "teacher_notes":"[HTML TEACHER NOTES]",
            "sequences":{  
              "data":[  
                {  
                  "id":1,
                  "sort":1,
                  "name":"Test",
                  "activities":{  
                    "data":[  
                      {  
                        "id":511,
                        "sort":1,
                        "type":"reading",
                        "title":"Who are you and where are you from?",
                        "activityData":{  
                          "data":{  
                            "body":""
                          }
                        }
                      }
                    ]
                  }
                }
              ]
            },
            "category": {
              "data": {
                "id": 3,
                "name": "Test Category",
                "colour": "#F44E3B"
              }
            },
            "associatedWords":{  
              "data":[  
                {  
                  "id":1589,
                  "language_id":1,
                  "word":"nankeri ngendi",
                  "alt":"",
                  "word_class":"Expression",
                  "english_word":"Good night",
                  "example":null,
                  "category":"expressions",
                  "comments":"",
                  "created_at":1489985508,
                  "updated_at":1508799287,
                  "deleted_at":0,
                  "recordings":{  
                    "data":{  
                      "female":{  
                        "data":{  
                          "id":6556,
                          "title":"nankeri ngendi - female",
                          "original_name":"nankeri ngendi - female",
                          "name":"5244bdc8-a07d-4414-aa03-9681e6891d6b.wav",
                          "type":"sound",
                          "thumbnail":null,
                          "speaker":null,
                          "copyright":null,
                          "notes":null,
                          "size":"173.41kB",
                          "download_link":null,
                          "vimeoURL":null
                        }
                      }
                    }
                  }
                },
                {  
                  "id":5085,
                  "language_id":1,
                  "word":"nguldi arndu",
                  "alt":null,
                  "word_class":"Expression",
                  "english_word":"Welcome (well-come)",
                  "example":null,
                  "category":"food, cooking, fire",
                  "comments":"",
                  "created_at":1489985508,
                  "updated_at":1508799361,
                  "deleted_at":0,
                  "image":{  
                    "data":{  
                      "id":10497,
                      "title":"100_2089",
                      "original_name":"100_2089",
                      "name":"d42452c1-f655-4a32-a34a-e0071d3f6369.jpg",
                      "type":"image",
                      "thumbnail":null,
                      "speaker":null,
                      "copyright":null,
                      "notes":null,
                      "size":0,
                      "download_link":null,
                      "vimeoURL":null
                    }
                  },
                  "recordings":{  
                    "data":{  
                      "female":{  
                        "data":{  
                          "id":6260,
                          "title":"nguldi arndu - female",
                          "original_name":"nguldi arndu - female",
                          "name":"8178b25a-e282-4876-99b8-a12a51f11c4f.wav",
                          "type":"sound",
                          "thumbnail":null,
                          "speaker":null,
                          "copyright":null,
                          "notes":null,
                          "size":"133.88kB",
                          "download_link":null,
                          "vimeoURL":null
                        }
                      }
                    }
                  }
                }
              ]
            },
            "tags":{  
              "data":[  

              ]
            }
          }
        ]
      },
      "teacher":{  
        "data":{  
          "id":131,
          "title":null,
          "first_name":"Phyllis",
          "last_name":"Williams",
          "email":""
        }
      },
      "school":{  
        "data":{  
          "id":31,
          "name":"Kainggi Thunggari Prap",
          "language":{  
            "data":{  
              "id":1,
              "language":"Ngarrindjeri",
              "shortcode":"nga",
              "timezone":"Australia\/Adelaide",
              "greeting":"Nguldi arndu"
            }
          }
        }
      }
    }
  ]
}	
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v3/classroom`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
languageID      | integer     | True    | `1` | 



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

`GET [API URL]/api/v3/dictionary/update`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Topics

> The API returns JSON structured like this:

```json
{  
  "data":[  
    {  
      "id":79,
      "sort":1,
      "title":"Greeting people",
      "description":"Greetings",
      "teacher_notes":"[HTML TEACHER NOTES]",
      "sequences":{  
        "data":[  
          {  
            "id":1,
            "sort":1,
            "name":"Test",
            "activities":{  
              "data":[  
                {  
                  "id":511,
                  "sort":1,
                  "type":"reading",
                  "title":"Who are you and where are you from?",
                  "activityData":{  
                    "data":{  
                      "body":""
                    }
                  }
                }
              ]
            }
          }
        ]
      },
      "associatedWords":{  
        "data":[  
          {  
            "id":1589,
            "language_id":1,
            "word":"nankeri ngendi",
            "alt":"",
            "word_class":"Expression",
            "english_word":"Good night",
            "example":null,
            "category":"expressions",
            "comments":"",
            "created_at":1489985508,
            "updated_at":1508799287,
            "deleted_at":0,
            "recordings":{  
              "data":{  
                "female":{  
                  "data":{  
                    "id":6556,
                    "title":"nankeri ngendi - female",
                    "original_name":"nankeri ngendi - female",
                    "name":"5244bdc8-a07d-4414-aa03-9681e6891d6b.wav",
                    "type":"sound",
                    "thumbnail":null,
                    "speaker":null,
                    "copyright":null,
                    "notes":null,
                    "size":"173.41kB",
                    "download_link":null,
                    "vimeoURL":null
                  }
                }
              }
            }
          },
          {  
            "id":5085,
            "language_id":1,
            "word":"nguldi arndu",
            "alt":null,
            "word_class":"Expression",
            "english_word":"Welcome (well-come)",
            "example":null,
            "category":"food, cooking, fire",
            "comments":"",
            "created_at":1489985508,
            "updated_at":1508799361,
            "deleted_at":0,
            "image":{  
              "data":{  
                "id":10497,
                "title":"100_2089",
                "original_name":"100_2089",
                "name":"d42452c1-f655-4a32-a34a-e0071d3f6369.jpg",
                "type":"image",
                "thumbnail":null,
                "speaker":null,
                "copyright":null,
                "notes":null,
                "size":0,
                "download_link":null,
                "vimeoURL":null
              }
            },
            "recordings":{  
              "data":{  
                "female":{  
                  "data":{  
                    "id":6260,
                    "title":"nguldi arndu - female",
                    "original_name":"nguldi arndu - female",
                    "name":"8178b25a-e282-4876-99b8-a12a51f11c4f.wav",
                    "type":"sound",
                    "thumbnail":null,
                    "speaker":null,
                    "copyright":null,
                    "notes":null,
                    "size":"133.88kB",
                    "download_link":null,
                    "vimeoURL":null
                  }
                }
              }
            }
          }
        ]
      },
      "tags":{  
        "data":[  

        ]
      }
    }
  ]
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v3/topics`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
topic      | int     | True    | `1` | 
languageID      | int     | True    | `81` | 


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

`GET [API URL]/api/v3/stories`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


## Language primer

> The API returns JSON structured like this:

```json
{
  "data": [
    {
      "id": 29,
      "title": "00 Acknowledgements and contributors",
      "content": "",
      "resource_id": 10325
    },
    {
      "id": 25,
      "title": "01 Tribute to Eileen McHughes: Katjeri Yailini-ambi",
      "content": "",
      "resource_id": 10685
    },
    ...
  ]
}
```

This endpoint 
AKA: basics, welcome, 101

### HTTP Request

`GET [API URL]/api/v3/primer`

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

`GET [API URL]/api/v3/auth`

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

`GET [API URL]/api/v3/games/current`

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

`GET [API URL]/api/v3/games/current`

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

`POST [API URL]/api/v3/games/score`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 


# Get a resource

> The API returns the file requested



### HTTP Request

`GET [API URL]/api/v3/resource/view/[ResourceID]`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
size      | integer     | False    | `100` | If the resource is an image, resize it based on width  

# Password reset 

## Request password reset

> The API returns JSON structured like this:

```json
{
  "status":"passwords.sent"
}
```




# Upload a resource

> The API returns a signed S3 url


```json
{  
  "error":false,
  "url":"[SIGNED SD URL]",
  "additionalData":{  
    "fileName":"80cfad18-61ac-4ea5-89ec-101e186c34fa-testfile.jpg"
  },
  "code":200
}
```

### HTTP Request

`POST [API URL]/api/v3/resource/upload`

### POST Parameters


Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
languageID      | integer     | True    | `1` | 
name      | string     | True    | `owls.jpg` | 
title      | string     | True    | `Brown Owls` | 
entity      | enum     | True    | See [entity-types](#entity-types)| 
entity_id      | integer     | False    | `1` or `empty` | 
type      | string     | True    | `image/jpeg` | Mimetype





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

`POST [API URL]/api/v3/password/forgot`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 


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

`POST [API URL]/api/v3/password/forgot`

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
email      | string     | True    | `Verna@email.com` | 
password      | string     | True    | `Ve73lxU90rZx` | 































# Me

## Get avatar

> The API returns an image

This endpoint returns a 512x512 image. 
The image is cached on the back end for 1 hour or until the user changes his or her avatar.

### HTTP Request

`GET [API URL]/api/v3/me/avatar`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.


## Update Avatar

> The API returns JSON structured like this:

```json
{  
  "url":"[SIGNED S3 URL]",
  "additionalData":{  
    "fileName":"80cfad18-61ac-4ea5-89ec-101e186c34fa-my_face.jpg"
  },
  "code":200
}
```

This endpoint returns a signed S3 url (PUT) for the app to upload the image to.

### HTTP Request

`POST [API URL]/api/v3/me/avatar`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.

### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
name      | string     | True    | `my_face.jpg` | The name of the image the user is uploading


## Get Profile

> The API returns JSON structured like this:

```json
{  
  "data":{  
    "id":1,
    "title":"Tsar",
    "first_name":"Jason",
    "last_name":"Millward",
    "email":"jason@email.com",
    "dob":"1902-11-30",
    "gender":"male",
    "postcode":5000,
    "indigenous":0,
    "role":"student"
  }
}
```

This endpoint returns the currently logged in users profile.

### HTTP Request

`GET [API URL]/api/v3/me/profile`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.


## Update Profile

> On success API returns JSON structured like this:

```json
{  
  "data":{  
    "id":1,
    "title":"Tsar",
    "first_name":"Jason",
    "last_name":"Millward",
    "email":"jason@email.com",
    "dob":"1902-11-30",
    "gender":"male",
    "postcode":5000,
    "indigenous":0,
    "role":"student"
  }
}
```

> On error the API returns JSON structured like this:

```json
{  
  "message":"The given data was invalid.",
  "errors":{  
    "email":[  
      "The email has already been taken."
    ]
  },
  "password":[  
    "The password must be at least 3 characters.",
    "The password confirmation does not match."
  ],
  "dob":[  
    "The dob is not a valid date."
  ]
}
```

This endpoint updates the currently logged in users profile.

### HTTP Request

`POST [API URL]/api/v3/me/profile`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.


### POST Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
password      | string     | False    | `Ve73lxU90rZx` | Users new password.
password_confirmation      | string     | False | `Ve73lxU90rZx` | Confirmation of users new password. Required if `password` is sent.
title      | string     | False    | `Tsar` | Users title. See allowed list of titles.
first_name      | string     | False    | `Jason` | Users first name.
last_name      | string     | False    | `Millward` | Users last name.
dob      | string     | False    | `Millward` | Date of Birth.
gender      | enum   | False    | `male` | See allowed list of genders.
postcode      | integer     | False    | `Millward` | Post code of current residence.
indigenous      | boolean     | False    | `false` | Are you a native Australian?
