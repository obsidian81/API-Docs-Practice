{
  "info": {
    "_postman_id": "dd332477-451f-476f-ab4d-b71c73dc8211",
    "name": "User Management API",
    "description": "A production-ready API specification for user profile management.",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
    "_exporter_id": "55919532",
    "_collection_link": "https://go.postman.co/collection/55919532-dd332477-451f-476f-ab4d-b71c73dc8211?source=collection_link"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "name": "{id}",
          "item": [
            {
              "name": "Retrieve a user by ID",
              "request": {
                "method": "GET",
                "header": [
                  {
                    "key": "Accept",
                    "value": "application/json"
                  }
                ],
                "url": {
                  "raw": "{{baseUrl}}/users/:id",
                  "host": [
                    "{{baseUrl}}"
                  ],
                  "path": [
                    "users",
                    ":id"
                  ],
                  "variable": [
                    {
                      "key": "id",
                      "value": "string",
                      "description": "Unique identifier of the user"
                    }
                  ]
                },
                "description": "Returns a single user object based on the provided unique ID."
              },
              "response": [
                {
                  "name": "User found",
                  "originalRequest": {
                    "method": "GET",
                    "header": [
                      {
                        "key": "Accept",
                        "value": "application/json"
                      }
                    ],
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "OK",
                  "code": 200,
                  "_postman_previewlanguage": "json",
                  "header": [
                    {
                      "key": "Content-Type",
                      "value": "application/json"
                    }
                  ],
                  "cookie": [],
                  "body": "{\n  \"id\": \"usr_998234\",\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}"
                },
                {
                  "name": "Resource Not Found - The specified entity does not exist",
                  "originalRequest": {
                    "method": "GET",
                    "header": [
                      {
                        "key": "Accept",
                        "value": "application/json"
                      }
                    ],
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "Not Found",
                  "code": 404,
                  "_postman_previewlanguage": "json",
                  "header": [
                    {
                      "key": "Content-Type",
                      "value": "application/json"
                    }
                  ],
                  "cookie": [],
                  "body": "{\n  \"code\": 400,\n  \"message\": \"Invalid JSON payload provided.\"\n}"
                }
              ]
            },
            {
              "name": "Update a user",
              "request": {
                "method": "PUT",
                "header": [
                  {
                    "key": "Content-Type",
                    "value": "application/json"
                  },
                  {
                    "key": "Accept",
                    "value": "application/json"
                  }
                ],
                "body": {
                  "mode": "raw",
                  "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
                  "options": {
                    "raw": {
                      "headerFamily": "json",
                      "language": "json"
                    }
                  }
                },
                "url": {
                  "raw": "{{baseUrl}}/users/:id",
                  "host": [
                    "{{baseUrl}}"
                  ],
                  "path": [
                    "users",
                    ":id"
                  ],
                  "variable": [
                    {
                      "key": "id",
                      "value": "string",
                      "description": "Unique identifier of the user"
                    }
                  ]
                },
                "description": "Updates the profile details for an existing user."
              },
              "response": [
                {
                  "name": "User updated successfully",
                  "originalRequest": {
                    "method": "PUT",
                    "header": [
                      {
                        "key": "Content-Type",
                        "value": "application/json"
                      },
                      {
                        "key": "Accept",
                        "value": "application/json"
                      }
                    ],
                    "body": {
                      "mode": "raw",
                      "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
                      "options": {
                        "raw": {
                          "headerFamily": "json",
                          "language": "json"
                        }
                      }
                    },
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "OK",
                  "code": 200,
                  "_postman_previewlanguage": "json",
                  "header": [
                    {
                      "key": "Content-Type",
                      "value": "application/json"
                    }
                  ],
                  "cookie": [],
                  "body": "{\n  \"id\": \"usr_998234\",\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}"
                },
                {
                  "name": "Bad Request - Missing required fields or invalid syntax",
                  "originalRequest": {
                    "method": "PUT",
                    "header": [
                      {
                        "key": "Content-Type",
                        "value": "application/json"
                      },
                      {
                        "key": "Accept",
                        "value": "application/json"
                      }
                    ],
                    "body": {
                      "mode": "raw",
                      "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
                      "options": {
                        "raw": {
                          "headerFamily": "json",
                          "language": "json"
                        }
                      }
                    },
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "Bad Request",
                  "code": 400,
                  "_postman_previewlanguage": "json",
                  "header": [
                    {
                      "key": "Content-Type",
                      "value": "application/json"
                    }
                  ],
                  "cookie": [],
                  "body": "{\n  \"code\": 400,\n  \"message\": \"Invalid JSON payload provided.\"\n}"
                },
                {
                  "name": "Resource Not Found - The specified entity does not exist",
                  "originalRequest": {
                    "method": "PUT",
                    "header": [
                      {
                        "key": "Content-Type",
                        "value": "application/json"
                      },
                      {
                        "key": "Accept",
                        "value": "application/json"
                      }
                    ],
                    "body": {
                      "mode": "raw",
                      "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
                      "options": {
                        "raw": {
                          "headerFamily": "json",
                          "language": "json"
                        }
                      }
                    },
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "Not Found",
                  "code": 404,
                  "_postman_previewlanguage": "json",
                  "header": [
                    {
                      "key": "Content-Type",
                      "value": "application/json"
                    }
                  ],
                  "cookie": [],
                  "body": "{\n  \"code\": 400,\n  \"message\": \"Invalid JSON payload provided.\"\n}"
                }
              ]
            },
            {
              "name": "Delete a user",
              "request": {
                "method": "DELETE",
                "header": [
                  {
                    "key": "Accept",
                    "value": "application/json"
                  }
                ],
                "url": {
                  "raw": "{{baseUrl}}/users/:id",
                  "host": [
                    "{{baseUrl}}"
                  ],
                  "path": [
                    "users",
                    ":id"
                  ],
                  "variable": [
                    {
                      "key": "id",
                      "value": "string",
                      "description": "Unique identifier of the user"
                    }
                  ]
                },
                "description": "Permanently removes a user record from the system."
              },
              "response": [
                {
                  "name": "User deleted successfully (no content returned)",
                  "originalRequest": {
                    "method": "DELETE",
                    "header": [],
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "No Content",
                  "code": 204,
                  "_postman_previewlanguage": "text",
                  "header": [],
                  "cookie": [],
                  "body": null
                },
                {
                  "name": "Resource Not Found - The specified entity does not exist",
                  "originalRequest": {
                    "method": "DELETE",
                    "header": [
                      {
                        "key": "Accept",
                        "value": "application/json"
                      }
                    ],
                    "url": {
                      "raw": "{{baseUrl}}/users/:id",
                      "host": [
                        "{{baseUrl}}"
                      ],
                      "path": [
                        "users",
                        ":id"
                      ],
                      "variable": [
                        {
                          "key": "id",
                          "value": "string",
                          "description": "Unique identifier of the user"
                        }
                      ]
                    }
                  },
                  "status": "Not Found",
                  "code": 404,
                  "_postman_previewlanguage": "json",
                  "header": [
                    {
                      "key": "Content-Type",
                      "value": "application/json"
                    }
                  ],
                  "cookie": [],
                  "body": "{\n  \"code\": 400,\n  \"message\": \"Invalid JSON payload provided.\"\n}"
                }
              ]
            }
          ]
        },
        {
          "name": "List all users",
          "request": {
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "application/json"
              }
            ],
            "url": {
              "raw": "{{baseUrl}}/users",
              "host": [
                "{{baseUrl}}"
              ],
              "path": [
                "users"
              ]
            },
            "description": "Returns a paginated list of user objects."
          },
          "response": [
            {
              "name": "A list of user accounts",
              "originalRequest": {
                "method": "GET",
                "header": [
                  {
                    "key": "Accept",
                    "value": "application/json"
                  }
                ],
                "url": {
                  "raw": "{{baseUrl}}/users",
                  "host": [
                    "{{baseUrl}}"
                  ],
                  "path": [
                    "users"
                  ]
                }
              },
              "status": "OK",
              "code": 200,
              "_postman_previewlanguage": "json",
              "header": [
                {
                  "key": "Content-Type",
                  "value": "application/json"
                }
              ],
              "cookie": [],
              "body": "[\n  {\n    \"id\": \"usr_998234\",\n    \"name\": \"Alex Mercer\",\n    \"email\": \"alex.mercer@example.com\",\n    \"role\": \"developer\"\n  },\n  {\n    \"id\": \"usr_998234\",\n    \"name\": \"Alex Mercer\",\n    \"email\": \"alex.mercer@example.com\",\n    \"role\": \"developer\"\n  }\n]"
            }
          ]
        },
        {
          "name": "Create a user",
          "request": {
            "method": "POST",
            "header": [
              {
                "key": "Content-Type",
                "value": "application/json"
              },
              {
                "key": "Accept",
                "value": "application/json"
              }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
              "options": {
                "raw": {
                  "headerFamily": "json",
                  "language": "json"
                }
              }
            },
            "url": {
              "raw": "{{baseUrl}}/users",
              "host": [
                "{{baseUrl}}"
              ],
              "path": [
                "users"
              ]
            },
            "description": "Creates a new user profile with the provided details."
          },
          "response": [
            {
              "name": "User created successfully",
              "originalRequest": {
                "method": "POST",
                "header": [
                  {
                    "key": "Content-Type",
                    "value": "application/json"
                  },
                  {
                    "key": "Accept",
                    "value": "application/json"
                  }
                ],
                "body": {
                  "mode": "raw",
                  "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
                  "options": {
                    "raw": {
                      "headerFamily": "json",
                      "language": "json"
                    }
                  }
                },
                "url": {
                  "raw": "{{baseUrl}}/users",
                  "host": [
                    "{{baseUrl}}"
                  ],
                  "path": [
                    "users"
                  ]
                }
              },
              "status": "Created",
              "code": 201,
              "_postman_previewlanguage": "json",
              "header": [
                {
                  "key": "Content-Type",
                  "value": "application/json"
                }
              ],
              "cookie": [],
              "body": "{\n  \"id\": \"usr_998234\",\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}"
            },
            {
              "name": "Bad Request - Missing required fields or invalid syntax",
              "originalRequest": {
                "method": "POST",
                "header": [
                  {
                    "key": "Content-Type",
                    "value": "application/json"
                  },
                  {
                    "key": "Accept",
                    "value": "application/json"
                  }
                ],
                "body": {
                  "mode": "raw",
                  "raw": "{\n  \"name\": \"Alex Mercer\",\n  \"email\": \"alex.mercer@example.com\",\n  \"role\": \"developer\"\n}",
                  "options": {
                    "raw": {
                      "headerFamily": "json",
                      "language": "json"
                    }
                  }
                },
                "url": {
                  "raw": "{{baseUrl}}/users",
                  "host": [
                    "{{baseUrl}}"
                  ],
                  "path": [
                    "users"
                  ]
                }
              },
              "status": "Bad Request",
              "code": 400,
              "_postman_previewlanguage": "json",
              "header": [
                {
                  "key": "Content-Type",
                  "value": "application/json"
                }
              ],
              "cookie": [],
              "body": "{\n  \"code\": 400,\n  \"message\": \"Invalid JSON payload provided.\"\n}"
            }
          ]
        }
      ]
    }
  ],
  "variable": [
    {
      "key": "baseUrl",
      "value": "/"
    }
  ]
}