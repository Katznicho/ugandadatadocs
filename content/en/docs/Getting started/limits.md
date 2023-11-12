---
title: Transaction Limits and Supported Currencies
description: Learn about transaction limits and supported currencies for the ssentezo Wallet API.
weight: 4
---

## Transaction Limits

The ssentezo Wallet API enforces certain limits and restrictions to ensure the security and integrity of transactions. Here are important details to keep in mind:

- **Input Restrictions:**
  The API does not support the entry of negative figures, exponential figures (e.g., e100), or characters when entering the amount to be transacted.

- **Withdrawal Limits:**
  - For withdrawing money, only transactions of 500 Uganda Shillings and above will be processed.

- **Collection Limits:**
  - For collecting money, transactions of any amount are allowed, provided the current account balance of the wallet can cover the associated charges as defined in your ssentezo agreement.

- **Transaction Charges:**
  Charges are applicable to all transactions as specified in your contract for the use of this service.

### Important Note

Using unsupported currency codes will result in an Unsupported Currency error with an HTTP Status Code of 500.

## Supported Currencies

As of the writing of this documentation, the ssentezo Wallet API supports only Uganda Shillings (UGX) for transactions.

| ISO Code | Currency Name      | Status   |
|----------|--------------------|----------|
| UGX      | Uganda Shillings   | Supported|

Attempting to use unsupported currency codes will result in an error, and the API will respond with an HTTP Status Code of 500.
