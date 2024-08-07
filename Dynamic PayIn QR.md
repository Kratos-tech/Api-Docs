# Dynamic PayIn QR

Generate Dynamic PayIn

## Method And EndPoint

```http
  POST https://api.kratostech.in/dynamic-qr-service
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
| `amount`              | `number` |
| `token`               | `string` |

### Sample Request Body

```json json
{
    "clientTransactionId": "cli123",
    "amount": 100,
    "token": "your-generated-auth-token"
}
```

### Sample cURL

```curl
curl --location 'https://api.kratostech.in/dynamic-qr-service' \
--header 'Authorization: bearer your-jwt-token' \
--header 'Content-Type: application/json' \
--data '{
  "clientTransactionId" : "cli123",
  "amount" : 100,
  "token" : "your-generated-auth-token"
}'
```

### Sample Response Body

```json
{
    "id": 5,
    "companyId": "1",
    "clientTransactionId": "1",
    "amount": "100.00",
    "timestamp": "2024-08-06T22:38:34.682Z",
    "qrIntent": "upi://pay?ver=01&mode=15&am=100.00&mam=100.00&cu=INR&pa=pay.xyzsales@bank&pn=XYZ&mc=5262&tr=XYZ37958311082811514205b2b&tn=XYZ37958311082811514205b2b&mid=xyzP3734&msid=xcxa-1462&mtid=zghfP-3734",
    "encoding": "Base64",
    "qrCodeEncoded": "iVBORw0KGgoAAAANSUhEUgAAAMgAAADIAQAAAACFI5MzAAADNklEQVR4Xu2XO47rOgyGGahQ52zAgLahTltyNuDHBuwtqdM2DGgDVqdCMM9PzySYe4FThOkORgiCWB8QSnz8pIn/tuj/G6/1S/5JchCNgUvNS6V7NadtRE5NCrch8FLbaPPp2yO2iT8gsR9tPwTHtQ3EG77tR+QR3WHdad0aDKf+QzLFvrM7EayZw/608z65fDBbU3D1JB79r3feI4jPI/U/Pz8i9zaRVXF1XtgdBINfW0pyUH+LvCU3E93ZnGRWryenpCGe8hH6qZolISWdnhB1IW+pDZ5PD9i6px0N8YhJP/pGfieP4+fVf9tRkBL3e8wHwQeMZORojg8IVzdb1C4OS4NHoPIsu0pSULuBcOQOcUaUAvJaT5DLh28dIXfyElEreat6UiqRpYHcSryS2aop8QMSDX5sSEbe75VXm3F2PeE2Ui4xr9fV4drhO3c05AwZQrWKtCDmODhqRU840mDNQabUvQtSc8dTDxSkJLPJYfdbpc5D+fIlCUrC2IuQ5HxalIgRpf+AnMialOEJ0aqwP1BzQU9KpBtLx5glfQw8SmJdSU6Pv8/InYWJAuLjSnUfkP5RAV1J7gp1//KBgpSIvTbF/cFu9u2eYEdPOMlhkS9oRBMjPi8faEhJKLhLq2gfvQjM8jyBgnDtoVUTnqrYROteWE8Q51JljkApP/AIpQ9OTQr+20vZzYE6a1ZrtvS8z/vkJCmyLUGV9zu7RQ7+ZUdDOCLCO+yckj7Y/hYtHSmcpfNDPll6o4xmrCcnrk4ifvDrxCJ75zPjFYQrjulWj36LoUz65O2VOwoS202mnjZ69AqplTPoySntwkCfFkkcniV39AQxGaXgDGSvC261cIlTEyyIMaan+yWBmHcgM2pyeJQvbo/KM2IEPS2wmiC2ELzB75NMiBgreqlmLUHDQR+7JTOLVsnnpWIach0cw+aNafRug6xGPZHZv7YpYRbu4dQJShP0RCaUIFq1oFdIzTl5QVETlGzC+yVGiR7qIr3x1X9UZCAIVSPJROh93/mXHQ15YDaxUCyEugHO4QOC9znfY0JkDLD+6+X15dG3icSH5d5zgPhhAr0GbS35y/olv0TWH7OiQ8idYetXAAAAAElFTkSuQmCC",
    "message": "QR generated successfully!",
    "status": "Success",
    "refid": "XYZ37958311082811514205b2b"
}
```
