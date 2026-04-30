<div align="center">

# PRIOR INTELLECTUAL PROPERTY DECLARATION

### Formal Declaration of Sole Ownership & Exclusion from Assignment

---

**12 Software Systems** &nbsp;&bull;&nbsp; **19,700+ Automated Tests** &nbsp;&bull;&nbsp; **620,000+ Lines of Code** &nbsp;&bull;&nbsp; **20+ Compliance Standards** &nbsp;&bull;&nbsp; **All Rights Reserved**

---

</div>

<br>

## I. Purpose

This document constitutes a formal declaration of **Prior Intellectual Property** ("Prior IP") owned solely by the undersigned ("Declarant"). All software, tools, frameworks, source code, documentation, architectures, designs, algorithms, and related materials described herein were **conceived, designed, developed, and completed by the Declarant** prior to and independent of any employment relationship.

This declaration is intended to be attached as an exhibit or addendum to any employment agreement containing an intellectual property assignment clause. **All works listed herein are explicitly excluded from any such assignment.**

<br>

---

<br>

## II. Declarant

| | |
|---|---|
| **Full Legal Name** | ________________________________________________ |
| **Date of Declaration** | ________________________________________________ |
| **Signature** | ________________________________________________ |

<br>

---

<br>

## III. Declaration Statement

> I, the undersigned, hereby declare that the following software projects, tools, and frameworks are my **sole and exclusive intellectual property**. Each was conceived, architected, developed, and brought to its current state **entirely by me, on my own time, using my own resources**, prior to any employment relationship with the receiving party.
>
> No employer resources, proprietary information, trade secrets, or work time were used in the creation of any of these works.
>
> I retain **all rights, title, and interest** in and to each of the works described below, including but not limited to all copyrights, patent rights, trade secret rights, and any other intellectual property rights therein.

<br>

---

<br>

## IV. Portfolio Overview

<div align="center">

```
┌─────────────────────────────────────────────────────────────────┐
│              AGENT & MCP GOVERNANCE PLATFORM                     │
│                                                                 │
│   CORE — the four Cs                                            │
│   Castellan    Charlotte    Chronicle    Citadel                │
│   (agents)     (context)    (attest)     (design)               │
│                                                                 │
├─────────────────────────────────────────────────────────────────┤
│                           PRODUCTS                               │
│   Audit Pro   Chancery    Verity     Steward                    │
│   (audit)     (PRD)       (SM/PM)    (PO/PM)                    │
│                                                                 │
│   Reeve       Author      Quaestor    Augur                    │
│   (admin)     (stories)   (RFP)       (CoE advisor)             │
└─────────────────────────────────────────────────────────────────┘
```

</div>

<br>

<div align="center">

| Metric | Value |
|:---|:---|
| **Total Software Systems** | 12 |
| **Combined Automated Tests** | 19,700+ |
| **Estimated Lines of Code** | 620,000+ |
| **Compliance Standards Covered** | 20+ (EU AI Act, NIST AI RMF, NIST 800-53, NIST 800-171 Rev 2, NIST CSF 2.0/CAISI, NIST IR 8596, FedRAMP Low/Moderate/High, DoD IL4/IL5, CMMC L1/L2/L3, CNSSP-12, CNSA 2.0, FIPS 140-3, FIPS 204 (ML-DSA), DoD STIG, HIPAA, PCI-DSS v4.0, SOC 2 Type II, ISO 42001, ISO 27001, ISO 42005, GDPR, GLBA Safeguards, FFIEC IT Handbook, SOX ITGC, OCC SR 11-7, FINRA 2026, MAS AI RM, Singapore IMDA, OWASP Top 10, CoSAI, COPPA) |
| **Status** | All systems complete and operational |

</div>

<br>

---

<br>

## V. Schedule of Prior Intellectual Property

<br>

### Core Platform &mdash; The Four Cs

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>1 &mdash; Castellan &nbsp;&nbsp;<sub>Agent Governance Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Framework &mdash; Python CLI with Rust Target Generation |
| **Repository** | `/projects/fleet/core/castellan` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 8,600+ automated tests |
| **Source Lines** | 122,545 |
| **Modules** | 531 |
| **Status** | Complete and operational |

#### Description

Castellan is the **agent governance compiler**. It takes YAML agent specifications and compiles them through a **5-stage pipeline** (parse, compose, optimize, validate, render) into executable, validated AI agents with structural governance. Constitutional governance, runtime guardrails, OWASP audit, and 12 export formats including **Level 6 hardened Rust binaries** (FROM scratch, static musl, RELRO+NX, mTLS via rustls) for DoD deployments.

#### Compliance Engine

Castellan's compliance engine provides typed, auditable compliance assessment across **18 regulatory frameworks** including EU AI Act, HIPAA, PCI-DSS v4.0, SOC 2 Type II, NIST AI RMF, NIST 800-53, NIST CSF 2.0 (CAISI), ISO 42001/27001, GDPR Article 22, FedRAMP, DoD IL4/IL5, CNSSP-12, FINRA 2026, OWASP Agentic, and COPPA.

#### Governance Features

- Constitutional governance with severity-ranked principles (`critical`/`high`/`medium`/`low`)
- Runtime guardrails (PII redaction, prompt injection filtering, hallucination detection) with most-restrictive-wins semantics
- Async-first ReAct execution engine with 4 LLM providers, MCP client, A2A protocol, RAG pipeline
- Multi-agent orchestration (Supervisor, Pipeline, Broadcast, Peer)
- CI/CD governance gate with `APPROVE / REVIEW / BLOCK` verdicts
- 12 export targets including Python package, Docker, FastAPI, Claude Code skill, Kubernetes, Temporal, and Level 6 Rust binaries

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `tiktoken` &bull; `httpx` &bull; `Anthropic SDK` &bull; `OpenAI SDK` &bull; `Google SDK` &bull; Rust target generation (`rmcp`, `rustls`, `aws-lc-rs`)

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>2 &mdash; Charlotte &nbsp;&nbsp;<sub>Context Engineering Compiler &amp; MCP Server Generator</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Repository** | `/projects/fleet/core/charlotte` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 3,700+ automated tests |
| **Source Lines** | 36,337 |
| **Modules** | 135 |
| **Status** | Complete and operational |

