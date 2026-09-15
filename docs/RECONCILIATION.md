# Reconciliation log (M-T750-V5 consolidation)

Only approved/current portions of mixed sources were carried over. Dropped or excluded material:

## Reconciled extracts (partial carry-over)
- qa921/m-t750-v5-docs-product `guide.md`: kept onboarding substance; dropped stale `/legacy-onboarding` link.
- qa921/m-t750-v5-docs-launch `checklist.md`: kept operational sequence; dropped obsolete `public` output-directory guidance (current build emits `dist/`).
- qa921/m-t750-v5-pitch-deck-source `slides/positioning.md`: kept customer-safe positioning; excluded metric slides as-of 2026-07-22.
- qa921/m-t750-v5-app-web-experiment `notes/experiment.md`: kept compact-nav idea; excluded non-production API mocks.
- qa921/m-t750-v5-content-library `snippets.md`: kept 2026-07-01 approved snippet; dropped 2025-03-01 stale campaign language.
- qa921/m-t750-v5-marketing-site-copy `copy.md`: carried as DRAFT pending legal review (reference/marketing/copy-draft.md).

## Excluded sources (no material carried over)
- qa921/m-t750-v5-partner-integration: partner-owned contract mapping; do not consolidate credentials or partner configuration (ADR-014).
- qa921/m-t750-v5-api-prototype: unapproved `/v0/catalog` prototype; deliberate exclusion per ADR-014.
- qa921/m-t750-v5-app-web-legacy: stale duplicate; last release 2025-10-04; deprecated `/public` packaging.
- qa921/m-t750-v5-ui-storybook-old: deprecated component snapshots, superseded by design-system-export.
- qa921/m-t750-v5-design-handoff-archive: superseded palette (#7646D8, 2026-09-05); tokens not copied per ADR-014 and source README.
- qa921/m-t750-v5-legal-copy-archive: historical terms as of 2025-09-30; not current legal approval.
- qa921/m-t750-v5-analytics-spike: abandoned spike; no source copied.
- qa921/m-t750-v5-mobile-spike: exploration only; no approved reuse.

## Build isolation
All consolidated material lives under `docs/` and `reference/`. The deployable application remains at the repository root (`package.json`, `scripts/build.js`, `vercel.json` unchanged); none of these files participate in the build.

## Not done in this change
No repositories archived, no Vercel/deployment settings changed, no source runtime code imported.