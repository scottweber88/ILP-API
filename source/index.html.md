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


# Community Feed

## Retrieve Community Feed

This endpoint returns the latest Community Feed for a language, in reverse (descending) time order.

> On Success this API returns json like

```json
{
  "data": [
    {
      "author_display_name": "craig snudden",
      "hash_tags": [
        "celebrate",
        "Kooriartexpressions",
        "ourlanguagesmatter"
      ],
      "id": 1,
      "image": null,
      "platform_name": "Twitter",
      "published": "2017-11-28 04:23:47",
      "text": "RT @Mrs_Tobias9: @BangorPS @craigsnudden #ourlanguagesmatter #Kooriartexpressions #celebrate https://t.co/Kont0HVjJj",
      "title": null
    }
  ]
}
```

### HTTP Request

`GET [API URL]/api/v3/community-feed`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.

### GET Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
languageID | integer | True | 1 | The ID of the language to retrieve social media for


# Topics


## Topics

> The API returns JSON structured like this:

```json
{
  "data": [
    {
      "id": 79,
      "sort": 0,
      "title": "Greeting people",
      "description": "Greetings",
      "teacher_notes": "",
      "offline_size": "743.23MB",
      "associatedWords": {
        "data": [
          {
            "id": 1926,
            "language_id": 1,
            "word": "ngapi",
            "alt": null,
            "word_class": "Pronoun",
            "english_word": "I (subject)",
            "example": null,
            "category": "personal pronouns",
            "comments": "",
            "created_at": 1489985508,
            "updated_at": 1508799295,
            "deleted_at": 0,
            "recordings": {
              "data": {
                "female": {
                  "data": {
                    "id": 6458,
                    "title": "ngapi - female",
                    "original_name": "ngapi - female",
                    "name": "8a7cdd3a-b381-4201-8228-0e6ceaf024d2.wav",
                    "type": "sound",
                    "thumbnail": null,
                    "speaker": null,
                    "copyright": null,
                    "notes": null,
                    "size": "129.71kB",
                    "download_link": null,
                    "vimeoURL": null
                  }
                }
              }
            }
          },
          {
            "id": 3534,
            "language_id": 1,
            "word": "nakan",
            "alt": "",
            "word_class": "Verb (trans)",
            "english_word": "See (you) later in the future",
            "example": null,
            "category": "senses",
            "comments": "",
            "created_at": 1489985508,
            "updated_at": 1508799334,
            "deleted_at": 0,
            "recordings": {
              "data": {
                "female": {
                  "data": {
                    "id": 6774,
                    "title": "nakan - female",
                    "original_name": "nakan - female",
                    "name": "604fc11e-3a67-46c7-8b3e-76340b694f13.wav",
                    "type": "sound",
                    "thumbnail": null,
                    "speaker": null,
                    "copyright": null,
                    "notes": null,
                    "size": "118.58kB",
                    "download_link": null,
                    "vimeoURL": null
                  }
                }
              }
            }
          },
          {
            "id": 4596,
            "language_id": 1,
            "word": "nginti",
            "alt": "",
            "word_class": "Pronoun",
            "english_word": "Thou, you (singular)",
            "example": null,
            "category": "personal pronouns",
            "comments": "",
            "created_at": 1489985508,
            "updated_at": 1508799353,
            "deleted_at": 0,
            "recordings": {
              "data": {
                "female": {
                  "data": {
                    "id": 6346,
                    "title": "nginti - female",
                    "original_name": "nginti - female",
                    "name": "fdb3cf97-e709-4e14-a8c9-4a859680cabf.wav",
                    "type": "sound",
                    "thumbnail": null,
                    "speaker": null,
                    "copyright": null,
                    "notes": null,
                    "size": "132.57kB",
                    "download_link": null,
                    "vimeoURL": null
                  }
                }
              }
            }
          },
          ...
```

This endpoint gets a list of topics available to a user.

### HTTP Request

`GET [API URL]/api/v3/topics`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.

### GET Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
languageID      | int     | True    | `1` | 
searchTerm      | string     | false    | `Greeting People` | 














## Topic Resources

> The API returns JSON structured like this:

```json
{
  "data": [
    {
      "id": 11383,
      "title": "Number 2 two",
      "original_name": 2,
      "name": "a490468c-6cda-406d-9b7f-2b59209474d7.jpg",
      "type": "image",
      "thumbnail": null,
      "speaker": "",
      "copyright": "",
      "notes": "",
      "size": "11.27kB",
      "download_link": null,
      "vimeoURL": null
    },
    {
      "id": 11409,
      "title": "Number 17 seventeen",
      "original_name": 17,
      "name": "e9e9b2c8-dcad-4feb-865b-05ca586972f3.jpg",
      "type": "image",
      "thumbnail": null,
      "speaker": "",
      "copyright": "",
      "notes": "",
      "size": "11.06kB",
      "download_link": null,
      "vimeoURL": null
    },
    {
      "id": 11387,
      "title": "number 3 three",
      "original_name": 3,
      "name": "903bed1e-aaa9-4174-a568-fa7df85becb3.jpg",
      "type": "image",
      "thumbnail": null,
      "speaker": "",
      "copyright": "",
      "notes": "",
      "size": "12.53kB",
      "download_link": null,
      "vimeoURL": null
    },
    ...
```

This endpoint gets an individual topics list of resources

### HTTP Request

`GET [API URL]/api/v3/topics/resources`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.

### GET Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
topicid      | int     | True    | `81` | 
languageID      | int     | True    | `1` | 





## Add Topic To "My Topics"

> The API returns JSON structured like this:

```json
{
  "data": {
    "id": 68,
    "name": "My topics",
    "year_level": null,
    "join_code": "9ff-4ee",
    "topic": {
      "data": [
        {
          "id": 183,
          "sort": 0,
          "title": "46 Playing games",
          "description": "",
          "teacher_notes": "",
          "offline_size": "13.91MB",
          "sequences": {
            "data": []
          },
          "associatedWords": {
            "data": []
          },
          "tags": {
            "data": []
          }
        }
      ]
    },
    "teacher": {
      "data": {
        "id": 1,
        "title": "Pope",
        "first_name": "Jason",
        "last_name": "M",
        "email": "email@domain.com",
        "dob": "1902-11-30",
        "gender": "male",
        "postcode": 0,
        "indigenous": 0,
        "role": ""
      }
    }
  }
}
```

This endpoint gets an individual topics list of resources

### HTTP Request

`POST [API URL]/api/v3/topics/join`

### Headers

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
Authorization | Bearer     | True    | `[User Token]` | This is the users API token.

### GET Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
topicid      | int     | True    | `79` | 
languageID      | int     | True    | `1` | 