#### Description

Charlotte transforms prompt engineering into **structured, validated, composable software engineering** through a 5-stage deterministic pipeline (Parse, Compose, Optimize, Validate, Render). It includes a **103-block template catalog** across 20 types with composition precedence and tier requirements, 30 assertion types, multi-provider rendering (Anthropic, OpenAI, Google Gemini, Ollama), Claude Code skill compilation, and MCP server generation with full DoD hardening.

#### Compliance & Security Scanning

Charlotte implements **89 security patterns across 22 categories** with deep defense/federal compliance coverage including 35+ DoD detection patterns aligned to NIST 800-53 control families (AC, AU, IA, SC, SI, CM, CP, IR, RA, SA), STIG checklist export with vulnerability IDs (V-222400 format) at CAT I&ndash;III severity, FIPS 140-3 compliance validation, mTLS/CAC enforcement, classification-banner display, MCP DoD hardening, and CoSAI threat modeling (MCP-T1/T2/T6/T9). Audit output formats include JSON, CEF (ArcSight/SIEM), and Syslog RFC 5424.

#### MCP Server Generation

Charlotte compiles prompt specs into **complete MCP servers** in two targets:

| Target | Description |
|:---|:---|
| **Python (FastMCP)** | Python MCP servers with governance spec integration |
| **Rust (Level 6)** | Level 6 hardened Rust MCP binaries (FROM scratch, static musl, mTLS via rustls, panic=abort) |

Additional quantized MCP server renderers support air-gapped Ollama deployments. 23 export formats total including Claude Code skills (`SKILL.md`), Cursor/OpenCode IDE skills, HTML+README export, eval trend dashboards, and GitHub Actions CI integrations.

#### 8-Pass Optimizer

Dedup &rarr; Merge &rarr; Strip &rarr; Normalize &rarr; Reorder &rarr; Compress &rarr; Budget &rarr; Provider hints. Three tier floors enforce structural depth: single-turn (18K tokens), multi-phase (35K tokens), agent-orchestrating (55K tokens). 10-factor quality scorer + 12 red-flag checks reject thin prompts at compile time.

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `deepdiff` &bull; `watchdog` &bull; `tiktoken` &bull; `Anthropic/OpenAI/Google SDKs`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>3 &mdash; Chronicle &nbsp;&nbsp;<sub>Runtime Attestation &amp; Compliance Observability Substrate</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Binary + gRPC + Postgres |
| **Repository** | `/projects/fleet/core/chronicle` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 394+ automated tests |
| **Source Lines** | 24,491 |
| **Crates** | 18 |
| **Status** | Complete and operational |

#### Description

Chronicle is the **runtime-attestation and compliance-observability substrate** for agent fleets. Agents emit events; Chronicle signs, verifies, Merkle-chains, persists, maps to controls, and produces auditor-shippable OSCAL packages and ATO bundles. Chronicle itself is **zero-LLM in the compliance-critical path** &mdash; signing, verification, transition gates, and build gates are all deterministic Rust. LLM assistance exists only in the advisory pack-authoring drafter layer.

#### Hybrid Post-Quantum Signing from v0

Every event, every OSCAL package, every ATO bundle is signed with **both Ed25519 and ML-DSA-65 (FIPS 204)** &mdash; the post-quantum lattice signature standardized by NIST. `verify_hybrid` requires BOTH halves to verify. This is the cryptographic floor that lets a 3PAO verify any artifact on a separate machine in 2026 *or* 2036.

#### Deterministic Attestation Substrate

| Layer | Implementation |
|:---|:---|
| **Canonicalization** | RFC 8785 JSON Canonicalization Scheme |
| **Hash chain** | SHA-256 Merkle tree, O(log N) inclusion proofs |
| **Signing** | Hybrid Ed25519 + ML-DSA-65 keyring; FIPS-only build feature substitutes AES-GCM for ChaCha20-Poly1305 |
| **Reproducible build** | `lto = "fat"`, `codegen-units = 1`, `strip = "symbols"`, `SOURCE_DATE_EPOCH` pinned |
| **Persistence** | PostgreSQL store with tenant isolation; in-memory store for tests |
| **Witness** | Internal log + external witness adapters (Mock, Rekor) for transparency |

#### 18-Crate Rust Workspace

chronicle-core, chronicle-crypto, chronicle-events, chronicle-chain, chronicle-store, chronicle-verifier, chronicle-packs, chronicle-mapping, chronicle-pipeline, chronicle-shred, chronicle-witness, chronicle-oscal, chronicle-admin, chronicle-server, chronicle-ingest, chronicle-otel-bridge, chronicle-pack-authoring, chronicle-ato.

#### Framework Packs &mdash; 92 Control Mapping Rules

Ships with 4 framework packs: **SOC 2** (Trust Services Criteria), **HIPAA** (Administrative/Physical/Technical safeguards, &sect;164.312 transcribed), **EU AI Act** (high-risk system controls, Annex IV references), **NIST 800-53 Moderate** (federal Moderate baseline subset). Pack-authoring uses a controlled transition pipeline with hybrid-signed `ReviewerAttestation` binding.

#### Three Deployment Tiers, One Codebase

`DeploymentTier::{Commercial, Regulated, Sovereign}` parameterizes witness policy, ConMon cadence, and pen-test scope &mdash; not forked code. Sovereign adds cross-jurisdictional witness quorum + HSM-backed keys.

#### OSCAL & ATO Export

