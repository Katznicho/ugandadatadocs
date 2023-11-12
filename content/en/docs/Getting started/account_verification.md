---
title: Account Verification
weight: 5
---

## Account Verification

To verify an account in the ssentezo Wallet, you can use the `https://wallet.ssentezo.com/api/verify_msisdn` endpoint. This is a POST request that accepts a parameter of `phoneNumber`. NB: This request must also contain a valid HTTP Authorization Header.

### Sample Request Body

```json
{
    "phoneNumber": "256709920188"
}
```

### Possible Error Codes

In case errors have occurred, either internally or at the third-party level, the API will expose an errorCode. A sample error response might look like::

```json
{
    "message": "failure",
    "data": null,
    "errorCode": "NOT_FOUND"
}

```