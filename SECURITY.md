# Security Policy

## Scope of this repository

This repository contains a **written reference architecture** (a document, diagrams, and supporting Markdown) —
it is not a running application, service, or infrastructure deployment. There is no live endpoint, no deployed
cluster, and no code in this repository that executes anywhere. Traditional vulnerability disclosure (CVEs,
exploitable endpoints, dependency scanning) does not apply here in the usual sense.

That said, two categories of report are genuinely useful and welcome:

## 1. Factual or technical errors with security implications

If you find a statement in the architecture document or README that:

- misrepresents a security control (for example, overstates what namespace isolation or mTLS actually guarantees),
- describes a pattern that would be unsafe if implemented literally as written, or
- conflicts with the document's own stated limitations (see [`DISCLAIMER.md`](DISCLAIMER.md)),

please open an issue describing the specific section and the concern. These are documentation corrections, not
security incidents, but they're taken seriously — this repository exists to model sound reasoning, and an inaccurate
security claim undermines that.

## 2. Repository / supply-chain hygiene

If you notice anything in this repository itself that looks like a credential, secret, internal hostname, account
identifier, or other sensitive artifact that should not be public, please report it privately rather than opening a
public issue:

- Open a [GitHub Security Advisory](../../security/advisories/new) on this repository, **or**
- Contact the maintainer directly (see the "About the Author" section of the README for current contact links).

This repository is intended to contain **no real credentials, account identifiers, internal IP addresses, or
production data of any kind** — everything here is illustrative. If you find something that looks otherwise, it's a
mistake and will be removed promptly.

## Response expectations

This is a personal portfolio/reference project, maintained on a best-effort basis. There is no formal SLA, but
reports under category 2 (accidental sensitive data exposure) will be prioritized and addressed as quickly as
possible.
