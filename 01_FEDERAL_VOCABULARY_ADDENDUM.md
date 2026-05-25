# 01_FEDERAL_VOCABULARY_ADDENDUM.md
# DefendableOS Federal Vocabulary Addendum

**Version:** 1.0
**Effective Date:** 2026-05-24
**Authority:** Defendable Tribunal Curator, Federal Demand Intelligence Division
**Status:** MANDATORY for all federal opportunity records

---

## I. PREAMBLE: WHY THIS VOCABULARY EXISTS

The DefendableOS vocabulary was built for commercial markets. It maps neatly onto the commercial demand cycle:

```
OFFENSE_SIGNAL  ->  PAIN_RECEIPT  ->  DEFENSE_FIXER  ->  DEFENDABLE_LEDGER
```

Federal procurement **does not follow this cycle**. In federal markets:

- Agencies **do not express pain** -- they issue **solicitations**.
- Problems are not discovered through customer interviews -- they are **published in SAM.gov**.
- Solutions are not pitched to buyers -- they are **proposed in response to structured notices**.
- Contracts are not closed in CRM -- they are **awarded through FAR-compliant procurement cycles**.

The Federal Vocabulary Addendum exists to bridge this gap. Every term defined here maps back to the DefendableOS core vocabulary while respecting the structural reality of federal procurement.

---

## II. THE CRITICAL DISTINCTION

### SAM Procurement Notices Are Demand Receipts, NOT Pain Receipts

This is the single most important concept in the federal vocabulary.

| Dimension | PAIN_RECEIPT (Commercial) | DEMAND_RECEIPT (Federal) |
|-----------|--------------------------|-------------------------|
| **Origin** | Customer expresses pain, problem, or gap | Agency publishes procurement notice per statute |
| **Trigger** | Discovery call, user complaint, churn signal | Congressional appropriation + agency mission need + policy mandate |
| **Format** | Unstructured: "We're losing money on fraud" | Highly structured: Sources Sought, RFI, RFQ, RFP, Solicitation, Award Notice |
| **Location** | CRM, support tickets, sales call notes | SAM.gov, agency websites, FedBizOpps successor |
| **Verification** | Requires customer interview | Self-verifying (published by contracting officer) |
| **Actionability** | Requires qualification and nurturing | May require immediate response with hard deadline |
| **Competition** | Unknown until late in sales cycle | Declared in the notice (set-aside, full-and-open) |
| **Budget** | Unknown until late in sales cycle | Often disclosed (ceiling values, estimated ranges) |

**Never confuse a Demand Receipt with a Pain Receipt.** A Pain Receipt represents an unvalidated expression of need. A Demand Receipt represents a **statutorily-mandated, publicly-documented, competitively-structured procurement action** backed by appropriated federal dollars. It is more rigorous, more structured, and more verifiable than any commercial Pain Receipt -- but it is also less flexible, less negotiable, and subject to hard deadlines that cannot be extended by relationship-building.

---

## III. TERM DEFINITIONS

---

### AGENCY_NEED_SIGNAL

**Definition:** The underlying requirement expressed by a federal agency within a procurement notice. It is the translation of policy mandate, mission gap, or operational deficiency into a structured statement of need.

**Vocabulary Connection:**
```
AGENCY_NEED_SIGNAL  =  Federal analog of  OFFENSE_SIGNAL
```

The OFFENSE_SIGNAL is the threat, vulnerability, or risk that creates demand for a DEFENSE_FIXER. The AGENCY_NEED_SIGNAL is the same threat, vulnerability, or risk -- but expressed through the lens of federal mission requirements, compliance obligations, and appropriated budgets.

**Examples from Research:**
- *"DIA needs a mature AI TEVV capability for the entire Defense Intelligence Enterprise -- standardized metrics, continuous automated testing, trustworthiness demonstration, and cross-domain validation."* (Pod 04, DIA TEVV RFI)
- *"Army requires certified cybersecurity professionals (CISSP, Security+, CASP+) for direct RMF lifecycle support."* (Pod 05, Army RMF Support)
- *"HUD OCDO requires support for activities under the 2018 Foundations for Evidence-Based Policymaking Act (Evidence Act)."* (Pod 06, HUD eDARMS)

**Usage in Records:**
```
agency_need_signal: "NRC needs cybersecurity assessment for AI/ML-integrated
                     reactor systems in nuclear regulatory context"
```

**Quality Standard:** An AGENCY_NEED_SIGNAL must be extracted from the agency's own words in the procurement notice, NOT inferred or extrapolated. If the curator adds interpretation, it must be flagged in brackets.

---

### DEMAND_RECEIPT

**Definition:** A verified procurement notice published by a federal agency on SAM.gov (or successor system) that documents a formal expression of acquisition need. It is the federal equivalent of a validated sales opportunity.

**Vocabulary Connection:**
```
DEMAND_RECEIPT  =  Federal analog of  PAIN_RECEIPT
                   BUT WITH CRITICAL DISTINCTIONS (see Section II above)
```

The PAIN_RECEIPT is a raw, unvalidated signal of customer distress. The DEMAND_RECEIPT is a **published, statutorily-compliant procurement notice** that has already cleared internal agency review, budgeting, and acquisition planning. It is PAIN_RECEIPT plus federal procedural rigor.

**Taxonomy of Demand Receipts (by Notice Type):**

| Notice Type | Federal Classification | Curator Classification | Typical Action Window |
|-------------|----------------------|----------------------|----------------------|
| Presolicitation / Sources Sought | Market research | `future_watch` | 6-18 months |
| Request for Information (RFI) | Market research | `future_watch` | 6-12 months |
| Special Notice | Agency announcement | `future_watch` or `human_review_required` | Varies |
| Solicitation / RFP / RFQ | Active procurement | `active_response_target` | 15-90 days |
| Combined Synopsis/Solicitation | Active procurement | `active_response_target` | 15-60 days |
| Award Notice | Contract executed | `award_receipt` | Monitor for recompete |
| Justification (J&A) | Sole source justification | `human_review_required` | Varies |

