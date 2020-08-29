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
      "images": [
        {"imageURL": "String", "description": "String"}
      ]
    }
```

### Add room
  * POST `/rooms`

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
      "images": [
        {"imageURL": "String", "description": "String"}
      ]
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
      "superhost": "Boolean",
      "location": "String"
    }
```

### Delete room
  * DELETE `/rooms/:id`

**Path Parameters:**
  * `id` room id

**Success Status Code:** `204`



### Add images
  * POST `/rooms/:id/images`

**Path Parameters:**
  * `id` room id

**Success Status Code:** `201`

**Request Body**: Expects JSON with the following keys.

```json
    {
      "id": "Number",
      "imageURL": "String",
      "description": "String"
    }
```


### Update images info
  * PATCH `/rooms/:id/images/:imagesId`

**Path Parameters:**
  * `id` room id
  * `imagesId` image id

**Success Status Code:** `204`

**Request Body**: Expects JSON with any of the following keys (include only keys to be updated)

```json
    {
      "id": "Number",
      "imagesId": "Number",
      "description": "String"
    }
```

### Delete images
  * DELETE `/rooms/:id/images/:imagesId`

**Path Parameters:**
  * `id` room id
  * `imagesId` image id

**Success Status Code:** `204`

