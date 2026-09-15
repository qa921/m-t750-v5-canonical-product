# M-T750-V5 Consolidation Inventory Record

- Compiled: 2026-09-15 (UTC), read-only inventory of 21 repositories owned by `qa921`
- Scope: M-T750-V5 repository family. No files moved or copied; nothing archived; no deployment/Vercel settings changed.
- Revisions: commit SHAs are `main` branch heads at time of inventory; blob SHAs are the git blob IDs of the listed paths.
- Authority: ADR-014 (2026-09-08) in `qa921/m-t750-v5-decisions-adr` names `qa921/m-t750-v5-canonical-product` as the canonical deployable source.

## 1. Product source of truth (canonical)

`qa921/m-t750-v5-canonical-product` @ commit `40f31b7643afba3438673d4a94f8508f910ce465`

| Path | Blob SHA | Note |
|---|---|---|
| README.md | 91709230a44f10858d29f5cb0a31e331f25c1e4e | Build intentionally emits `dist/`; warns a Vercel project may still carry old config (tail unread, see Open items) |
| package.json | a01fbf06a05da5c4603554056a9fd0c6a2cfc028 | build = `node scripts/build.js` |
| scripts/build.js | 53d23e3abd09c448b035e7207b804dd202da0f8c | Writes `dist/index.html` |
| vercel.json | 72ac824ebbea8e5ae8ce46c093e7b3d6fa2515c3 | `{framework:null, buildCommand:npm run build}` — DO NOT change yet |

## 2. Decision material (retain)

| Repository | Commit | Path | Blob SHA | Note |
|---|---|---|---|---|
| qa921/m-t750-v5-decisions-adr | 19972a3bc9cd497b2ca59522a37c04b49978927d | adr/014-canonical-source.md | cf4432c957848a3a7911e18943b5765fc9fecdf4 | ADR-014: canonical source decision; exclusion list partially unread (see Open items) |
| qa921/m-t750-v5-decisions-adr | 19972a3bc9cd497b2ca59522a37c04b49978927d | README.md | ff2af352304f67cc1a3fd33a23021fd840e2f434 | Index of decisions |

## 3. Retained reference material (current; reference only, not deployable source)

