<div align="center">

# PRIOR INTELLECTUAL PROPERTY DECLARATION

### Formal Declaration of Sole Ownership & Exclusion from Assignment

---

**14 Software Systems** &nbsp;&bull;&nbsp; **19,800+ Automated Tests** &nbsp;&bull;&nbsp; **398,000+ Lines of Code** &nbsp;&bull;&nbsp; **18+ Compliance Standards** &nbsp;&bull;&nbsp; **All Rights Reserved**

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

    COMPILE         AUDIT           COMMUNICATE     SCAN        DESIGN
    ___________________________________________________________________________

    Castellan       Aegis           Herald          Recon       Citadel
    (Agent          (Security       (Command        (Governance (Design
     Compiler)       Audit)          Channel)        Scanner)    Intelligence)

    Charlotte                       Drawbridge
    (Prompt                         (Cross-Org
     Compiler)                       A2A Bridge)

    ┌─ Castellan Sub-Components ──────────────────────────────────────┐
    │  SENESCHAL (On-Prem Runtime)  vigil-edge (Behavioral Monitor)  │
    │  Citadel-edge (Air-Gapped Policy Manager)                      │
    └────────────────────────────────────────────────────────────────┘
    ___________________________________________________________________________

                        AUTOMATION & UTILITY TOOLING
    ___________________________________________________________________________

    QUALITY         INTELLIGENCE    PRD             PLUGINS
    ___________________________________________________________________________

    Stratum         VC+             Chancery        CoWork
    (QA             (Capital        (AI CPO         (Governed
     Compiler)       Intelligence)   PRD Compiler)   Plugin Designer)

    Gauntlet
    (Code
     Adjudicator)
    ___________________________________________________________________________

                        DOMAIN-SPECIFIC PLATFORMS
    ___________________________________________________________________________

    LEGAL                           MEDICAL
    ___________________________________________________________________________

    LawClaw                         Rampart
    (ABA-Governed                   (HIPAA-Governed
     Legal Plugins)                  Clinical Telemetry)
    ___________________________________________________________________________
```

</div>

<br>

<div align="center">

| Metric | Value |
|:---|:---|
| **Total Software Systems** | 14 |
| **Combined Automated Tests** | 19,800+ |
| **Estimated Lines of Code** | 398,000+ |
| **Quality Gates & Checks** | 100+ |
| **Compliance Standards Covered** | 18+ (EU AI Act, NIST AI RMF, NIST 800-53, NIST CSF 2.0/CAISI, CNSSP-12, CNSA 2.0, GDPR, HIPAA, PCI-DSS v4.0, SOC 2 Type II, ISO 42001, ISO 27001, FZ-152, OWASP Top 10, CoSAI, FedRAMP, FIPS 140-3, DoD STIG/IL4/IL5, ABA Model Rules, FINRA 2026, COPPA, HL7 FHIR) |
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
| **Type** | Software Framework &mdash; Python CLI + Rust Sub-Components |
| **Version** | `0.5.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 7,501+ automated tests |
| **Source Lines** | 145,730 (121,000 Python + 20,150 Rust SENESCHAL + 3,621 Rust vigil-edge + 959 Rust Citadel-edge) |
| **Status** | Complete and operational |

#### Description

Castellan is a spec-driven agent development framework and agentic compiler. It takes YAML agent specifications and compiles them through a **6-stage pipeline** (parse, compose, optimize, validate, scan, render) into executable, validated AI agents with structural governance. Features include 104 CLI commands, multi-provider support (Anthropic, OpenAI, Google), constitutional governance, runtime guardrails, OWASP security auditing, circuit breaker patterns, multi-agent orchestration, A2A protocol support, MCP client, and 7 deployment targets with embedded governance across LangGraph, CrewAI, AutoGen, and Haystack. Includes **OpenClaw governance** (C17) &mdash; a transparent WebSocket gateway proxy for the OpenClaw open-source agent platform (247K+ GitHub stars), with per-channel policy enforcement, skill supply chain scanning (22 detection patterns across 6 threat categories), 4-dimensional trust scoring, output filtering with PII redaction, tamper-evident attestation chains, and rate limiting.

