<div align="center">

# PRIOR INTELLECTUAL PROPERTY DECLARATION

### Formal Declaration of Sole Ownership & Exclusion from Assignment

---

**12 Software Systems** &nbsp;&bull;&nbsp; **20,800+ Automated Tests** &nbsp;&bull;&nbsp; **301,000+ Lines of Code** &nbsp;&bull;&nbsp; **All Rights Reserved**

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
                         AGENT GOVERNANCE PLATFORM
    ___________________________________________________________________________

    COMPILE         AUDIT           COMMUNICATE     SCAN            MONITOR
    ___________________________________________________________________________

    Castellan       Aegis           Herald          Recon           Vigil
    (Agent          (Security       (Command        (Governance     (Fleet
     Compiler)       Audit)          Channel)        Scanner)        Dashboard)

                    Arbiter
                    (Batch Audit)
    ___________________________________________________________________________

                            SUPPORTING TOOLS
    ___________________________________________________________________________

    DESIGN          BUILD           VALIDATE        ANALYZE
    ___________________________________________________________________________

    Designer-SDD    Charlotte       Stratum         Dissector
    (Spec Docs)     (Prompt         (Quality        (Opportunity
                     Compiler)       Gates)          Mapper)

    Axle            ClaudeMD
    (API Compiler)  (CLAUDE.md
                     Compiler)
    ___________________________________________________________________________
```

</div>

<br>

<div align="center">

| Metric | Value |
|:---|:---|
| **Total Software Systems** | 12 |
| **Combined Automated Tests** | 20,800+ |
| **Estimated Lines of Code** | 301,000+ |
| **Quality Gates & Checks** | 100+ |
| **Compliance Standards Covered** | 11 (EU AI Act, NIST AI RMF, GDPR, HIPAA, PCI-DSS, SOC 2, ISO 42001, ISO 27001, FZ-152, OWASP, CoSAI) |
| **Status** | All systems complete and operational |

</div>

<br>

---

<br>

## V. Schedule of Prior Intellectual Property

<br>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>1 &mdash; Castellan &nbsp;&nbsp;<sub>Spec-Driven Agent Development Framework</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Framework &mdash; Python CLI |
| **Version** | `0.3.2` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 6,712+ automated tests |
| **Source Lines** | 101,007 |
| **Status** | Complete and operational |

#### Description

Castellan is a spec-driven agent development framework. It takes YAML agent specifications and compiles them through a **5-stage pipeline** (parse, compose, optimize, validate, render) into executable, validated AI agents. Features include 87 CLI commands, multi-provider support (Anthropic, OpenAI, Google), constitutional governance, runtime guardrails, OWASP security auditing, circuit breaker patterns, multi-agent orchestration, A2A protocol support, MCP client, and 7 deployment targets with embedded governance across LangGraph, CrewAI, AutoGen, and Haystack. Includes **OpenClaw governance** (C17) &mdash; a transparent WebSocket gateway proxy for the OpenClaw open-source agent platform (247K+ GitHub stars), with per-channel policy enforcement, skill supply chain scanning (22 detection patterns across 6 threat categories), 4-dimensional trust scoring, output filtering with PII redaction, tamper-evident attestation chains, and rate limiting. Three integration surfaces: WebSocket gateway proxy, skill supply chain scanner, and HTTP endpoint governance.

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
<summary><h3>2 &mdash; Aegis &nbsp;&nbsp;<sub>Pre-Deployment Security Audit for AI Agents</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | February 2026 |
| **Test Suite** | 728+ automated tests |
| **Source Lines** | 19,688 |
| **Status** | Complete and operational |

#### Description

Aegis is a pre-deployment security audit service for AI agents. It orchestrates multiple analysis tools into a unified five-stage pipeline that performs **three audit layers** (prompt, behavior, code) in parallel, conducts cross-layer analysis with six static graph analyzers and three behavioral probes, maps findings to **OWASP Top 10 for Agentic Applications**, and produces scored, evidence-backed security reports with exploit tests proving vulnerabilities and remediation tests verifying fixes.

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
<summary><h3>3 &mdash; Arbiter &nbsp;&nbsp;<sub>Batch Agent Governance Auditor</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `0.1.0` |
| **Initial Development** | March 2026 |
| **Test Suite** | 84+ automated tests |
| **Source Lines** | 2,679 |
| **Status** | Complete and operational |

#### Description

Arbiter is a batch agent governance auditing service that scans folders of AI agent artifacts and produces structured audit reports. It processes any mix of formats through a **three-stage pipeline** (LLM extraction, deterministic rules scoring, LLM narrative generation) across **six governance audit layers** (system prompt, tool policy, orchestration, context coverage, validation, governance). The rules engine is fully deterministic with zero LLM calls &mdash; identical input produces identical scores every run.

#### Architecture

```
Artifact Folder ──> [ Stage 1: LLM Extraction ]
                    [ Stage 2: Deterministic Rules (6 layers, zero LLM) ]
                    [ Stage 3: LLM Narrative ]
                         │
                         v
                    Per-Artifact Reports (MD + JSON) + Batch Summary
