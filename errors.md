# Error Handling

The User Profile and Posts APIs use standard HTTP response codes to indicate the success or failure of an API request.

In general:

* Codes in the `2xx` range indicate success.
* Codes in the `4xx` range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a resource was missing, etc.).
* Codes in the `5xx` range indicate an error with the API servers.

---

## Error Response Format

When an error occurs, the API returns a structured JSON payload containing a specific error code and a human-readable message to help you debug the issue.

```json
{
  "error": {
    "code": "resource_not_found",
    "message": "The requested post with ID 'pst_999' could not be found.",
    "doc_url": "[https://docs.example.com/errors#resource_not_found](https://docs.example.com/errors#resource_not_found)"
  }
}
```

## HTTP Status Codes Reference

| Status Code | Error Code | Description |
| :--- | :--- | :--- |
| `Bad Request` | `invalid_request` | The request body was malformed JSON or missed a required parameter. |
| `401 Unauthorized` | `invalid_api_key` | The `Authorization` header is missing, invalid, or expired. |
| `404 Not Found` | `resource_not_found` | The request object (User or Post) does not exist in our database. |
| `429 Too Many Requests` | `rate_limit_exceeded` | You have hit your rate limit. Reduce the frequency of your API calls. |
| `500 Internal Error` | `api_error` | Something went wrong on our servers. Please try again later. |
