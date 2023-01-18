# User

## Summary or Introduction

These are the APIs for all 3 types of `users` `job-seeker`, `employer`, and `vendor`

- [User](#user)
  - [Summary or Introduction](#summary-or-introduction)
  - [**Create User**](#create-user)

## **Create User**

- route: `api/v1/user`
- method: `POST`
- request: request can be one of the following types:
  ```json
  {
    "body": {
      "email": "saral@digimonk.in",
      "mobileNumber": "",
      "password": "abcd",
      "role": "job-seeker" || "employer" || "vendor",
      "countryCode": ""
    }
  }
  ```
  ```json
  {
    "body": {
      "email": "",
      "mobileNumber": "1234567890",
      "password": "abcd",
      "role": "job-seeker" || "employer" || "vendor",
      "countryCode": "+91"
    }
  }
  ```
  ```json
    {
      "body": {
        "email": "saral.shrivastava@digimonk.in",
        "mobileNumber": "1234567890",
        "password": "abcd",
        "role": "job-seeker" || "employer" || "vendor",
        "countryCode": "+91"
      }
    }
  ```
- response:
  ```json
  {
    "code": 200,
    "headers": {
      "x-access": "${JWT_TOKEN}",
      "x-refresh": "${JWT_TOKEN}"
    },
    "data": {
      "message": "User Created Successfully"
    }
  }
  ```