Castellan includes three hardened **Rust sub-components**:

- **SENESCHAL** &mdash; On-premises runtime authority. Enforces policy gates for all A2A and MCP communication. SPIFFE/SPIRE identity, FIPS 140-3 crypto via `aws-lc-rs`, MLS RFC 9420 encrypted messaging, CDS classification governance (Unclassified through TS/SCI), 15-check policy gates (7 A2A + 8 MCP), 100+ named violation types, 36+ event attestation chains. Tool integrity verification (SHA-384 manifest hashing, rug-pull detection), call chain governance (depth limits, circular detection, prohibited sequences), behavioral cost limits, and Drawbridge A2A support. Air-gapped operation for classified environments. 20,150 Rust LOC, 114 tests.
- **vigil-edge** &mdash; Edge behavioral monitoring agent. Reads JSONL telemetry from SENESCHAL, builds behavioral fingerprints, computes 5-dimensional governance scores (Policy 30%, Behavior 25%, Schema 20%, Candor 15%, Manifest 10%), detects anomalies via z-score analysis across 5 classes (behavioral drift, tool pattern, score, data flow, temporal). Tool rug-pull detection via SHA-256 manifest verification. 3,621 Rust LOC.
- **Citadel-edge** &mdash; Scoped policy management for air-gapped deployments. Loads HMAC-signed policy bundles, allows bounded operator adjustments within compliance profiles, validates against compliance floors (hard &mdash; cannot be violated). CNSA 2.0 crypto alignment (SHA-384). Crossing policy support for Drawbridge integration. 959 Rust LOC, 23 tests.

#### Compliance & Regulatory Coverage

Castellan includes a full **compliance engine** covering **18 regulatory frameworks**:

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
| **ISO 27001** | Information security management |
| **GDPR Article 22** | Automated decision-making rights, erasure support |
| **FZ-152** | Data protection assessment |
| **FINRA 2026** | Financial regulatory assessment |
| **FedRAMP** | Federal risk authorization (Low/Moderate/High) |
| **DoD IL4/IL5** | Impact level controls for defense environments |
| **CNSSP-12** | Classified environment compliance |
| **CNSA 2.0** | Post-quantum cryptographic alignment |
| **OWASP Agentic Security** | Full Top 10 vulnerability mapping (ASI01&ndash;ASI10) |
| **COPPA** | Children's privacy protection |

Additional compliance features: SHA-256/SHA-384 tamper-evident attestation chains, system card generation (NIST/EU AI Act aligned), compliance manifests with regulatory classification, DoD delivery packages (SSP, CMR, integration guides), typed governance models (autonomy ceiling, human oversight, data sensitivity, trust policy, memory governance, identity, capability scope), agentic JWT with PoP keys and delegation chains, A2A bilateral policy enforcement, CBRA 4-dimension risk scoring, SPIFFE/SPIRE identity with mTLS, FIPS 140-3 cryptography, MLS RFC 9420 encrypted messaging, CDS classification governance (Unclassified through TS/SCI), and air-gapped autonomous operation.

#### Architecture

```
agent.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Scan ] ──> [ Render ]
                                                                    │
                                                   ┌────────────────┼────────────────┐
                                                   v                v                v
                                              Constitutional    Circuit          Plugin Gates
                                              Governance +      Breaker          (Provider, Tool,
                                              Compliance Engine                   Gate, Exporter)

Rust Sub-Components:
┌─────────────────────────────────────────────────────────────────────┐
│  SENESCHAL          vigil-edge           Citadel-edge              │
│  (Runtime Auth)     (Behavioral Monitor) (Policy Manager)          │
│  15-check gates     5D scoring           CNSA 2.0 signing         │
│  SPIFFE/MLS/FIPS    Z-score anomalies    Compliance floors         │
│  100+ violations    Rug-pull detection   Drawbridge integration    │
└─────────────────────────────────────────────────────────────────────┘
```

