# Authentiation

All API requests must include a secure token in the header to be authorized

```bash

Authorization: Bearer YOUR_API_TOKEN

```

## Success Response

When your token response is verified, the server returns to a `200 OK` status with the following payload:

```json

{
    "authenticated": true,
    "user_id": "usr_81obsidian",
    "expires_at": "2026-12-31T23:59:59Z"
}
```

### Step 3: Commit and Push Your Branch

Now, let's commit this change to your new branch. Run these commands in your terminal:

## Bash

```bash
git add .
git commit -m "docs: add authentication json payload example"
```

## Create User Profile

Creates a new user profile in the system database.

### Request Body

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `username` | string | Yes | A unique alphanumeric identifier for the user. |
| `email` | string | Yes | The primary contact email address. |
| `bio` | string | No | A brief text description for the profile. |

### Request Example

```json
{ 
    "username" "uthini_miti",
    "emial": "uthinimiti202@gmail.com",
    "bio": "Focused on mastery."

}

JSON
{ "id": "usr_99",
"username": "uthini_miti",
"email": "uthinimiti202@gmail.com",
"created_at": "2026-07-06T08:12:54Z"}
```

---

## Retrieve User Profile

`GET v1/users/{id}`

Retrieves the profile details for a specific user by their unique identifier

### Path Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `id` | string | Yes | The unique string identifier (e.g., `usr_99` ) of the user profile. |

### Response Example (`200 OK`)

```json
{ 
    "id": "usr_99",
    "username": "uthini_miti",
    "email",: "uthinimiti202@gmail.com",
    "bio": "Focused on mastery.",
    "created_at": "2026-07-06T08:12:54Z"
}
```

## Error Handling

The API returns standard HTTP status codes to indicate the success or failure of an API request.

### Error Response Codes

| Status Code | Type | Description |
| :--- | :--- | :--- |
| `400 Bad Request` | Client Error | The request was unacceptable, often due to missing a required parameter or malformed JSON syntax. |
| `401 Unauthorized` | Client Error | No valid API token was provided in the authorization header. |
| `404 Not Found` | Client Error | The requested resource (e.g., a user profile ID) does not exist. |

### Error Payload Example

When an error occurs, the response body contains a detailed error object instead of the resource payload:

```json
{
  "error": {
    "code": "resource_not_found",
    "message": "No user profile found with the ID 'usr_99'.",
    "doc_url": "[https://api.example.com/docs/errors#resource_not_found](https://api.example.com/docs/errors#resource_not_found)"
  }
}
