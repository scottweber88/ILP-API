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
			"id": 49,
			"name": "Kainggi Thunggari Prap",
			"year_level": "Years 3 to 6",
			"topic": {
				"data": [
					{
						"id": 79,
						"title": "01 Greeting people",
						"description": "Greetings",
						"resource_id": 10741,
						"activities": {
							"data": [
								{
									"id": 401,
									"type": "word_matching",
									"title": "Greeting people",
									"activityData": {
										"data": {
											"word": "Nginti nankeri?",
											"words": [
												"Is he good?",
												"Are you good?",
												"Good day",
												"",
												""
											],
											"answer": 1
										}
									}
								},
								{
									"id": 403,
									"type": "word_matching",
									"title": "Greeting people",
									"activityData": {
										"data": {
											"word": "Ngurli nankeri?",
											"words": [
												"Are you all good?",
												"Good night",
												"Are you two good?",
												"",
												""
											],
											"answer": 2
										}
									}
								},
								...
							]
						},
						"resource": {
							"data": {
								"id": 10741,
								"title": "INSERT 5 PHOTO for back of insert P1040884",
								"original_name": "INSERT 5 PHOTO for back of insert P1040884",
								"name": "f2eb869b-e80d-47fa-a322-428638ab4fe6.jpg",
								"type": "image",
								"thumbnail": null,
								"speaker": null,
								"copyright": null,
								"notes": null,
								"vimeoURL": null
							}
						},
                         "associatedWords": {
                            "data": [
                                {
                                    "id": 1830,
                                    "language_id": 1,
                                    "word": "buning",
                                    "alt": "ngamat; yuwuntal",
                                    "word_class": "Noun",
                                    "english_word": "Hooded dotterel (a bird species)",
                                    "example": null,
                                    "category": "birds",
                                    "comments": "",
                                    "created_at": 1489985508,
                                    "updated_at": 1508702915,
                                    "deleted_at": 0,
                                    "recordings": {
                                        "data": {
                                            "male": {
                                                "data": {
                                                    "id": 7893,
                                                    "title": "buning; ngamat; yuwuntal - male",
                                                    "original_name": "buning; ngamat; yuwuntal - male",
                                                    "name": "30e2867c-3498-4681-86ee-b02b93bdf871.wav",
                                                    "type": "sound",
                                                    "thumbnail": null,
                                                    "speaker": null,
                                                    "copyright": null,
                                                    "notes": null,
                                                    "vimeoURL": null
                                                }
                                            },
                                            "female": {
                                                "data": {
                                                    "id": 8067,
                                                    "title": "buning; ngamat; yuwuntal - female",
                                                    "original_name": "buning; ngamat; yuwuntal - female",
                                                    "name": "7d60d6d5-13d4-4b1e-9fe6-041444da1638.mp4",
                                                    "type": "sound",
                                                    "thumbnail": null,
                                                    "speaker": null,
                                                    "copyright": null,
                                                    "notes": null,
                                                    "vimeoURL": null
                                                }
                                            }
                                        }
                                    }
                                },
                                {
                                    "id": 2725,
                                    "language_id": 1,
                                    "word": "kalu",
                                    "alt": "keiwuki",
                                    "word_class": "Noun",
                                    "english_word": "Night bird",
                                    "example": null,
                                    "category": "birds",
                                    "comments": "",
                                    "created_at": 1489985508,
                                    "updated_at": 1508702917,
                                    "deleted_at": 0,
                                    "recordings": {
                                        "data": {
                                            "female": {
                                                "data": {
                                                    "id": 7836,
                                                    "title": "kalu; keiwuki - female",
                                                    "original_name": "kalu; keiwuki - female",
                                                    "name": "ab5659dd-c6cd-4988-b7f8-c528ac6fbd56.wav",
                                                    "type": "sound",
                                                    "thumbnail": null,
                                                    "speaker": null,
                                                    "copyright": null,
                                                    "notes": null,
                                                    "vimeoURL": null
                                                }
                                            }
                                        }
                                    }
                                }
                            ]
                        }
					},
					...
				]
			},
			"teacher": {
				"data": {
					"id": 1,
					"title": "Auntie",
					"first_name": "Phyllis Williams",
					"last_name": "",
					"email": ""
				}
			},
			"school": {
				"data": {
					"id": 31,
					"name": "Kainggi Thunggari Prap",
					"language": {
						"data": {
							"id": 1,
							"language": "Ngarrindjeri",
							"shortcode": "nga",
							"timezone": "Australia\/Adelaide",
							"greeting": "Nguldi arndu"
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


## Topics

> The API returns JSON structured like this:

```json
{
	"data": [
		{
			"id": 81,
			"title": "Farewelling people",
			"description": "",
			"resource_id": 99,
			"activities": {
				"data": [
					{
						"id": 455,
						"type": "word_matching",
						"title": "Farewelling people",
						"activityData": {
							"data": {
								"word": "Nakan ya",
								"words": [
									"Good night",
									"I am going",
									"See you later",
									"",
									""
								],
								"answer": 2
							}
						}
					},
					{
						"id": 457,
						"type": "word_matching",
						"title": "Farewelling people",
						"activityData": {
							"data": {
								"word": "Nakan ngum",
								"words": [
									"Nakan lom",
									"See you later",
									"Nakan nom",
									"",
									""
								],
								"answer": 1
							}
						}
					},
					...
				]
			},
			"resource": {
				"data": {
					"id": 99,
					"title": "Image 1",
					"original_name": "Image 1",
					"name": "cb5ed22886d4715659424732b.jpg",
					"type": "image",
					"thumbnail": null,
					"speaker": null,
					"copyright": null,
					"notes": null,
					"vimeoURL": null
				}
			},
			"associatedWords": {
				"data": [
					{
						"id": 1830,
						"language_id": 1,
						"word": "buning",
						"alt": "ngamat; yuwuntal",
						"word_class": "Noun",
						"english_word": "Hooded dotterel (a bird species)",
						"example": null,
						"category": "birds",
						"comments": "",
						"created_at": 1489985508,
						"updated_at": 1508702915,
						"deleted_at": 0,
						"recordings": {
							"data": {
								"male": {
									"data": {
										"id": 7893,
										"title": "buning; ngamat; yuwuntal - male",
										"original_name": "buning; ngamat; yuwuntal - male",
										"name": "30e2867c-3498-4681-86ee-b02b93bdf871.wav",
										"type": "sound",
										"thumbnail": null,
										"speaker": null,
										"copyright": null,
										"notes": null,
										"vimeoURL": null
									}
								},
								"female": {
									"data": {
										"id": 8067,
										"title": "buning; ngamat; yuwuntal - female",
										"original_name": "buning; ngamat; yuwuntal - female",
										"name": "7d60d6d5-13d4-4b1e-9fe6-041444da1638.mp4",
										"type": "sound",
										"thumbnail": null,
										"speaker": null,
										"copyright": null,
										"notes": null,
										"vimeoURL": null
									}
								}
							}
						}
					},
					{
						"id": 2725,
						"language_id": 1,
						"word": "kalu",
						"alt": "keiwuki",
						"word_class": "Noun",
						"english_word": "Night bird",
						"example": null,
						"category": "birds",
						"comments": "",
						"created_at": 1489985508,
						"updated_at": 1508702917,
						"deleted_at": 0,
						"recordings": {
							"data": {
								"female": {
									"data": {
										"id": 7836,
										"title": "kalu; keiwuki - female",
										"original_name": "kalu; keiwuki - female",
										"name": "ab5659dd-c6cd-4988-b7f8-c528ac6fbd56.wav",
										"type": "sound",
										"thumbnail": null,
										"speaker": null,
										"copyright": null,
										"notes": null,
										"vimeoURL": null
									}
								}
							}
						}
					}
				]
			}
		}
	],
	"meta": {
		"pagination": {
			"total": 1,
			"count": 1,
			"per_page": 50,
			"current_page": 1,
			"total_pages": 1,
			"links": []
		}
	}
}
```

This endpoint 

### HTTP Request

`GET [API URL]/api/v2/topics`

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

> The API returns the file requested



### HTTP Request

`GET [API URL]/api/v2/resource/view/[ResourceID]`

### Parameters

Parameter | Type | Required | Example | Description
--------- | ---- | -------- | ------- | -----------
size      | integer     | False    | `100` | If the resource is an image, resize it based on width  

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




# Upload a resource

> The API returns a signed S3 url


```json
{
  "status": "success",
  "data": {
    "signed_url": "",
    "method": "PUT"
  }
}
```

### HTTP Request

`GET [API URL]/api/v2/resource/upload/`

### Parameters

None


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