#### Technology Stack

**Python:** `Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `tiktoken` &bull; `httpx` &bull; `Anthropic SDK`

**Rust (SENESCHAL):** `Rust 2021` &bull; `Tokio` &bull; `Axum` &bull; `rusqlite` &bull; `Ed25519-Dalek` &bull; `AES-GCM` &bull; `SHA-384` &bull; `Clap` &bull; `Tracing`

**Rust (vigil-edge):** `Rust 2021` &bull; `rusqlite` &bull; `SHA-256` &bull; `HMAC` &bull; `Clap` &bull; `Chrono`

**Rust (Citadel-edge):** `Rust 2021` &bull; `Clap` &bull; `SHA-384` &bull; `HMAC` &bull; `Serde`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>2 &mdash; Charlotte &nbsp;&nbsp;<sub>Prompt Compiler & Application Compiler</sub></h3></summary>

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

Includes `dod_governance_preset()` with FIPS requirement, mTLS, CAC authentication, and human approval enforcement. STIG profile support: full, cat1, cat2, none. SENESCHAL integration adapter for compliance enforcement propagation.

#### Architecture

```
prompt.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Render ]
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
<summary><h3>3 &mdash; Aegis &nbsp;&nbsp;<sub>Pre-Deployment Security Audit for AI Agents</sub></h3></summary>

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
<summary><h3>4 &mdash; Herald &nbsp;&nbsp;<sub>Authenticated Command Channel for Agent Fleets</sub></h3></summary>

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
<summary><h3>5 &mdash; Recon &nbsp;&nbsp;<sub>Agent Governance Reverse-Engineering Scanner</sub></h3></summary>

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
<summary><h3>6 &mdash; Citadel &nbsp;&nbsp;<sub>Unified Design Intelligence Platform</sub></h3></summary>

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
<summary><h3>7 &mdash; Drawbridge &nbsp;&nbsp;<sub>Governed A2A Communication Backbone</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software System &mdash; Python CLI + Gateway |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 127+ automated tests |
| **Source Lines** | 4,180 |
| **Status** | Complete and operational |

#### Description

Drawbridge is the governed agent-to-agent (A2A) communication backbone for cross-organizational coordination. Two sovereign agent territories coordinate through encrypted channels with **CNSA 2.0 cryptographic proof** of every policy decision. Designed for DoD TS/SCI deployment with **CNSSP-12** as the compliance floor.

#### Compliance & Security Architecture

| Capability | Standard / Implementation |
|:---|:---|
| **Cryptography** | CNSA 2.0 &mdash; SHA-384 for all hashing, HMAC-SHA384 for signing, constant-time comparison |
| **Post-Quantum** | Drawbridge Plus &mdash; X25519+ML-KEM-1024 key exchange, Ed25519+ML-DSA-87+SLH-DSA-256 signing |
| **Replay Protection** | Persistent nonce tracking (SQLite), survives restarts |
| **Classification** | CNSSP-12 compliance floor for classified environments |
| **Attestation** | SHA-384 linked chain, immutable, append-only |
| **Kill Switch** | Cross-organizational propagation &mdash; revocation blocks all further communication |

**Bilateral Crossing Gate (7 checks):** peer not blocked, peer in allowlist, message type allowed, payload size limits, TTL bounds, non-expired, rate limit. Both sides check independently.

#### Architecture

