# Reference material (non-runtime)

Retained non-runtime material consolidated into the canonical repository per `INVENTORY.md` and ADR-014. Nothing under `reference/` or `docs/` participates in the build: the build is `npm run build` -> `scripts/build.js` -> `dist/`, and `vercel.json` is unchanged by the consolidation.

- `design/` - approved design tokens (current)
- `sales/` - approved sales demo copy
- `ops/` - operations runbook material (current)
- `release/` - release checklist material (current)
- `research/` - research synthesis (reference only)
- `marketing/` - DRAFT marketing copy, pending legal review
- `launch/` - prior launch checklist (reconciled; obsolete output-directory guidance removed)
- `experiments/` - retained experiment ideas (no production-ready code)
- `content/` - approved content snippets (dated)
- `positioning/` - customer-safe positioning (historical metrics excluded)

Provenance for every file is recorded in `reference/PROVENANCE.md`; dropped/stale portions are documented in `docs/RECONCILIATION.md`.