OSCAL evidence packages (signed, cross-referenced control evidence), System Security Plan (SSP), Continuous Monitoring (ConMon) plan, pen-test scope specification, and signed ATO bundle binding all artifacts under hybrid signature. Every signed artifact verifies on a separate machine using only the signer's public-key bundle.

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `tonic` (gRPC) &bull; `PostgreSQL` &bull; `Ed25519-Dalek` &bull; ML-DSA-65 (FIPS 204) &bull; `aws-lc-rs` (FIPS 140-3) &bull; `rustls` &bull; OSCAL &bull; Rekor

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>4 &mdash; Citadel &nbsp;&nbsp;<sub>Compliance-Aware Design Intelligence Platform</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI + FastMCP Server |
| **Repository** | `/projects/fleet/core/citadel` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 1,000+ automated tests |
| **Source Lines** | 30,519 |
| **Modules** | 88 |
| **Status** | Complete and operational |

#### Description

Citadel is the compliance-aware design intelligence platform. It generates compiler-ready YAML specs with governance fields that become runtime enforcement rules, compiles behavioral intent into enforceable policy, and runs a full compliance engine for regulatory documentation and live codebase scanning.

#### Three Operating Modes, 43 Tools

- **`citadel design`** &mdash; Interactive CLI via Anthropic API (user-driven, reactive)
- **`citadel forge`** &mdash; Voice-first automated pipeline (4 stages, 3 approval gates)
- **`citadel serve`** &mdash; FastMCP server (stdio/SSE) for MCP clients

#### Fleet-Level Artifact Generation

`gen_fleet_specs` produces coordinated artifacts for multi-agent deployments: Castellan agent specs + Charlotte MCP server specs (compliance + behavioral aware), A2A trust policy (bilateral pairs with delegation types), runtime registration config, Herald C2 config (protected fields, HMAC signing), behavioral baseline, HMAC manifest, provenance manifest (Merkle root), tool description scan (poisoning detection), tool integrity manifest (SHA-384 description hashes), call stack policy (chain depth, circular detection), autonomy progression (tier-based promotion/demotion), crossing policy (territory allowlists, crypto suite selection), redundancy protocol policy (governed failover), MCP topology policy (interaction graph, undeclared edge detection), trust scoring policy (behavioral trust decay), and SR 11-7 model cards.

#### Compliance Engine &mdash; 26 Frameworks

Live codebase scanning + regulatory document generation:

- **`generate_fedramp_ssp(level)`** &mdash; FedRAMP SSP (OSCAL JSON, POA&M, low/moderate/high)
- **`generate_nist800171_ssp(system_name)`** &mdash; NIST 800-171 Rev 2 SSP (CMMC L2)
- **`run_stig_checklist(component)`** &mdash; DISA STIG with 45 findings, CKL export
- **`generate_glba_safeguards_report()`** &mdash; GLBA Safeguards Rule (16 safeguards)
- **`generate_pcidss_report()`** &mdash; PCI-DSS v4.0 (12 requirements, SAQ determination)
- **`generate_ffiec_report()`** &mdash; FFIEC IT Examination Handbook (48 requirements, 5 domains)
- **`generate_sox_itgc_report()`** &mdash; SOX ITGC (17 controls, 4 domains)
- **`generate_model_card_report()`** &mdash; SR 11-7 model card per agent
- ISO/IEC 42001 AI Management System assessment (32 clauses + Annexes A/B)
- FDA PCCP tracking (7 change categories with bounded autonomy)
- IEC 62304 SDP/SRS/SAD, ISO 14971 RMF, FDA PCCP, SOUP list

#### MCP Security Pipeline

Design-time defense against MCP attack vectors (tool poisoning, rug pulls, preference manipulation, call chain abuse). All modules regex-based, deterministic, air-gap safe: `scan_tool_descriptions` (20 patterns, 4 severity levels), `verify_tool_integrity` (SHA-384 hashes), `compile_call_stack_policy`, `compile_topology_policy`, `compile_trust_scoring_policy`.

#### Technology Stack

`Python 3.10+` &bull; `MCP[cli]` &bull; `Pydantic v2` &bull; `PyYAML` &bull; `Typer` &bull; `Rich` &bull; `Anthropic SDK`

<br>
</details>

<br>

### Products

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>5 &mdash; Audit Pro &nbsp;&nbsp;<sub>Productized Governance Audit</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust CLI + Compiled Agents + MCP Servers |
| **Repository** | `/projects/fleet/products/audit-pro` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 215+ automated tests |
| **Source Lines** | 19,114 |
| **Crates** | 5 Rust crates &bull; 89 modules |
| **Status** | Complete and operational |

#### Description

Audit Pro is the **productized governance audit** for third-party AI agents. The architecture matches the platform's own self-hosting principle: Audit Pro's analytical layer is itself **seven Castellan-compiled audit agents and seven Charlotte-compiled MCP servers**. The Rust outer shell is the *delivery vehicle*: CLI, orchestrator state machine, deliverable assembly, verify pipeline, remediation patch emit/apply, retirement + redaction.

#### What Customers Hand Over, What Audit Pro Returns

| Customer hands over | Audit Pro returns |
|:--|:--|
| Agent code, specs, configs | Premium HTML deliverable with verbatim citations |
| Optional runtime logs | Behavioral baseline (when logs provided) |
| Framework selection | Framework-mapped findings, severity-graded |
| Authorized signer | Signed scope attestation |
| | **Drop-in recompiled Castellan/Charlotte spec** that closes priority-1 findings |
| | **Chronicle-signed evidence bundle** (hybrid Ed25519 + ML-DSA-65) |
| | OSCAL package + SR 11-7 model card per agent |
| | Auditor handoff document (12+ pages) |

#### Frameworks Supported

NIST AI Risk Management Framework (Govern/Map/Measure/Manage), EU AI Act (High-Risk; Annex III/IV), SR 11-7 (Federal Reserve Model Risk Management), SOC 2 Common Criteria 6 (CC6/CC7), NIST SP 800-53 Moderate, CMMC Level 2, HIPAA, PCI-DSS v4.0.

#### The Engagement Pipeline