```
Territory A                                         Territory B
┌────────────┐                                     ┌────────────┐
│ Agent Fleet │──[ CNSA 2.0 Signed Envelope ]─────>│ Agent Fleet │
│             │<─[ Bilateral Gate (7 checks) ]─────│             │
│  SENESCHAL  │                                     │  SENESCHAL  │
└────────────┘                                     └────────────┘
                    Persistent Nonce Tracking
                    SHA-384 Attestation Chain
                    Kill Switch Propagation
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `httpx` &bull; `PyYAML` &bull; `Rich` &bull; `FastAPI` (optional gateway)

<br>
</details>

<br>

### Automation & Utility Tooling

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
<summary><h3>9 &mdash; Gauntlet &nbsp;&nbsp;<sub>Code Adjudication System</sub></h3></summary>

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
<summary><h3>10 &mdash; VC+ &nbsp;&nbsp;<sub>Capital Intelligence System</sub></h3></summary>

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
<summary><h3>11 &mdash; Chancery &nbsp;&nbsp;<sub>AI Chief Product Officer &mdash; PRD Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI + MCP Server |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Source Lines** | 11,817 |
| **Status** | Complete and operational |

#### Description

Chancery is an AI Chief Product Officer that transforms unstructured product input (voice transcripts, Slack threads, meeting notes, emails, bullet points) into **production-quality PRDs** through a disciplined 3-phase, 3-gate workflow with deterministic quality scoring. Features 30-item quality checklist (21 code-evaluated, 9 AI-evaluated), 7 cognitive bias detection with reframing challenges, and structured output targeting downstream toolchains.

#### Compliance Framework Detection

Chancery automatically detects when a product touches regulated domains, identifying **10 compliance frameworks**:

| Framework | Detection Triggers |
|:---|:---|
| **PCI-DSS** | Payment processing, credit card handling |
| **HIPAA** | Healthcare data, patient information |
| **GDPR** | EU personal data processing |
| **EU AI Act** | AI system deployment in EU |
| **NIST 800-53** | Federal system requirements |
| **COPPA** | Children under 13, educational products |
| **SOC 2** | Service organization controls |
| **FedRAMP** | Federal cloud services |
| **HL7 FHIR** | Healthcare interoperability |
| **FINRA** | Financial services regulation |

#### Architecture

```
Unstructured Input ──> [ Phase 1: Intake ] ──> [ Phase 2: Compilation ] ──> [ Phase 3: Export ]
                           │                        │                           │
                      Normalize &              Quality Gates              Compliance-Annotated
                      Structure                (30-item checklist)        Production PRD
                                               7 Bias Detectors
