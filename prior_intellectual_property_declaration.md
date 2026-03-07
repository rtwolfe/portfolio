<div align="center">

# PRIOR INTELLECTUAL PROPERTY DECLARATION

### Formal Declaration of Sole Ownership & Exclusion from Assignment

---

**9 Software Systems** &nbsp;&bull;&nbsp; **13,000+ Automated Tests** &nbsp;&bull;&nbsp; **106,000+ Lines of Code** &nbsp;&bull;&nbsp; **All Rights Reserved**

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
                         AGENT LIFECYCLE COVERAGE
    ___________________________________________________________________________

    DESIGN          BUILD           VALIDATE        DEPLOY          MONITOR
    ___________________________________________________________________________

    Designer-SDD    Castellan       Stratum         Herald          Vigil
    (Spec Docs)     (Agent Compiler)(Quality Gates) (Command Auth)  (Fleet Dashboard)

    Axle            Charlotte       Aegis                           Recon
    (API Compiler)  (Prompt Compiler)(Security Audit)               (Governance Scan)
    ___________________________________________________________________________
```

</div>

<br>

<div align="center">

| Metric | Value |
|:---|:---|
| **Total Software Systems** | 9 |
| **Combined Automated Tests** | 13,000+ |
| **Estimated Lines of Code** | 106,000+ |
| **Quality Gates & Checks** | 100+ |
| **Compliance Standards Covered** | 10 (EU AI Act, NIST, GDPR, HIPAA, PCI-DSS, SOC 2, ISO 42001, ISO 27001, FZ-152, OWASP) |
| **Status** | All systems complete and operational |

</div>

<br>

---

<br>

## V. Schedule of Prior Intellectual Property

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>1 &mdash; Aegis &nbsp;&nbsp;<sub>Pre-Deployment Security Audit for AI Agents</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | February 2026 |
| **Test Suite** | 677+ automated tests |
| **Status** | Complete and operational |

#### Description

Aegis is a pre-deployment security audit service for AI agents. It orchestrates multiple analysis tools into a unified pipeline that performs **three audit layers** (prompt, behavior, code) in parallel, conducts cross-layer analysis, maps findings to **OWASP Top 10 for Agentic Applications**, and produces scored, evidence-backed security reports with exploit tests proving vulnerabilities and remediation tests verifying fixes.

#### Architecture

```
Intake ──> [ Prompt Audit ]──┐
           [ Behavior Audit ]├──> Cross-Layer Analysis ──> Scored Report
           [ Code Audit ]────┘
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `concurrent.futures` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>2 &mdash; Axle &nbsp;&nbsp;<sub>Design-First API Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Status** | Complete and operational |

#### Description

Axle is a design-first API compiler that takes a **single canonical YAML specification** and generates multiple production-ready artifacts: FastAPI server, OpenAPI 3.1 spec, MCP tool definitions, MCP server, and pytest suite. It uses a three-stage pipeline (Parse, Flatten, Render) with Jinja2 templates for code generation.

#### Architecture

```
api.yaml ──> [ Parse ] ──> [ Flatten ] ──> [ Render ] ──> FastAPI Server
                                                      ──> OpenAPI 3.1 Spec
                                                      ──> MCP Tool Definitions
                                                      ──> MCP Server
                                                      ──> Pytest Suite
```

#### Technology Stack

`Python 3.11+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `watchdog`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>3 &mdash; Castellan &nbsp;&nbsp;<sub>Spec-Driven Agent Development Framework</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Framework &mdash; Python CLI |
| **Version** | `0.3.2` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 6,417+ automated tests |
| **Status** | Complete and operational |

#### Description

Castellan is a spec-driven agent development framework. It takes YAML agent specifications and compiles them through a **5-stage pipeline** (parse, compose, optimize, validate, render) into executable, validated AI agents. Features include 61+ CLI commands, multi-provider support (Anthropic, OpenAI, Google), constitutional governance, circuit breaker patterns, and a full plugin system.

#### Architecture

```
agent.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Render ]
                                                                    │
                                                   ┌────────────────┼────────────────┐
                                                   v                v                v
                                              Constitutional    Circuit          Plugin Gates
                                              Governance        Breaker          (Provider, Tool,
                                                                                  Gate, Exporter)
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `tiktoken` &bull; `httpx` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>4 &mdash; Charlotte &nbsp;&nbsp;<sub>Prompt Compiler & Application Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `2.2.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | Comprehensive automated test suite |
| **Status** | Complete and operational |

#### Description

Charlotte transforms prompt engineering into **structured, validated, composable software engineering** through a 5-stage pipeline (Parse, Compose, Optimize, Validate, Render). It includes 94 built-in block templates across 17 types, 30 assertion types for testing, 50+ security checks across 20 categories, multi-provider rendering, environment management, GitHub Actions CI generation, and multi-prompt workflow chaining.

#### Architecture

```
prompt.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Render ]
                   │               │                │               │               │
              94 Block Types   Composition      Token Mgmt     30 Assertion    Multi-Provider
              17 Categories    & Chaining       & Budget       Types + 50+     (OpenAI, Anthropic,
                                                               Security Checks  Google Gemini)
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `deepdiff` &bull; `watchdog` &bull; `tiktoken` &bull; `Anthropic/OpenAI/Google SDKs`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>5 &mdash; Designer-SDD &nbsp;&nbsp;<sub>Spec-Driven Documentation Generator</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | Comprehensive automated test suite |
| **Status** | Complete and operational |