**Usage in Records:**
```
demand_receipt_id: "31310026R0012"
demand_receipt_type: "Solicitation"
demand_receipt_status: "ACTIVE"
demand_receipt_deadline: "2026-05-26"
```

**Quality Standard:** A Demand Receipt is only valid if it includes a SAM.gov URL, a notice ID, and a published date. Demand Receipts without source URLs are **NOT ACTIONABLE** and must be flagged for `human_review_required`.

---

### DEFENDABLE_FIXER_MATCH

**Definition:** The mapping between an AGENCY_NEED_SIGNAL and a specific DefendableOS product or service offering. It answers the question: "Which DefendableOS product fixes this agency's problem?"

**Vocabulary Connection:**
```
DEFENDABLE_FIXER_MATCH  =  Direct mapping of  DEFENSE_FIXER  to  AGENCY_NEED_SIGNAL
```

The DEFENSE_FIXER is the commercial product or service that resolves the OFFENSE_SIGNAL. The DEFENDABLE_FIXER_MATCH is the same product -- but positioned to address the specific federal requirement documented in the AGENCY_NEED_SIGNAL.

**Scoring Scale (1-10):**

| Score | Label | Meaning |
|-------|-------|---------|
| 10 | Perfect Match | Product capability directly, explicitly, and uniquely addresses every stated requirement |
| 8-9 | Strong Match | Product capability directly addresses most requirements; minor gaps manageable |
| 6-7 | Good Match | Product addresses core requirements; some gaps require augmentation or partnership |
| 4-5 | Partial Match | Product tangentially addresses requirements; significant adaptation needed |
| 1-3 | Weak Match | Product has theoretical applicability but requires heavy repositioning |
| 0 | No Match | Product does not address any stated requirement |

**Examples from Research:**
- DIA AI TEVV RFI -> DefendableOS AI TEVV Ledger = **10/10** (explicit TEVV requirement)
- Army RMF Support -> DefendableOS Cyber Defense Ledger = **9/10** (RMF lifecycle is core capability)
- NRC Cyber/AI Reactors -> DefendableOS AI TEVV Ledger = **7/10** (cybersecurity for AI/ML systems)
- GSA SmartPay Fraud -> DefendableOS Fraud Signal Ledger = **5/10** (payment fraud is adjacent)

**Usage in Records:**
```
defendable_fixer_match: "DefendableOS Cyber Defense Ledger"
fit_score_1_to_10: 9
justification: "Army explicitly requires RMF lifecycle support, security controls
               implementation, and multi-platform security management -- all
               core capabilities of the Cyber Defense Ledger."
```

**Quality Standard:** Every DEFENDABLE_FIXER_MATCH must include a scored justification. Scores above 7 require evidence from the procurement notice. Scores below 4 should be classified as `not_actionable` unless strategic value justifies pursuit.

---

### BID_PATH

**Definition:** The recommended strategy for pursuing a specific Demand Receipt. It prescribes the contractual mechanism, timing, and positioning approach for DefendableOS to capture the opportunity.

**Vocabulary Connection:**
```
BID_PATH  =  Federal analog of  the commercial sales motion
             (outbound, inbound, partner-led, product-led)
```

In commercial sales, the "path" is the go-to-market strategy for a specific account. In federal procurement, the BID_PATH is the **contractual and procedural strategy** for a specific opportunity.

**Bid Path Taxonomy:**

| Bid Path Code | Label | When to Use | Example |
|---------------|-------|-------------|---------|
| `prime_direct` | Bid directly as prime contractor | Set-aside opportunity where DefendableOS qualifies | Small business set-aside RFP |
| `prime_gwac` | Bid as prime through GWAC task order | DefendableOS holds the GWAC vehicle | Alliant 2, OASIS+ task order |
| `subcontract` | Perform as subcontractor under prime | Large opportunity where DefendableOS lacks scale or past performance | CISA CEEOSS recompete |
| `teaming_agreement` | Formal teaming with another bidder | Opportunity requires combined capabilities | Joint venture for cyber + AI TEVV |
| `sbir` | Submit SBIR/STTR proposal | R&D-focused opportunity; small business eligible | Army AI/ML Open Topic Phase I |
| `ota` | Pursue Other Transaction Agreement | DoD prototype opportunity; non-traditional contractor | DoD CDAO frontier AI |
| `future_watch` | Monitor for active solicitation | Market research phase (RFI, Sources Sought) | DIA TEVV RFI follow-on |
| `award_receipt` | Monitor for recompete or subcontract | Contract already awarded; track for follow-on | USCG $160M RMF award |
| `expired_market_signal` | Documented demand proof; no current action | Solicitation closed; award likely made | DARPA SABER |
| `human_review_required` | Curator cannot determine path | Insufficient information in notice | Limited Sources Justification |
| `not_actionable` | Cannot pursue at this time | DefendableOS does not meet requirements | 8(a) sole source without 8(a) status |

**Usage in Records:**
```
bid_path: "future_watch"
bid_path_rationale: "This RFI signals an upcoming major procurement. DIA explicitly
                     states intent to implement a mature AI TEVV capability.
                     Follow-on solicitation expected within 3-6 months."
```

**Quality Standard:** Every BID_PATH must include a rationale. If the path is `human_review_required` or `not_actionable`, the specific blocker must be documented.

---

### AWARD_RECEIPT

**Definition:** A verified contract award notice published on SAM.gov or USAspending.gov documenting that a federal agency has obligated funds to a specific contractor for a specific scope of work.

