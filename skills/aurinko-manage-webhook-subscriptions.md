---
name: aurinko-manage-webhook-subscriptions
description: Create, view, check, and delete push event webhook subscriptions.
api: openapi/aurinko-openapi.json
operations:
- subscribe
- getSubscriptions
- getSubscription
- unsubscribe
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/aurinko-openapi.json ; every operationId checked against the contract
---

# aurinko-manage-webhook-subscriptions

Create, view, check, and delete push event webhook subscriptions.

## Steps

1. 1. `subscribe` – Provide the subscription payload fields as defined in the contract.
2. 2. `getSubscriptions` – Retrieve the list of subscriptions; include any pagination query parameters shown in the contract.
3. 3. `getSubscription` – Supply the path parameter `id` to check a specific subscription’s status.
4. 4. `unsubscribe` – Supply the path parameter `id` to remove a subscription.

## Rules

- Include the `X-Aurinko-Account-Id` header (AccountIdHeader) on every request.
- Include the `X-Aurinko-Auth-Type` header (AuthTypeHeader) if required by the endpoint.