#### Description

Designer-SDD converts JSON specifications into **complete, GitHub-ready documentation packages**. It produces standardized artifacts (CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, RESEARCH.md, HANDOFF.md, README.md) with tier-gated extras. Features include dual-gate scoring (Quality: 28 checks, Buildability: 8 checks), iterative AI refinement (up to 3 passes), and round-trip verification.

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
<summary><h3>6 &mdash; Herald &nbsp;&nbsp;<sub>Authenticated Command Channel for Agent Fleets</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Library &mdash; Python |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 166+ automated tests |
| **Status** | Complete and operational |

#### Description

Herald is an authenticated bidirectional command channel between operator portals and deployed agent fleets. It provides a complete command loop with **HMAC-SHA256 signed message envelopes**, supporting message types for query, config_update, broadcast, and recall operations with constitutional bounds enforcement and full audit trail logging via append-only JSONL.

#### Architecture

```
Operator Portal ──[ HMAC-SHA256 Signed Envelope ]──> Agent Fleet
                                                         │
         ┌───────────────────────────────────────────────┘
         v
    [ Query | Config Update | Broadcast | Recall ]
         │
         v
    Constitutional Bounds ──> Audit Trail (JSONL)
```

#### Technology Stack

`Python 3.10+` &bull; `Pydantic v2` &bull; `httpx`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>7 &mdash; Recon &nbsp;&nbsp;<sub>Agent Governance Reverse-Engineering Scanner</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 2,632+ automated tests |
| **Status** | Complete and operational |

#### Description

Recon is a 3-stage pipeline that **reverse-engineers governance contracts** from AI agent source code. It scans agents (Python, LangChain, CrewAI, YAML specs, MCP manifests) and produces comprehensive governance audit packages including reconstructed agent specs, compliance manifests, OWASP scorecards, and assessments across **10 international standards**.

#### Compliance Standards

| Standard | Domain |
|:---|:---|
| EU AI Act | European AI regulation |
| NIST AI RMF | US federal AI risk management |
| GDPR | European data protection |
| HIPAA | US healthcare privacy |
| PCI-DSS | Payment card security |
| SOC 2 | Service organization controls |
| ISO 42001 | AI management systems |
| ISO 27001 | Information security |
| FZ-152 | Russian data protection |
| OWASP Top 10 | Agentic application security |

#### Technology Stack

`Python 3.10+` &bull; `PyYAML` &bull; `pathspec` &bull; `Anthropic SDK`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>8 &mdash; Stratum &nbsp;&nbsp;<sub>Unified Code Quality & Architecture Pipeline</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 3,046+ automated tests |
| **Status** | Complete and operational |

#### Description

Stratum is a unified code quality, architecture extraction, test generation, and documentation pipeline. It consolidates **8 quality gates** and executes a DAG-based pipeline with 3-layer context extraction, test generation, documentation rendering, and comprehensive validation across **12 modules**.

#### Module Architecture

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
<summary><h3>9 &mdash; Vigil &nbsp;&nbsp;<sub>Fleet Governance & Health Dashboard</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Application &mdash; Full-Stack Web |
| **Version** | `0.3.2` |
| **Initial Development** | Prior to March 2026 |
| **Status** | Complete and operational |

#### Description

Vigil is a fleet health, compliance, and governance dashboard for AI agents. It is a **multi-tenant portal** that ingests HMAC-signed health packets from deployed agents, evaluates governance compliance, fires alerts on threshold breaches, and serves real-time dashboards. Features include 13 database tables, WebSocket real-time events, cost governance, incident management, and attestation chain tracking.

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

**Frontend:** `Node.js 20+` &bull; `Next.js 14` &bull; `TypeScript` &bull; `Tailwind CSS` &bull; `shadcn/ui` &bull; `Recharts`

**Infrastructure:** `PostgreSQL + TimescaleDB` &bull; `SQLite` &bull; `Redis` &bull; `Clerk JWT`

<br>
</details>

<br>

---

<br>

## VI. Ecosystem Relationships

These nine systems form a **complete agent lifecycle platform**. Each is an independent, standalone work. Integration between them does not diminish the independent IP status of any individual work.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   DESIGN PHASE              BUILD PHASE              VALIDATE PHASE      │
│   ─────────────             ───────────              ──────────────      │
│   Designer-SDD ──────────>  Castellan ──────────────> Stratum            │
│   (Spec Docs)               (Agent Compiler)          (Quality Gates)    │
│                                                                          │
│   Axle ─────────────────>   Charlotte ──────────────> Aegis              │
│   (API Compiler)            (Prompt Compiler)         (Security Audit)   │
│                                                                          │
│                                                                          │
│   DEPLOY PHASE              MONITOR PHASE                                │
│   ────────────              ─────────────                                │
│   Herald ────────────────>  Vigil                                        │
│   (Command Channel)        (Fleet Dashboard)                             │
│                                                                          │
│                             Recon                                        │
│                             (Governance Scanner)                         │
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