**Vocabulary Connection:**
```
AWARD_RECEIPT  =  Federal proof that a  DEMAND_RECEIPT  was resolved with
                  actual spending. It validates the entire demand signal chain.
```

While commercial deals are tracked in CRM as "closed-won," federal awards are published as public records. The AWARD_RECEIPT is the **definitive proof** that an AGENCY_NEED_SIGNAL resulted in actual procurement.

**Components of an Award Receipt:**

| Field | Description | Source |
|-------|-------------|--------|
| Award Notice ID | SAM.gov notice identifier | SAM.gov |
| Contract Number | Official contract number | SAM.gov / USAspending.gov |
| Award Date | Date of award | SAM.gov |
| Awardee | Contractor name and UEI | SAM.gov |
| Award Amount | Ceiling value or obligated amount | SAM.gov / USAspending.gov |
| Contract Vehicle | BPA, IDIQ, GWAC, OTA, standalone | SAM.gov |
| Contract Type | FFP, CPFF, T&M, etc. | SAM.gov |
| Period of Performance | Contract duration | SAM.gov |
| NAICS Code | Industry classification | SAM.gov |

**Award Receipts as Competitive Intelligence:**

Every AWARD_RECEIPT tells DefendableOS:
- **Who won** -- incumbents to monitor and potentially partner with
- **How much** -- budget validation for future recompetes
- **How long** -- when the recompete window opens
- **What vehicle** -- the contract mechanism to target
- **What NAICS** -- the industry codes to register in SAM.gov

**Examples from Research:**

| Award | Agency | Awardee | Amount | Vehicle | Recompete Window |
|-------|--------|---------|--------|---------|-----------------|
| USCG IA/RMF Support | DHS/USCG | ONEOMEGA LLC | $160,000,000 | 8(a) Set-Aside | ~2030 |
| DHS AI/Data Analytics BPA | DHS | Palantir | $1,000,000,000 | BPA | Task orders ongoing |
| DoD CDAO Frontier AI | DoD | Anthropic/Google/OpenAI/xAI | $800,000,000 | OTA | Through 2026 |
| WAEDS | DIA/DTRA | Booz Allen Hamilton | $1,580,000,000 | Alliant 2 | 5-year POP |
| USMC Data Mgmt Cyber | USMC | Lumbee IT Solutions | $99,995,410 | Award | Recompete cycle |

**Usage in Records:**
```
award_receipt_id: "70Z04425DESD40001"
award_agency: "Department of Homeland Security / US Coast Guard"
award_awardee: "ONEOMEGA LLC"
award_amount: 160000000.00
award_vehicle: "8(a) Set-Aside"
award_date: "2025-08-26"
recompete_signal: "MEDIUM -- 5-year contract; recompete expected ~2030"
```

**Quality Standard:** An AWARD_RECEIPT must include a source URL from SAM.gov or USAspending.gov. Ceiling values must be labeled as "ceiling" not "contract value." All award data reflects the status at time of research and must be re-verified before action.

---

### ACTIVE_RESPONSE_TARGET

**Definition:** A Demand Receipt that is currently open for response on SAM.gov -- meaning the response deadline has not passed and the notice status is "Active."

**Vocabulary Connection:**
```
ACTIVE_RESPONSE_TARGET  =  A  DEMAND_RECEIPT  that requires IMMEDIATE action.
                           It is the federal equivalent of a hot commercial
                           opportunity in the final stage of the sales cycle.
```

**Critical Properties:**

| Property | Requirement |
|----------|-------------|
| Status on SAM.gov | Must show "Active" or equivalent |
| Response deadline | Must be in the future (not passed) |
| SAM.gov URL | Must be included and clickable |
| Set-aside eligibility | Must be verified before action |
| Fit score | Must be >= 6/10 to qualify as a target |

**Active Response Targets in This Research:**

| Notice ID | Agency | Title | Deadline | Set-Aside | Fit | Status |
|-----------|--------|-------|----------|-----------|-----|--------|
| 31310026R0012 | NRC | Cybersecurity of Novel Tech - AI/ML Reactors | 2026-05-26 | Small Business | 7/10 | ACTIVE |
| (Special Notice) | USPTO | Cybersecurity and Privacy Support Services | 2026-05-28 | Limited Sources | 5/10 | ACTIVE |
| PANAPG-26-P-0000041835 | Army | Cyber Security Engineering and RMF Support | 2026-05-29 | 8(a) Sole Source | 9/10 | ACTIVE |
| 6913G626QSBIR1 | DOT | SBIR FY2026 Edge AI-V2X Solutions | 2026-05-29 | Small Business | 6/10 | ACTIVE |

**Curator's Warning:** Active Response Targets have **hard deadlines** that cannot be negotiated. The NRC opportunity (due May 26, 2026) is likely expired by the time this document is read. All deadlines must be re-verified on SAM.gov before action.

**Usage in Records:**
```
classification: "ACTIVE_RESPONSE_TARGET"
response_deadline: "2026-05-29"
deadline_status: "URGENT -- 5 days remaining"
eligibility_requirement: "8(a) certified firm with CISSP-cleared personnel"
recommended_action: "Verify 8(a) status; respond immediately if eligible"
```

**Quality Standard:** An ACTIVE_RESPONSE_TARGET classification must be re-verified within 24 hours of action. If the deadline has passed, reclassify as `expired_market_signal` or `award_receipt` depending on outcome.

---

### EXPIRED_MARKET_SIGNAL

**Definition:** A Demand Receipt whose response deadline has passed and which did not result in an award to DefendableOS. It is preserved in the ledger as **proof of market demand** -- evidence that the federal government is actively buying in this capability area.

**Vocabulary Connection:**
```
EXPIRED_MARKET_SIGNAL  =  A  DEMAND_RECEIPT  that is closed but NOT worthless.
                          It is evidence that the market exists, the budget
                          exists, and the agency has a recurring need.
```