Init &rarr; Scan &rarr; Analyze &rarr; Evidence pack &rarr; Finalize &rarr; Verify &rarr; Diff &rarr; Remediate &rarr; Retire (`audit-pro retire --purge` for GDPR right-to-erasure).

#### Architectural Invariants

1. Audit Pro never re-implements engine logic &mdash; it composes existing engines (Citadel, Forge, Castellan, Charlotte, Bailiff, Chronicle).
2. Intelligence lives in compiled artifacts.
3. The Rust shell is the outer wrapper. No LLM-calling logic in the shell.
4. Auditor-independent verification on a separate machine using only the signer's public-key bundle.
5. Customer-facing product is Rust &mdash; single Level 6 hardened binary, no Python runtime in customer environments at delivery time.

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `rustls` &bull; `aws-lc-rs` (FIPS) &bull; ML-DSA-65 &bull; Ed25519 &bull; Level 6 hardening profile

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>6 &mdash; Chancery &nbsp;&nbsp;<sub>AI Chief Product Officer &amp; Design Front Door</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI + MCP Server + Claude Desktop Project |
| **Repository** | `/projects/fleet/products/chancery` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 822+ automated tests |
| **Source Lines** | 19,829 |
| **Modules** | 70 |
| **Status** | Complete and operational |

#### Description

Chancery is an **AI Chief Product Officer** that transforms unstructured product input (voice transcripts, Slack threads, meeting notes, emails, bullet points) into **production-quality PRDs and agent/MCP fleet architectures** through a disciplined 4-phase, 3-gate workflow with deterministic quality scoring.

#### 4-Phase Workflow

| Phase | Gate | Output |
|:---|:---|:---|
| **Assessment** | Structured input | Normalized problem statement |
| **Discovery** | Domain interrogation | Branch-adapted discovery (5 branches) |
| **Spec** | Quality gates (30-item checklist) | Compliance-annotated PRD |
| **SDD** | Per-component validation | SDD bundles for Charlotte + Castellan |

#### Architect Mode

Chancery's architect mode deploys as a **Claude Desktop Project** and **Claude Code skill** (`/chancery-architect`). Embeds V1 Agent Architecture Design methodology: conversational decomposition into min-correct agent/MCP architectures with per-component SDD bundles validated by Charlotte + Castellan. Ships with 7 fat knowledge files (~89K tokens), QA'd on 4 synthetic scenarios.

#### Stateful FastMCP Server &mdash; 21 Tools

12 legacy PRD tools (normalize_input, compliance_check, web_search, conflict_detector, confirm_product_definition, compile_prd, generate_artifacts, record_assumption, update_assumption, issue_challenge, record_interrogation, score_prd) + 7 architect-mode actions + 2 artifact tools.

#### Compliance Framework Detection

Automatically detects **10 compliance frameworks**: PCI-DSS, HIPAA, GDPR, EU AI Act, NIST 800-53, COPPA, SOC 2, FedRAMP, HL7 FHIR, FINRA. Citadel bridge surfaces compliance gaps as PRD NFRs and risks.

#### Quality Infrastructure

- 30-item quality checklist (21 deterministic + 9 LLM-assisted)
- 7 cognitive bias detectors (sunk cost, confirmation, IKEA effect, planning fallacy, survivorship, anchoring, scope creep) with reframing challenges
- Small-agents philosophy (code-enforced &lt;6 agents per fleet)
- 9-enum / 17-dataclass state machine with absolute gate enforcement (`GateNotApprovedError`)
- Subprocess-based LLM orchestration (no SDK lock-in)
- 15 knowledge files (~140K tokens, knowledge budget ratio 0.80)
- 18-archetype catalog with 13-step deterministic interrogation pipeline

#### Technology Stack

`Python 3.11+` &bull; `Typer` &bull; `Anthropic SDK` &bull; `Pydantic v2` &bull; `MCP[cli]` &bull; `PyYAML` &bull; `Rich` &bull; `claude -p` passthrough

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>7 &mdash; Verity &nbsp;&nbsp;<sub>Scrum Master / Project Manager Intelligence Platform</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Workspace (33 Crates) |
| **Repository** | `/projects/fleet/products/verity` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 3,900+ automated tests |
| **Source Lines** | 172,941 |
| **Status** | Complete and operational |

#### Description

Verity is the Scrum Master / Project Manager intelligence platform. Reads across Jira, Confluence, GitHub, Bitbucket, Slack, and Teams to surface the conversations a team needs to have today. Fleet architecture: **33 workspace crates**, 58 CLI subcommands, **17 MCP servers**, **8 governed agents**. SOC 2 compliant fleet artifacts generated by Citadel. **Read-only by compile-time construction** &mdash; the HTTP client is GET-only, enforced at the type level.

#### Intelligence Capabilities

- **23 antipattern detectors** &mdash; 12 Scrum + 3 Review Quality + 8 Kanban
- **Methodology system** &mdash; Scrum, Kanban, Scrumban, PM with profile-driven cadence schedules
- **5 ceremony pipelines** &mdash; Standup (daily), Planning (per-sprint), Review (per-sprint), Retro (per-sprint), Refine (weekly)
- **5-layer signal observability** &mdash; Raw, Feature, Correlation, Pattern, Insight
- **Day-Zero scan pipeline** &mdash; 24-hour onboarding intelligence
- **Career log** &mdash; ChaCha20-Poly1305 + Argon2id encrypted personal history
- **Web UI** &mdash; axum + rustls, full route coverage
- **9 report kinds** with voice-initiated publish; SMTP/Slack/Teams delivery with audience fan-out

#### 8 Governed Agents

Sprint intelligence, antipattern detector, ceremony brief composer, review quality analyst, GitHub intel, signal correlator, delivery dispatcher, report writer. Each compiled by Castellan, every prompt by Charlotte, every fleet spec by Citadel under SOC 2.

#### Compile-Time Governance

