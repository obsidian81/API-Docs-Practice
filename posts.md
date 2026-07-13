# Posts API

The Posts API allows you to create, manage, and retrieve content updates published by user profiles.

All endpoints in this section are relative to the base URL: `https://api.example.com/v1`.

---

## Create a Post

`POST /posts`

Creates a new post record associated with an active user profile.

### Request Body

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `user_id` | string | Yes | The unique identifier (`usr_99`) of the profile creating the post. |
| `content` | string | Yes | The body text of the post. Maximum 280 characters. |

### Request Example

```json
{
  "user_id": "usr_99",
  "content": "Building out a comprehensive API documentation portal from the ground up! #TechnicalWriting"
}
```

### Response Example (`201 Created`)

```json
{
  "post_id": "pst_101",
  "user_id": "usr_99",
  "content": "Building out a comprehensive API documentation portal from the ground up! #TechnicalWriting",
  "published_at": "2026-07-13T10:50:00Z"
}
```

### List All Posts

`GET/posts`

Retrieves a paginated list of all posts across the platform, ordered by the most recent publication date.

### Query Parameters

| Parameter | Type | Required | Description | Default |
| :--- | :--- | :--- | :--- | :--- |
| `limit` | integer | No | The maximum number of posts to return in the response array. Max is 100. | `20` |

### Response Example (`200 OK`)

When returning a list, the API wraps the payload in a JSON array block `[]`:

```json
[
  {
    "post_id": "pst_101",
    "user_id": "usr_99",
    "content": "Building out a comprehensive API documentation portal from the ground up! #TechnicalWriting",
    "published_at": "2026-07-13T10:50:00Z"
  },
  {
    "post_id": "pst_100",
    "user_id": "usr_12",
    "content": "Just finished mastering the core Git branch lifecycle.",
    "published_at": "2026-07-12T14:22:15Z"
  }
]
```