Expired Market Signals are **not actionable** for immediate pursuit, but they are **critically valuable** for:
- Proving market demand to investors, partners, and internal stakeholders
- Predicting recompete cycles
- Understanding competitive landscape
- Informing product roadmap priorities
- Building agency-specific pursuit strategies

**Lifecycle of a Demand Receipt:**

```
DEMAND_RECEIPT posted to SAM.gov
         |
         v
[ACTIVE_RESPONSE_TARGET]  -->  Respond before deadline
         |
         | (deadline passes)
         v
[EXPIRED_MARKET_SIGNAL]   -->  Document award outcome
         |
         | (award announced)
         v
[AWARD_RECEIPT]           -->  Monitor for recompete
         |
         | (recompete window)
         v
[FUTURE_WATCH]            -->  Prepare for new solicitation
         |
         v
[ACTIVE_RESPONSE_TARGET]  -->  Cycle repeats
```

**Examples from Research:**

| Opportunity | Agency | Expired | Value | Why It Matters |
|-------------|--------|---------|-------|----------------|
| DIA AI TEVV RFI | DIA | Feb 2026 | TBD | 10/10 fit; signals major upcoming procurement |
| DARPA SABER AI Red Teaming | DARPA | May 2025 | TBD | Premier AI TEVV/safety program; Phase 2 likely |
| IRS Fraud Analytics RFI | IRS | Jun 2025 | TBD | Second consecutive year; signals ongoing program |
| DOE/PNNL AI Data Center | DOE | Apr 2026 | $2B+ | 40MW AI data center for national missions |
| VA Data Governance (12 tasks) | VA | Mar 2022 | TBD | Massive scope; multiple award IDIQ planned |

**Usage in Records:**
```
classification: "EXPIRED_MARKET_SIGNAL"
expired_date: "2026-02-06"
recompete_signal: "HIGH -- DIA explicitly stated intent to implement mature
                   AI TEVV capability. Follow-on expected within 3-6 months."
strategic_value: "Perfect-fit opportunity (10/10). Top priority for
                  future_watch monitoring and agency relationship building."
```

**Quality Standard:** Every EXPIRED_MARKET_SIGNAL must include a `recompete_signal` rating (HIGH / MEDIUM / LOW) and a `strategic_value` statement. If the recompete_signal is HIGH, it must be added to the agency watchlist.

---

### PRIME_PATH

**Definition:** The strategy of bidding directly as the prime contractor on a federal opportunity. The prime holds the contract, manages the relationship with the government, and bears full responsibility for delivery.

**Vocabulary Connection:**
```
PRIME_PATH  =  DefendableOS acts as the  DEFENSE_FIXER  directly,
               with full contractual and delivery responsibility.
```

**Prime Path Requirements:**

| Requirement | When Needed | DefendableOS Status |
|-------------|-------------|-------------------|
| SAM.gov registration (UEI + CAGE) | Always | UNKNOWN |
| Small business self-certification | For set-aside opportunities | UNKNOWN |
| GSA Schedule or GWAC contract | For task order opportunities | UNKNOWN |
| Past performance (1-3 contracts) | For competitive solicitations | ZERO |
| 8(a) / SDVOSB / WOSB certification | For sole source / set-aside pools | UNKNOWN |
| CMMC Level 2 | For DoD cyber contracts | UNKNOWN |
| TS/SCI clearance (firm or personnel) | For IC opportunities | UNKNOWN |

**When to Take the PRIME_PATH:**

- Small business set-aside where DefendableOS qualifies (8/10 fit or higher)
- SBIR/STTR opportunities (Phase I or Direct-to-Phase II)
- GSA Schedule task orders (once on Schedule)
- Sources Sought responses (market research participation)

**Prime Path Scoring:**

| Factor | Score Impact |
|--------|-------------|
| Set-aside eligibility matched | +3 points |
| Fit score >= 8/10 | +2 points |
| Past performance in similar work | +2 points |
| GSA Schedule / GWAC holder | +2 points |
| Within 90 days of SAM registration | +1 point |
| **Minimum to recommend PRIME_PATH** | **6+ points** |

**Usage in Records:**
```
bid_path: "prime_direct"
bid_path_rationale: "Small business set-aside; DefendableOS qualifies as SB
                     in NAICS 541715; fit score 7/10; SAM registration in progress."
prime_path_readiness: "CONDITIONAL -- SAM registration must be active before
                       proposal submission."
```

---

### SUBCONTRACT_PATH

**Definition:** The strategy of performing work as a subcontractor under a prime contractor's federal contract. The prime holds the government contract; DefendableOS delivers specific capabilities as a named or unnamed subcontractor.

**Vocabulary Connection:**
```
SUBCONTRACT_PATH  =  DefendableOS provides  DEFENSE_FIXER  capabilities
                     through a partner's contract vehicle, building past
                     performance while the prime manages the government
                     relationship.
```

**Subcontract Path Advantages:**

| Advantage | Explanation |
|-----------|-------------|
| **No SAM registration required** | Prime handles government interface |
| **No past performance required** | Prime's past performance satisfies the requirement |
| **No GSA Schedule required** | Prime's vehicle is used |
| **Faster revenue** | Can start within weeks of teaming agreement |
| **Capability building** | Learn federal delivery requirements |
| **Relationship building** | Build agency visibility and trust |

**Subcontract Path Disadvantages:**

| Disadvantage | Explanation |
|--------------|-------------|
| **Lower margins** | Prime takes overhead and fee (typically 5-15%) |
| **Less control** | Prime manages government relationship |
| **No direct past performance** | May not be credited as prime contractor |
| **Dependent on prime** | Revenue tied to prime's contract health |

**When to Take the SUBCONTRACT_PATH:**