```

#### Technology Stack

`Python 3.11+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Anthropic SDK` &bull; `Instructor` &bull; `PyYAML` &bull; `asyncio`

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
| **Test Suite** | 260+ automated tests |
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
| **Version** | `1.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 2,705+ automated tests |
| **Source Lines** | 45,022 |
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
| FZ-152 | Russian data protection |
| Cross-Standard | Synthesis across all standards |

#### Technology Stack

`Python 3.10+` &bull; `PyYAML` &bull; `pathspec` &bull; `Anthropic SDK` &bull; `tree-sitter`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>6 &mdash; Vigil &nbsp;&nbsp;<sub>Fleet Governance & Health Dashboard</sub></h3></summary>

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

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>7 &mdash; Charlotte &nbsp;&nbsp;<sub>Prompt Compiler & Application Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `2.2.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 3,592+ automated tests |
| **Source Lines** | 25,221 |
| **Status** | Complete and operational |

#### Description

Charlotte transforms prompt engineering into **structured, validated, composable software engineering** through a 5-stage pipeline (Parse, Compose, Optimize, Validate, Render). It includes 94 built-in block templates across 17 types, 30 assertion types for testing, 54 security checks across 21 categories, multi-provider rendering (OpenAI, Anthropic, Google Gemini), environment management, GitHub Actions CI generation, multi-prompt workflow chaining, Claude Code skill compilation, and MCP server generation.

#### Architecture

```
prompt.yaml ──> [ Parse ] ──> [ Compose ] ──> [ Optimize ] ──> [ Validate ] ──> [ Render ]
                   │               │                │               │               │
              94 Block Types   Composition      Token Mgmt     30 Assertion    Multi-Provider
              17 Categories    & Chaining       & Budget       Types + 54      (OpenAI, Anthropic,
                                                               Security Checks  Google Gemini)
```

#### Technology Stack

`Python 3.10+` &bull; `Typer` &bull; `Rich` &bull; `Pydantic v2` &bull; `Jinja2` &bull; `PyYAML` &bull; `deepdiff` &bull; `watchdog` &bull; `tiktoken` &bull; `Anthropic/OpenAI/Google SDKs`

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
| **Test Suite** | 4,436+ automated tests |
| **Source Lines** | 73,793 |
| **Status** | Complete and operational |

#### Description

Stratum is a unified code quality, architecture extraction, test generation, and documentation pipeline. It consolidates **8 quality gates** and executes a pipeline with 3-layer context extraction across 6 languages, test generation across 4 frameworks, documentation rendering with 7 independent analyzers, and comprehensive validation across **13 modules**.

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
<summary><h3>9 &mdash; Designer-SDD &nbsp;&nbsp;<sub>Spec-Driven Documentation Generator</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 800+ automated tests |
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
<summary><h3>10 &mdash; Axle &nbsp;&nbsp;<sub>Design-First API Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; Python CLI |
| **Version** | `0.1.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 1,252+ automated tests |
| **Source Lines** | 2,151 |
| **Status** | Complete and operational |

#### Description

