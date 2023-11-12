---
title: Authorization
description: Learn how to authorize access to the ssentezo Wallet API.
weight: 3
---

## Authorization

The ssentezo Wallet API utilizes the Auth Basic authorization method to ensure secure access to its services. To interact with the API, users must possess valid API credentials, which can be generated from the API Access menu within their wallet account.

### Auth Basic Authorization

Auth Basic is a simple and widely used method for securing API endpoints. It involves including a set of credentials, typically a username and password, in the HTTP headers of the API request. The ssentezo Wallet API utilizes this method to authenticate and authorize users.

### Generating API Credentials

Follow these steps to generate API credentials:

1. **Log in to Your Wallet Account:**
   - Visit [wallet.ssentezo.com](https://wallet.ssentezo.com) and log in to your ssentezo Wallet account.

2. **Navigate to API Access:**
   - In your wallet account, locate the API Access menu. This is typically found in the account settings or developer sections.

3. **Generate API Credentials:**
   - Inside the API Access menu, you should find an option to generate API credentials. Click on this option to create a set of credentials specifically for API access.

4. **Note Your Credentials:**
   - Once generated, take note of your API credentials. These typically include a username and password.

### Using API Credentials

To make API requests, include your API credentials in the HTTP headers of your requests. Here is an example using the `curl` command-line tool:

```bash
curl -u YOUR_USERNAME:YOUR_PASSWORD https://api.ssentezo-wallet.com/v1/endpoint