- DefendableOS has zero federal past performance (current state)
- Opportunity is large ($10M+) where scale is required
- Opportunity requires clearances or certifications DefendableOS lacks
- Opportunity is a recompete with established incumbent
- DefendableOS needs to build federal delivery capability

**Target Prime Contractors for Subcontracting:**

| Prime | Relevant Contracts | Why Partner |
|-------|-------------------|-------------|
| Booz Allen Hamilton | WAEDS $1.58B, CDC DMAC $234M | Largest AI contractor; AI TEVV gap in portfolio |
| Palantir | DHS BPA $1B, Project Maven $1.3B+ | Platform-focused; needs governance/TEVV overlay |
| SoKat LLC | Treasury AI $50M, GSA AI Challenge | 8(a) small business; complementary capabilities |
| Aquia Inc. | VA NAII $11.4M, fraud detection | SDVOSB; health AI and fraud focus |
| Lumbee IT Solutions | USMC Data Mgmt $100M | Small business; data + cyber integration |

**Usage in Records:**
```
bid_path: "subcontract"
bid_path_rationale: "DefendableOS has zero federal past performance. CISA CEEOSS
                     recompete requires established enterprise IT delivery.
                     Recommend teaming with incumbent (Sev1Tech) or competing
                     prime for AI governance subcontractor role."
target_prime: "Sev1Tech LLC (incumbent) or competing CEEOSS bidder"
subcontract_role: "AI governance and continuous monitoring capabilities"
```

---

### PARTNER_PATH

**Definition:** The strategy of forming a formal partnership (joint venture, mentor-protege, or teaming agreement) with another entity to pursue federal opportunities. It differs from subcontracting in that the partnership is **bidirectional and opportunity-specific**.

**Vocabulary Connection:**
```
PARTNER_PATH  =  Two or more entities combine their  DEFENSE_FIXER
                 capabilities to create a stronger combined offering
                 than either could provide alone.
```

**Partnership Mechanisms:**

| Mechanism | Structure | Best For |
|-----------|-----------|----------|
| **Teaming Agreement** | Letter of intent to pursue specific opportunity | Pre-proposal alignment |
| **Joint Venture (JV)** | New legal entity combining partners | Large set-aside opportunities |
| **Mentor-Protege Program** | SBA-sanctioned large + small business relationship | Capability development |
| **Contractor Team Arrangement (CTA)** | GSA Schedule-specific teaming | GSA Schedule task orders |
| **Consortium Membership** | OTA-style collaboration (e.g., LETHA) | R&D and prototype opportunities |

**When to Take the PARTNER_PATH:**

- Opportunity requires capabilities across multiple DefendableOS lanes
- JV eligibility unlocks set-aside opportunities (e.g., SDVOSB JV)
- Mentor-protege relationship accelerates capability development
- OTA consortium membership provides access to non-traditional procurement

**Usage in Records:**
```
bid_path: "partner_path"
partner_mechanism: "joint_venture"
partner_target: "SDVOSB-qualified firm for VA opportunities"
partner_rationale: "VA sets aside ~40% of IT opportunities for SDVOSB.
                    DefendableOS lacks SDVOSB status. JV with SDVOSB
                    partner unlocks $8.5B annual SDVOSB spending pool."
```

---

### HUMAN_REVIEW_REQUIRED

**Definition:** A classification flag indicating that automated or algorithmic processing cannot determine the correct action for a Demand Receipt. A human curator must review the record before it can be promoted to LEDGER_READY status.

**Vocabulary Connection:**
```
HUMAN_REVIEW_REQUIRED  =  The federal equivalent of a sales opportunity
                          that cannot be auto-scored and requires sales
                          engineering or executive review.
```

**Triggers for HUMAN_REVIEW_REQUIRED:**

| Trigger | Example |
|---------|---------|
| Notice type is ambiguous | "Special Notice" with no clear action |
| Set-aside status is unclear | "Limited Sources" without justification |
| Fit score is borderline (5-6/10) | Product applicability is uncertain |
| Award amount is not disclosed | Cannot assess opportunity value |
| Contract vehicle is unusual | OTA, CSO, or other non-standard mechanism |
| Requirements appear contradictory | Notice includes both services and products |
| Deadline is not specified | Open-ended RFI with no response date |
| Agency is not a standard buyer | First-time procurement from unexpected agency |

**Usage in Records:**
```
classification: "HUMAN_REVIEW_REQUIRED"
review_trigger: "Limited Sources Justification -- unable to determine
                set-aside eligibility or incumbent status from
                publicly available information."
recommended_reviewer: "Federal BD Lead"
review_deadline: "2026-05-27"
```

**Quality Standard:** Every HUMAN_REVIEW_REQUIRED record must include a `review_trigger`, a `recommended_reviewer`, and a `review_deadline`. Records in this status for more than 7 days must be escalated.

---

### NOT_ACTIONABLE

**Definition:** A classification flag indicating that a Demand Receipt cannot be pursued by DefendableOS at this time due to a blocking requirement that cannot be overcome in the available timeframe.

**Vocabulary Connection:**
```
NOT_ACTIONABLE  =  The federal equivalent of a "dead" sales opportunity.
                   It is preserved in the ledger for competitive
                   intelligence but requires no action.
```

**Common NOT_ACTIONABLE Blockers:**

| Blocker | Explanation | Mitigation |
|---------|-------------|------------|
| **8(a) sole source** | Requires 8(a) certification DefendableOS lacks | Apply for 8(a) (9-month process) |
| **Expired deadline** | Response deadline has passed | Monitor for amendment or recompete |
| **Incumbent advantage** | Sole source justification names incumbent | Monitor for full-and-open recompete |
| **Clearance requirement** | Requires TS/SCI or higher | Build uncleared capabilities first |
| **CMMC Level 3+** | Requires advanced cybersecurity certification | Start CMMC Level 2 journey |
| **GSA Schedule required** | Opportunity only open to Schedule holders | Apply for GSA MAS |
| **Large business only** | No small business set-aside | Partner as subcontractor |
| **Overseas performance** | Requires OCONUS delivery capability | Evaluate capability |