- Read-only by construction &mdash; type system rejects POST/PUT/PATCH/DELETE at compile time
- Citadel-generated specs &mdash; all agents compiled with governance embedded
- Castellan + Charlotte validation &mdash; every component passes compliance floors

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `rustls` &bull; `ChaCha20-Poly1305` &bull; `Argon2id` &bull; `rusqlite` &bull; `rmcp`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>8 &mdash; Steward &nbsp;&nbsp;<sub>Product Owner / Product Manager Intelligence Platform</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Workspace (21 Crates) |
| **Repository** | `/projects/fleet/products/steward` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 145+ automated tests |
| **Source Lines** | 94,780 |
| **Status** | Complete and operational |

#### Description

Steward is the Product Owner / Product Manager intelligence platform &mdash; sibling to Verity, same read-only architecture. Reads Jira, Confluence, GitHub, Slack, and Teams. Fleet architecture: **21 workspace crates**, 50 CLI subcommands, **5 MCP servers**, **8 PO-specific governed agents**. SOC 2 compliant fleet artifacts generated by Citadel. **62 knowledge bundles** (1.1 MB total, 59 wired to MCP server specs).

#### 8 PO-Specific Agents

roadmap-intelligence-agent, backlog-quality-agent, stakeholder-dynamics-agent, product-drift-agent, outcome-intelligence-agent, decision-archaeology-agent, communication-agent (drafts external sends, never auto-sends), individual-mirror-agent (one-way data firewall).

#### 5 PO Intelligence Cadences

| Cadence | Frequency | Purpose |
|:---|:---|:---|
| **roadmap_review** | Weekly | Roadmap drift, epic health, milestone risk |
| **backlog_health** | Daily | Story readiness, refinement debt, stale-ticket pruning |
| **stakeholder_pulse** | Biweekly | Engagement patterns, silent-veto detection, alignment scoring |
| **release_readiness** | Per-release | Scope-vs-promise diff, defect risk, rollout gating |
| **outcome_review** | Monthly | Post-release adoption signals, value-delivered audit |

#### 16 PO Antipattern Detectors

roadmap_drift, backlog_bloat, refinement_desert, stakeholder_silent_veto, scope_vs_vision_drift, feature_factory, acceptance_criteria_thin, story_breakdown_horizontal_only, dependency_silent, release_promise_overrun, adoption_signal_unmonitored, decision_unrecorded, priority_conflict_unsurfaced, stakeholder_engagement_decay, backlog_age_skew, epic_correlation_missing, outcome_review_skipped &mdash; all with real detection logic over the data store.

#### Delivery & Web UI

- 9 PO-specific report kinds with voice-initiated publish
- Multi-channel delivery &mdash; SMTP/Slack/Teams with audience fan-out
- Web UI &mdash; 20 routes + 5 SVG visualizations
- 5 synthetic test scenarios for deterministic validation
- Individual mirror as one-way firewall &mdash; data IN (with consent), nothing flows OUT

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `rustls` &bull; `ChaCha20-Poly1305` &bull; `Argon2id` &bull; `rusqlite` &bull; `rmcp`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>9 &mdash; Reeve &nbsp;&nbsp;<sub>Governed Atlassian Administration Platform</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Workspace (17 Crates) |
| **Repository** | `/projects/fleet/products/reeve` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 532+ automated tests |
| **Source Lines** | 31,019 |
| **Status** | Complete and operational |

#### Description

Reeve is the governed Atlassian administration platform &mdash; the **writer** where Verity and Steward are **readers**. Exposes 5 MCP servers for governed project, workflow, and permission updates with compliance-aware fleet artifacts generated by Citadel when the framework demands traceable Atlassian admin actions (SOX change control, HIPAA access review, SOC 2 privilege separation).

#### 5 Governed MCP Servers (102 Atlassian Tools)

| Server | Domain |
|:---|:---|
| **jira-config** | Projects, workflows, schemes, permissions |
| **jira-reporting** | Dashboards, filters, custom fields |
| **jsm** | Service desk configuration, request types, SLAs, queue management |
| **confluence-admin** | Spaces, permissions, page templates, label governance |
| **plugin-governance** | Plugin lifecycle, marketplace allowlists, license attestation |

#### 4 Governed Agents

config architect (reasons over configuration intent), reporting analyst (builds JQL filters/dashboards from plain-language asks), hygiene enforcer (drift detection from declared baselines), process optimizer (workflow inefficiency surfacing).

#### Governed Write Architecture

- **7 CLI subcommands** for governed Atlassian admin
- **Plain-language intent** &mdash; natural language config description
- **Approval gates** &mdash; HITL checkpoints for regulated changes
- **State snapshots + rollback** &mdash; recoverable configuration changes
- **Read-write-http client** &mdash; governed write access (contrasts with Verity/Steward read-only); type system distinguishes read vs. write operations
- **12 knowledge files** (20,982 words) covering Atlassian admin patterns, audit-trail requirements per framework

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `rustls` &bull; `rusqlite` &bull; `rmcp`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>10 &mdash; Author &nbsp;&nbsp;<sub>Story/Epic Coaching Tool</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Workspace (6 Crates) |
| **Repository** | `/projects/fleet/products/author` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 181+ automated tests |
| **Source Lines** | 59,474 |
| **Status** | Complete and operational |

#### Description

Author generates epics and stories on command and enforces authoring discipline through a deterministic refusal layer that catches shallow authoring before it reaches Jira. The primary function is **generation** &mdash; the refusal layer is the safety net.

#### 6-Crate Workspace

| Crate | Role |
|:---|:---|
| **author-core** | Domain types, INVEST scoring, anti-pattern detection, refusal evaluator, gold-signature matcher |
| **author-store** | SQLite persistence for stories, drafts, gold signatures, adaptive tuning state |
| **author-llm** | LLM provider abstraction (Anthropic, OpenAI, Ollama) + keyword-skeleton fallback for air-gap |
| **author-control** | Workflow state machine: draft &rarr; coach &rarr; refusal-eval &rarr; accept/reject |
| **author-mcp** | MCP stdio server exposing authoring tools to other agents |
| **author-web** | axum web UI with story browser, draft authoring surface, refusal explanations |