| Repository | Commit | Path | Blob SHA | Note |
|---|---|---|---|---|
| qa921/m-t750-v5-design-system-export | c74343e29070b63ea4a3ed2cc29168653760ef93 | tokens.json | 7a43f4d939a78e4f2f80d3b8bd321363b524f085 | Current approved tokens (brand #2457F5, body #172033, version 2026-09-05) |
| qa921/m-t750-v5-design-system-export | c74343e29070b63ea4a3ed2cc29168653760ef93 | README.md | 1cb5432d79360286944035bb11a9b2309880fb2e | States export is reference material, not deployable |
| qa921/m-t750-v5-sales-demo-assets | c88615ff1fcf46a439a0e357ecef843c0ca01d0c | copy/demo.txt | 8293119fa973103b102247dc1ca876289903a644 | Approved demo copy; instructs exporting asset references before moving files |
| qa921/m-t750-v5-sales-demo-assets | c88615ff1fcf46a439a0e357ecef843c0ca01d0c | README.md | cbde6bec9dfa040f6bfba228ff1d13ed231edb0c | Screenshots are reference assets only |
| qa921/m-t750-v5-marketing-site-copy | faef383161a4dc0856c8fb2573624d51ec98386f | copy.md | a3ba7f5fdfba2e0dd0a3c8922f32e33ec1484fd7 | Current headline candidate; draft pending legal review |
| qa921/m-t750-v5-marketing-site-copy | faef383161a4dc0856c8fb2573624d51ec98386f | README.md | b70f150c6a09f5e5b60b9d5175c23f45b5969fbb | Requires product review before inclusion |
| qa921/m-t750-v5-ops-runbooks | 4cca44f15810d72950cda10989f124a24f03b228 | deploy.md | fde57e86c7ff7b15d497afbc38a43446e04872c1 | Current deploy verification procedure (inspect failed deployment by ID/revision/build events) |
| qa921/m-t750-v5-ops-runbooks | 4cca44f15810d72950cda10989f124a24f03b228 | README.md | bba4a728de102786403e6aa064c4c1ee2509a074 | Do not trust historic green state |
| qa921/m-t750-v5-release-checklists | a902edc2fc3231773b91e886f99b820cacb0e3d8 | release.md | 5e7aac58110d7f812b5ae64c88ffcb921ad590f4 | Current sequence: inventory, PR+review, confirm merged SHA, diagnose failed deployment, redeploy |
| qa921/m-t750-v5-release-checklists | a902edc2fc3231773b91e886f99b820cacb0e3d8 | README.md | c19d9d5eb4f6be4e1757638890a108c441a08c46 | Checklist expectations |
| qa921/m-t750-v5-research-notes | b1d257a937064c7610f9a91b164428d6c69dc1f2 | synthesis.md | 27a85b9547208346a4999e73d12c288002436877 | Interview synthesis; reference only |
| qa921/m-t750-v5-research-notes | b1d257a937064c7610f9a91b164428d6c69dc1f2 | README.md | 457d954f49dcc7c1c18ebb74d4693200219408be | No implementation artifacts |

## 4. Selective extracts requiring reconciliation (mixed current/stale; do not copy wholesale)

| Repository | Commit | Path | Blob SHA | Keep / Reconcile |
|---|---|---|---|---|
| qa921/m-t750-v5-content-library | d39bbf36ced1298c9661696171924ba8f9229e44 | snippets.md | 14d484bd6e60e68dd0e67ded20019b40b6cfd460 | Keep 2026-07-01 approved snippet; drop 2025-03-01 stale campaign language |
| qa921/m-t750-v5-content-library | d39bbf36ced1298c9661696171924ba8f9229e44 | README.md | 0df0248fb826c66a399caf015375c734818db9ee | Compare dated entries before preserving |
| qa921/m-t750-v5-pitch-deck-source | e724f79db5ee55e29bbe2fe8ffe6a07aa60d9c51 | slides/positioning.md | b05c641744dc2ca842971deae00d5879aabb7e1d | Keep positioning; metric slides as-of 2026-07-22 must not overwrite current data |
| qa921/m-t750-v5-pitch-deck-source | e724f79db5ee55e29bbe2fe8ffe6a07aa60d9c51 | README.md | b576c84df2e3a60952799457dfff3ca340df8f5d | Customer-safe positioning only |
| qa921/m-t750-v5-docs-product | 226bbf8e21ffba138d5f221204d46735422538ec | guide.md | c3f8c2620bf63aaed41510887221ee6f52872e9b | Onboarding substance usable; stale `/legacy-onboarding` link must be reconciled |
| qa921/m-t750-v5-docs-product | 226bbf8e21ffba138d5f221204d46735422538ec | README.md | c3dd69b1930a8cc55699640be06779fbda05d04e | Links point to legacy app routes |
| qa921/m-t750-v5-docs-launch | ef75e8c6fa8c4e793f9a71d8a2ad1851ea69e0ff | checklist.md | d9d8114724ef050e204f180f7c22312320561073 | `public` build-output guidance is historical only; verify current deploy evidence |
| qa921/m-t750-v5-docs-launch | ef75e8c6fa8c4e793f9a71d8a2ad1851ea69e0ff | README.md | 740b26d548c27402f30e6c8ef581fbac95dfcd69 | Prior launch checklist dated 2025-11-16; operational sequence still useful |
| qa921/m-t750-v5-app-web-experiment | 7c64ea4cb149a0d021fb00e52ac41cb73aed11ca | notes/experiment.md | fc9f19e01a92ee6508b77d337d1402cb3d48b86d | Keep `compact-nav` idea (2026-08-28) for comparison only |
| qa921/m-t750-v5-app-web-experiment | 7c64ea4cb149a0d021fb00e52ac41cb73aed11ca | README.md | 17eb69a48870d7b2aa851096667ef4be71d18602 | API mocks not production-ready; no release approval |

## 5. Exclusions (stale duplicates / not approved for consolidation; nothing archived yet)

| Repository | Commit | Path | Blob SHA | Reason for exclusion |
|---|---|---|---|---|
| qa921/m-t750-v5-app-web-legacy | 06b7bcae33245d39a8b5e174c1ec8901e05390fb | src/routes.txt | 55d94129395e5d09ebde828402081125966e84f0 | Stale duplicate; last release 2025-10-04; deprecated `/public` packaging |
| qa921/m-t750-v5-app-web-legacy | 06b7bcae33245d39a8b5e174c1ec8901e05390fb | README.md | 97d2d8517be424c7f0b700d519266c256bcc9057 | Archival requires explicit approval; not assumed |
| qa921/m-t750-v5-ui-storybook-old | d5535298d8e83bc2859d922dfe8bf99f64a438b4 | stories/button.md | 4e8efc41b608f3398017c6b7cc7614282bafe3b1 | Deprecated purple button; superseded by design-system-export |
| qa921/m-t750-v5-ui-storybook-old | d5535298d8e83bc2859d922dfe8bf99f64a438b4 | README.md | 8fe327c94089fbf267ae64c773f1a97ed71a395d | Retain as history only if archival approved |
| qa921/m-t750-v5-design-handoff-archive | 01fcb9ae3d34517a63682f5400ef92c2ac8d661d | handoff.txt | 7fb112fcca61ea2e4651c998b6452336fce23df3 | Superseded palette #7646D8 (2026-09-05); do not copy tokens |
| qa921/m-t750-v5-design-handoff-archive | 01fcb9ae3d34517a63682f5400ef92c2ac8d661d | README.md | 37b11bb85a74c5d1db6600c5f13a2fc5661f589a | Preserve history if archival approved |
| qa921/m-t750-v5-legal-copy-archive | c4e50f34c62e83eca75f8056af1179fc4f90c2fe | terms.md | f7404b8a0d49fe7ba7499f068011cc7e3c5ba50c | Historical as of 2025-09-30; not current legal approval |
| qa921/m-t750-v5-legal-copy-archive | c4e50f34c62e83eca75f8056af1179fc4f90c2fe | README.md | 127aef605133de9e7a05bc8c1490327a93f6db78 | Legal owner must resolve any reuse |
| qa921/m-t750-v5-analytics-spike | 9e52d956664fe7b19313c497af05cd3dbbad4b7d | spike.sql | e3ce8d1c1012dbe5feadbecaaec15341d6c69098 | Abandoned cohort experiment; no source to be copied |
| qa921/m-t750-v5-analytics-spike | 9e52d956664fe7b19313c497af05cd3dbbad4b7d | README.md | 42c5d3f85b3bb7558c2f5138ba9d16d2be34cecd | May be archived after inventory |
| qa921/m-t750-v5-mobile-spike | b7676d8777023a01b9d445429018a6a517346f32 | spike.md | af35cdce3088f86ca30984d4533ab6c89a65f350 | Exploration only; incomplete authentication; no approved reuse |
| qa921/m-t750-v5-mobile-spike | b7676d8777023a01b9d445429018a6a517346f32 | README.md | 40b108222623ee26343aec0b8eb01ab6216bca76 | Archive decision requires owner approval |
| qa921/m-t750-v5-api-prototype | df83ddd96d830a6104b66cea09afa9a69c702a21 | openapi.txt | 7e765375524dad90356fc78de7bf861afbfa3986 | Unapproved `/v0/catalog` prototype; excluded per ADR-014 |
| qa921/m-t750-v5-api-prototype | df83ddd96d830a6104b66cea09afa9a69c702a21 | README.md | 51414a2a316c97dca7426b6909fe75e40bb91ac2 | Deliberate exclusion expected |
| qa921/m-t750-v5-partner-integration | 5896be263958db09ce7ce0498fb4040c799d087b | contract.md | 5dbf3ce8517c12d590febc9d7c97974d54530347 | Partner-owned mapping; owner approval required for any migration |
| qa921/m-t750-v5-partner-integration | 5896be263958db09ce7ce0498fb4040c799d087b | README.md | 19a5dec1990e223973c04b342f919f3cd188ec2a | Do not consolidate credentials or partner configuration (ADR-014) |

## 6. Open items / caveats

- Tails of `m-t750-v5-canonical-product/README.md` and `adr/014-canonical-source.md` (and a few README tails in sections 3-5) were truncated during transfer; re-read before relying on the full Vercel warning text or ADR-014's complete exclusion list.
- Vercel output-directory config is unverified: build emits `dist/` while old docs reference `public`. Do not change deployment settings until the failed deployment is diagnosed per `m-t750-v5-ops-runbooks/deploy.md`.
- `m-t750-v2-canonical-product` is an older V2 fixture and out of scope.
- No PR opened, no source material copied, no repositories archived, no deployment settings changed as part of this record.