Axle is a design-first API compiler that takes a **single canonical YAML specification** and generates six production-ready artifacts: FastAPI server, OpenAPI 3.1 spec, MCP tool definitions, MCP server, pytest suite, and pytest config. It uses a three-stage pipeline (Parse, Flatten, Render) with Jinja2 templates for code generation. Includes AI-assisted design via Charlotte-compiled architect prompt and browser-based intake form.

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
<summary><h3>11 &mdash; Dissector &nbsp;&nbsp;<sub>Domain Agent Opportunity Mapper</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | AI Prompt System &mdash; Charlotte-Compiled |
| **Version** | `1.0.0` |
| **Initial Development** | March 2026 |
| **Source Lines** | 1,993 |
| **Status** | Complete and operational |

#### Description

The Dissector is a domain agent opportunity mapper that analyzes any organization type and produces comprehensive AI agent opportunity blueprints. It decomposes organizations into **nine functional categories**, identifies minimum 15 opportunity cards per domain with build-ready specifications (agent name, data requirements, build complexity, value tier, ROI, wave assignment), generates **three-wave implementation roadmaps** (0&ndash;90, 90&ndash;180, 180&ndash;365 days), and evaluates off-the-shelf tools against custom build opportunities. Includes explicit human-in-the-loop flagging for privilege-sensitive and liability-creating zones.

#### Architecture

Two Charlotte-compiled implementations: a full agent-orchestrating system (10 blocks, 7,507 tokens) and a multi-phase skill version (6 blocks, 4,653 tokens).

#### Technology Stack

`Charlotte Prompt Compiler` &bull; `Claude Opus 4.6` &bull; `Claude Sonnet 4.6`

<br>
</details>

<!-- ═══════════════════════════════════════════════════════════════════════ -->

<details open>
<summary><h3>12 &mdash; ClaudeMD &nbsp;&nbsp;<sub>CLAUDE.md Quality Compiler</sub></h3></summary>

<br>

| | |
|:--|:--|
| **Type** | Software Tool &mdash; TypeScript CLI |
| **Version** | `1.0.0` |
| **Initial Development** | Prior to March 2026 |
| **Test Suite** | 90+ automated tests |
| **Source Lines** | 1,919 |
| **Status** | Complete and operational |

#### Description

ClaudeMD is a CLI tool that treats CLAUDE.md files as **engineered artifacts with measurable quality**. Built on research-backed best practices &mdash; the ~150 instruction limit, periphery bias in LLM attention, the WHAT/WHY/HOW framework from Anthropic&rsquo;s official guidance, and progressive disclosure via skills and rules. Features include 15 validation rules, quality grading across 5 weighted dimensions (Conciseness, Coverage, Specificity, Progressive Disclosure, Anti-patterns), automated fixes with unified diff output, and full ecosystem audit across CLAUDE.md, `.claude/rules/`, agents, skills, and `.mcp.json`.

#### Architecture

```
CLAUDE.md ──> [ Validate (15 rules) ] ──> [ Score (5 dimensions) ] ──> [ Improve (auto-fix) ]
                                                                    ──> [ Doctor (ecosystem audit) ]
```

#### Technology Stack

`Node.js 20+` &bull; `TypeScript`

<br>
</details>

<br>

---

<br>

## VI. Ecosystem Relationships

These twelve systems form a **complete agent governance and lifecycle platform**. Each is an independent, standalone work. Integration between them does not diminish the independent IP status of any individual work.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   AGENT GOVERNANCE PLATFORM                                              │
│   ─────────────────────────                                              │
│                                                                          │
│   COMPILE              AUDIT                COMMUNICATE                  │
│   Castellan ─────────> Aegis                Herald                       │
│   (Agent Compiler)     (Security Audit)     (Command Channel)            │
│                        Arbiter                                           │
│                        (Batch Governance)                                │
│                                                                          │
│   SCAN                 MONITOR                                           │
│   Recon ─────────────> Vigil                                             │
│   (Reverse-Engineer)   (Fleet Dashboard)                                 │
│                                                                          │
│                                                                          │
│   SUPPORTING TOOLS                                                       │
│   ────────────────                                                       │
│                                                                          │
│   DESIGN               BUILD                VALIDATE                     │
│   Designer-SDD ──────> Charlotte ──────────> Stratum                     │
│   (Spec Compiler)      (Prompt Compiler)     (QA Compiler)               │
│                                                                          │
│   Axle                 Dissector              ClaudeMD                   │
│   (API Compiler)       (Opportunity Mapper)   (CLAUDE.md Compiler)       │
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