#### The Deterministic Refusal Layer

- **INVEST scoring** &mdash; numeric scoring with per-dimension thresholds
- **DoR gates** &mdash; Definition of Ready compliance
- **15 anti-pattern detectors** &mdash; vague_value, role_missing_user_type, ac_implementation_detail, scope_horizontal_slice, dependency_silent, estimate_unmoored, story_disguised_epic, technical_task_as_story, etc.
- **Gold-signature matcher** &mdash; auto-anchoring against validated exemplars
- **Adaptive tuning state** &mdash; coach learns from accepted/rejected outputs

A draft that fails the refusal layer is rejected with structured reason and specific guidance. Calibrated against the user's authoring bar, not against the median.

#### Capabilities

- 5 domain packs &mdash; domain-specific authoring templates
- Scan + rewrite &mdash; bulk analysis of existing Jira stories with suggested rewrites
- Live Jira JQL read + push &mdash; optional integration
- Confluence export &mdash; epic-level export with structured layout
- MCP stdio server + axum web UI &mdash; multi-surface access (terminal, browser, agent integration)
- LLM coaching with keyword-skeleton fallback &mdash; works with or without LLM access (air-gap capable)

#### Quality Metrics

| Metric | Value | Meaning |
|:---|:---|:---|
| **MAE** | 0.109 | Mean absolute error between predicted and human-graded scores |
| **F1** | 0.97 | Anti-pattern detector precision/recall balance |
| **one-shot-good** | 10/10 | Reference corpus pass rate on first generation |

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `rusqlite` &bull; `rmcp` &bull; Shared regex library

<br>
</details>

<br>

<details open>
<summary><h3>11 &mdash; Quaestor &nbsp;&nbsp;<sub>RFP Intelligence Engine</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Workspace (7 Crates, V0) |
| **Repository** | `/projects/fleet/products/quaestor` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 83 automated tests |
| **Source Lines** | 4,014 |
| **Status** | V0 Complete and operational; V1 9-component fleet on disk as design reference |

#### Description

Quaestor is the procurement-response validation engine. Reads federal solicitations (`.docx` and `.pdf`), judges every offeror response against the question it claims to address via `claude -p` subprocess, and emits a dark-themed dual HTML+PDF verdict report plus structured JSON with full source provenance. Roman quaestors audited state procurement contracts; this binary does the same job two thousand years later.

#### V0 Architecture &mdash; 7-Crate Workspace

| Crate | Role |
|:---|:---|
| **qsr-core** | IDs, errors, provenance, verdict, classification |
| **qsr-crypto** | CNSA 2.0 wrappers (SHA-384, HMAC-SHA384, FIPS module verify) |
| **qsr-cui** | DoDM 5200.01 V4 banner injection trait + classification scanner |
| **qsr-judge** | docx/pdf extract &rarr; `claude -p` subprocess &rarr; HTML render &rarr; PDF post-process |
| **qsr-cli** | binary `quaestor` with `judge`/`render`/`pdf`/`selftest` subcommands |
| **qsr-chronicle-client** | Attestation event emission (V0 stub, V1 substrate) |
| **qsr-drawbridge-client** | A2A signed messaging (V0 stub, V1 substrate) |

#### Judging Philosophy &mdash; Demonstrate vs Name-Drop

Three-state verdict (`pass` / `weak` / `miss`) with 0&ndash;100 confidence and five sub-scores: **completeness**, **specificity**, **evidence_quality**, **framework_demonstration**, **fluff** (lower is better). Mentioning FedRAMP is name-drop; citing an ATO date, level, and authorizing officer is demonstration. Quaestor scores against the demonstration bar.

#### Risk Signal Taxonomy

- **false_claim_signal** &mdash; certification/ATO/contract claimed without offered corroboration
- **oci_signal** &mdash; Organizational Conflict of Interest (impaired objectivity / unequal access)
- **ceiling_above_signal** &mdash; framework invoked above what a reasonable offeror would carry (e.g. FedRAMP High but no ATO)
- **date_inconsistency** &mdash; internal date conflicts (period of performance vs completion vs award)
- **fabricated_quote** &mdash; Quaestor-injected: model returned a supporting quote not present in source; auto-detected via verbatim source round-trip; downgrades evidence_quality by 20 per quote

#### Three-Stage PDF Rendering Pipeline

1. wkhtmltopdf renders the dark-themed HTML to PDF
2. pdftocairo (poppler-utils) normalizes the malformed xref table for strict PDF parsers
3. `qsr_judge::pdf_post::add_page_background` opens the PDF with `lopdf`, prepends a save-state / set-non-stroke-RGB / fill-rect-covering-MediaBox / restore-state to every page's content stream &mdash; universal PDF op codes that every viewer (Chrome PDFium, Safari, Adobe, Preview) honors

#### Three Skews, One Binary

- **Hosted** &mdash; public CSPs allowed, Claude API hosted
- **On-prem IL4/IL5** &mdash; tenant VPC, FIPS module mandatory
- **Air-gap SCIF** &mdash; no network, local model (Ollama-class) via redirected `claude -p`

#### Compliance & Provenance

- CNSA 2.0 alignment (SHA-384 + HMAC-SHA384 only)
- DoDM 5200.01 V4 banner discipline with strict standalone-line detection
- Reproducibility envelope: source SHA-384 + run timestamp (RFC 3339 UTC) + model identifier + per-quote verification
- Federal Procurement domain pack auto-loaded; demonstrate-vs-namedrop YAMLs inject into the judgment prompt
- Resumable runs &mdash; `--resume` skips sections with prior verdicts (no double-billing for tokens)

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `clap` &bull; `lopdf` (PDF read + content-stream patching) &bull; `printpdf` &bull; `zip` + `quick-xml` (.docx) &bull; `regex-lite` &bull; `sha2` + `hmac` (SHA-384) &bull; `wkhtmltopdf` + `pdftocairo` (subprocess)

<br>
</details>

<br>

