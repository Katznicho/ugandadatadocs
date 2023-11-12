---
title: Withdraw Funds
description: Learn how to withdraw funds from your ssentezo Wallet account.
weight: 3
---

## Withdraw Funds from Your Wallet Account

To withdraw funds from your ssentezo Wallet account, you can use the `https://wallet.ssentezo.com/api/withdraw` endpoint. The endpoint is accessed via the POST method and requires the following request body. Ensure that all requests contain an authorization header.

### Example - Setting up a Withdraw Request

```php
$testingPhoneNumbers = ['256770691484', '256756291975', '256778292573'];

// Example request body
$requestBody = [
    'amount' => 100,
    'msisdn' => 256770691484,
    'reason' => 'Your reason for the transaction',
    'currency' => 'UGX', // Should be a valid ISO code and supported by your wallet
    'environment' => 'sandbox',
    'externalReference' => '{Your external reference}',
    'name' => '{Optional Field, You may send the name of the recipient}',
];

// With PHP, you can use cURL, Http Request 2, or Guzzle Http to perform this request.
// To mimic responses, use the provisioned testingPhoneNumbers and set the environment to sandbox.
```

### Description

The request body should contain the following parameters:

- **amount:** The amount of money being transacted. It should not be formatted or contain any non-numeric items. Amounts less than or equal to zero will throw an error.
- **msisdn:** The phone number formatted to international standards.
- **reason:** Your reason for the transaction.
- **currency:** Valid ISO format of the currency. Currently, UGX is the only currency supported for transactions.
- **environment:** Specify the environment to be utilized. "sandbox" is the testing environment. Set the environment property to production or live to enable transactions.
- **externalReference:** A string or number or reference that you use to refer to your transaction in your own application. It supports up to 250 characters.
- **account_name:** Name of the recipient (Optional Field).

### Example - Success Response

All responses are JSON-encoded strings:

```json
{
    "message": "success",
    "data": {
        "externalReference": "2391",
        "request_id": "b997c60c6f445185fcd9a3a595533734",
        "transactionStatus": "SUCCEEDED",
        "financialTransactionId": "12282913328"
    }
}
```

### Example - Failed  Response

All responses are JSON-encoded strings:

```json
{
    "message": "failed",
    "data": {
        "externalReference": "2381",
        "request_id": "b997c60c6f445185fcd9a3a595533734",
        "transactionStatus": "FAILED",
        "financialTransactionId": ""
    }
}

```

-  **NB: The financialTransactionId is the transaction reference from the Network service provider.**

### Transaction Statuses

| Status          | Description               |
| --------------- | ------------------------- |
| SUCCEEDED       | Succeeded Transaction     |
| FAILED          | Failed Transaction        |
| PENDING         | Transaction still pending |
| INDETERMINATE   | RESPONSE NOT YET DETERMINED CONTACT SUPPORT |

### Expected HTTP Response Codes

| Status Code | Interpretation                  |
| ----------- | ------------------------------- |
| 202         | Succeeded Transaction           |
| 400         | Failed Transaction              |
| 401         | No Authorization Header        |
| 403         | Invalid Credentials             |
| 500         | An error occurred (check message)|
| 422         | Unprocessable Entity (check request body)|


