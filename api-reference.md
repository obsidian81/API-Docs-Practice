# API Reference

Below is the developer integration guide for the User Management API.

## API Reference & Security Guide

All API requests must use HTTP Bearer authentication over HTTPS.

### Authentication

Include your API Bearer token in the `Authorization` header for every request:

```http
Authorization: Bearer <your_jwt_token>
```

An unauthenticated request returns:

```json
{
  "code": 401,
  "message": "Authentication token missing or invalid."
}
```

## Quick Start Code Samples

### List All Users (`GET /users`)

```bash
curl -X GET "https://api.example.com/v1/users" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "Accept: application/json"
```

```javascript
fetch("https://api.example.com/v1/users", {
  method: "GET",
  headers: {
    "Authorization": "Bearer YOUR_JWT_TOKEN",
    "Accept": "application/json"
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```

```python
import requests

headers = {"Authorization": "Bearer YOUR_JWT_TOKEN"}
response = requests.get("https://api.example.com/v1/users", headers=headers)
print(response.json())
```

### Create a User (`POST /users`)

```bash
curl -X POST "https://api.example.com/v1/users" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Alex Mercer",
    "email": "alex.mercer@example.com",
    "role": "developer"
  }'
```

```python
import requests

payload = {
    "name": "Alex Mercer",
    "email": "alex.mercer@example.com",
    "role": "developer"
}

response = requests.post(
    "https://api.example.com/v1/users",
    json=payload,
    headers={"Authorization": "Bearer YOUR_JWT_TOKEN"}
)
response.raise_for_status()
print(response.json())
```