<details open>
<summary><h3>12 &mdash; Augur &nbsp;&nbsp;<sub>AI Strategy & Center-of-Excellence Advisor</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Python Package + Citadel/Chancery Bridge |
| **Repository** | `/projects/fleet/products/augur` |
| **Initial Development** | Prior to April 2026 |
| **Test Suite** | 209 automated tests |
| **Source Lines** | 5,551 |
| **Status** | Complete and operational; integrated as evidence layer under Citadel and Chancery |

#### Description

Augur is a CoE-as-a-Service consulting product and the **evidence layer underneath Citadel and Chancery's spec generators**. The operator walks into a company and *is* the AI Center of Excellence function for the engagement. Augur's auditable model catalog, framework catalog, CoE playbook, and use-case library substitute for years of accumulated institutional knowledge; the operator's judgment plus Augur's structural verifiers provide the institutional discipline. **One agent, four fat MCP servers, six wired bridges, two refresh sources, one portable skill.**

#### Five-Mode Engagement Workflow

| Mode | Output |
|:---|:---|
| **Discovery** | Stakeholder intake interview, candidate use cases, data requirements |
| **Shortlist** | Model and Framework Catalogs queried, candidates ranked, optional Forge eval, adopt-or-reject recommendation with full evidence trail |
| **Translate** | BRDs, FRDs, user stories, data mapping documents from the locked use case |
| **Govern** | Model cards, risk register, ROI scorecards, governance gate checklists via Citadel compliance engine |
| **Present** | Workshop deck, POC scaffold, executive presentation; rendered live through Folio |

#### Four Fat MCP Servers

