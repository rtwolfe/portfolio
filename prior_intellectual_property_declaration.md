<div align="center">

# PRIOR INTELLECTUAL PROPERTY DECLARATION

### Formal Declaration of Sole Ownership & Exclusion from Assignment

---

**16 Software Systems** &nbsp;&bull;&nbsp; **19,400+ Automated Tests** &nbsp;&bull;&nbsp; **365,000+ Lines of Code** &nbsp;&bull;&nbsp; **All Rights Reserved**

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
                    CASTELLAN AGENT & MCP GOVERNANCE PLATFORM
    ___________________________________________________________________________

    COMPILE         ENFORCE         AUDIT           COMMUNICATE     MONITOR
    ___________________________________________________________________________

    Castellan       Seneschal       Aegis           Herald          Vigil
    (Agent          (On-Prem        (Security       (Command        (Fleet
     Compiler)       Runtime)        Audit)          Channel)        Dashboard)

    Charlotte                       SCAN
    (Prompt                         Recon
     Compiler)                      (Governance
                                     Scanner)
    ___________________________________________________________________________

                            AUTOMATION TOOLING
    ___________________________________________________________________________

    QUALITY         DESIGN          INTELLIGENCE    VALIDATE
    ___________________________________________________________________________

    Stratum         Designer-SDD    VC+             Agent-Test-
    (QA             (Spec           (Capital         Harness
     Compiler)       Compiler)       Intelligence)   (Governance
                                                      Tester)
    Gauntlet        Citadel         PRD+
    (Code           (Design         (PRD            Passport
     Adjudicator)    Intelligence)   Compiler)       (Agent
                                                      Passports)
                                    Agent-
                                    Dissector
                                    (Opportunity
                                     Mapper)
    ___________________________________________________________________________
```

</div>

<br>

<div align="center">

| Metric | Value |
|:---|:---|
| **Total Software Systems** | 16 |
| **Combined Automated Tests** | 19,400+ |
| **Estimated Lines of Code** | 365,000+ |
| **Quality Gates & Checks** | 100+ |
| **Compliance Standards Covered** | 16+ (EU AI Act, NIST AI RMF, NIST 800-53, NIST CSF 2.0, GDPR, HIPAA, PCI-DSS v4.0, SOC 2 Type II, ISO 42001, ISO 27001, FZ-152, OWASP Top 10, CoSAI, FedRAMP, FIPS 140-3, DoD STIG) |
| **Status** | All systems complete and operational |

</div>

<br>

---

<br>

## V. Schedule of Prior Intellectual Property

<br>

### Castellan Agent & MCP Governance Platform

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>1 &mdash; Castellan &nbsp;&nbsp;<sub>Spec-Driven Agent Development Framework</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Framework &mdash; Python CLI |
| **Version** | `0.5.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 7,310+ automated tests |
| **Source Lines** | 118,014 |
| **Status** | Complete and operational |

#### Description

Castellan is a spec-driven agent development framework and agentic compiler. It takes YAML agent specifications and compiles them through a **6-stage pipeline** (parse, compose, optimize, validate, scan, render) into executable, validated AI agents with structural governance. Features include 87 CLI commands, multi-provider support (Anthropic, OpenAI, Google), constitutional governance, runtime guardrails, OWASP security auditing, circuit breaker patterns, multi-agent orchestration, A2A protocol support, MCP client, and 7 deployment targets with embedded governance across LangGraph, CrewAI, AutoGen, and Haystack. Includes **OpenClaw governance** (C17) &mdash; a transparent WebSocket gateway proxy for the OpenClaw open-source agent platform (247K+ GitHub stars), with per-channel policy enforcement, skill supply chain scanning (22 detection patterns across 6 threat categories), 4-dimensional trust scoring, output filtering with PII redaction, tamper-evident attestation chains, and rate limiting.

#### Compliance & Regulatory Coverage

Castellan includes a full **compliance engine** (27+ modules) covering:

| Standard | Implementation |
|:---|:---|
| **EU AI Act** | Risk tier classification, article-by-article compliance assessment |
| **HIPAA** (45 CFR 164) | Administrative, Physical, Technical safeguard mapping; HHS AI Guidance |
| **PCI-DSS v4.0** | 6-goal compliance mapping with AI/ML supplement |
| **SOC 2 Type II** | Dual-mode evidence generation for audit |
| **NIST AI RMF** | Governance-to-function/category alignment |
| **NIST 800-53** | 30+ federal security control patterns |
| **NIST IR 8596 / CSF 2.0** | CAISI AI Agent Standards Initiative, 6-function structure |
| **ISO 42001** | AI management system mapping |
| **GDPR Article 22** | Automated decision-making rights, erasure support |
| **FZ-152** | Data protection assessment |
| **FINRA 2026** | Financial regulatory assessment |
| **FedRAMP** | Federal risk authorization |
| **OWASP Agentic Security** | Full Top 10 vulnerability mapping (ASI01&ndash;ASI10) |

Additional compliance features: SHA-256 tamper-evident attestation chains, system card generation (NIST/EU AI Act aligned), compliance manifests with regulatory classification, DoD delivery packages (SSP, CMR, integration guides), typed governance models (autonomy ceiling, human oversight, data sensitivity, trust policy, memory governance, identity, capability scope), agentic JWT with PoP keys and delegation chains, A2A bilateral policy enforcement, and CBRA 4-dimension risk scoring.

#### Architecture

```
agent.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Scan ] ──> [ Render ]
                                                                    │
                                                   ┌────────────────┼────────────────┐
                                                   v                v                v
                                              Constitutional    Circuit          Plugin Gates
                                              Governance +      Breaker          (Provider, Tool,
                                              Compliance Engine                   Gate, Exporter)
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `tiktoken` &bull; `httpx` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>2 &mdash; Seneschal &nbsp;&nbsp;<sub>On-Premises Governed Agent Infrastructure</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Rust Binary |
| **Version** | `2.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 119+ automated tests |
| **Source Lines** | 15,633 (Rust) |
| **Status** | Complete and operational |

#### Description

Seneschal is the on-premises runtime authority for the Castellan agent governance platform. It enforces policy gates for all agent-to-agent (A2A) and agent-to-MCP-server communication, manages dual-node registration (Castellan agents + Charlotte MCP servers), maintains tamper-evident attestation chains, and provides FIPS 140-3 cryptographic operations via `aws-lc-rs`. Designed for **air-gapped and classified environments** with full autonomous operation independent of cloud connectivity.

#### Compliance & Security Architecture

| Capability | Standard / Implementation |
|:---|:---|
| **Identity** | SPIFFE/SPIRE (CNCF-graduated) &mdash; X.509 SVIDs, trust domain management, mTLS credential provisioning |
| **Messaging** | MLS RFC 9420 (IETF-ratified) &mdash; encrypted group messaging with forward secrecy |
| **Cryptography** | FIPS 140-3 via `aws-lc-rs` &mdash; Ed25519-Dalek, AES-GCM, SHA-256 |
| **Classification** | CDS governance across 6 levels: Unclassified, FOUO, CUI, SECRET, TOP SECRET, TS/SCI |
| **DoD Alignment** | Zero Trust Architecture, CAC/PKI authentication, STIG compliance |
| **Federation** | NIST CAISI compliance (checks 17&ndash;23) for cross-organization trust |
| **Authentication** | Operator-mTLS, delegation certificates signed with Ed25519 root keys |

**Policy Gates:** 7-check A2A gate (delegation scope, JWT verification, bilateral policy, autonomy gating, data flow control, rate limiting, trust scoring) + 8-check MCP gate (node validation, status checks, policy existence, kill switch, agent permission, server trust, tool access control, rate limiting). 25 named violation types &mdash; all rule-based, fully explainable.

