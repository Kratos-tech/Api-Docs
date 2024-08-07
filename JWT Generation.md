# Access Token Generation

Generate API Access Token

## Method And EndPoint

```http
  POST https://api.kratostech.in/authentication
```

### Headers

| Key            | Value            |
| :------------- | :--------------- |
| `Content-type` | application/JSON |

### Body Parameters

| Key        | Value    |
| :--------- | :------- |
| `strategy` | `string` |
| `email`    | `string` |
| `password` | `string` |

### Sample Request Body

```json json
{
    "strategy": "local",
    "email": "your-email",
    "password": "your-password"
}
```

### Sample Response Body

```json
{
    "response": {
        "accessToken": "eyJhbGciOiJIUzI1NiIsIbdb556cCI6ImFjY2VzcyJ9.eyJpYXQiOjE3MjI5Ookm66NjMsImV4cCI6MTcyMzA2Njc2MywiYXVkIjoiaHR0cHM6Ly9rcmF0b3N0ZWNoLmluIiwic3ViIjoiNCIsImp0aSI6IjFjZjQxYTNhLWRlNjAtNDJhMi05M2RhLWNiZTIxNjE2OGFkMyJ9.81LxyWKoKKtb_cJkHlcnIvZeZ3T1eGZTZrVF02PL3KA",
        "authentication": {
            "strategy": "local",
            "payload": {
                "iat": 1722980363,
                "exp": 1723066763,
                "aud": "https://kratostech.in",
                "sub": "4",
                "jti": "1cf4edc7f3a-d450-42ar2-93dra-cbe21ggr68ad3"
            }
        },
        "user": {
            "id": 4,
            "email": "example@example.com",
            "companyId": 1,
            "firstName": "w",
            "lastName": "w",
            "role": "user",
            "isActive": true,
            "lastLoginAt": null,
            "signingKey": "dvIidQTrMMqdfbdbeULJDqLQbHcqkBQkapfc",
            "createdAt": "2024-08-06T20:06:32.934Z",
            "updatedAt": "2024-08-06T20:06:32.934Z"
        }
    }
}
```

### Sample cURL

```curl
curl --location 'https://api.kratostech.in/authentication' \
--header 'Content-Type: application/json' \
--data '{
 "strategy" : "local",
  "email" : "your-email",
  "password" : "your-password",
}'
```
