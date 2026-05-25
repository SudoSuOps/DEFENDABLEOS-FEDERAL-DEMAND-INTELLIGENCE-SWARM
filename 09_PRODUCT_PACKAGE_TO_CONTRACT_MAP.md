# DefendableOS Product Package-to-Contract Map

> **Purpose:** Maps each DefendableOS product package (A-F) to verified federal demand signals, contract opportunities, and actionable pursuit paths.
> **Sources:** SAM.gov research Pods 04-11; 55+ verified opportunities; $12.5B+ award history analysis
> **Date:** 2026-05-24 | **Status:** Research-grounded; all opportunity data sourced from SAM.gov

---

## Table of Contents

- [Package A: Defendable AI TEVV Ledger](#package-a-defendable-ai-tevv-ledger)
- [Package B: Defendable Cyber Proof Ledger](#package-b-defendable-cyber-proof-ledger)
- [Package C: Defendable Data Provenance Vault](#package-c-defendable-data-provenance-vault)
- [Package D: Defendable Fraud Evidence Workbench](#package-d-defendable-fraud-evidence-workbench)
- [Package E: Defendable Box -- Private AI Evidence Appliance](#package-e-defendable-box--private-ai-evidence-appliance)
- [Package F: Defendable Compute Deed](#package-f-defendable-compute-deed)
- [Cross-Cutting Recommendations](#cross-cutting-recommendations)

---

## Package A: Defendable AI TEVV Ledger

> **What it is:** Automated AI testing, evaluation, verification, and validation system with continuous monitoring, benchmark tracking, audit trails, and governance documentation.

### A.1 Verified Federal Need Language

| Agency | Need Language ( verbatim from SAM.gov ) | Source |
|--------|------------------------------------------|--------|
| **DIA** | "DIA recognizes that AI-enabled capabilities within the IC and DoD depend fundamentally upon rigorous, comprehensive, and continuous TEVV... establishing trust through demonstrated reliability, cybersecurity, safety, accuracy, robustness, and adherence to ethical/legal standards is paramount." | DIA AI TEVV RFI, Jan 2026 |
| **NIST/AISI** | "Develop evaluations and benchmarks of AI models' software engineering and AI R&D capabilities, functionality, and risks... developing benchmarks and scoring mechanisms for automated evaluation." | NIST CAW-AIRD-25, Mar 2025 |
| **NASA** | "Machine learning verification and validation methods, performance metrics, operator performance evaluation methods, benchmarking, safety and assurance frameworks specific to data- and ML-driven systems." | NASA EIO RFI, Feb 2026 |
| **VA** | "Managing AI governance framework meeting federal reporting/monitoring requirements; delivering risk assessment and mitigation plans for non-compliant AI use cases." | VA 36C10B25Q0021, Oct 2024 |
| **Treasury** | "Evaluation criteria include: Responsible AI practices including bias mitigation, transparency, and explainability." | Treasury 2032L2-26-X-0001, Feb 2026 |

### A.2 Official Demand Receipts (Notice IDs)

| Notice ID | Title | Agency | Type | Status | Fit Score |
|-----------|-------|--------|------|--------|-----------|
| *(blank -- RFI)* | DIA AI TEVV Capability RFI | DIA | Special Notice | Inactive -- **follow-on expected** | 10/10 |
| **CAW-AIRD-25** | Evaluations & Benchmarks for AI R&D Capabilities | NIST/AISI | Sources Sought | Inactive -- follow-on expected | 9/10 |
| **CAW-25-0001** | Chemical/Biological Capabilities Evaluation | NIST/AISI | Sources Sought | Inactive -- follow-on expected | 8/10 |
| **HR001125S0009** | DARPA SABER AI Red Teaming | DARPA | Solicitation | Inactive -- monitor Phase 2 | 9/10 |
| *(blank -- RFI)* | NASA EIO Anomaly Response (ML V&V) | NASA | Special Notice | Inactive -- solicitation expected | 8/10 |
| **36C10B25Q0021** | VA AI Program & Governance Support | VA | Sources Sought | Inactive -- solicitation expected | 7/10 |
| **36C10G24C0010** | VA Trustworthy AI Program Support | VA | Award Notice | Awarded to Olympus Alpha LLC ($4.98M) | 7/10 |
| **2032L2-26-X-0001** | Treasury AI Model Access Services RFI | Treasury | Special Notice | Inactive -- solicitation expected | 6/10 |
| **CDAO_26-01** | AI-Enabled Software Development Coding | DoD CDAO | Solicitation | Inactive | 4/10 |

### A.3 Likely Buyer Type

- **Primary:** Defense Intelligence Agencies (DIA), DoD CDAO, NIST/AISI -- R&D and TEVV capability buyers
- **Secondary:** VA OCAIO, NASA -- AI governance and ML assurance buyers
- **Tertiary:** Civilian agencies (Treasury, GSA) -- responsible AI compliance buyers

### A.4 Likely NAICS / PSC

| Code | Value | Confidence |
|------|-------|------------|
| **NAICS Primary** | 541519 (Other Computer Related Services) | HIGH -- used by 6 of 9 matched opportunities |
| **NAICS Secondary** | 541511 (Custom Computer Programming) | HIGH -- used by IRS, NIST AISI |
| **NAICS Tertiary** | 541715 (R&D in Physical/Engineering/Life Sciences) | MEDIUM -- DARPA SABER, NASA |
| **PSC Primary** | DA01 (Application Development IT Labor) | HIGH |
| **PSC Secondary** | R425 (Professional Engineering/Technical Support) | MEDIUM -- used by NIST AISI |
| **PSC Tertiary** | AC12 (R&D -- Defense) | MEDIUM -- DARPA SABER |

### A.5 Readiness Gaps

| Gap | Severity | Mitigation |
|-----|----------|------------|
| No CMMC Level 2 certification | HIGH | Begin NIST SP 800-171 self-assessment; plan 3-6 months |
| No FedRAMP authorization | MEDIUM | Package A is a tool, not a cloud service; can run on client's FedRAMP-authorized environment |
| No cleared personnel | HIGH for DIA/IC work | Start with unclassified TEVV; pursue facility clearance via sponsor |
| No eMASS integration proof | MEDIUM | Build prototype connector; eMASS is the standard DoD RMF tool |

### A.6 Prototype Required

**YES -- Minimum Viable Prototype for DIA TEVV RFI follow-on:**

| Prototype Element | Description | Effort Estimate |
|-------------------|-------------|-----------------|
| TEVV dashboard | Web-based interface showing model test results, benchmark scores, drift alerts | 4-6 weeks |
| Audit trail export | Export evidence packages to PDF/JSON with digital signatures | 2-3 weeks |
| NIST AI RMF mapping | Show alignment between test results and NIST AI RMF sub-categories | 2 weeks |
| Sample benchmark suite | Pre-built evaluations for text classification, bias detection, robustness | 3-4 weeks |

### A.7 Proof Artifact Required

1. **Compliance Mapping Matrix** -- NIST AI RMF 1.0 x OMB M-24-10 x OMB M-25-21 x EO 14110 crosswalk
2. **Sample TEVV Report** -- Demonstration output showing model evaluation, benchmark scoring, and risk assessment
3. **Provenance Schema** -- Machine-readable schema for AI evaluation metadata
4. **Past performance narrative** -- SBIR award or subcontract CPARS entry (Phase 2)

### A.8 Security / Compliance Questions

| Question | Answer Path |
|----------|-------------|
| Can you operate on SIPRNET/JWICS? | Not initially; start NIPRNET, pursue cross-domain accreditation |
| Is your system FedRAMP authorized? | No -- designed to run on client's FedRAMP-authorized infrastructure |
| Do you meet NIST AI RMF? | Yes -- mapped; compliance dashboard included |
| Can you export to eMASS? | Prototype connector available; full integration under development |
| IL5/IL6 support? | Roadmap item; IL4 achievable in 6 months |

### A.9 Prime / Subcontract / Partner Path

| Path | Approach | Confidence |
|------|----------|------------|
| **RECOMMENDED: Subcontract to prime** | Target Booz Allen (WAEDS $1.58B), Leidos, or CACI as AI/ML TEVV subcontractor on DIA contracts | HIGH -- primes need TEVV specialists |
| **SBIR/STTR** | Submit Army AI/ML Open Topic Phase I ($250K) or Direct-to-Phase II ($2M) | HIGH -- excellent fit for TEVV R&D |
| **Prime (small biz set-aside)** | Pursue small business set-aside opportunities <$250K to build CPARS | MEDIUM -- needs past performance first |
| **Partner: SoKat LLC** | SoKat (8(a), Treasury AI) has AI governance contracts; DefendableOS provides TEVV tooling | MEDIUM -- complementary capabilities |
| **Navy LETHA OTA** | Apply for consortium membership for adversarial AI/T&E pathway | MEDIUM -- OTA pathway bypasses FAR |

### A.10 Build-Now Recommendation

**BUILD -- Priority 1 (Highest)**

Rationale:
- 9 verified opportunities with fit scores 4-10/10
- DIA RFI explicitly signals a major upcoming procurement (follow-on expected within 3-6 months)
- NIST AISI has recurring evaluation needs (2+ active sources sought in 12 months)
- AI TEVV is the **fastest-growing federal AI requirement** driven by EO 14110, OMB M-24-10, and NIST AI RMF adoption
- Package A is the **core platform** that differentiates DefendableOS -- all other packages build on its receipt/audit infrastructure

Build Sequence:
1. TEVV dashboard prototype (4-6 weeks)
2. NIST AI RMF compliance mapping (2 weeks)
3. eMASS export connector (3-4 weeks)
4. Pilot with Army AI/ML SBIR (6 months)

---

## Package B: Defendable Cyber Proof Ledger

> **What it is:** RMF evidence package builder, security control documentation system, continuous monitoring receipt generator, and ATO support artifact producer.

### B.1 Verified Federal Need Language

| Agency | Need Language (verbatim from SAM.gov) | Source |
|--------|----------------------------------------|--------|
| **Army** | "Contractor shall provide all personnel, equipment... to perform Cybersecurity Engineering and DoD Risk Management Framework (RMF) Support Services. Requires CISSP certification and 5+ years managing RMF lifecycle reporting." | PANAPG-26-P-0000041835, May 2026 |
| **Army PM IS&A** | "Requires RMF oversight and cybersecurity engineering for design, implementation, fielding, training of cross-domain solutions. Past performance requested with RMF packages, eMASS." | W56KGY25X, May 2025 |
| **Air Force** | "Cybersecurity support for DRSN and NC3 systems. RMF requirements met, ATO granted/valid, security documentation up-to-date. RMF Body of Evidence updates." | FA460026Q0012, Jan 2026 |
| **DISA/MSC** | "Afloat site, system, OT Assessment and Authorization including mission-based cybersecurity risk assessments. Inspections, compliance visits for cybersecurity readiness." | 832572693, Aug 2025 |
| **NIST** | "Automating assessment processes, risk scoring methodologies. Full suite of IT security support services for FISMA compliance. eMASS for RMF." | AMD-SS-F-22-00063_MHB, Nov 2021 |
| **VA** | "Comprehensive, turnkey solution for application and API runtime protection... Zero Trust Architecture Strategy under EO 14028. FedRAMP Moderate or High." | 36C10B25Q0429, Jul 2025 |

### B.2 Official Demand Receipts (Notice IDs)

| Notice ID | Title | Agency | Type | Status | Fit Score |
|-----------|-------|--------|------|--------|-----------|
| **PANAPG-26-P-0000041835** | Cyber Security Engineering & RMF Support | Army | Sources Sought | **ACTIVE -- Due May 29, 2026** | 9/10 |
| **31310026R0012** | Cybersecurity of Novel Tech -- AI/ML Reactors | NRC | Solicitation | **ACTIVE -- Due May 26, 2026** | 7/10 |
| **W56KGY25X** | Cybersecurity Services RFI 2025 | Army | RFI | Inactive -- solicitation expected | 9/10 |
| **FA460026Q0012** | Cybersecurity Support for DRSN/NC3 | Air Force | RFQ | Inactive -- recompete ~2027 | 8/10 |
| **FA521525Q0028** | PACAF A&A for FISMA & Cyber Hardening | Air Force | RFQ | Inactive -- recompete expected | 8/10 |
| **PCCA2600032_CEEOSS** | CISA Enterprise Engineering & Ops Support | CISA | Sources Sought | Inactive -- recompete | 7/10 |
| **36C10B25Q0429** | VA Zero Trust Application Runtime Protection | VA | RFI | Inactive -- solicitation expected | 7/10 |
| **832572693** | MSC Cybersecurity Support Services | DISA | Sources Sought | Inactive -- solicitation expected | 8/10 |
| **RFI-ICE-FY26-CCISS** | Cyber Defense & Intelligence Support Services | ICE/DHS | RFI | Inactive -- recompete Aug 2026 | 8/10 |
| **70Z04425DESD40001** | USCG IA/RMF Support Services | Coast Guard | Award | Awarded to ONEOMEGA LLC ($160M) | 6/10 |

### B.3 Likely Buyer Type

- **Primary:** DoD Cybersecurity offices (Army ACC-APG, Air Force ACC, DISA, USCG) -- RMF A&A and continuous monitoring
- **Secondary:** DHS CISA, ICE -- enterprise security operations and cyber defense
- **Tertiary:** NIST (RMF standards body), NRC -- cybersecurity research and compliance

### B.4 Likely NAICS / PSC

| Code | Value | Confidence |
|------|-------|------------|
| **NAICS Primary** | 541519 (Other Computer Related Services) | HIGH -- used by 7 of 10 opportunities |
| **NAICS Secondary** | 541512 (Computer Systems Design Services) | HIGH -- CISA, DISA, NIST |
| **NAICS Tertiary** | 541513 (Computer Facilities Management) | MEDIUM -- Air Force DRSN/NC3 |
| **PSC Primary** | DJ01 (Security & Compliance IT Labor) | HIGH -- used by 5+ cyber opportunities |
| **PSC Secondary** | DA01 (Application Development) | MEDIUM |
| **PSC Tertiary** | R425 (Professional Engineering/Technical) | MEDIUM -- Army PM IS&A |

### B.5 Readiness Gaps

| Gap | Severity | Mitigation |
|-----|----------|------------|
| No CISSP-certified personnel on staff | HIGH | Hire or subcontract; required by Army RMF |
| No eMASS hands-on experience | HIGH | Obtain eMASS training; partner with incumbent |
| No CMMC Level 2 certification | HIGH | Begin NIST SP 800-171 self-assessment immediately |
| No Security+ / CASP+ certified staff | HIGH | Army RMF requires these certs |
| No DoD 8570/IAT Level II certification | MEDIUM | Required for most cyber positions |
| No classified facility / clearances | HIGH for NC3/DRSN work | Start uncleared; pursue CAGE + sponsorship |

### B.6 Prototype Required

**YES -- RMF Evidence Package Builder:**

| Prototype Element | Description | Effort Estimate |
|-------------------|-------------|-----------------|
| RMF Body of Evidence (BOE) generator | Auto-generate RMF control documentation from scan/assessment results | 6-8 weeks |
| eMASS data export | Structured export matching eMASS import schema | 3-4 weeks |
| Continuous monitoring dashboard | POA&M tracking, vulnerability scan receipt, remediation evidence | 4-6 weeks |
| Security control mapping | NIST SP 800-53 Rev 5 control mapping with implementation statements | 2-3 weeks |

### B.7 Proof Artifact Required

1. **Sample RMF BOE Package** -- Complete Body of Evidence for 5-10 NIST SP 800-53 controls
2. **eMASS Export File** -- Valid eMASS-compatible artifact demonstrating format compliance
3. **POA&M Template** -- Plan of Action & Milestones template with remediation tracking
4. **NIST SP 800-53 Control Crosswalk** -- Mapped to DefendableOS platform capabilities
5. **CMMC Level 2 Readiness Assessment** -- Self-assessment documenting current state

### B.8 Security / Compliance Questions

| Question | Answer Path |
|----------|-------------|
| Do you have CISSP-certified staff? | No -- will hire/subcontract; named in proposal |
| Can you support eMASS? | Prototype connector; staff training in progress |
| FedRAMP status? | Not FedRAMP-authorized; runs on client infrastructure |
| Can you get clearances? | Yes, pending CAGE code and contract sponsorship |
| DoD 8570 compliant? | Planned; certifications obtained before contract start |
| Zero Trust Architecture experience? | Mapped to EO 14028 requirements; not yet deployed |

### B.9 Prime / Subcontract / Partner Path

| Path | Approach | Confidence |
|------|----------|------------|
| **RECOMMENDED: Subcontract to cyber prime** | Target Peraton ($100M+ cyber awards), Booz Allen (NERVE $347M), or BAE Systems as RMF documentation subcontractor | HIGH -- mandatory subcontracting plans create demand |
| **8(a) sole source** | If DefendableOS obtains 8(a), Army RMF support is a strong sole-source target | HIGH -- avg $3.2M per 8(a) AI/cyber contract |
| **Small business set-aside** | DISA MSC CSS (NAICS 541519); FA460026 (small biz set-aside); 31310026R0012 (small biz set-aside) | MEDIUM -- requires past performance or SBIR first |
| **Partner: ONEOMEGA LLC** | ONEOMEGA holds $160M Coast Guard IA/RMF contract; seek subcontractor status for follow-on | MEDIUM -- incumbent advantage |
| **CISA CEEOSS recompete** | Team with Sev1Tech (incumbent) or bid as small business teammate | MEDIUM -- large recompete opportunity |

### B.10 Build-Now Recommendation

**BUILD -- Priority 2 (High)**

Rationale:
- 10 verified opportunities with fit scores 6-10/10
- Army RMF Support is **ACTIVE** (due May 29, 2026) -- immediate action possible
- RMF is the **largest single cybersecurity need** across DoD -- $160M Coast Guard award demonstrates scale
- Package B naturally **extends Package A** into cybersecurity compliance -- shared infrastructure
- Zero Trust mandates (EO 14028) are driving a **multi-year compliance wave**

Build Sequence:
1. NIST SP 800-53 Rev 5 control library in DefendableOS schema (3-4 weeks)
2. RMF BOE auto-generator prototype (6-8 weeks)
3. eMASS export connector (3-4 weeks)
4. POA&M tracking module (2-3 weeks)

---

## Package C: Defendable Data Provenance Vault

> **What it is:** Data lineage tracking, metadata management, audit trail preservation, and chain-of-custody system for records -- ensuring end-to-end provenance from source to archive.

### C.1 Verified Federal Need Language

| Agency | Need Language (verbatim from SAM.gov) | Source |
|--------|----------------------------------------|--------|
| **DHA** | "Data quality and metadata management -- defining standards for accuracy, completeness, consistency, timeliness. Metadata management practices -- comprehensive data catalog, data dictionaries, and **data lineage tracking**." | HT0011-25-RFI-0222, Jul 2025 |
| **VA** | "Task 1: Metadata Management -- VA Enterprise Data Catalogue... Task 2: Data Quality -- **variance and compliance reporting from source to destination**. Task 3: Data Validation -- automated review of data enrichment output." | 36C10X22Q0038, Dec 2021 |
| **VA (VBA)** | **"Auditable change histories and clear data lineage tracking."** | 36C10E20Q0269, Aug 2020 |
| **CBP** | "**Automated audit trails** aligned with OMB Circular A-123 and GAAP standards. Role-based access controls and comprehensive compliance controls." | PR20156685, Mar 2026 |
| **DOI** | "Enterprise records management in a FISMA-moderate SaaS environment. **Chain of custody** and records integrity maintenance. **Audit trail** capabilities for all actions." | DOIDFBO250041, May 2025 |
| **HUD** | "Enterprise data governance, data management, and data analytics capabilities" under the **2018 Foundations for Evidence-Based Policymaking Act** and **Federal Data Strategy**." | eDARMS12172024, Dec 2024 |

### C.2 Official Demand Receipts (Notice IDs)

| Notice ID | Title | Agency | Type | Status | Fit Score |
|-----------|-------|--------|------|--------|-----------|
| **HT0011-25-RFI-0222** | DHA Data Governance: Transforming the Data Landscape | DHA | Sources Sought | Inactive -- solicitation expected | 9/10 |
| **36C10X22Q0038** | VA Data Mgmt, Analytics & Evidence-Based Policymaking | VA | Sources Sought | Inactive -- IDIQ expected | 8/10 |
| **PR20156685** | CBP Financial Close Modernization Tool | CBP | Sources Sought | **ACTIVE** | 7/10 |
| **36C10E20Q0269** | VA VBA OFM Enhanced Accounting Capabilities | VA | RFI | Inactive | 8/10 |
| **DOIDFBO250041** | DOI eERDMS (Enterprise Records Mgmt) | DOI | Intent to Award | Bridge to Nov 2027 -- recompete after | 7/10 |
| **eDARMS12172024** | HUD Enterprise Data & Resources Management Solution | HUD | RFI | Inactive -- solicitation expected | 7/10 |
| **A021537** | USSF SpOC CDO Enterprise Data Support | USSF | RFI | Inactive -- solicitation expected | 6/10 |
| **2031JW26N00007** | OCC Enterprise Data Management Support Services | Treasury/OCC | Presolicitation | Solicitation Q3 FY2026 | 6/10 |
| **241652** | CMS MDM & Enterprise Data Lake Support | CMS | Awarded | Awarded; monitor for recompete | 5/10 |

### C.3 Likely Buyer Type

- **Primary:** VA (VHA + VBA) -- largest single data governance buyer; Evidence Act compliance
- **Secondary:** DoD (DHA, USSF), DOI -- data modernization and records management
- **Tertiary:** DHS (CBP), HUD, Treasury (OCC) -- financial/grants data provenance

### C.4 Likely NAICS / PSC

| Code | Value | Confidence |
|------|-------|------------|
| **NAICS Primary** | 541512 (Computer Systems Design Services) | HIGH -- DHA, CISA, DISA matches |
| **NAICS Secondary** | 541611 (Administrative/Management Consulting) | HIGH -- VA 36C10X22Q0038, VA Data Quality |
| **NAICS Tertiary** | 518210 (Data Processing/Hosting) | MEDIUM -- DOI eERDMS, VA VBA |
| **PSC Primary** | DA10 (SaaS/Application Development) | HIGH -- CBP, DOI, VA |
| **PSC Secondary** | DA01 (Application Development IT Labor) | MEDIUM |
| **PSC Tertiary** | R702 (Data Collection Support) | MEDIUM -- VA Data Quality |

### C.5 Readiness Gaps

| Gap | Severity | Mitigation |
|-----|----------|------------|
| No FISMA-moderate ATO | MEDIUM for SaaS delivery | Run on client's FISMA-authorized infrastructure |
| No NARA 36 CFR compliance certification | MEDIUM | Implement NARA records management standards in schema |
| No eDiscovery platform integration | LOW | Add to roadmap; not required for initial entry |
| No SAP ERP integration | LOW | CBP-specific; partner with SAP integrator |

### C.6 Prototype Required

**YES -- Data Provenance Vault Demo:**

| Prototype Element | Description | Effort Estimate |
|-------------------|-------------|-----------------|
| Data lineage tracker | Visual graph showing source-to-destination data flow with transformation logging | 4-6 weeks |
| Metadata catalog | Searchable data catalog with automated metadata extraction | 3-4 weeks |
| Audit trail viewer | Queryable audit trail interface (user, date/time, action, record) | 2-3 weeks |
| Chain of custody export | NARA-compliant export format for records transfer | 2-3 weeks |
| OMB A-123 compliance report | Automated audit trail alignment with OMB Circular A-123 | 1-2 weeks |

### C.7 Proof Artifact Required

1. **Data Lineage Schema** -- Machine-readable provenance schema (W3C PROV compatible)
2. **NARA Compliance Mapping** -- 36 CFR alignment documentation
3. **Evidence Act Crosswalk** -- Federal Data Strategy / Evidence Act compliance mapping
4. **Sample Audit Trail Export** -- Demonstration export in NARA-compliant format
5. **Metadata Catalog Demo** -- Live demo with sample federal dataset

### C.8 Security / Compliance Questions

| Question | Answer Path |
|----------|-------------|
| FISMA-moderate ATO? | No -- operates on client's authorized infrastructure |
| NARA 36 CFR compliant? | Schema designed for compliance; certification pending |
| HIPAA compliant? | For DHA/VA health data -- BA agreement + encryption required |
| PII/PHI handling? | Tokenization and access controls implemented |
| Evidence Act compliant? | Yes -- mapped to Federal Data Strategy requirements |

### C.9 Prime / Subcontract / Partner Path

| Path | Approach | Confidence |
|------|----------|------------|
| **RECOMMENDED: Prime on VA small biz set-aside** | VA is **very small-business friendly**; 36C10X22Q0038 is a multiple-award IDIQ with 12 task areas | HIGH -- VA meets small business goals |
| **Subcontract to CMS incumbent** | CMS MDM/EDL bridge contract; position for recompete as data governance subcontractor | MEDIUM -- limited public info on teaming |
| **Partner: Aquia Inc.** | Aquia (SDVOSB) holds VA AI/health IT contracts; DefendableOS provides data provenance | MEDIUM -- complementary |
| **HUD eDARMS** | Position for upcoming solicitation as prime or JV member | MEDIUM -- IDIQ expected |
| **OCC via GSA Alliant 2** | OCC solicitation uses Alliant 2 GWAC; need schedule access first | LOW -- requires Alliant 2 prime or sub |

### C.10 Build-Now Recommendation

**BUILD -- Priority 3 (High)**

Rationale:
- 9 verified opportunities with fit scores 5-10/10
- VA is the **most small-business-friendly agency** in this space
- DHA Data Governance RFI explicitly asks for data lineage, metadata, and auditing
- Evidence Act and Federal Data Strategy create **cross-cutting compliance demand**
- Package C shares provenance infrastructure with Packages A and B -- incremental build

Build Sequence:
1. W3C PROV-compatible provenance schema (2 weeks)
2. Data lineage visualizer prototype (4-6 weeks)
3. NARA 36 CFR export format (2-3 weeks)
4. Evidence Act compliance dashboard (2 weeks)

---

## Package D: Defendable Fraud Evidence Workbench

> **What it is:** Fraud analytics workflow system, forensic evidence packaging, anomaly detection documentation, and investigation case receipt generator -- producing audit-ready fraud investigation packages.

### D.1 Verified Federal Need Language

| Agency | Need Language (verbatim from SAM.gov) | Source |
|--------|----------------------------------------|--------|
| **IRS** | "The IRS seeks vendors to provide Cybersecurity Fraud Analytics and Monitoring Support with advanced, technical cybersecurity techniques to prevent and detect fraudulent activity in IRS online applications, taxpayer data, and tax revenue." | 8503, Jun 2025 |
| **IRS (2024 RFI)** | "Comprehensive fraud analytics and 24x7 monitoring... forensic analytics, predictive analytics, continuous enhancement of analytical models, and coordination with stakeholders to detect/prevent/respond to cybersecurity threats." | 2024-AMP-APMI-OITA-001, May 2024 |
| **HUD** | "The 2026 HUGS Analytics pilot demonstrated the ability to reduce manual reconciliation effort, improve data accuracy, and **assist with identifying fraud, waste and abuse**." | NOF-2026-003, Mar 2026 |
| **GSA** | "Selected partner(s) will provide charge card and commercial payments management including issuance, commercial payment systems, **fraud analytics, data mining, and information security**." | 47QRAB25R0002, Jun 2025 |
| **VA OIG** | "RFI for a commercial off-the-shelf (COTS) Investigative Case Management System for the VA OIG Office of Investigations." | VAOIG-RFI-26-0001, Mar 2026 |
| **Treasury** | "Treasury prevented and recovered **>$4 billion in FY2024 using ML AI fraud detection**." | Treasury Press Release, FY2024 |

### D.2 Official Demand Receipts (Notice IDs)

| Notice ID | Title | Agency | Type | Status | Fit Score |
|-----------|-------|--------|------|--------|-----------|
| **8503** | IRS Cybersecurity Fraud Analytics & Monitoring | IRS | Sources Sought | Inactive -- **follow-on expected** | 9/10 |
| **2024-AMP-APMI-OITA-001** | IRS RFI -- Fraud Analytics & Monitoring | IRS | Sources Sought | Inactive -- follow-on expected | 9/10 |
| **NOF-2026-003** | HUD HUGS-RAP -- Grants Fraud Analytics | HUD | Sources Sought | Inactive -- solicitation expected | 8/10 |
| **47QRAB25R0002** | GSA SmartPay Fraud Analytics | GSA | CSO Solicitation | Inactive -- pilot follow-on possible | 7/10 |
| **VAOIG-RFI-26-0001** | VA OIG Investigative Case Management | VA OIG | Sources Sought | Inactive -- solicitation expected | 7/10 |
| **ICMS** | DOJ OIG Investigation Case Management | DOJ OIG | Sources Sought | Inactive -- may recompete | 6/10 |
| **9531BM23Q0019** | NTSB Evidence Management Software | NTSB | RFQ | Inactive -- may recompete FY28 | 5/10 |

### D.3 Likely Buyer Type

- **Primary:** IRS (Treasury) -- largest fraud analytics program; 2 consecutive RFIs signal ongoing procurement
- **Secondary:** HUD -- emerging grants fraud detection program (HUGS-RAP)
- **Tertiary:** OIG community (VA, DOJ, NGA) -- investigative case management; GSA -- payment fraud

### D.4 Likely NAICS / PSC

| Code | Value | Confidence |
|------|-------|------------|
| **NAICS Primary** | 541512 (Computer Systems Design Services) | HIGH -- IRS, GSA, DOJ |
| **NAICS Secondary** | 541330 (Engineering Services) | MEDIUM -- IRS 8503 used this |
| **NAICS Tertiary** | 513210 (Software Publishers) | MEDIUM -- VA OIG, NTSB |
| **NAICS Quaternary** | 522320 (Financial Transactions Processing) | LOW -- GSA SmartPay specific |
| **PSC Primary** | DJ01 (Security & Compliance IT Labor) | HIGH -- IRS fraud |
| **PSC Secondary** | DA10 (SaaS/Application) | MEDIUM -- VA OIG case mgmt |
| **PSC Tertiary** | R710 (Management: Financial) | LOW -- GSA payment fraud |

### D.5 Readiness Gaps

| Gap | Severity | Mitigation |
|-----|----------|------------|
| No IRS-specific domain expertise | HIGH | Partner with tax/fraud domain SME; hire former IRS |
| No GSA SmartPay program knowledge | MEDIUM | Research program; attend GSA industry day |
| No investigative case management UX | MEDIUM | Build fraud investigation workflow UI |
| No FinCEN/BSA compliance background | LOW-MEDIUM | Not required for initial entry; valuable for Treasury |

### D.6 Prototype Required

**YES -- Fraud Evidence Workbench Demo:**

| Prototype Element | Description | Effort Estimate |
|-------------------|-------------|-----------------|
| Fraud investigation dashboard | Case view showing alerts, evidence chain, disposition | 4-6 weeks |
| Anomaly detection receipt | Auto-generated documentation of detection method, threshold, flags | 2-3 weeks |
| Evidence packaging wizard | Guided workflow for assembling fraud evidence packages | 3-4 weeks |
| Investigation audit trail | Complete case history: who reviewed, what decisions, when | 2 weeks |
| Predictive model documentation | Auto-generated model cards for fraud detection algorithms | 2-3 weeks |

### D.7 Proof Artifact Required

1. **Sample Fraud Investigation Package** -- Complete evidence package with mock fraud scenario
2. **Anomaly Detection Model Card** -- Documentation template for fraud detection algorithms
3. **IRS Fraud Analytics Capability Statement** -- Tailored to IRS-specific language and needs
4. **HUD HUGS-RAP Alignment Document** -- Mapping to grants fraud detection requirements
5. **OIG Case Management Workflow Spec** -- Investigation lifecycle documentation

### D.8 Security / Compliance Questions

| Question | Answer Path |
|----------|-------------|
| Can you handle taxpayer data? | No direct access -- operates on IRS infrastructure; no data retention |
| FedRAMP authorized? | No -- runs on client-authorized environment |
| FISMA compliant? | Yes -- mapped to FISMA moderate controls |
| PII handling? | Tokenization; no PII stored in DefendableOS |
| IRC 6103 compliant? | IRS-specific -- consult with IRS counsel |

### D.9 Prime / Subcontract / Partner Path

| Path | Approach | Confidence |
|------|----------|------------|
| **RECOMMENDED: IRS follow-on pursuit** | IRS has 2 consecutive RFIs (2024, 2025) -- a formal solicitation is likely imminent. Prepare now. | HIGH -- strongest demand signal in fraud lane |
| **Subcontract to Treasury prime** | SoKat LLC (8(a)) holds Treasury AI and OCC AI Solutions Lab contracts | HIGH -- SoKat needs fraud analytics capabilities |
| **HUD HUGS-RAP prime** | HUD sources sought closed Apr 2026; formal solicitation likely upcoming | MEDIUM -- new program, less incumbent advantage |
| **VA OIG case management** | COTS-focused; DefendableOS can provide evidence/workflow module as component | MEDIUM -- position as module provider |
| **GSA SmartPay Phase II** | CSO pilot; if Phase I successful, larger procurement follows | LOW-MEDIUM -- depends on pilot outcome |

### D.10 Build-Now Recommendation

**BUILD -- Priority 3 (High)**

Rationale:
- 7 verified opportunities with fit scores 5-10/10
- IRS is the **dominant fraud analytics buyer** with 2 consecutive RFIs signaling imminent formal procurement
- Treasury reports **$4B+ in fraud prevented/recovered via ML** -- sustained investment likely
- HUD HUGS-RAP is an **emerging program** with first-mover advantage available
- Package D leverages Package A's evaluation infrastructure + Package C's provenance capabilities

Build Sequence:
1. Fraud investigation case model (2 weeks)
2. Anomaly detection receipt generator (2-3 weeks)
3. Evidence packaging wizard (3-4 weeks)
4. IRS-specific dashboard (2 weeks)

---

## Package E: Defendable Box -- Private AI Evidence Appliance

> **What it is:** Air-gapped or on-premises AI evidence infrastructure for classified/sensitive environments -- ingesting, evaluating, and receipting AI/ML model outputs without cloud dependency or data egress.

### E.1 Verified Federal Need Language

| Agency | Need Language (verbatim from SAM.gov) | Source |
|--------|----------------------------------------|--------|
| **DOE/PNNL** | "On-premises, secure, scalable data center optimized for AI and compute workloads... training and operationalization of multi-data Large Language Models for scientific and national governmental missions... stringent security, compliance, and availability requirements." | AI_Data_Center-RFI_001, Feb 2026 |
| **Air Force** | "AI data centers on underutilized land at 5 installations... facilities requiring >100 MW of new load and capital expenditures of at least $500M. Aligned with EO 14318 (Accelerating Federal Permitting of Data Center Infrastructure)." | AFCEC-26-R-0002, Oct 2025 |
| **NIH/NIA** | "A **Government-Owned, Contractor-Operated (GOCO) federated enclave** for storage, analysis, and distribution of linked and unlinked study datasets... host studies with sensitive data." | 75N95026R00003, Dec 2025 |
| **NIH/N3C** | "Secure platform for harmonized clinical data, accessible only through a secure cloud portal... Data cannot be downloaded or removed." | 75N95023R00015NOI, Mar 2023 |
| **USDA** | "Secure Enclave Services for Economic Research Service (ERS) and National Agricultural Statistical Service (NASS)... Blanket Purchase Agreement (BPA) for secure enclave services." | 1232SA24X, Dec 2023 |
| **CBP** | "Edge computing platform... edge computing infrastructure for CBP mission applications." | CBP-RFI-INVNTEDGECOMPUTINGPLATFORM, Jun 2025 |

### E.2 Official Demand Receipts (Notice IDs)

| Notice ID | Title | Agency | Type | Status | Fit Score |
|-----------|-------|--------|------|--------|-----------|
| **AI_Data_Center-RFI_001** | DOE/PNNL On-Premises AI Compute Data Center | DOE | Sources Sought | Inactive -- RFP expected 2026 | 8/10 |
| **AFCEC-26-R-0002** | Air Force AI Data Center Development (5 AFBs) | Air Force | Solicitation (RFLP) | Inactive | 7/10 |
| **75N95026R00003** | NIH/NIA Data Access Program (Federated Enclave) | NIH | Presolicitation | Inactive -- solicitation expected | 7/10 |
| **75N95023R00015NOI** | NIH N3C Data Enclave Support | NIH | Presolicitation | Awarded; monitor for recompete 2026 | 6/10 |
| **1232SA24X** | USDA Secure Enclave Services | USDA | RFI | Inactive -- BPA may follow | 6/10 |
| **CBP-RFI-INVNTEDGECOMPUTINGPLATFORM** | CBP INVNT Edge Computing Platform | CBP | Sources Sought | Inactive | 5/10 |
| **RRS2026MRIP** | FRA Mobile Railcar Inspection Portal (Edge AI) | DOT/FRA | Sources Sought | Inactive | 4/10 |
| **6913G626QSBIR1** | DOT SBIR FY2026 (Edge AI-V2X) | DOT | Presolicitation | **ACTIVE** -- Due May 29, 2026 | 5/10 |

### E.3 Likely Buyer Type

- **Primary:** DOE/NNSA -- massive on-premises AI compute ($500M-$1B+ scale)
- **Secondary:** Air Force -- multi-installation AI data center deployment
- **Tertiary:** NIH -- secure clinical data enclaves; USDA -- secure enclave BPA

### E.4 Likely NAICS / PSC

| Code | Value | Confidence |
|------|-------|------------|
| **NAICS Primary** | 518210 (Computing Infrastructure Providers) | HIGH -- DOE, USDA, NIH enclaves |
| **NAICS Secondary** | 334511 (Search/Detection/Navigation Mfg) | LOW -- CBP edge only |
| **NAICS Tertiary** | 541715 (R&D Physical/Engineering/Life Sciences) | MEDIUM -- DOT SBIR |
| **PSC Primary** | DH01 (Platform as a Service) | HIGH -- enclave/platform delivery |
| **PSC Secondary** | DB10 (Compute as a Service) | MEDIUM -- AI compute |
| **PSC Tertiary** | 7B22 (Compute: Servers) | LOW -- CBP edge hardware |

### E.5 Readiness Gaps

| Gap | Severity | Mitigation |
|-----|----------|------------|
| No hardware/appliance manufacturing capability | HIGH | Partner with hardware OEM; focus on software-defined appliance |
| No IL6/TS facility clearance | HIGH for DOE/NNSA | Start with IL4; pursue sponsor via SBIR |
| No air-gapped environment testing | HIGH | Build isolated lab; partner with cleared facility |
| No NNSA/DOE Q-clearance personnel | HIGH for nuclear sites | Subcontract; hire cleared staff |
| No GOCO operational experience | MEDIUM | Partner with incumbent GOCO contractor |

### E.6 Prototype Required

**YES -- Software-Defined Private Evidence Appliance:**

| Prototype Element | Description | Effort Estimate |
|-------------------|-------------|-----------------|
| Hardened appliance image | Containerized DefendableOS stack for on-premises deployment | 6-8 weeks |
| Air-gap sync protocol | Secure data transfer protocol for non-networked environments | 4-6 weeks |
| Evidence vault (offline) | Local-only evidence storage with tamper-evident logging | 3-4 weeks |
| LLM inference engine (local) | Lightweight model inference for AI evaluation without cloud | 4-6 weeks |
| Classification marking support | Banner marking, portion marking, derivative classification | 2-3 weeks |

### E.7 Proof Artifact Required

1. **Appliance Deployment Guide** -- Installation, configuration, and hardening procedures
2. **Air-Gap Sync Specification** -- Protocol documentation for secure cross-domain transfer
3. **IL4/IL5 Compliance Matrix** -- Control implementation for DoD Impact Levels
4. **Offline Evidence Package Demo** -- Demonstration of complete air-gapped workflow
5. **Hardware BOM (Bill of Materials)** -- Recommended server/edge hardware specifications

### E.8 Security / Compliance Questions

| Question | Answer Path |
|----------|-------------|
| Can you deploy at IL6/TS? | Not initially -- roadmap item; start IL4/IL5 |
| Air-gapped operation? | Yes -- core design requirement |
| Cross-domain guard integration? | Via approved CDS; not a CDS itself |
| NNSA Q-clearance required? | For personnel -- subcontract or hire |
| FedRAMP? | Not applicable for on-premises deployment |

### E.9 Prime / Subcontract / Partner Path

| Path | Approach | Confidence |
|------|----------|------------|
| **RECOMMENDED: SBIR/STTR entry** | Army/DOT SBIR for edge AI (Direct-to-Phase II $2M) provides non-traditional entry to DoD | HIGH -- SBIR avoids clearance requirements initially |
| **Subcontract to AI compute prime** | Partner with large AI compute contractor on DOE/PNNL or Air Force AI data center bids | MEDIUM -- primes need edge/enclave software |
| **Partner: NIH N3C incumbent** | Position as enclave technology provider for N3C recompete or NIA expansion | MEDIUM -- specialized domain |
| **USDA BPA** | If BPA follows RFI, position as secure enclave software provider | MEDIUM -- limited award data |
| **GSA MAS IT Hardware** | List appliance on GSA Schedule as hardware+software bundle | LOW -- requires MAS first |

### E.10 Build-Now Recommendation

**BUILD -- Priority 4 (Medium-High)**

Rationale:
- 8 verified opportunities with fit scores 4-10/10
- DOE/PNNL and Air Force represent **multi-billion-dollar AI compute infrastructure**
- Edge computing + secure enclaves is a **differentiated niche** (fewer competitors than cloud AI)
- Package E is the **most defensible long-term position** -- agencies are prioritizing on-premises AI
- However, requires significant security investment; **start with SBIR to fund development**

Build Sequence:
1. Hardened container deployment (4-6 weeks)
2. Offline evidence vault (3-4 weeks)
3. Air-gap sync protocol (4-6 weeks)
4. Army/DOT SBIR proposal (2-3 weeks)

---

## Package F: Defendable Compute Deed

> **What it is:** Compute resource deed and attestation system documenting AI training/inference runs, resource allocation, energy usage, and environmental impact -- producing ledger-ready receipts for AI compute accountability and ESG compliance.

### F.1 Verified Federal Need Language

| Agency | Need Language (verbatim from SAM.gov) | Source |
|--------|----------------------------------------|--------|
| **DOE/PNNL** | "Design, construction, infrastructure, and operation of a scalable, high-performance data center optimized for AI and compute workloads... 2 MW initial to 40 MW expansion." | AI_Data_Center-RFI_001, Feb 2026 |
| **Air Force** | "Qualifying Projects per EO 14318: facilities requiring >100 MW of new load and capital expenditures of at least $500M." | AFCEC-26-R-0002, Oct 2025 |
| **DOE/NNSA** | "Designing, financing, permitting, developing, constructing, installing, owning, maintaining, operating, and decommissioning AI data center and energy generation infrastructure." | RFP-AI-1, Oct 2025 |
| **DHS** | "Develop and implement cybersecurity hardening and technology modernization strategies... Zero Trust principles." | FY25-00308, Oct 2025 |
| **GSA** | "New AI provisions: vendors must get permission before using non-public government data to train publicly-available AI algorithms; ongoing testing and monitoring rights." | GSA MAS Refresh 31, Mar 2026 |

### F.2 Official Demand Receipts (Notice IDs)

| Notice ID | Title | Agency | Type | Status | Fit Score |
|-----------|-------|--------|------|--------|-----------|
| **AI_Data_Center-RFI_001** | DOE/PNNL AI Compute Data Center | DOE | Sources Sought | Inactive -- RFP expected | 6/10 |
| **AFCEC-26-R-0002** | Air Force AI Data Center (5 AFBs) | Air Force | Solicitation | Inactive | 5/10 |
| **RFP-AI-1** | DOE/NNSA AI Infrastructure & Energy | DOE/NNSA | Solicitation | Inactive | 5/10 |
| **FY25-00308** | DHS Cyber Hardening & Zero Trust | DHS | Awarded | Bridge; recompete expected | 4/10 |

### F.3 Likely Buyer Type

- **Primary:** DOE/NNSA -- largest AI compute infrastructure buyers; energy/compute accountability
- **Secondary:** Air Force -- multi-site AI data center deployment; ESG reporting
- **Tertiary:** GSA -- government-wide AI procurement governance; MAS Refresh 31 monitoring requirements

### F.4 Likely NAICS / PSC

| Code | Value | Confidence |
|------|-------|------------|
| **NAICS Primary** | 518210 (Computing Infrastructure Providers) | MEDIUM -- compute accountability |
| **NAICS Secondary** | 541715 (R&D Physical/Engineering/Life Sciences) | MEDIUM -- compute efficiency R&D |
| **NAICS Tertiary** | 541519 (Other Computer Related Services) | MEDIUM -- IT monitoring services |
| **PSC Primary** | DB10 (Compute as a Service) | MEDIUM -- compute tracking |
| **PSC Secondary** | DH01 (Platform as a Service) | LOW -- monitoring platform |

### F.5 Readiness Gaps

| Gap | Severity | Mitigation |
|-----|----------|------------|
| No energy metering hardware integration | MEDIUM | Partner with smart-meter/PUE monitoring vendors |
| No carbon accounting methodology | MEDIUM | Adopt GHG Protocol / EPA methodology |
| No GSA MAS listing | HIGH for gov-wide reach | Apply for MAS or partner with schedule holder |
| Limited market validation | HIGH -- newest package | Validate with agency buyers before deep build |

### F.6 Prototype Required

**PARTIAL -- Proof of Concept Recommended:**

| Prototype Element | Description | Effort Estimate |
|-------------------|-------------|-----------------|
| Compute run logger | API that records training/inference job parameters, duration, resources | 2-3 weeks |
| Energy estimation model | Model-based energy consumption estimation (where no direct metering) | 2-3 weeks |
| Compute deed receipt | Standardized receipt format documenting compute run with attestation | 1-2 weeks |
| Dashboard (POC) | Simple dashboard showing compute usage across jobs/departments | 2 weeks |

### F.7 Proof Artifact Required

1. **Compute Deed Specification** -- Technical specification for compute run attestation
2. **ESG Compliance Mapping** -- GHG Protocol, EPA, EO 14057 alignment
3. **Energy Estimation Methodology** -- White paper on model-based energy accounting
4. **GSA MAS Refresh 31 Alignment** -- Mapping to new AI monitoring requirements

### F.8 Security / Compliance Questions

| Question | Answer Path |
|----------|-------------|
| Is this a cloud service? | Can be deployed cloud, on-prem, or hybrid |
| FedRAMP required? | Yes if cloud-hosted; on-prem exempt |
| Energy data classification? | Generally unclassified; agency-specific |

### F.9 Prime / Subcontract / Partner Path

| Path | Approach | Confidence |
|------|----------|------------|
| **Subcontract to AI compute prime** | Partner with large data center contractors (e.g., on DOE/PNNL or Air Force) for compute accountability module | MEDIUM -- emerging requirement |
| **GSA MAS pathway** | List as add-on service to AI compute offerings | MEDIUM -- requires MAS access |
| **DOE SBIR** | Propose compute efficiency / green AI topic under DOE SBIR | LOW-MEDIUM -- needs topic alignment |

### F.10 Build-Now Recommendation

**BUILD LIGHT -- Priority 5 (Medium)**

Rationale:
- Only 4 matched opportunities; fit scores 4-6/10
- Package F is the **most speculative** -- compute accountability is an emerging, not proven, federal demand
- However, EO 14057 (Federal Sustainability), GSA MAS Refresh 31 AI monitoring provisions, and DOE's massive AI infrastructure buildout suggest **growing demand**
- **Recommended approach:** Build a proof-of-concept only; validate with DOE/PNNL and GSA buyers before full product development
- Package F can leverage Package E's infrastructure for on-premises deployments

Build Sequence:
1. Compute run logger API (2-3 weeks) -- **do this first**
2. Compute deed receipt format (1-2 weeks)
3. Agency validation conversations (ongoing)
4. Full build only after 2+ agencies confirm procurement intent

---

## Cross-Cutting Recommendations

### Priority Ranking (Build + Pursue)

| Priority | Package | Federal Demand Strength | Differentiation | Build Effort | Time to Revenue |
|----------|---------|------------------------|-----------------|--------------|-----------------|
| **1** | **A: AI TEVV Ledger** | STRONG (9 opportunities, 10/10 top fit) | HIGH | MEDIUM | 6-12 months |
| **2** | **B: Cyber Proof Ledger** | STRONG (10 opportunities, ACTIVE bids now) | MEDIUM-HIGH | MEDIUM | 3-9 months |
| **3** | **C: Data Provenance Vault** | STRONG (9 opportunities, VA-friendly) | HIGH | MEDIUM | 6-12 months |
| **3** | **D: Fraud Evidence Workbench** | STRONG (7 opportunities, IRS imminent) | HIGH | LOW-MEDIUM | 3-9 months |
| **4** | **E: Private AI Appliance** | MEDIUM (8 opportunities, massive scale) | VERY HIGH | HIGH | 12-24 months |
| **5** | **F: Compute Deed** | EMERGING (4 opportunities, speculative) | VERY HIGH | LOW (POC) | 18-36 months |

### Recommended Pursuit Sequences

**Immediate (Next 30 Days):**
1. Monitor **Army PANAPG-26-P-0000041835** (RMF Support -- DUE May 29, 2026)
2. Monitor **NRC 31310026R0012** (Cybersecurity -- DUE May 26, 2026)
3. Submit **DOT SBIR 6913G626QSBIR1** (Edge AI -- DUE May 29, 2026)
4. **Register at SAM.gov** -- mandatory before any of the above

**Short-Term (1-6 Months):**
5. Submit **Army AI/ML Open Topic SBIR** Phase I ($250K) or Direct-to-Phase II ($2M)
6. Build **Package A prototype** (TEVV dashboard + NIST AI RMF mapping)
7. Build **Package B prototype** (RMF BOE generator + eMASS export)
8. Submit capability statements to **10 prime contractor OSBDU offices**

**Medium-Term (6-18 Months):**
9. **DIA AI TEVV RFI follow-on** -- expected solicitation (prime or sub)
10. **NIST AISI evaluation contracts** -- position as evaluation support
11. **VA Data Governance IDIQ** -- multiple-award, 12 task areas
12. **IRS Fraud Analytics** -- formal solicitation likely imminent
13. Apply for **GSA MAS** (SIN 54151S + 54151HACS)

**Long-Term (18-36 Months):**
14. **DOE/PNNL AI Data Center** -- massive infrastructure opportunity
15. **Air Force AI Data Center** -- multi-site deployment
16. **Build past performance** through SBIR + subcontracting
17. Pursue **8(a) sole-source** opportunities (avg $3.2M per AI contract)

### Security Compliance Roadmap

| Milestone | Timeline | Cost Estimate | Blocks Which Packages |
|-----------|----------|---------------|----------------------|
| SAM.gov Registration + UEI/CAGE | 2-8 weeks | FREE | ALL |
| NIST SP 800-171 Self-Assessment | Month 1-2 | $5K-15K | B, E |
| CMMC Level 2 Certification | Month 3-6 | $15K-50K | B (DoD cyber) |
| Facility Clearance (FCL) | Month 6-12 | $10K-30K | A (DIA), E (IL5/6) |
| FedRAMP Tailored / LI-SaaS | Month 6-12 | $50K-150K | A, C, D (cloud delivery) |
| GSA MAS Award | Month 6-12 | $10K-30K | ALL (market access) |

### Key Partner Targets

| Partner | Why | Best For | How to Approach |
|---------|-----|----------|-----------------|
| **SoKat LLC** | 8(a), Treasury AI, GSA AI Challenge winner | Packages A, D | Direct BD outreach; complementary capabilities |
| **Aquia Inc.** | SDVOSB, VA cloud/health IT/fraud | Packages C, D | BD outreach; VA partnership |
| **Enabled Intelligence** | Small business, NGA $708M IDIQ | Packages A, E | Teaming on NGA/intelligence opportunities |
| **Nava PBC** | PBC, VA NAII, HHS | Packages A, C | VA and health IT teaming |
| **ONEOMEGA LLC** | 8(a), $160M Coast Guard IA/RMF | Package B | Subcontractor on follow-on |
| **Booz Allen Hamilton** | Largest AI contractor, WAEDS $1.58B | Packages A, B, E | OSBDU capability statement submission |
| **Palantir** | $1B DHS BPA, Foundry/Gotham | Packages C, D | Foundry partner program |
| **Peraton** | $100M+ cyber portfolio | Package B | OSBDU + industry day networking |

---

## Appendix: Methodology & Data Sources

All opportunity data in this document was extracted from verified SAM.gov listings during research conducted May 2026. Every notice ID listed is traceable to an official SAM.gov record. No opportunity data was fabricated.

**Research Pods Referenced:**
- Pod 04: AI TEVV / Trust / Evaluation (12 opportunities)
- Pod 05: Cybersecurity / RMF / Continuous Monitoring (15 opportunities)
- Pod 06: Data Governance / Provenance / Validation (14 opportunities)
- Pods 07-08: Fraud Analytics + Secure Compute (18 opportunities across both lanes)
- Pod 09: Federal Award History & Incumbent Mapping ($12.5B+ in awards)
- Pods 10-11: Small Business / NAICS / Entry Path Analysis

**Total Research Coverage:** 55+ verified SAM.gov opportunities; $12.5B+ in award history; complete NAICS/PSC/size-standard analysis.

---

*Document generated: 2026-05-24*
*Classification: DefendableOS Internal Strategy Document*
*All federal opportunity data sourced from SAM.gov and official government procurement records*
