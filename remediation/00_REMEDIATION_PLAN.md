# 00_REMEDIATION_PLAN.md · Federal Demand Intelligence Corpus v0.1 → v0.2

> Branch: `remediation/federal-corpus-v0.2-source-receipts`
> Parent commit: `760f8f0` (federal corpus v0.1 initial push)
> Audit basis: `audit/00_RECEIPT_AUDIT_VERDICT.md`
> Verdict at start: **HONEY_PENDING_REMEDIATION** (65/93 ledger_ready claims confirmed · 28 failing §3 federal policy)

## Why we did the work

The v0.1 audit confirmed the federal corpus has real substance · 58 URL-grounded SAM
opportunities, 35 URL-grounded award receipts, $10.38B in observed ceiling, 0 personal
PII outside the operational allowlist, 0 duplicate IDs, 0 parse errors. But the
manifest carried four discoverable lies and 28 records claimed `ledger_ready` while
failing federal-adapted §3 checks. Same shape as the swarm-research v0.1 audit:
real data, sloppy reporting layer.

## What we changed (in this branch)

### Manifest fixes (R1–R6)

- **R1 · record_counts.total_opportunities=73 retired.** Replaced with explicit
  `record_counts_derivation_v0_2` block enumerating per-file counts. Observed totals: 58 opps + 35 awards + 4 active + 52 expired = 149 unique records.
- **R2 · file_manifest regenerated** with accurate `exists` flags + `size_bytes` for all 16 canonical files (00–14 + README).
- **R3 · in-house sha256 embedded** for every file in `file_manifest`. `hash_status: "in_house_sha256_embedded"`. Honors the "kill Hedera · datasets hash in-house · DefendableLedger is the anchor" doctrine.
- **R4 · award-ceiling reconciliation.** Sum of `05_AWARD_RECEIPTS.jsonl` = `$10.384B`. README's `$10.4B+` claim is correct to two sig figs. `00_EXECUTIVE_VERDICT.md` claim of `$12.5B+` was footnoted in this branch with a pointer to the v0.2 reconciliation; v0.3 should rewrite the exec verdict to match observed.
- **R5 · rejection-log acceptance criteria** published in `manifest.acceptance_criteria_doctrine`. The 6 v0.1 criteria that produced 0 rejections are now explicit. v0.2 downgraded 12 records to `context_only` rather than rejecting them — preserves training value.
- **R6 · tier_2 corroboration policy.** Every `tier_2` record carries `corroboration_required: true`. Promotion to `ledger_ready` requires either a tier_1 secondary citation or named human review.

### Per-record remediation (R8)

- **R8.A · F3_ID** · 4 opps backfilled with `notice_id` extracted from their SAM.gov `source.reference` URL. Provenance recorded under `source._v0_2_audit.notice_id_provenance = 'extracted_from_sam_gov_url'`.
- **R8.B · F5_FACT_VS_INFERENCE** · 16 opps re-noted with structured `[v0.2 audit]` notes naming agency, sub-agency, notice type, dates, NAICS, set-aside, SAM notice as documented facts vs capability-lane and DefendableOS fixer mapping as analytic inferences. Each note ≥ 200 chars.
- **R8.C · F6_TIER_1_NOT_GOV_URL** · 4 awards downgraded from `tier_1` to `tier_2` because their `source_url` resolves to a contractor `.com` press release (sokat.com, skymantics.com, aquia.us, etc.), not a `.gov`/`.mil` domain. `ledger_status` flipped to `context_only`. `corroboration_required: true` set.
- **R8.D · F8_AMOUNT** · 4 awards downgraded to `context_only` because no public dollar value is disclosed in the source. Records retained as evidence of agency-contractor relationship without claiming a ceiling.

## What we did not change

- `audit/` v0.1 receipts are immutable books-and-records and were not touched.
- No record was deleted. Every opp/award retains its evidentiary value.
- README left untouched · its `$10.4B+` claim already reconciles with observed.
- Active targets (4 deadlines this week · Army RMF May 29, NRC May 26, DOT SBIR May 29, USPTO May 28) were not modified — operational priority outranks editorial remediation.

## What is still open for v0.3

- 4 F6-downgraded tier_1→tier_2 awards may be promoted back to `ledger_ready` if a named human reviewer corroborates against a tier_1 secondary source.
- `00_EXECUTIVE_VERDICT.md` table row formatting beyond the two reconciliation footnotes — the prose underneath should be rewritten in v0.3 to match observed totals.
- Rejection log doctrine should add per-record traceability when v0.2+ research runs produce real rejections.

## Counts · v0.1 → v0.2

| Measure | v0.1 | v0.2 | Δ |
| --- | ---: | ---: | --- |
| Records claiming `ledger_ready` | 93 | 85 | −8 (4 F6 + 4 F8 to context_only) |
| Records confirmed `ledger_ready` against §3 | 65 | 85 | +20 (F3 + F5 backfill closed 20 prior fails) |
| Records claiming ready but failing §3 | 28 | 0 | −28 ✅ |
| tier_1 records (sources) | 7 of 15 | 7 of 15 | 0 |
| tier_2 records flagged `corroboration_required` | 0 | 14 records | +14 ✅ |
| Manifest `hash_status` | pending_generation | in_house_sha256_embedded | ✅ |
| File_manifest stale `exists` flags | 4 | 0 | ✅ |
| Manifest count mismatches vs observed | 7 | 0 | ✅ |
| Personal PII outside allowlist | 0 | 0 | (already clean) |
| Total registry records | 58 | 58 | (no deletes) |
| Award ceiling observed | $10.38B | $10.38B | (no change) |

`A lower but truthful ledger_ready count is stronger than an inflated count.`

## Final verdict label

See `audit-v0.2/00_RECEIPT_AUDIT_VERDICT.md`.