**Attestation Chain:** Append-only SHA-256 hash chain with 32 event types across 6 categories (governance, security, infrastructure, operational, audit, federation). Tamper-evident, immutable, with upstream Herald sync.

#### Architecture

```
                    ┌─────────────────────────────────────────┐
                    │            Seneschal                     │
                    │                                         │
                    │  Layer 4: Identity (SPIFFE/SPIRE)       │
                    │  Layer 3: The Record (Attestation)      │
                    │  Layer 2: The Brain (Policy Gates)      │
                    │  Layer 1: The Fabric (MLS Messaging)    │
                    │                                         │
                    │  ┌─────────┐      ┌─────────────────┐  │
                    │  │ Agents  │◄────►│  MCP Servers     │  │
                    │  │(Castellan)     │ (Charlotte)      │  │
                    │  └─────────┘      └─────────────────┘  │
                    │         ▲                               │
                    │         │ Herald Sync (when connected)  │
                    └─────────┼───────────────────────────────┘
                              │
                         [ Herald ]
```

#### Technology Stack

`Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `SQLite (rusqlite)` &bull; `Ed25519-Dalek` &bull; `AES-GCM` &bull; `Clap` &bull; `Tracing`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>3 &mdash; Charlotte &nbsp;&nbsp;<sub>Prompt Compiler & Application Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `2.3.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 3,034+ automated tests |
| **Source Lines** | 34,045 |
| **Status** | Complete and operational |

#### Description

Charlotte transforms prompt engineering into **structured, validated, composable software engineering** through a 5-stage pipeline (Parse, Compose, Optimize, Validate, Render). It includes 94 built-in block templates across 17 types, 30 assertion types for testing, multi-provider rendering (OpenAI, Anthropic, Google Gemini), environment management, GitHub Actions CI generation, multi-prompt workflow chaining, Claude Code skill compilation, and MCP server generation with full DoD hardening support.

#### Compliance & Security Scanning

Charlotte implements **89 security patterns across 22 categories** with deep defense/federal compliance coverage:

| Capability | Implementation |
|:---|:---|
| **DoD Patterns** | 35+ detection patterns aligned to NIST 800-53 control families (AC, AU, IA, SC, SI, CM, CP, IR, RA, SA) |
| **STIG Export** | Full checklist generation with vulnerability IDs (V-222400 format), CAT I&ndash;III severity, status tracking |
| **FIPS 140-3** | Non-FIPS algorithm detection (MD5, weak crypto), FIPS transport requirement validation |
| **mTLS / CAC** | Mutual TLS enforcement, Common Access Card / PKI authentication support |
| **Classification Banners** | CUI, UNCLASSIFIED//FOUO, SECRET, TOP SECRET display enforcement |
| **MCP DoD Hardening** | TLS 1.2+, AES-256, non-root containers, read-only filesystems, capability dropping |
| **CoSAI Threat Model** | MCP-T1 (session token leakage), MCP-T2 (tenant isolation), MCP-T6 (shadow servers), MCP-T9 (consent fatigue) |
| **Audit Format** | JSON, CEF (ArcSight/SIEM), Syslog (RFC 5424) export |
| **OWASP LLM Top 10** | Full coverage with red team testing alignment |

Includes `dod_governance_preset()` with FIPS requirement, mTLS, CAC authentication, and human approval enforcement. STIG profile support: full, cat1, cat2, none. Seneschal integration adapter for compliance enforcement propagation.

#### Architecture

