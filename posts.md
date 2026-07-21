# Posts API

Manage blog posts and associated user content within the system.

---

## Create a Post

`POST /v1/posts`

Creates a new blog post entry. Requires an active Bearer Token.

### Request Body Schema

| Field | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `title` | `string` | Yes | Title of the post (max 100 chars). |
| `body` | `string` | Yes | Main content body of the post. |
| `tags` | `array` | No | List of string tags (e.g., `["tech", "api"]`). |

### Code Examples

#### cURL

```bash
curl -X POST [https://api.example.com/v1/posts](https://api.example.com/v1/posts) \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "title": "Mastering Docs-as-Code",
    "body": "Docs-as-code treats documentation like software source code.",
    "tags": ["developer-experience", "documentation"]
  }'
  ```

#### JavaScript

  ```

  const response = await fetch('[https://api.example.com/v1/posts](https://api.example.com/v1/posts)', {
  method: 'POST',
  headers: {
    'Authorization': 'Bearer YOUR_API_TOKEN',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    title: 'Mastering Docs-as-Code',
    body: 'Docs-as-code treats documentation like software source code.',
    tags: ['developer-experience', 'documentation']
  })
});

const data = await response.json();
console.log(data);
```

#### Python

```
import requests

url = "[https://api.example.com/v1/posts](https://api.example.com/v1/posts)"
headers = {
    "Authorization": "Bearer YOUR_API_TOKEN",
    "Content-Type": "application/json"
}
payload = {
    "title": "Mastering Docs-as-Code",
    "body": "Docs-as-code treats documentation like software source code.",
    "tags": ["developer-experience", "documentation"]
}

response = requests.post(url, json=payload, headers=headers)
print(response.json())

```

### Response Schema

#### Success Response (`201 Created`)

```json
{
  "id": "post_987654321",
  "title": "Mastering Docs-as-Code",
  "body": "Docs-as-code treats documentation like software source code.",
  "tags": [
    "developer-experience",
    "documentation"
  ],
  "created_at": "2026-07-21T20:41:59Z",
  "updated_at": "2026-07-21T20:41:59Z"
}
```