**Usage in Records:**
```
classification: "NOT_ACTIONABLE"
actionability_blocker: "8(a) Sole Source -- DefendableOS does not hold
                        8(a) certification."
mitigation_path: "Assess 8(a) eligibility. If eligible, initiate
                  application (6-9 month process). Add to watchlist
                  for recompete as full-and-open or SDVOSB set-aside."
watchlist_priority: "MEDIUM"
```

**Quality Standard:** Every NOT_ACTIONABLE record must include a `mitigation_path`. If there is no path to actionability, the record is classified as `REJECTED` and archived.

---

### LEDGER_READY_DEMAND_RECEIPT

**Definition:** A Demand Receipt that has passed ALL quality gates and is ready for promotion to the Defendable Ledger. It is the highest-quality classification in the federal opportunity lifecycle.

**Vocabulary Connection:**
```
LEDGER_READY_DEMAND_RECEIPT  =  The federal equivalent of a  PAIN_RECEIPT
                                that has been fully qualified, scored, and
                                approved for active pursuit. It maps
                                directly to the  DEFENDABLE_LEDGER.
```

**Quality Gates (ALL must pass):**

| Gate | Requirement | Verification |
|------|-------------|--------------|
| **Q1: Source Verified** | SAM.gov URL or USAspending.gov URL included | Clickable, live link |
| **Q2: Identity Verified** | Notice ID + solicitation number + agency confirmed | Matches SAM.gov record |
| **Q3: Status Verified** | Active status and deadline confirmed on SAM.gov | Within 24 hours of action |
| **Q4: Need Signal Extracted** | AGENCY_NEED_SIGNAL documented with agency's own words | Not inferred or extrapolated |
| **Q5: Fixer Match Scored** | DEFENDABLE_FIXER_MATCH scored 1-10 with justification | Score >= 6 for ledger-ready |
| **Q6: Bid Path Assigned** | BID_PATH assigned with rationale | Not `human_review_required` |
| **Q7: Eligibility Verified** | Set-aside requirements checked against DefendableOS status | SAM registration confirmed |
| **Q8: Deadline Actionable** | Response deadline is in the future OR recompete is tracked | Not expired without follow-up |
| **Q9: No Duplicate** | Not already recorded in the ledger with same notice ID | Deduplication check passed |
| **Q10: Tribunal Review** | Final curator sign-off with confidence statement | Verdict assigned |

**Ledger-Ready Classification Hierarchy:**

```
ALL 10 GATES PASSED
         |
         v
+-----------------------------+
| LEDGER_READY_DEMAND_RECEIPT |  -->  Promote to DEFENDABLE_LEDGER
|     (HONEY classification)  |
+-----------------------------+
         |
    +----+----+
    |         |
    v         v
+-------+  +-------+
| PRIME |  | SUB / |
| PATH  |  | PARTNER|
+-------+  +-------+
```

**Usage in Records:**
```
ledger_status: "LEDGER_READY"
quality_gates: "10/10 PASSED"
tribunal_verdict: "HONEY"
classification: "ACTIVE_RESPONSE_TARGET"
bid_path: "prime_direct"
ledger_ready_date: "2026-05-24"
promoted_by: "Defendable Tribunal Curator"
```

**Quality Standard:** A Demand Receipt is ONLY promoted to LEDGER_READY when all 10 gates pass. Any gate failure results in classification as `HUMAN_REVIEW_REQUIRED` or `NOT_ACTIONABLE`. No record may be promoted to the Defendable Ledger without Tribunal sign-off.

---

## IV. VOCABULARY CONNECTION MAP

### How Federal Terms Map to Core Defendable Vocabulary

```
CORE DEFENDABLE VOCABULARY          FEDERAL VOCABULARY ADDENDUM
+-------------------+               +-------------------------+
|                   |               |                         |
|  OFFENSE_SIGNAL   |  <------->   |  AGENCY_NEED_SIGNAL     |
|  (Threat/risk     |   Maps to    |  (Federal agency's      |
|   creating need)  |               |   stated requirement)   |
|                   |               |                         |
+-------------------+               +-------------------------+
          |                                    |
          v                                    v
+-------------------+               +-------------------------+
|                   |               |                         |
|  PAIN_RECEIPT     |  <------->   |  DEMAND_RECEIPT         |
|  (Customer's      |   Maps to    |  (SAM.gov procurement   |
|   expression of   |    BUT       |   notice)               |
|   need/pain)      |   DISTINCT   |                         |
|                   |               |                         |
+-------------------+               +-------------------------+
          |                                    |
          v                                    v
+-------------------+               +-------------------------+
|                   |               |                         |
|  DEFENSE_FIXER    |  <------->   |  DEFENDABLE_FIXER_MATCH |
|  (Product/service |   Maps to    |  (Scored product-       |
|   that resolves   |               |   to-need mapping)      |
|   the pain)       |               |                         |
|                   |               |                         |
+-------------------+               +-------------------------+
          |                                    |
          v                                    v
+-------------------+               +-------------------------+
|                   |               |                         |
|  DEFENDABLE_LEDGER|  <------->   |  LEDGER_READY_DEMAND_   |
|  (The system of   |   Maps to    |  RECEIPT                |
|   record)         |               |  (Qualified federal     |
|                   |               |   opportunity ready     |
|                   |               |   for ledger)           |
+-------------------+               +-------------------------+
```

### Bid Path Decision Tree

