### Detail illustration of /posts Endpoints

### 1.Get All Posts

Endpoint: `GET {{baseurl}}/posts`

Method: `GET`

**Description**

> Retrieves a list of all blog posts from JSONPlaceholder.
> Returns an array of post objects with the following fields:

- userId
- id
- title
- body

Use this endpoint to verify the /posts route and structure of multiple resources.

```JSON

  {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
  }
```

### Tests Included:

- Status code is 200
- Response is a JSON array

### 2. GET Single Post

Endpoint: `GET {{baseurl}}/posts/1`
Method: `GET`

**Description:**
Retrieves a single post by ID. Validates data structure for a specific post resource.

#### Tests Included:

- Status code is 200
- Response includes userId, title

```JSON
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere...",
  "body": "quia et suscipit..."
}
```

#### 3. POST Create Post

Endpoint: `POST {{baseurl}}/posts`

Method: **POST**
**Description**: Simulates creating a new post. JSONPlaceholder returns a fake response with a new ID.

```JSON
{
"title": "foo",
 "body": "bar",
 "userId": 1
}
```

#### Tests Included:

- Status code is 201
- Response contains id

### 4. PUT Update Post

Endpoint: `PUT {{baseurl}}/posts/1`

Method: **PUT**

**Description:** Replaces an existing post with new data. Simulates a full resource update.

```JSON
{
  "id": 1,
  "title": "updated title",
  "body": "updated body",
  "userId": 1
}
```

#### Tests Included:

- Status code is 200
- Updated title in response matches expected val

### 5. DELETE Post

Endpoint: `DELETE {{baseurl}}/posts/1`

Method: **DELETE**

**Description:** Simulates deletion of a post. JSONPlaceholder always returns success.

#### Tests Included:

- Status code is 200

```JSON

{}

```
