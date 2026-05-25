# Federal-adapted Trust-Tier Policy · DefendableOS Federal Demand Intelligence Corpus v0.2

> Inherits the spirit of `defendableos-swarm-research/remediation/03_TRUST_TIER_POLICY.md`
> and adapts §3 mandatory checks to federal procurement record schema.
>
> *Books and records. No proof, no honey.*

## 1 · Scope

Applies to every record in:
- `02_RAW_SAM_OPPORTUNITY_REGISTRY.jsonl` (opportunities)
- `05_AWARD_RECEIPTS.jsonl` (awards)
- `03_ACTIVE_TARGETS.csv` (active solicitations)
- `04_EXPIRED_MARKET_PROOF.csv` (expired demand signals)

Applies to every source in `manifest.source_manifest`.

Does not retroactively rewrite the v0.1 audit receipts in `audit/`.

## 2 · Trust-tier definitions (federal-adapted)

| Tier | Label | Definition | Examples |
| ---- | ----- | ---------- | -------- |
| 1 | Government / Statutory | SAM.gov direct record, USAspending.gov, agency .gov/.mil official publication, OMB/GAO publication, federal court of record, statutory text on Congress.gov/govinfo.gov. | SAM.gov solicitation page, ai.mil press release, gsa.gov news release |
| 2 | Authoritative non-govt | Contractor primary-source press release, recognized media outlet (Reuters, Wired, etc.), industry research with verifiable methodology. | boozallen.com press release, wired.com reporting, govcdoiq.org analysis |
| 3 | Industry / Trade | Trade publication, recognized industry analyst. | (no v0.2 records at this tier) |
| 4 | Operational | Smaller publication, blog post from named expert. | (no v0.2 records at this tier) |
| 5 | Unverified | No primary source, unknown owner. | (no v0.2 records at this tier · would be rejected at intake) |

## 3 · Mandatory `ledger_ready` checks (federal opportunities)

A record in `02_RAW_SAM_OPPORTUNITY_REGISTRY.jsonl` is **ledger_ready** if and only if:

- **F1 TRUST_TIER_DECLARED** · `source.trust_tier ∈ {tier_1, tier_2}`
- **F2 URL_RESOLVABLE** · `source.reference` matches `^https?://`
- **F3 NOTICE_OR_SOLICITATION_ID** · `source.notice_id` OR `source.solicitation_number` non-empty
- **F4 AGENCY_PRESENT** · `opportunity.agency` non-empty
- **F5 FACT_VS_INFERENCE** · `trust.fact_vs_inference_notes` ≥ 40 chars · names what is documented fact vs analytic inference
- **F6 SAM_OR_AGENCY_FOR_TIER_1** · if `tier_1`, the URL must resolve to `sam.gov`, `.gov`, or `.mil`
- **F7 LEDGER_STATUS_SET** · `trust.ledger_status` non-empty

## 3.A · Mandatory `ledger_ready` checks (federal awards)

A record in `05_AWARD_RECEIPTS.jsonl` is **ledger_ready** if and only if:

- F1, F2, F4, F6, F7 above
- **F3' CONTRACT_OR_AWARD_ID** · `contract_number` OR `award_id` non-empty
- **F8 AMOUNT_DISCLOSED** · `ceiling_amount` OR `award_amount` is a positive number

Awards without F8 are downgraded to `context_only` and retained as evidence of agency-contractor relationship without a defensible dollar value.

## 4 · Tier-2 corroboration gate

Every `tier_2` record carries `corroboration_required: true`. A `tier_2` record may be promoted to `ledger_ready` only when one of:
- A `tier_1` secondary citation is added to the record's source manifest entry, OR
- A named human reviewer audits the record and signs the registry row to `primary_source_confirmed: yes`.

Until either condition is met, `tier_2` records remain `context_only`.

## 5 · Path discipline (carried from swarm-research)

- **Path A (add to registry)** · only when source owner is recognized govt (tier_1) or recognized authoritative non-govt (tier_2), URL resolves, and source-type is admissible.
- **Path B (remap to canonical source_id)** · only on URL_EXACT match against existing source_manifest entry.
- **Path C (downgrade to context_only)** · default for records that fail F1-F8 but have evidentiary value · seed/record retained, `trust.fact_vs_inference_notes` records the reason.
- **Path D (quarantine / reject)** · reserved for records that contradict a tier_1 primary source or assert facts that cannot be defended.

v0.2 federal remediation used Path C for 4 F6 tier-downgrades, 4 F8 amount-undisclosed, and 0 Path D rejections.

## 6 · Enforcement

Every release tag (`vX_X`) must include:
- `audit/` v0.1 receipts (immutable),
- `audit-vX_X/` re-audit receipts with verdict label,
- `manifest.hash_status = "in_house_sha256_embedded"`,
- 0 records claiming `ledger_ready` but failing §3 / §3.A checks,
- 0 personal PII outside the operational allow-list (govt POC, role addresses, FAR clauses).

A tag failing any of these is **not** ledger-ready and must carry the `HONEY_PENDING_REMEDIATION` or `PROPOLIS_REMAINS` verdict label.

---

`books and records. no proof, no honey. kill hedera. defendableledger is the anchor.`
