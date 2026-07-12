# Disclaimer

This disclaimer restates and expands on the scope note already present on page 2 of
[`docs/FinTech_Payments_Platform_Architecture.pdf`](docs/FinTech_Payments_Platform_Architecture.pdf). If anything here
and in the document itself ever appear to conflict, the document is authoritative.

## What this is

This repository contains a **reference architecture** — inspired by production cloud-native patterns and real-world
fintech engineering practices, written for **educational and portfolio purposes**. It illustrates how a set of
architectural decisions fit together for a payments platform of this shape and scale.

## What this is not

- **Not a claim of ownership** of, or direct operational experience running, any specific named company's production
  system beyond what is explicitly described in the document.
- **Not a disclosure of any real company's infrastructure.** Any resemblance to a particular organization's actual
  account structure, network layout, or internal configuration is coincidental; no real account IDs, IP ranges,
  credentials, or internal hostnames appear anywhere in this repository.
- **Not measured production data.** Every number in the document's "Production Metrics" section is explicitly
  labeled illustrative — representative of a platform operating at this scale, not a disclosed measurement.
- **Not a tested disaster-recovery capability.** The "Regional Disaster Recovery" section describes a reference
  design for how a region-level failure *would* be handled — it has not been operationally tested, drilled, or
  measured, and the document says so directly.
- **Not a compliance determination.** Namespace isolation, mesh mTLS, and routing card data directly to a
  PCI-DSS-compliant processor are reasonable technical patterns that reduce scope and blast radius — they are not,
  on their own, a PCI-DSS compliance verdict. Any real deployment's actual compliance scope must be validated through
  a formal assessment by a Qualified Security Assessor (QSA), never inferred from this document.

## Known, deliberately stated limitations

The architecture document is explicit about what it does not (yet) solve, rather than hiding these gaps:

- A compliance-retention gap between `PaymentCompleted` (7-day retention) and downstream compliance consumer
  downtime longer than that window.
- Single-region operational scope — every resilience mechanism described operates within one AWS region across
  multiple Availability Zones.
- Namespace and mesh isolation are explicitly *not* treated as a substitute for network- and workload-level
  segmentation that a PCI assessment would require around cardholder-data-adjacent workloads.

These are documented as **known limitations**, not oversights discovered after the fact — see "Known Limitations &
Operational Edge Cases" in the full document.

## If you use this work

You're welcome to learn from, reference, and build on this architecture under the terms of the
[license](LICENSE). If you cite or adapt it, please carry this disclaimer's spirit forward: be clear about what is a
documented pattern versus a tested, measured, or certified capability.
