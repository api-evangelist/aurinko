---
name: aurinko-manage-contact
description: Create a contact, retrieve it, update its details, and then delete it.
api: openapi/aurinko-openapi.json
operations:
- createContact
- contact
- updateContact
- deleteContact
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/aurinko-openapi.json ; every operationId checked against the contract
---

# aurinko-manage-contact

Create a contact, retrieve it, update its details, and then delete it.

## Steps

1. 1. `createContact` – send a POST with the contact fields in the request body and include the required authentication headers (e.g., `X-Aurinko-Account-Id`, `X-Aurinko-Auth-Type`).
2. 2. `contact` – GET the newly created contact using the `{contId}` path parameter and the same authentication headers.
3. 3. `updateContact` – PATCH the contact using `{contId}`, providing the fields to modify in the request body and the authentication headers.
4. 4. `deleteContact` – DELETE the contact using `{contId}` and the authentication headers.

## Rules

- All requests must include the `X-Aurinko-Account-Id` header for account identification.
- All requests must include the `X-Aurinko-Auth-Type` header to specify the authentication method.