```
                    DEMAND_RECEIPT received
                           |
                           v
              +------------------------+
              |  Is DefendableOS       |
              |  SAM-registered?       |
              +------------------------+
                     |           |
                     | NO        | YES
                     v           v
              +----------+  +------------------+
              | NOT_     |  | Is opportunity   |
              | ACTION-  |  | a set-aside?     |
              | ABLE     |  | (SB, 8(a), SDVOSB|
              | (Block:  |  | WOSB, HUBZone)?  |
              |  SAM reg)|  +------------------+
              +----------+        |        |
                                  | NO     | YES
                                  v        v
                            +---------+  +------------------+
                            | Does    |  | Does DefendableOS|
                            | oppty   |  | qualify for the  |
                            | require |  | set-aside?       |
                            | GWAC or |  +------------------+
                            | Schedule|       |        |
                            | vehicle?|       | NO     | YES
                            +---------+       v        v
                               | |       +---------+ +---------+
                               | |       | PARTNER | | PRIME   |
                               | |       | PATH    | | PATH    |
                    +----------+ +--+    +---------+ +---------+
                    |             |
                    | YES         | NO
                    v             v
              +---------+   +------------------+
              | Is      |   | Is fit score     |
              | Defend- |   | >= 8/10?         |
              | ableOS  |   +------------------+
              | on the  |        |        |
              | vehicle?|        | NO     | YES
              +---------+        v        v
                 | |        +---------+ +---------+
                 | |        | SUBCON- | | PRIME   |
                 | |        | TRACT   | | PATH    |
                 | |        | PATH    | |         |
        +--------+ +-----+  +---------+ +---------+
        |               |
        | NO            | YES
        v               v
   +---------+     +---------+
   | PARTNER |     | PRIME   |
   | PATH    |     | (GWAC   |
   | (Get on |     |  task   |
   | vehicle)|     |  order) |
   +---------+     +---------+
```

---

## V. CLASSIFICATION QUICK REFERENCE

### Verdict Classifications (Tribunal-Level)

| Classification | Definition | Action |
|----------------|-----------|--------|
| **HONEY** | Verified, sourced, actionable demand. Ready for pursuit. | Promote to ledger; assign bid path; execute |
| **JELLY** | Partial or incomplete data. Needs more research before action. | Flag for follow-up research; set review deadline |
| **PROPOLIS** | Interesting but not actionable at this time. May become actionable later. | Archive; add to watchlist; review quarterly |
| **REJECTED** | No demand found, demand is fabricated, or opportunity is permanently blocked. | Archive; do not pursue; document reason |

### Action Classifications (Operational-Level)

| Classification | Definition | Action |
|----------------|-----------|--------|
| **RESPOND FIRST** | Active opportunities exist; respond immediately. | Execute bid path; meet deadlines |
| **BUILD FIRST** | Prerequisites required before any bidding. | Complete SAM registration, certifications, GSA Schedule |
| **PARTNER FIRST** | Subcontracting or teaming is the recommended path. | Identify prime partners; execute teaming agreements |
| **NEVER CLAIM WITHOUT PROOF** | Certain claims are prohibited until independently verified. | See Limitations section of Executive Verdict |

### Demand Receipt Status Classifications

| Classification | Definition |
|----------------|-----------|
| **ACTIVE_RESPONSE_TARGET** | Open for response; deadline in the future; action required |
| **FUTURE_WATCH** | Market research phase (RFI, Sources Sought); monitor for solicitation |
| **AWARD_RECEIPT** | Contract awarded; monitor for recompete or subcontract |
| **EXPIRED_MARKET_SIGNAL** | Deadline passed; preserved as demand proof; track recompete |
| **HUMAN_REVIEW_REQUIRED** | Curator cannot determine classification; requires manual review |
| **NOT_ACTIONABLE** | Blocking requirement prevents pursuit; document mitigation path |
| **LEDGER_READY** | All quality gates passed; ready for Defendable Ledger |

---

## VI. USAGE EXAMPLES

### Example 1: Complete Opportunity Record Using Federal Vocabulary

```yaml
# DIA AI TEVV Capability RFI
# Classification: EXPIRED_MARKET_SIGNAL -> FUTURE_WATCH

ledger_record_id: "FED-2026-001"

demand_receipt:
  notice_id: "(blank -- Special Notice)"
  title: "AI Test, Evaluation, Verification, and Validation (TEVV) Capability RFI"
  agency: "Defense Intelligence Agency"
  notice_type: "Special Notice"
  posted_date: "2026-01-12"
  response_deadline: "2026-02-06"
  active_status: "EXPIRED"
  sam_url: "https://sam.gov/workspace/contract/opp/d91ada1a22074523a8cc9b2c970f9b9c/view"
  tribunal_verified: true

agency_need_signal:
  extracted_text: "DIA seeks concepts providing enterprise-level standardization
                  and flexibility for mission-specific validation. DIA seeks
                  automated TEVV capabilities for continuous testing throughout
                  AI lifecycle. Solutions must span NIPRNET, SIPRNET, JWICS."
  curator_interpretation: "[CURATOR: DIA needs a comprehensive AI TEVV platform
                          with cross-domain security and continuous automated
                          testing across classification levels.]"

defendable_fixer_match:
  product: "DefendableOS AI TEVV Ledger"
  fit_score: 10
  justification: "Explicit match for automated AI testing, evaluation,
                 verification, validation with audit trails and
                 cross-domain documentation."

bid_path:
  classification: "future_watch"
  rationale: "RFI stage signals upcoming major procurement. Follow-on
              solicitation expected within 3-6 months."
  recommended_action: "Monitor SAM.gov weekly. Build DIA contracting office
                      relationship. Prepare capability statement."

expired_market_signal:
  expired_date: "2026-02-06"
  recompete_signal: "HIGHEST"
  strategic_value: "Perfect-fit opportunity. DIA is the Intelligence Community's
                   primary AI TEVV buyer. This RFI is the precursor to a
                   major multi-year contract."

tribunal_verdict: "HONEY"
quality_gates: "10/10 PASSED"
ledger_status: "LEDGER_READY"
```

