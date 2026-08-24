
# API Reference

Below is the interactive specification and developer integration guide for the User Management API.

## Quick Start Code Samples

### 1. List All Users (`GET /users`)

#### cURL

```bash
curl -X GET "[https://api.example.com/v1/users](https://api.example.com/v1/users)" \
  -H "Accept: application/json"

  ```json
fetch("[https://api.example.com/v1/users](https://api.example.com/v1/users)", {
  method: "GET",
  headers: {
    "Accept": "application/json"
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```python
import requests

response = requests.get("[https://api.example.com/v1/users](https://api.example.com/v1/users)")
print(response.json())
```bash
curl -X POST "[https://api.example.com/v1/users](https://api.example.com/v1/users)" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Alex Mercer",
    "email": "alex.mercer@example.com",
    "role": "developer"
    ```
  }'
  ```python
  import requests

payload = {
    "name": "Alex Mercer",
    "email": "alex.mercer@example.com",
    "role": "developer"
}

response = requests.post("[https://api.example.com/v1/users](https://api.example.com/v1/users)", json=payload)
print(response.json())
```