```

#### Technology Stack

`Python 3.11+` &bull; `Typer` &bull; `Anthropic SDK` &bull; `Pydantic v2` &bull; `MCP[cli]` &bull; `PyYAML` &bull; `Rich`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>12 &mdash; CoWork &nbsp;&nbsp;<sub>Governed Plugin Designer</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 307+ automated tests |
| **Source Lines** | 6,161 |
| **Status** | Complete and operational |

#### Description

CoWork generates **governed Claude Code plugins by default**. It decomposes natural language role descriptions into 15&ndash;30 plugin opportunities, then compiles them into complete plugin directories with SENESCHAL runtime enforcement, audit trails, HITL gates, and compliance framework support. Every plugin ships with a `.castellan/` governance sidecar containing SENESCHAL-gated policy hooks, tool allowlists, HITL approval gates, and immutable audit trails. 32-check SENESCHAL policy gate per tool use.

#### Compliance Framework Support

CoWork supports **10 compliance frameworks** for governed plugin generation:

| Framework | Implementation |
|:---|:---|
| **FedRAMP** | Low/Moderate/High profile selection |
| **DoD IL4** | Impact level 4 controls |
| **DoD IL5** | Impact level 5 controls |
| **HIPAA** | Healthcare privacy safeguards |
| **SOC 2** | Service organization trust criteria |
| **PCI-DSS v4.0** | Payment card industry controls |
| **EU AI Act** | European AI regulation alignment |
| **GDPR** | Data protection compliance |

**Three-tier degradation:** Full enforcement (SENESCHAL online), local enforcement (SENESCHAL offline), fail-closed (regulated environments &mdash; all actions blocked without enforcement).

#### Architecture

```
Role Description ──> [ Decompose ] ──> [ Generate Plugins ] ──> [ Package with Governance ]
                     15-30 opportunities    Complete directories    .castellan/ sidecar
                                            per plugin              SENESCHAL hooks
                                                                    HITL gates
                                                                    Audit trails
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Anthropic SDK` &bull; `Pydantic v2` &bull; `Rich`

<br>
</details>

<br>

### Domain-Specific Platforms

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>13 &mdash; LawClaw &nbsp;&nbsp;<sub>Governed Legal Plugin Suite</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Governed Plugin Suite &mdash; CoWork-Compiled |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Source Lines** | 34 plugins per discipline (3 disciplines) |
| **Status** | Complete and operational |

#### Description

LawClaw is the **governed legal plugin suite** for law firms &mdash; 34 plugins per discipline (privacy/security, family law, general) compiled through CoWork Plugin Designer with **ABA Model Rules compliance** baked into every plugin. Every email, time entry, and client communication passes through governance gates.

#### ABA Model Rules Compliance Mapping

| ABA Rule | Obligation | Enforcement Mechanism |
|:---|:---|:---|
| **Rule 1.1** (Competence) | Competent representation | HITL gate on all legal advice |
| **Rule 1.5** (Fees) | Reasonable fees | HITL gate on all billing actions |
| **Rule 1.6** (Confidentiality) | Client confidences | HITL gate on privileged communications |
| **Rule 1.7** (Conflicts) | Conflict of interest | Conflict check gates before engagement |
| **Rule 1.15** (Trust Accounts) | Safekeeping property | Disbursement control gates |
| **Rule 5.1** (Supervision &mdash; Partners) | Supervisory responsibility | Full audit trails for all AI actions |
| **Rule 5.3** (Supervision &mdash; Nonlawyers) | Supervisory responsibility | Full audit trails for AI-assisted work |

#### Governance Enforcement

- **13 HITL gates per profile** &mdash; 7 base gates + 6 discipline-specific gates
- **Strict governance tier** &mdash; Bash denied, 25-turn cap
- **Conflict check gates** &mdash; automated conflict detection before client engagement
- **Full audit trails** &mdash; every action logged for supervisory review per Rules 5.1/5.3

#### Jurisdiction-Specific Regulatory Awareness

- **50+ state breach notification laws** &mdash; jurisdiction-specific requirements
- **33 jurisdiction-specific privacy regulations** &mdash; including CCPA, BIPA, state-specific rules
- **International privacy frameworks** &mdash; GDPR, PIPEDA, LGPD, POPIA awareness

#### Technology Stack

`CoWork Plugin Designer` &bull; `SENESCHAL Runtime Enforcement` &bull; `Advocate MCP Server (Rust)`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>14 &mdash; Rampart &nbsp;&nbsp;<sub>Governed Clinical Device Telemetry Platform</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Platform &mdash; Python CLI + MCP Server |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 762+ automated tests |
| **Source Lines** | 40,410 |
| **Status** | Complete and operational |

#### Description

Rampart is a governed AI agent platform for clinical device telemetry management. It integrates with healthcare data systems (HL7, FHIR) and provides MCP-based access to structured clinical data under strict **HIPAA governance**. Features PHI encryption, access logging, role-based access control, 6-year audit retention, BAA execution support, patient right of access implementation, and breach notification procedures.

#### HIPAA Safeguard Implementation

| Safeguard Category | Requirements Implemented |
|:---|:---|
| **Administrative Safeguards** | BAA execution support, workforce training tracking, sanction policy, information access management |
| **Physical Safeguards** | Device telemetry access controls, workstation security, device and media controls |
| **Technical Safeguards** | PHI encryption (mandatory), access logging (mandatory), RBAC (mandatory), audit controls, integrity controls, transmission security |
| **Organizational Requirements** | Covered entity vs. business associate differentiation, BAA requirements, group health plan requirements |

#### Compliance Requirements

| Requirement | Status | Implementation |
|:---|:---|:---|
| **PHI Encryption** | Mandatory | All PHI encrypted at rest and in transit |
| **Access Logging** | Mandatory | Every PHI access logged with timestamp, user, and purpose |
| **6-Year Retention** | Mandatory | All audit logs retained for minimum 6 years per 45 CFR 164.530(j) |
| **RBAC** | Mandatory | Role-based access control for all data access |
| **Patient Right of Access** | Implemented | Patient data export and access request handling per 45 CFR 164.524 |
| **Breach Notification** | Implemented | Automated breach detection and notification per 45 CFR 164.400-414 |
| **Minimum Necessary** | Implemented | Minimum necessary standard for PHI disclosure per 45 CFR 164.502(b) |

#### Healthcare Interoperability

- **HL7** &mdash; Health Level 7 message parsing and integration
- **FHIR** &mdash; Fast Healthcare Interoperability Resources support
- **Clinical Device Telemetry** &mdash; real-time device data ingestion, signal processing, anomaly detection
- **MCP-Based Data Access** &mdash; governed tool access to structured clinical data

#### Architecture

```
Clinical Devices ──> [ Telemetry Ingestion ] ──> [ Signal Processing ] ──> [ MCP Data Access ]
                          │                           │                         │
                     HL7/FHIR Parsing            Anomaly Detection        Governed Tool Access
                     PHI Encryption              Clinical Alerts          RBAC Enforcement
                     Access Logging              Device Monitoring        Audit Trail (6yr)
