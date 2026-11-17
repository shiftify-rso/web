# `web` — Service Spec

## Purpose
- **Tier:** Shiftify-specific (general SPEC §10)
- **Responsibility:** Shiftify web app (SvelteKit).

## Resolved open decisions
| ID | Choice | Why |
|---|---|---|
| O-… | | |

## Owned data
The entities this service writes (it is their only writer) and their schema. Note indexes and constraints that matter.

## API
- Contract: `contracts/openapi.yaml` (or `.proto` / `.graphql`)
- Endpoint summary: method, path, purpose and roles allowed

## Events
| Direction | Event | Schema (Apicurio ID) | Notes |
|---|---|---|---|
| produces | | | |
| consumes | | | idempotency key, ordering |

## Tasks (RabbitMQ)
Queues produced or consumed, retries, DLQ. Omit if none.

## Dependencies
| Needs | From | Mechanism (sync call / replica) | Protocol |
|---|---|---|---|

## Failure behaviour
What still works when each dependency (DB, Kafka, RabbitMQ, each service) is down; timeouts and fallbacks.

## Config & secrets
Env vars, secret names (no values), and the Helm values that differ per environment.

## Acceptance tests
Which general SPEC §15 criteria this service covers, plus service-level tests.
