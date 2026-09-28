---
id: cheatsheet-web-http-001
title: HTTP interview cheatsheet
type: cheatsheet
domain: general
category: web-platform
audience: interview candidates
tags: [http, caching, networking]
status: review
---

# Methods and Semantics

- Safe methods are intended not to request state change; idempotent methods can be repeated with the same intended effect. Implementation bugs can violate intent.
- Status families: 2xx success, 3xx redirect, 4xx client-facing request issue, 5xx server failure.
- Authentication proves identity/context; authorization checks allowed action.

# Caching

| Directive/concept | Meaning |
| --- | --- |
| `max-age` | Freshness lifetime |
| `no-cache` | May store, but revalidate before reuse |
| `no-store` | Do not store under normal compliant behavior |
| `private` | Not for shared caches |
| ETag | Validator for conditional requests |
| `Vary` | Selected request headers participate in cache key |

# Reliability

Retry only when semantics permit; use backoff/jitter, cancellation, deadlines, and idempotency mechanisms for writes. Distinguish transport, HTTP, and domain errors.

# Security

TLS protects transport. Validate/authorize server-side. Configure cookies, CORS, caching, and content handling according to the threat model.
