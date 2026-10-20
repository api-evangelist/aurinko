---
name: aurinko-upsert-and-get-account
description: Create or update a personal account and then retrieve its details.
api: openapi/aurinko-openapi.json
operations:
- upsertPersonal
- getAccount
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/aurinko-openapi.json ; every operationId checked against the contract
---

# aurinko-upsert-and-get-account

Create or update a personal account and then retrieve its details.

## Steps

1. 1. Call `upsertPersonal` with the account data in the request body and include the required header `X-Aurinko-Account-Id`.
2. 2. Call `getAccount` with the newly created/updated account ID in the path parameter `{id}` and include the required header `X-Aurinko-Account-Id`.

## Rules

- Auth: Include the `X-Aurinko-Account-Id` header (AccountIdHeader) on each request.
- Idempotency: The `upsertPersonal` operation is idempotent – sending the same payload with the same account ID will not create duplicate accounts.
- Errors: The API returns standard HTTP error codes (e.g., 400 for validation errors, 401 for missing/invalid authentication, 404 if the account ID is not found).
