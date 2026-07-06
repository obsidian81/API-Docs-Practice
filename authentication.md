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