```

#### Technology Stack

`Python 3.11+` &bull; `Typer` &bull; `Pydantic v2` &bull; `MCP[cli]` &bull; `neurokit2` &bull; `numpy` &bull; `HL7apy` &bull; `FHIR.resources` &bull; `FastAPI` (optional)

<br>
</details>

<br>

---

<br>

## VI. Ecosystem Relationships

These fourteen systems form a **complete agent governance, compliance, and lifecycle platform** with domain-specific extensions for regulated industries. Each is an independent, standalone work. Integration between them does not diminish the independent IP status of any individual work.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   CASTELLAN AGENT & MCP GOVERNANCE PLATFORM                              │
│   ──────────────────────────────────────────                             │
│                                                                          │
│   COMPILE              AUDIT               DESIGN                        │
│   Castellan ──────────>Aegis               Citadel                       │
│   (Agent Compiler)     (Security Audit)    (Design Intelligence)         │
│        │                                                                 │
│   Charlotte            COMMUNICATE         BRIDGE                        │
│   (Prompt Compiler)    Herald              Drawbridge                    │
│                        (Command Channel)   (Cross-Org A2A)               │
│        │                                                                 │
│   ┌────┴─ Sub-Components ─────────────────────────────────────────┐      │
│   │  ENFORCE: SENESCHAL (15-check policy gates, FIPS, MLS, SPIFFE)│      │
│   │  MONITOR: vigil-edge (5D governance scoring, anomaly detection)│      │
│   │  POLICY:  Citadel-edge (air-gapped policy, CNSA 2.0 signing) │      │
│   └───────────────────────────────────────────────────────────────┘      │
│                                                                          │
│   SCAN                                                                   │
│   Recon                                                                  │
│   (Reverse-Engineer)                                                     │
│                                                                          │
│                                                                          │
│   AUTOMATION & UTILITY TOOLING                                           │
│   ─────────────────────────────                                          │
│                                                                          │
│   QUALITY              INTELLIGENCE        PRD / PLUGINS                 │
│   Stratum              VC+                 Chancery                      │
│   (QA Compiler)        (Capital Intel)     (PRD Compiler)                │
│                                                                          │
│   Gauntlet                                 CoWork                        │
│   (Code Adjudicator)                       (Plugin Designer)             │
│                                                                          │
│                                                                          │
│   DOMAIN-SPECIFIC PLATFORMS                                              │
│   ─────────────────────────                                              │
│                                                                          │
│   LawClaw                                  Rampart                       │
│   (ABA-Governed Legal Plugins)             (HIPAA-Governed Clinical)     │
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