| MCP Server | Substance |
|:---|:---|
| **Model Catalog** | 12 cataloged agentic-capable models scored across 8 dimensions (tool-use, multi-turn reliability, MCP support, RAG fit, cost-per-decision, deployment surface, license posture, agentic loop behavior). Hardware envelope filtering (VRAM, RAM, quantization). SHA-384 hashed entries with fetch timestamp + source URL + scorer version |
| **Framework Catalog** | 10 reference frameworks (LangChain, LangGraph, LlamaIndex, AutoGen, CrewAI, Anthropic Agents SDK, OpenAI Agents SDK, Google ADK, MCP, A2A) with governance posture overlays |
| **CoE Playbook** | AI Center of Excellence adoption patterns: intake gates, ROI scoring rubrics, governance scorecards, model risk classification, autonomy progression. Sourced from public CoE writeups + ISO 42005 + EU AI Act + NIST AI RMF + OCC SR 11-7 |
| **Use Case Library** | 19 patterns (12 synthetic_seed + 7 pilot_validated, mined from operator's deployed platform). Tagged with outcome data: what shipped, what flopped, why, ROI realized, governance overhead actually incurred |

#### Six Anti-Hallucination Structural Verifiers

- **CatalogIntegrityVerifier** &mdash; cited models/frameworks exist in catalog at the cited version
- **CatalogResidenceVerifier** &mdash; score values match catalog values exactly
- **ScoreVerifier** &mdash; composite scoring math reproducible from cataloged sub-scores
- **CitationVerifier** &mdash; citation byte-ranges round-trip against source documents
- **ROIVerifier** &mdash; ROI claims trace to use-case-library outcome data, not generated narrative
- **ComplianceVerifier** &mdash; framework attestations align with the Citadel compliance engine

Tamper-evident audit log writes per call.

#### Six Wired Bridges

- **Citadel bridge** &mdash; recommendations replace hardcoded defaults in `castellan_gen` (model + provider), `charlotte_gen` (MCP target model), and `fleet_gen` (runtime tier + local-quantized open-weights model with vendor-id-to-Ollama-tag translation)
- **Chancery bridge** &mdash; same pattern for PRD-driven spec generation
- **Folio bridge** &mdash; live PDF rendering during workshops
- **Forge bridge** &mdash; real eval harness fired during Shortlist mode
- **Refresh source: HuggingFace** &mdash; catalog refresh from model card metadata
- **Refresh source: vendor docs** &mdash; catalog refresh from API documentation

Behavior contract: Augur is graceful, optional, and additive &mdash; never a hard dependency. When installed, recommendations carry catalog provenance recorded as `augur_recommendation` blocks in spec output. When absent, hardcoded defaults are used exactly as before.

#### Compliance Posture

EU AI Act High-Risk as the primary framework, with ISO 42005 AI risk management and OCC SR 11-7 model risk available as overlays. Two runtime tiers from day one: **frontier** (Claude via passthrough) for fast iteration on commercial engagements, and **local_quantized** (Ollama llama 3.1 8B class) for air-gap or sovereign engagements. Selected per engagement, not baked in.

#### Conductor Tier

Regulated tier: full governance layers (A2A, Seneschal registration, Herald, Vigil baseline, tool integrity, call stack, autonomy progression, behavioral, topology, trust scoring, crossing policy, SRP), HMAC-SHA384 manifests, single-tenant Chronicle, software HSM, 7-year retention, five gates. Sovereign tier reserved for DoD-adjacent CoE engagements.

#### Technology Stack

`Python 3.10+` &bull; `pyyaml` &bull; `pytest` (209 tests) &bull; YAML-resident catalogs (air-gap-safe, no LLM dependency on disk-resident seeds) &bull; HuggingFace + vendor-doc refresh sources &bull; Citadel + Chancery + Folio + Forge Python bridges

<br>
</details>

<br>

---

<br>

## VI. Ecosystem Relationships

These twelve systems form a **complete agent governance, compilation, attestation, audit, RFP-validation, CoE-advisory, and product-lifecycle platform** with defense-grade hardening and federal compliance coverage. Each is an independent, standalone work. Integration between them does not diminish the independent IP status of any individual work.

```
┌──────────────────────────────────────────────────────────────────────┐
│                       CORE PLATFORM — the four Cs                     │
│                                                                      │
│  ┌────────────┐                                                      │
│  │  Citadel   │──> compliance-aware design intelligence              │
│  │ (design)   │    (fleet specs, compliance docs, behavioral policy) │
│  └─────┬──────┘                                                      │
│        │                                                             │
│        v                                                             │
│  ┌────────────┐      ┌────────────┐                                  │
│  │ Castellan  │─────>│  Charlotte │  (compilers produce specs)       │
│  │ (agents)   │      │  (context) │                                  │
│  └─────┬──────┘      └─────┬──────┘                                  │
│        │                    │                                         │
│        v                    v                                         │
│  ┌────────────────────────────────┐                                  │
│  │       Chronicle (attestation)  │  hybrid signing, OSCAL, ATO      │
│  │   sign → verify → Merkle-chain │  92 control mappings, 4 packs    │
│  └────────────────────────────────┘                                  │
│                                                                      │
├──────────────────────────────────────────────────────────────────────┤
│                            PRODUCTS                                   │
│                                                                      │
│   Audit Pro ───────> Productized audit of third-party agents.        │
│                      Chronicle-signed evidence + recompiled specs.   │
│                                                                      │
│   Chancery                                                           │
│   (AI CPO)      ──> PRDs + SDD bundles feed Charlotte + Castellan    │
│                                                                      │
│   Verity + Steward ──> Read Jira/Confluence/GitHub/Slack/Teams       │
│   (SM/PM)  (PO/PM)     surface intelligence, deliver reports         │
│                                                                      │
│   Reeve ───────────> Write Atlassian admin (governed, approval-gated)│
│                                                                      │
│   Author ──────────> Story/epic coaching with refusal layer          │
│                                                                      │
│   Quaestor ────────> RFP intelligence — judges federal solicitation  │
│                      responses; demonstrate-vs-namedrop calibration  │
│                                                                      │
│   Augur ───────────> AI Strategy + CoE advisor; evidence layer       │
│                      under Citadel/Chancery spec generators          │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘

Product Lifecycle Loop:
Chancery (discover) → Author (write) → Jira → Verity + Steward (read) → Reeve (admin)
                                              SM / PM      PO / PM       Atlassian

Audit Loop (third-party customers):
Customer agents → Audit Pro → Citadel scan + Castellan/Charlotte recompile
                            → Chronicle sign → 3PAO-verifiable evidence bundle

RFP Loop (federal procurement):
Solicitation .docx/.pdf → Quaestor judge → forensic verdict report
                                          + reproducibility envelope (SHA-384)

CoE Engagement Loop:
Stakeholder intake → Augur Discovery → Shortlist → Translate → Govern → Present
              (Augur's catalog feeds Citadel + Chancery for governed spec gen)
```

### The Governance Loop

1. **Design** &mdash; Chancery compiles PRDs and SDD bundles. Citadel generates governance-aware fleet specs and regulatory documentation.
2. **Build** &mdash; Charlotte compiles context/prompts/MCP servers. Castellan compiles agents. Both enforce compliance floors.
3. **Attest** &mdash; Chronicle signs runtime events with hybrid Ed25519 + ML-DSA-65; produces OSCAL packages and signed ATO bundles.
4. **Audit** &mdash; Audit Pro composes the engines into a customer-facing productized audit; emits Chronicle-signed evidence + drop-in recompiled specs.
5. **Operate** &mdash; Verity (SM/PM), Steward (PO/PM), Reeve (admin), Author (authoring), Chancery (PRDs) cover the product lifecycle. Quaestor judges federal RFP responses; Augur runs the CoE engagement and feeds the rest of the platform an evidence-backed model + framework + use-case catalog.

<br>

---

<br>

## VII. Terms & Conditions

<br>

### 1. Sole Ownership

The Declarant is the **sole author, inventor, and owner** of all works listed in this declaration. No other person or entity has contributed to, funded, or directed the development of these works.

### 2. Pre-Employment Creation

All works listed herein were created **prior to and independent of** any employment relationship with the receiving party. No employer resources, facilities, equipment, proprietary information, or trade secrets were used in their creation.

### 3. Exclusion from Assignment

All works listed in this declaration &mdash; including all source code, documentation, architectures, designs, algorithms, test suites, build configurations, deployment scripts, and any derivative works thereof &mdash; are **explicitly excluded** from any intellectual property assignment clause in any employment agreement between the Declarant and the receiving party.

### 4. Continued Development

The Declarant **reserves the right** to continue developing, modifying, licensing, distributing, selling, or otherwise exploiting these works during and after any employment relationship, provided such activities do not utilize the employer's proprietary information or resources.

### 5. No Implied License

Nothing in any employment agreement shall be construed as granting the employer **any license, right, title, or interest** in any of the works listed herein.

### 6. Derivative Works

Any improvements, enhancements, extensions, or derivative works based on the Prior IP listed herein, made on the Declarant's own time and without use of employer resources, shall remain the **exclusive property of the Declarant**.

### 7. Completeness

This declaration represents a complete and accurate list of the Declarant's Prior IP as of the date of signing. The Declarant **reserves the right to amend** this declaration to include additional prior works that may have been inadvertently omitted.

<br>

---

<br>

## VIII. Signatures

<br>

### Declarant

| | |
|:--|:--|
| **Name** | ________________________________________________ |
| **Date** | ________________________________________________ |
| **Signature** | ________________________________________________ |

<br>

### Receiving Party (Employer)

By signing below, the receiving party **acknowledges receipt** of this Prior Intellectual Property Declaration and agrees that the works described herein are **excluded from any intellectual property assignment provisions** in any employment agreement between the parties.

| | |
|:--|:--|
| **Representative Name** | ________________________________________________ |
| **Title** | ________________________________________________ |
| **Company** | ________________________________________________ |
| **Date** | ________________________________________________ |
| **Signature** | ________________________________________________ |

<br>

---

<div align="center">

<br>

*This document is a legal declaration of prior intellectual property ownership.*
*All works described herein are protected under applicable copyright, patent, and trade secret laws.*

<br>

**All Rights Reserved.**

<br>

</div>
