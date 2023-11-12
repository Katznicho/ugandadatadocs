---
title: Account Balance
weight: 8
---

## Checking the Account Balance

To check the account balance in the ssentezo Wallet, you can use the `https://wallet.ssentezo.com/api/acc_balance` endpoint. The endpoint is accessed via the POST method and does not require a request body, but a valid authorization is necessary.

### Example Request

```json
{
    "currency": "UGX"
}
```
### Sample Response 

Provided the Parameters are Satisfying:

```json
{
    "data": {
        "amount": "2976.000",
        "formatted": "2,976",
        "currency": "UGX"
    },
    "message": "success"
}

```
