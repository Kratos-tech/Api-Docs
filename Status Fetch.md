# Status Fetch

Know Transaction Status

## Method And EndPoint

```http
 POST https://api.kratostech.in/transaction-status-service
```

### Headers

| Key             | Value            |
| :-------------- | :--------------- |
| `Content-type`  | application/JSON |
| `Authorization` | `jwtToken`       |

### Body Parameters

| Key                   | Value    |
| :-------------------- | :------- |
| `clientTransactionId` | `string` |

### Sample Request Body

```json json
{
    "clientTransaction": "cli123"
}
```

### Sample cURL

```curl
curl --location 'https://api.kratostech.in/transaction-status-service' \
--header 'Authorization: bearer your-jwt-token' \
--header 'Content-Type: application/json' \
--data '{
  "clientTransactionId" : "cli123"
}'
```