```
prompt.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Render ]
                   │               │                │               │               │
              94 Block Types   Composition      Token Mgmt     30 Assertion    Multi-Provider
              17 Categories    & Chaining       & Budget       Types + 89      (OpenAI, Anthropic,
                                                               Security Checks  Google Gemini)
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `deepdiff` &bull; `watchdog` &bull; `tiktoken` &bull; `Anthropic/OpenAI/Google SDKs`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>4 &mdash; Aegis &nbsp;&nbsp;<sub>Pre-Deployment Security Audit for AI Agents</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | February 2026 |
| **Test Suite** | 675+ automated tests |
| **Source Lines** | 20,017 |
| **Status** | Complete and operational |

#### Description

Aegis is a pre-deployment security audit service for AI agents. It orchestrates multiple analysis tools into a unified five-stage pipeline that performs **three audit layers** (prompt, behavior, code) in parallel, conducts cross-layer analysis with six static graph analyzers and three behavioral probes, maps findings to **OWASP Top 10 for Agentic Applications**, and produces scored, evidence-backed security reports with exploit tests proving vulnerabilities and remediation tests verifying fixes. Compliance mapping to EU AI Act, NIST AI RMF, ISO 42001, CoSAI, and NIST 800-53.

#### Architecture

```
Intake ──> [ Prompt Audit (54 checks) ]──┐
           [ Behavior Audit (22 patterns) ]├──> Cross-Layer Analysis ──> Scored Report
           [ Code Audit (11 detectors) ]───┘
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `concurrent.futures` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>5 &mdash; Herald &nbsp;&nbsp;<sub>Authenticated Command Channel for Agent Fleets</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Library &mdash; Python |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 219+ automated tests |
| **Source Lines** | 3,596 |
| **Status** | Complete and operational |

#### Description

Herald is an authenticated bidirectional command channel between operator portals and deployed agent fleets. It provides a complete command loop with **HMAC-SHA256 signed message envelopes**, supporting message types for query, config_update, broadcast, and recall operations with constitutional bounds enforcement and full audit trail logging. Includes governed A2A inter-agent communication, MCP tool governance gateway with OAuth 2.1 + DPoP, and non-human identity (NHI) registry with trust protocol support (Visa TAP, CSA ATF, W3C Verifiable Credentials, Microsoft Entra Agent ID).

#### Architecture

```
Operator Portal ──[ HMAC-SHA256 Signed Envelope ]──> Agent Fleet
                                                         │
         ┌───────────────────────────────────────────────┘
         v
    [ Query | Config Update | Broadcast | Recall ]
         │
         v
    Constitutional Bounds ──> A2A Gateway ──> MCP Gateway ──> Audit Trail (JSONL)
```

#### Technology Stack

`Python 3.10+` &bull; `Pydantic v2` &bull; `httpx`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>6 &mdash; Recon &nbsp;&nbsp;<sub>Agent Governance Reverse-Engineering Scanner</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 2,705+ automated tests |
| **Source Lines** | 44,596 |
| **Status** | Complete and operational |

#### Description

Recon is a 3-stage pipeline that **reverse-engineers governance contracts** from AI agent source code. It scans agents across 21 framework adapters (Python, LangChain, LangGraph, CrewAI, AutoGen, OpenAI Agents, AWS Bedrock, Google ADK, and more) and produces comprehensive governance audit packages including reconstructed agent specs with confidence annotations, compliance manifests, OWASP scorecards, AI SBOM, and assessments across **11 international standards**.

#### Compliance Standards

| Standard | Domain |
|:---|:---|
| EU AI Act | European AI regulation |
| NIST AI RMF | US federal AI risk management |
| OWASP LLM Top 10 | Agentic application security |
| GDPR | European data protection |
| HIPAA | US healthcare privacy |
| PCI-DSS | Payment card security |
| SOC 2 | Service organization controls |
| ISO 42001 | AI management systems |
| ISO 27001 | Information security |
| FZ-152 | Data protection |
| Cross-Standard | Synthesis across all standards |

#### Technology Stack

`Python 3.10+` &bull; `PyYAML` &bull; `pathspec` &bull; `Anthropic SDK` &bull; `tree-sitter`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>7 &mdash; Vigil &nbsp;&nbsp;<sub>Fleet Governance & Health Dashboard</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Application &mdash; Full-Stack Web |
| **Version** | `0.3.2` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 185+ automated tests |
| **Source Lines** | 15,632 (8,308 Python + 7,324 TypeScript) |
| **Status** | Complete and operational |

