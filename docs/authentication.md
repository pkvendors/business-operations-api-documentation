# API Authentication

## Overview
The BOMS API uses Bearer Token authentication
to verify API requests.

## Authorization Header

Developers must include an access token in
the Authorization header.

Example:

Authorization: Bearer YOUR_ACCESS_TOKEN

## Example Request

GET /employees

Headers:
Authorization: Bearer YOUR_ACCESS_TOKEN
Content-Type: application/json

## Security Recommendations

- Never share API access tokens.
- Do not store tokens in public repositories.
- Use HTTPS for API communications.
- Replace expired or compromised tokens.

## Authentication Errors

| Status Code | Description |
|---|---|
| 401 | Unauthorized |
| 403 | Forbidden |

