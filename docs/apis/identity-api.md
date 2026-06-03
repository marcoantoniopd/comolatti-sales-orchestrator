# Identity API

## Login

POST /auth/login

### Request

```json
{
  "cnpj": "12345678000199"
}
```

### Response

```json
{
  "customer_id": "C123",
  "sales_wallet": "Pellegrino SP",
  "distribution_center": "CD Guarulhos",
  "token": "jwt-token"
}
```
