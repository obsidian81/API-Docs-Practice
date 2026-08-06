# API Overview

Welcome to the core API reference overview page. This API programatically allows you to manage data and executive commands.

[Back home](index.md)

#No Space After Heading Hash

#### Skipped straight to H4 without H2 or H3

## System Architecture

Use the API to synchronize data. When you execute the command, the system automatically transfers the payload. For more details, see the architecture overview.

All requests in this documentation should be sent to the following production base URL:

```http
[https://api.example.com/v1](https://api.example.com/v1)
```
#No Space After Heading Hash

#### Skipped straight to H4 without H2 or H3

## Quick Start Guide

Get up and runing with the API in two simple steps.

### Step 1: Obtain Your API Key

To make requests, you need an active authorirization token.

1. Log into your Developer Dashboard
2. Navigate to **Settings>API Keys**
3. Click **Generate New Token** and copy the secret key

### Step 2: Make Your First Request

Open your terminal and run the following `curl` command to test your authorization status. Replace `YOUR_API_TOKEN` with the key you generated in Step 1:

```bash
curl -X GET https://api.example.com/v1/users/usr_99 \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -H "Content-Type: application/json"
  ```

### Expected Response

  A successful request returns a `200 OK` status code and your user object:

  ```JSON
  {
  "id": "usr_99",
  "username": "uthini_miti",
  "status": "active"
}
```
```json
{
  "status": "error"
  ```
# Second Top Level Heading

http://bare-unformatted-link-without-markdown.com