#### Description

Vigil is a fleet health, compliance, and governance dashboard for AI agents. It is a **multi-tenant portal** that ingests HMAC-signed health packets from deployed agents, evaluates governance compliance, fires alerts on threshold breaches, and serves real-time dashboards. Features include 20 database tables, 69 API endpoints, WebSocket real-time events, cost governance, incident management, A2A communication tracking, attestation chain verification, kill switch management, recertification cycles, and Herald fleet command integration.

#### Architecture

```
Agent Fleet ──[ HMAC Health Packets ]──> Ingestion API
                                              │
                    ┌─────────────────────────┼─────────────────────────┐
                    v                         v                         v
             Compliance Engine          Alert Engine              Cost Tracker
                    │                         │                         │
                    └─────────────────────────┼─────────────────────────┘
                                              v
                                    ┌─────────────────────┐
                                    │  Real-Time Dashboard │
                                    │  (WebSocket + SSE)   │
                                    └─────────────────────┘
```

#### Technology Stack

**Backend:** `Python 3.11+` &bull; `FastAPI` &bull; `SQLAlchemy 2.0 (async)` &bull; `Pydantic v2`

**Frontend:** `Next.js 16` &bull; `React 19` &bull; `TypeScript` &bull; `Tailwind CSS 4` &bull; `shadcn/ui` &bull; `Recharts 3`

**Infrastructure:** `PostgreSQL + TimescaleDB` &bull; `SQLite` &bull; `Redis` &bull; `Clerk JWT`

<br>
</details>

<br>

### Automation Tooling

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>8 &mdash; Stratum &nbsp;&nbsp;<sub>Unified Code Quality & Architecture Pipeline</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 4,322+ automated tests |
| **Source Lines** | 73,508 |
| **Status** | Complete and operational |

#### Description

Stratum is a unified code quality, architecture extraction, test generation, and documentation pipeline. It consolidates **8 quality gates** and executes a pipeline with 3-layer context extraction across 6 languages, test generation across 4 frameworks, documentation rendering with 7 independent analyzers, and comprehensive validation across **13 modules**.

#### Architecture

```
┌─────────────────────────────────────────────────────────┐
│                      STRATUM                            │
├──────────┬──────────┬──────────┬──────────┬─────────────┤
│ Arbiter  │ Forge    │ Candor   │ Sentinel │ Hydra       │
│ (Rules)  │ (7 Laws) │ (Report) │ (Watch)  │ (Parallel)  │
├──────────┼──────────┼──────────┼──────────┼─────────────┤
│ Specter  │Chronicle │ Aegis    │ Prophet  │ Oracle      │
│ (Ghost)  │ (History)│ (Secure) │ (Predict)│ (Analyze)   │
├──────────┼──────────┴──────────┴──────────┴─────────────┤
│ Mimic    │ Verdict                                      │
│ (Mirror) │ (Final Judgment)                              │
└──────────┴──────────────────────────────────────────────┘

Context Extraction:  L1 Skeleton (AST) ──> L2 Feature Slices ──> L3 Cross-Cutting
```

#### Technology Stack

`Python 3.10+` &bull; `Click` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `tree-sitter` &bull; `tiktoken` &bull; `Anthropic SDK` &bull; `weasyprint` &bull; `watchdog`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>9 &mdash; Designer-SDD &nbsp;&nbsp;<sub>Spec-Driven Documentation Generator</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 693+ automated tests |
| **Source Lines** | 8,258 |
| **Status** | Complete and operational |

#### Description

Designer-SDD converts JSON specifications into **complete, GitHub-ready documentation packages**. It produces standardized artifacts (CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, RESEARCH.md, HANDOFF.md, README.md) with tier-gated extras. Features include dual-gate scoring (Quality: 28 checks, Buildability: 8 checks), iterative AI refinement (up to 3 passes), round-trip verification, interactive brainstorming, web-powered market research, and browser-based intake forms.