### Example 2: Active Opportunity Using Federal Vocabulary

```yaml
# Army Cyber Security Engineering and RMF Support
# Classification: ACTIVE_RESPONSE_TARGET

ledger_record_id: "FED-2026-002"

demand_receipt:
  notice_id: "PANAPG-26-P-0000041835"
  title: "Cyber Security Engineering and Risk Management Framework Support Services"
  agency: "Department of the Army"
  notice_type: "Sources Sought"
  posted_date: "2026-05-14"
  response_deadline: "2026-05-29"
  active_status: "ACTIVE"
  set_aside: "8(a) Sole Source"
  sam_url: "https://sam.gov/workspace/contract/opp/743b8cad81004f2fb91acbf41e195a24/view"
  tribunal_verified: true

agency_need_signal:
  extracted_text: "Contractor shall provide Cybersecurity Engineering and DoD
                  Risk Management Framework (RMF) Support Services. Requires
                  IT Solutions Architect Sr with CISSP certification and 5+
                  years managing RMF lifecycle."
  curator_interpretation: "[CURATOR: Army needs comprehensive RMF lifecycle
                          support with certified personnel. Direct match
                          for DefendableOS Cyber Defense Ledger plus
                          cleared staffing capability.]"

defendable_fixer_match:
  product: "DefendableOS Cyber Defense Ledger"
  fit_score: 9
  justification: "Direct RMF engineering support requirement. DoD security
                 controls implementation, multi-platform security management,
                 and continuous monitoring are core capabilities."

bid_path:
  classification: "human_review_required"
  blocker: "8(a) sole source -- DefendableOS 8(a) status unknown"
  mitigation: "Verify 8(a) eligibility immediately. If eligible, respond
               by May 29. If not eligible, classify as NOT_ACTIONABLE
               and add to watchlist for full-and-open recompete."

active_response_target:
  deadline_urgency: "CRITICAL -- 5 days remaining"
  eligibility_gate: "8(a) certification"
  recommended_action: "URGENT: Verify 8(a) status. If qualified, respond
                      immediately as this is the highest-fit active
                      opportunity in the entire research set."

tribunal_verdict: "HONEY"
quality_gates: "9/10 PASSED (Q7 pending 8(a) verification)"
ledger_status: "CONDITIONALLY LEDGER READY -- PENDING 8(a) STATUS"
```

---

## VII. COMPLIANCE AND GOVERNANCE

### Record-Keeping Requirements

1. **Every Demand Receipt** must include a SAM.gov or USAspending.gov URL
2. **Every AGENCY_NEED_SIGNAL** must be sourced from the agency's own words
3. **Every DEFENDABLE_FIXER_MATCH** must include a scored justification
4. **Every BID_PATH** must include a rationale with actionable next steps
5. **Every classification change** must be timestamped and attributed
6. **Every AWARD_RECEIPT** must distinguish ceiling value from obligated amount
7. **No claim of federal contract award** may be made without Tribunal verification

### Prohibited Claims (Enforced by Tribunal)

The following claims are **STRICTLY PROHIBITED** in any DefendableOS communication until verified:

- "DefendableOS has federal contracts" -- UNPROVEN
- "$12.5B addressable market" -- MISLEADING (use "$12.5B in identified awards")
- "Federal agencies are buying DefendableOS" -- FALSE
- "DefendableOS is GSA Schedule approved" -- UNPROVEN until awarded
- "DefendableOS qualifies for 8(a) set-asides" -- UNPROVEN until certified
- "X opportunity is guaranteed" -- NEVER (federal procurement is competitive)

### Review Cycle

This vocabulary addendum shall be reviewed:
- After every major policy update (EO, OMB memo, NIST standard)
- After every Tribunal verdict that introduces new classifications
- Quarterly at minimum
- Upon curator request when edge cases emerge

---

## VIII. APPENDIX: ACRONYMS AND REFERENCES

| Acronym | Definition |
|---------|------------|
| 8(a) | SBA Business Development Program |
| BPA | Blanket Purchase Agreement |
| CAGE | Commercial and Government Entity Code |
| CTA | Contractor Team Arrangement |
| CDAO | Chief Digital and Artificial Intelligence Office |
| CMMC | Cybersecurity Maturity Model Certification |
| DIA | Defense Intelligence Agency |
| FAR | Federal Acquisition Regulation |
| GWAC | Government-Wide Acquisition Contract |
| HUBZone | Historically Underutilized Business Zone |
| IDIQ | Indefinite Delivery / Indefinite Quantity |
| JV | Joint Venture |
| MAS | Multiple Award Schedule |
| NAICS | North American Industry Classification System |
| NIST | National Institute of Standards and Technology |
| OMB | Office of Management and Budget |
| OSDBU | Office of Small and Disadvantaged Business Utilization |
| OTA | Other Transaction Agreement |
| RFI | Request for Information |
| RFP | Request for Proposal |
| RFQ | Request for Quotation |
| RMF | Risk Management Framework |
| SAM | System for Award Management |
| SBIR | Small Business Innovation Research |
| SDVOSB | Service-Disabled Veteran-Owned Small Business |
| SIPRNET | Secret Internet Protocol Router Network |
| TEVV | Test, Evaluation, Verification, and Validation |
| TS/SCI | Top Secret / Sensitive Compartmented Information |
| UEI | Unique Entity Identifier |
| USCYBERCOM | US Cyber Command |
| WOSB | Women-Owned Small Business |

---

*End of Federal Vocabulary Addendum*

*Authority: Defendable Tribunal Curator, Federal Demand Intelligence Division*
*Effective Date: 2026-05-24*
*Version: 1.0*
*File: /mnt/agents/output/federal/01_FEDERAL_VOCABULARY_ADDENDUM.md*
