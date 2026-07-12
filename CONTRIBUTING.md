# Contributing

Thanks for your interest in this project. This repository holds a **reference architecture document**, not a
running codebase — so contributions look a little different from a typical software repo.

## What contributions are welcome

- **Corrections** — a typo, a broken link, a mislabeled diagram, a factual inconsistency between the README and the
  document itself.
- **Clarity improvements** — a section that's confusing, a term that needs a short definition, a diagram that's hard
  to read at a given resolution.
- **Discussion** — if you think a documented tradeoff, decision, or known limitation deserves a different framing,
  open an issue and make the case. The document is opinionated on purpose; disagreement is welcome as long as it's
  specific.

## What's out of scope

- Redesigning the architecture itself. This document reflects a specific, deliberate set of decisions explained in
  [Architecture Tradeoffs](docs/FinTech_Payments_Platform_Architecture.pdf) — proposing "just use X instead" without
  engaging with the stated reasoning isn't actionable feedback.
- Adding new production claims, metrics, or capabilities not already present in the document. See
  [`DISCLAIMER.md`](DISCLAIMER.md) for why this matters here specifically.
- Turning this into a runnable Terraform/Kubernetes codebase. That would be a great *separate* project, but it isn't
  the scope of this one.

## How to propose a change

1. Open an issue describing what you found and, if you have one, a suggested fix.
2. For small, obvious fixes (typos, broken links, dead badge), a pull request is welcome directly — reference the
   file and line.
3. For anything touching the architecture document itself (`docs/`), please open an issue first rather than a PR —
   the PDF/DOCX are the source of truth and are edited outside of Git.

## Style notes

- Keep additions to `README.md` in the same voice as the existing sections: concrete, sourced from the document,
  and explicit about what's illustrative versus what's a hard claim.
- Don't add tooling, badges, or claims that imply this is a deployed, monitored, production system. It isn't.