#### Architecture

```
spec.json ──> [ Dual-Gate Scoring ]──> [ AI Refinement (x3) ] ──> [ Tier-Gated Export ]
                    │                                                     │
              Quality: 28 checks                                    7 / 9 / 11 files
              Buildability: 8 checks                              (by project size)
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Anthropic SDK` &bull; `PyYAML` &bull; `Rich`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>10 &mdash; Gauntlet &nbsp;&nbsp;<sub>Code Adjudication System</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 115+ automated tests |
| **Source Lines** | 4,427 |
| **Status** | Complete and operational |

#### Description

Gauntlet is a code adjudication system built to catch AI-generated code failures before production. It features a **3-layer pipeline** with a mechanical layer (file walker, parser, chunker, dependency mapper via tree-sitter), an intelligence layer (18 domain adjudicators across 21 Charlotte-compiled prompts), and a reporting layer. Includes a universal JSON output contract, an integrated OODA loop (Observe &rarr; Orient &rarr; Decide &rarr; Act) for self-correction with re-scanning for stability, and a guardrail block preventing prompt injection. 21 adjudicator prompts span orchestration, correctness, security, architecture, quality, risk, and integrity domains.

#### Architecture

```
Repository ──> [ Mechanical Layer ]──> [ Intelligence Layer ]──> [ Reporting Layer ]
                  │                        │                          │
             Walker, Parser,          18 Adjudicators            Severity-Ranked
             Chunker, Deps            (21 Prompts)               Verdict
                                           │
                                      [ OODA Loop ]
                                      (Re-scan for stability)
```

#### Technology Stack

`Python 3.10+` &bull; `Anthropic SDK` &bull; `Click` &bull; `Pydantic v2` &bull; `PyYAML` &bull; `Rich` &bull; `tree-sitter`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>11 &mdash; Citadel &nbsp;&nbsp;<sub>Unified Design Intelligence Platform</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI + MCP Server |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 117+ automated tests |
| **Source Lines** | 4,558 |
| **Status** | Complete and operational |

#### Description

Citadel is a compliance-aware design intelligence front end for the Castellan and Charlotte compilers. It reads live from both compiler codebases, iterates on designs conversationally, and produces **compiler-ready specs with wiring already done**. Two operating modes: interactive CLI (via Anthropic API) and FastMCP server (for MCP clients). Features 14 FastMCP tools for codebase introspection, spec generation, validation, and decomposition. Governance-aware with compliance profile support covering FedRAMP, DoD IL4/IL5, HIPAA, SOC 2, PCI-DSS, EU AI Act, and GDPR. AST-based Pydantic model extraction with provenance chains.

#### Architecture

```
Compiler Codebase ──> [ AST Introspection ] ──> [ Design Intelligence ] ──> Compiler-Ready Spec
       │                     │                          │
  Castellan +           14 FastMCP Tools          Compliance Profile
  Charlotte              (5 introspect,            Resolution
                          2 generate,               (7 frameworks)
                          2 validate,
                          3 design,
                          2 decompose)
```

#### Technology Stack

`Python 3.10+` &bull; `MCP[cli] 1.0+` &bull; `Pydantic v2` &bull; `PyYAML` &bull; `Typer` &bull; `Rich` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>12 &mdash; VC+ &nbsp;&nbsp;<sub>Capital Intelligence System</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | MCP Server Suite + Multi-Agent Pipeline |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Source Lines** | 5,537 |
| **Status** | Complete and operational |

#### Description

VC+ is a multi-agent capital intelligence pipeline that helps founders find VC, PE, growth equity, and M&A capital through pattern matching and live data gathering. Runs on Claude Code Max where Claude is the runtime and MCP servers are the data layer. Features a **5-stage pipeline** (Router &rarr; Research &rarr; Analysis &rarr; Intelligence &rarr; Dossier) with live data from SEC EDGAR, Crunchbase, NewsAPI, and website scanning. Three operating modes: company &rarr; capital path matching, market queries for capital opportunities, and firm intelligence dossiers. Includes 52K tokens of domain knowledge (glossary, frameworks, red flag library) and data contracts via Pydantic.

