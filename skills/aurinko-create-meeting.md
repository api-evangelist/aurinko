---
name: aurinko-create-meeting
description: Create a booking profile, schedule a meeting, and confirm the reservation.
api: openapi/aurinko-openapi.json
operations:
- create
- bookingAccountCreateMeeting
- bookingAccountReservationConfirm
generated: '2026-10-19'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/aurinko-openapi.json ; every operationId checked against the contract
---

# aurinko-create-meeting

Create a booking profile, schedule a meeting, and confirm the reservation.

## Steps

1. 1. `create` – send required profile fields in the request body and include the `X-Aurinko-Account-Id` header.
2. 2. `bookingAccountCreateMeeting` – provide the newly created profile `id` in the path, meeting details in the body, and include the `X-Aurinko-Account-Id` header.
3. 3. `bookingAccountReservationConfirm` – supply the reservation `id` returned from the meeting creation in the path and include the `X-Aurinko-Account-Id` header.

## Rules

- Include the `X-Aurinko-Account-Id` header (AccountIdHeader) on every request.
- Use the appropriate HTTP authentication scheme (e.g., `AccountToken` or `AppAuth`) as required by the API.
