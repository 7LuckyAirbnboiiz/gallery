## Server API

### Get room info
  * GET `/rooms/:id`

**Path Parameters:**
  * `id` room id

**Success Status Code:** `200`

**Returns:** JSON

```json
    {
      "id": "Number",
      "description": "String",
      "starRating": "Number",
      "reviewTotal": "Number",
      "superhost": "Boolean",
      "location": "String",
      "images": {
        "house": { //change this to array of objects
          "imageURL": "String",
          "description": "String"
        },
        "backyard": {
          "imageURL": "String",
          "description": "String"
        },
        "kitchen": {
          "imageURL": "String",
          "description": "String"
        },
        "bedrooms": "Array",
        "bathrooms": "Array"
      }
    }
```

### Add room
  * POST `/rooms/:id`

**Success Status Code:** `201`

**Request Body**: Expects JSON with the following keys.

```json
    {
      "id": "Number",
      "description": "String",
      "starRating": "Number",
      "reviewTotal": "Number",
      "superhost": "Boolean",
      "location": "String",
      "images": {
        "house": {
          "imageURL": "String",
          "description": "String"
        },
        "backyard": {
          "imageURL": "String",
          "description": "String"
        },
        "kitchen": {
          "imageURL": "String",
          "description": "String"
        },
        "bedrooms": "Array",
        "bathrooms": "Array"
      }
    }
```


### Update room info
  * PATCH `/rooms/:id`

**Path Parameters:**
  * `id` room id

**Success Status Code:** `204`

**Request Body**: Expects JSON with any of the following keys (include only keys to be updated)

```json
    {
      "id": "Number",
      "description": "String",
      "starRating": "Number",
      "reviewTotal": "Number",
      "superhost": "Boolean",
      "location": "String",
      "images": {
        "house": {
          "imageURL": "String",
          "description": "String"
        },
        "backyard": {
          "imageURL": "String",
          "description": "String"
        },
        "kitchen": {
          "imageURL": "String",
          "description": "String"
        },
        "bedrooms": "Array",
        "bathrooms": "Array"
      }
    }
```

### Delete room
  * DELETE `/rooms/:id`

**Path Parameters:**
  * `id` room id

**Success Status Code:** `204`