#### Architecture

```
Query ──> [ Router ] ──> [ Research ] ──> [ Analysis ] ──> [ Intelligence ] ──> [ Dossier ]
                              │
                    ┌─────────┼─────────┐
                    v         v         v
              SEC EDGAR   Crunchbase  NewsAPI
              Scanner     API         Scanner
```

#### Technology Stack

`Python 3.11+` &bull; `FastMCP` &bull; `httpx` &bull; `BeautifulSoup` &bull; `lxml` &bull; `Pydantic v2` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>13 &mdash; PRD+ &nbsp;&nbsp;<sub>AI CPO PRD Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | AI Prompt System &mdash; Charlotte-Compiled |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Status** | Complete and operational |

#### Description

PRD+ is a Charlotte-compiled AI Chief Product Officer that normalizes any natural-language product input, researches competitive landscape in real time, challenges assumptions with evidence, and compiles **production-quality PRDs grounded in market reality**. Operates as a 20-year veteran CPO executing a 13-step workflow with multi-turn state tracking, evaluation checklists (29 items, 90% threshold), and a post-PRD pipeline producing 5 artifacts. Two variants: full Agent Orchestrating (13 blocks, 13,615 tokens) and Skill (6 blocks, 5,253 tokens). Includes integrated compliance framework library with 5 tool definitions for artifact generation.

#### Architecture

Two Charlotte-compiled implementations with 4-stage pipeline: Parse &rarr; Compose &rarr; Validate &rarr; Render. 13-block composition (System Identity, Guardrails, Safety, Routing, Task, Few-Shot, CoT, Tools, State Management, ReAct Agent, Evaluation).

#### Technology Stack

`Charlotte Prompt Compiler` &bull; `Claude Opus 4.6`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>14 &mdash; Agent-Dissector &nbsp;&nbsp;<sub>Domain Agent Opportunity Mapper</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | AI Prompt System &mdash; Charlotte-Compiled |
| **Version** | `1.0.0` |
| **Initial Development** | March 2026 |
| **Source Lines** | 1,886 |
| **Status** | Complete and operational |

#### Description

Agent-Dissector is a governance-ready AI automation opportunity intelligence platform. It operates in two modes: **Panoramic** (given a domain, produces complete briefing covering what AI agents/MCP servers should be built, in what order, with what governance) and **Targeted** (corrects decomposition, produces governance-ready cards, generates intake briefs). Five-layer analytical workflow producing six structured output sections per dissection with 15&ndash;40+ opportunity cards per domain. Features autonomy classification (Agent vs MCP Server vs Agent+MCP), OTS tool landscape assessment, governance tiering (8 data classification levels, compliance framework mapping), three-wave implementation roadmaps (0&ndash;90, 90&ndash;180, 180&ndash;365 days), and explicit human-in-the-loop flagging for privilege-sensitive zones.

#### Architecture

Two Charlotte-compiled implementations: a full agent-orchestrating system (10 blocks, 7,507 tokens) and a multi-phase skill version (6 blocks, 4,653 tokens).

#### Technology Stack

`Charlotte Prompt Compiler` &bull; `Claude Opus 4.6` &bull; `Claude Sonnet 4.6`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>15 &mdash; Agent-Test-Harness &nbsp;&nbsp;<sub>Agent Governance Test Harness</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | AI Prompt System &mdash; Charlotte-Compiled |
| **Version** | `1.0.0` |
| **Initial Development** | March 2026 |
| **Source Lines** | 10,677 |
| **Status** | Complete and operational |

#### Description

Agent-Test-Harness is a Charlotte-compiled orchestrating agent that validates AI agents against their Castellan governance contracts and A2A channels through Seneschal. It exercises constitutional compliance, bilateral policy gate enforcement, attestation chain verification, and runtime guardrail enforcement. Features **eight assertion types** covering governance boundary testing from prompt injection resistance to kill switch responsiveness, spec-derived assertion generation, and Aegis-compatible output format. Uses a 5-layer stack: Spec Loader &rarr; Discovery Runner &rarr; Scenario Sequencer &rarr; Assertion Engine &rarr; Reporter.

#### Architecture

Charlotte-compiled agent-orchestrating system (12 blocks, 11,148 tokens) with spec-derived assertion framework.

```
Agent Artifact ──> [ Extract Governance Contract ]
                   [ Generate Spec-Derived Assertions ]
                   [ Execute 8 Assertion Types ]
                        │
                        v
                   Aegis-Compatible Evidence Package
```

#### Technology Stack

`Charlotte Prompt Compiler` &bull; `Claude Opus 4.6`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>16 &mdash; Passport &nbsp;&nbsp;<sub>Agent Passport Generator</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | AI Prompt System &mdash; Charlotte-Compiled |
| **Version** | `1.0.0` |
| **Initial Development** | March 2026 |
| **Source Lines** | 4,676 |
| **Status** | Complete and operational |

#### Description

Passport is a Charlotte-compiled multi-phase system that reads any AI agent artifact and produces structured **Agent Passports** &mdash; self-contained HTML documents that document exactly what an agent is, how it's configured, what tools and capabilities it has, and what governance gaps exist. It processes artifacts across all major frameworks (Castellan YAML, LangChain, LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, MCP manifests, raw system prompts) and maintains an obsessive distinction between what is **configured** versus what is merely **implied**. The passport is documentation, not evaluation &mdash; trustworthy because it reports what's there, not what should be.

#### Architecture

Charlotte-compiled multi-phase system (9 blocks, 8,014 tokens) with field extraction pipeline and HTML passport rendering.

```
Agent Artifact ──> [ Identify Framework Format ]
                   [ Extract Identity & Configuration ]
                   [ Map Capabilities & Tools ]
                   [ Document Constraints & Guardrails ]
                   [ Flag Governance Gaps ]
                        │
                        v
                   Self-Contained HTML Agent Passport
```

#### Technology Stack

`Charlotte Prompt Compiler` &bull; `Claude Sonnet 4.6`

<br>
</details>

<br>

---

<br>

## VI. Ecosystem Relationships

These sixteen systems form a **complete agent governance, compliance, and lifecycle platform**. Each is an independent, standalone work. Integration between them does not diminish the independent IP status of any individual work.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   CASTELLAN AGENT & MCP GOVERNANCE PLATFORM                              │
│   ──────────────────────────────────────────                             │
│                                                                          │
│   COMPILE              ENFORCE              AUDIT                        │
│   Castellan ─────────> Seneschal            Aegis                        │
│   (Agent Compiler)     (On-Prem Runtime)    (Security Audit)             │
│                                                                          │
│   Charlotte            COMMUNICATE          SCAN                         │
│   (Prompt Compiler)    Herald               Recon                        │
│                        (Command Channel)    (Reverse-Engineer)           │
│                             │                    │                       │
│                             └──────> MONITOR <───┘                       │
│                                      Vigil                               │
│                                      (Fleet Dashboard)                   │
│                                                                          │
│                                                                          │
│   AUTOMATION TOOLING                                                     │
│   ──────────────────                                                     │
│                                                                          │
│   QUALITY              DESIGN               INTELLIGENCE                 │
│   Stratum              Designer-SDD         VC+                          │
│   (QA Compiler)        (Spec Compiler)      (Capital Intel)              │
│                                                                          │
│   Gauntlet             Citadel              PRD+                         │
│   (Code Adjudicator)   (Design Intel)       (PRD Compiler)               │
│                                                                          │
│   VALIDATE                                  Agent-Dissector              │
│   Agent-Test-Harness   Passport             (Opportunity Mapper)         │
│   (Governance Tester)  (Agent Passports)                                 │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

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
