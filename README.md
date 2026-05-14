<div align="center">

# Tim Wolfe

### Agentic AI Architect | Governed Agents · A2A Transport · Runtime Attestation | Post-Quantum · DoD-Hardened | 2× IPOs · 5× Exits

<br>

**I build the compilers, runtime authorities, and intelligence platforms that make AI agents safe to deploy.**

*Open to Principal / Staff / Chief Architect roles in regulated-industry, federal, or defense-tier AI infrastructure.*

<br>

![Tests](https://img.shields.io/badge/24%2C000%2B-Tests_Passing-16A34A?style=for-the-badge)
![Systems](https://img.shields.io/badge/20-Production_Systems-7C3AED?style=for-the-badge)
![Standards](https://img.shields.io/badge/20%2B-Compliance_Standards-DC2626?style=for-the-badge)
![Architecture](https://img.shields.io/badge/4--Tier-Platform-DEA584?style=for-the-badge)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-2021-DEA584?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=flat-square&logo=typescript&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Axum](https://img.shields.io/badge/Axum-Rust-000000?style=flat-square)
![License](https://img.shields.io/badge/License-Proprietary-orange?style=flat-square)

<br>

Los Altos, CA · [rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

</div>

<br>

---

## About

I build **governance infrastructure for AI agents** &mdash; the compilers, pre-deployment audit gate, runtime authority, A2A transport, observability substrate, design intelligence platforms, and production products that make autonomous agents safe to deploy in DoD, federal, and regulated-industry environments. Not wrappers. Not demos. Not prompt templates. **Five design-time compilers, a seven-component runtime substrate, four production products, and a four-app Operator Loop tier** that close the loop from raw idea to deployed, governed, monitored, cryptographically attested agent fleet &mdash; with FIPS 140-3 / CNSA 2.0 alignment and defense-grade compliance enforcement at every stage.

**Governance is the core problem.** Every team shipping AI agents hits the same wall: the prototype works, but production demands governance &mdash; constitutional constraints, runtime guardrails, OWASP security auditing, compliance drift detection, kill switches, audit trails, cryptographic evidence. Most frameworks hand you a runtime and leave governance as an exercise for the reader. I built a platform that makes governance structural. It's enforced at compile time. It travels with the deployed agent. It's monitored in real time. It's signed and attested. It's not optional.

**Compliance runs deep.** This platform carries full regulatory compliance coverage across **20+ frameworks**: **EU AI Act** risk classification, **HIPAA** safeguard mapping, **PCI-DSS v4.0** goal compliance, **SOC 2 Type II** evidence generation, **NIST 800-53** federal security controls, **NIST 800-171 Rev 2** CUI protection, **NIST AI RMF**, **NIST CSF 2.0 (CAISI)**, **NIST IR 8596**, **FedRAMP** (Low/Moderate/High), **FIPS 140-3** cryptography, **CNSA 2.0** post-quantum alignment, **CNSSP-12** classified environment compliance, **DoD STIG** checklist export, **DoD IL4/IL5** impact level controls, **CMMC L1/L2/L3**, **ISO 42001/27001/42005**, **GDPR**, **GLBA Safeguards**, **FFIEC IT Handbook**, **SOX ITGC**, **OCC SR 11-7**, **FINRA 2026**, **MAS AI RM**, **Singapore IMDA**, **OWASP Top 10**, **CoSAI** threat modeling, and **COPPA**.

**Design-Time Compilers &mdash; the four Cs + Recon:**

- **Castellan** &mdash; the agent governance compiler. YAML spec in, governed production agent out. Constitutional governance, runtime guardrails, OWASP audit, 12 export formats including Level 6 hardened Rust binaries. 18-framework compliance engine
- **Charlotte** &mdash; context engineering compiler. 103-block template catalog across 20 types, 89 security patterns, multi-provider rendering (OpenAI, Anthropic, Google Gemini), and MCP server generation in Python and Level 6 Rust
- **Chronicle** &mdash; runtime attestation and compliance observability substrate. Hybrid Ed25519 + ML-DSA-65 (FIPS 204) signing, RFC 8785 JCS canonicalization, Merkle-chained event ledger, OSCAL evidence packages, signed ATO bundles. 18-crate Rust workspace, zero-LLM in compliance-critical path
- **Citadel** &mdash; compliance-aware design intelligence platform. 43 FastMCP tools for introspection, fleet decomposition, spec generation, and regulatory document generation (FedRAMP SSP, NIST 800-171 SSP, STIG CKL, ISO 42001, GLBA, PCI-DSS, FFIEC, SOX, OCC SR 11-7)
- **Recon** &mdash; the inbound complement to the four Cs. Reverse-engineers compliance contracts from already-built AI agent artifacts (Python, LangChain, LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Bedrock, Semantic Kernel, DSPy, MCP manifests, A2A agent cards). 21 framework adapters, 48 checks, 272 priority-tagged citations, 4 output formats (JSON / Markdown / HTML / SARIF 2.1.0), deterministic three-tier verdict (CERTIFIED / CONDITIONAL / REJECTED)

**Runtime Substrate &mdash; the pre-deployment gate, enforcement, transport, and observability layer:**

- **Aegis** &mdash; pre-deployment security audit gate. Six-dimension spec validation (tool description poisoning, integrity-manifest SHA-384 agreement, MCP topology, behavioral policy floor, attestation provenance chain, license-token presence) producing a binary SHIP / BLOCK verdict. BLOCK verdicts carry remediation pointers back into the spec. Nothing reaches runtime substrate until Aegis says SHIP. Produces the pre-deployment attestation artifact required for FedRAMP ATO, DoD ATO, and CMMC packages
- **Seneschal** &mdash; on-premises Rust runtime authority enforcing the policy compiled by Citadel. 30-check policy gate, 80 attestation event types, 83 violation classifications, kill-switch surface, FIPS 140-3 cryptography, HMAC-SHA384 signing of every policy decision
- **Garrison** &mdash; the customer-facing shell. Hardened single-operator Rust runtime hosting Castellan-compiled agent binaries and Charlotte-compiled MCP servers. Closed-allowlist (only Aegis-attested, Key-Server-licensed binaries load). Level 6 release profile (LTO, strip, panic=abort, overflow checks, opt-level=z) with stripped PIE binaries, four SKU tiers (Hosted / Stronghold / Enclave / Sovereign)
- **Drawbridge** &mdash; governed agent-to-agent transport stack. Per-message signing, encryption, attestation binding, and policy gating across territory boundaries. Four components: **Drawbridge** (the transport, classical FIPS 140-3 primitives), **Drawbridge Console** (sovereign operator command channel), **Outpost** (remote-operator client), **Portcullis** (standalone cryptographic CLI)
- **Vigil + Vigil-Edge** &mdash; fleet behavioral monitoring. Vigil is the hosted multi-tenant FastAPI + Next.js portal; Vigil-Edge is the per-node Rust observer for air-gapped sovereign deployments. Behavioral baseline comparison, drift alerts, governance-amendment proposals
- **Bailiff** &mdash; hardened Rust agent runtime executing Castellan's Rust-target binaries in environments where Python is not permitted. Closes the DoD IL5 / CNSSP-12 execution gap
- **Key Server** &mdash; fleet licensing backbone. axum REST service on PostgreSQL + Redis with AWS SNS cross-region revocation, HSM-backed token signing, sovereign offline tokens for SCIF / air-gap operation. License check is bootstrap step zero for every governed binary in the fleet

**Products:**

- **Audit Pro** &mdash; productized governance audit for third-party AI agents. Customer-facing Rust outer shell + seven Castellan-compiled audit agents + seven Charlotte-compiled MCP servers + Chronicle-signed evidence bundles. Independent verification by any 3PAO
- **Chancery** &mdash; AI Chief Product Officer. Transforms unstructured product input into production-quality PRDs and per-component SDD bundles through a 4-phase, 3-gate workflow. Deployed as Claude Desktop Project and Claude Code skill (`/chancery-architect`)
- **Quaestor** &mdash; RFP intelligence engine. 7-crate Rust workspace that judges federal solicitation responses against the questions they claim to address. Three-state verdicts with five sub-scores, risk-signal taxonomy, fabricated-quote detection, dark-themed dual HTML+PDF report. Federal Procurement domain pack consumer; three skews (hosted / on-prem IL5 / air-gap SCIF)
- **Augur** &mdash; AI Strategy & Center-of-Excellence Advisor. CoE-as-a-Service consulting product and the **evidence layer** under Citadel and Chancery's spec generators. One agent + four MCP servers (Model Catalog, Framework Catalog, CoE Playbook, Use Case Library), six anti-hallucination structural verifiers, six wired bridges into the rest of the platform. EU AI Act High-Risk + ISO 42005 + OCC SR 11-7

**Operator Loop &mdash; the practitioner-side complement, built on the platform:**

- **Verity** &mdash; Scrum Master / Project Manager intelligence platform. 33 crates, 17 MCP servers, 8 governed agents, 23 antipattern detectors, 5 ceremony pipelines. Read-only by compile-time construction. Reads Jira / Confluence / GitHub / Bitbucket / Slack / Teams; surfaces the conversations you need to have today
- **Steward** &mdash; Product Owner / Product Manager intelligence platform. 21 crates, 5 MCP servers, 8 PO-specific agents, 16 PO antipattern detectors, 5 PO intelligence cadences. Sibling to Verity, tuned for product cadences
- **Reeve** &mdash; governed Atlassian administration. The *writer* where Verity / Steward are *readers*. 5 MCP servers covering 102 Atlassian admin tools, approval gates, state snapshots + rollback
- **Author** &mdash; story / epic coaching tool. 6-crate Rust workspace with INVEST scoring, 15 anti-pattern detectors, deterministic refusal layer that catches shallow authoring before it reaches Jira

Every system is standalone. Together they automate the full lifecycle for AI agents &mdash; from rapid prototyping through governed deployment to real-time fleet monitoring with cryptographic attestation. **The platform is self-hosting** &mdash; Charlotte compiles the prompts inside Verity, Castellan compiles the agents inside Audit Pro and Steward, Chronicle signs the attestation events emitted by Reeve, and Citadel emits the compliance specs that gate the operator-loop tools I use daily. Eat-your-own-dog-food isn't a slogan; it's the production posture.

Before AI infrastructure: 20+ years of enterprise operations leadership &mdash; two IPOs (**Quinstreet**, **Responsys**), four acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior technical roles at **Salesforce**, **iHeartMedia**, and **Axway**.

---

<div align="center">

```
┌─────────────────────────────────────────────────────────────────────────┐
│              AGENT & MCP GOVERNANCE PLATFORM                            │
│      Built against FIPS 140-3 · CNSA 2.0 · DoD IL5 · FedRAMP High       │
│                                                                         │
│   DESIGN-TIME COMPILERS — the four Cs + Recon                           │
│   Castellan    Charlotte    Chronicle    Citadel    Recon               │
│   (agents)     (context)    (attest)     (design)   (inbound auditor)   │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│                     RUNTIME SUBSTRATE                                   │
│   Aegis   Seneschal   Garrison    Drawbridge   Vigil    Bailiff  Key Sv │
│   (gate)  (policy)    (shell)     (A2A)        (telem)  (Rust)   (lic)  │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│                           PRODUCTS                                      │
│   Audit Pro   Chancery    Quaestor    Augur                             │
│   (audit)     (PRD)       (RFP)       (CoE advisor)                     │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│                        OPERATOR LOOP                                    │
│   Verity      Steward     Reeve       Author                            │
│   (SM/PM)     (PO/PM)     (admin)     (stories)                         │
└─────────────────────────────────────────────────────────────────────────┘
```

<br>

**Design-Time Compilers** &nbsp;&nbsp; [Castellan](#1-castellan--agent-governance-compiler) · [Charlotte](#2-charlotte--context-engineering-compiler) · [Chronicle](#3-chronicle--runtime-attestation--compliance-observability) · [Citadel](#4-citadel--compliance-aware-design-intelligence) · [Recon](#5-recon--ai-agent-inspector)

**Runtime Substrate** &nbsp;&nbsp; [Aegis](#6-aegis--pre-deployment-audit-gate) · [Seneschal](#7-seneschal--runtime-policy-authority) · [Garrison](#8-garrison--hardened-operator-console) · [Drawbridge](#9-drawbridge--governed-a2a-transport-stack) · [Vigil](#10-vigil--vigil-edge--fleet-behavioral-monitoring) · [Bailiff](#11-bailiff--rust-agent-runtime) · [Key Server](#12-key-server--fleet-licensing-backbone)

**Products** &nbsp;&nbsp; [Audit Pro](#13-audit-pro--productized-governance-audit) · [Chancery](#14-chancery--ai-chief-product-officer) · [Quaestor](#15-quaestor--rfp-intelligence-engine) · [Augur](#16-augur--ai-strategy--center-of-excellence-advisor)

**Operator Loop** &nbsp;&nbsp; [Verity](#17-verity--smpm-intelligence-platform) · [Steward](#18-steward--popm-intelligence-platform) · [Reeve](#19-reeve--governed-atlassian-administration) · [Author](#20-author--storyepic-coaching-tool)

[How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Platform

AI agents have a governance problem. And a compilation problem. And an SDLC problem. And an evidence problem.

Code gets compiled. Databases get migrated. Infrastructure gets provisioned through declarative configs with validation and version control. But AI agents &mdash; the specs they're built from, the prompts they use, the tests that prove they work, the governance that keeps them safe, the evidence that proves they behaved &mdash; are still assembled by hand, shipped on instinct, and debugged in production. There's no compiler. No governance enforcement. No automated SDLC. No cryptographic ledger of what the agent did at runtime. No way to prove an agent won't go off-script next week, and no way to prove what it did last week.

I built five design-time compilers, a seven-component runtime substrate, four production products, and a four-app Operator Loop tier to fix that. The compilers handle agent generation, context engineering, runtime attestation, design intelligence, and reverse-engineering compliance from already-built agents. The runtime substrate enforces the compiled policy: Aegis as the pre-deployment audit gate, Seneschal as the runtime policy authority, Garrison as the hardened operator shell, Drawbridge as the governed A2A transport (FIPS 140-3, classical + post-quantum), Vigil for fleet observability, Bailiff for Rust-only sovereign deployments, and Key Server as the licensing backbone. The products deploy the stack in specific domains &mdash; productized audit, conversational PRD design, federal RFP intelligence, and AI Center-of-Excellence advisory. The Operator Loop is the practitioner-side complement — the daily SM/PM, PO/PM, Atlassian admin, and authoring tooling I run on top of the platform to do my own job.

Every system is standalone. Together they close the loop from unstructured idea to deployed, tested, governed, monitored, signed, attested agent fleet. The platform is self-hosting &mdash; Chancery compiles the PRDs, Charlotte compiles the prompts, Castellan compiles the agents, Citadel generates compliance evidence, Chronicle signs runtime events, and the products demonstrate the stack in production.

---

<br>

<div align="center">

# Design-Time Compilers

*Five systems. The four Cs plus Recon. Compile outward, audit inward.*

</div>

<br>

---

## 1. Castellan &mdash; Agent Governance Compiler

**The agent compiler. YAML in, governed production agent out. Governance is structural, not optional.**

> The problem: every team building AI agents hits the same wall. The prototype works. Then production demands governance &mdash; the agent says things it shouldn't, costs $47 on a single session, crashes on a flaky API call, and nobody can prove it won't go off-script next week. Most agent frameworks are code-first and governance-last. They hand you a runtime and leave governance, testing, compliance, and deployment as an exercise for the reader.

Castellan is the **agent governance compiler**. Write a declarative YAML spec. Castellan compiles it through a 5-stage pipeline, enforces constitutional governance at compile time and runtime, gates every response through inline guardrails, audits the entire agent against the OWASP Top 10 for Agentic Applications, and exports to 12 targets including **Level 6 hardened Rust binaries** (FROM scratch, static musl, RELRO+NX, mTLS via rustls) for DoD deployments.

This isn't a framework. It's a **compiler**. The agent is governed before it runs. Validated before it deploys. Monitored after it ships.

### The Compilation Pipeline

Every agent spec runs through 5 deterministic stages before a single token is generated:

| Stage | Purpose |
|:--|:--|
| **Parse** | Validates YAML, resolves block references, applies `!include` directives and `extends`/`mixins` inheritance |
| **Compose** | Assembles the system prompt from prioritized blocks, injects Jinja2 variables |
| **Optimize** | Token budget analysis, prompt compression, cost estimation |
| **Validate** | Schema validation, gate threshold checks, tool permission verification, 10+ completeness rules |
| **Render** | Produces a `CompiledAgent` &mdash; ready for execution, export, testing, or audit |

### Constitutional Governance

Every compiled agent carries a constitution: core values, technical boundaries, quality standards, user commitments. Severity-ranked principles (`critical` / `high` / `medium` / `low`) determine whether violations block output, penalize gate scores, or get logged for audit. All 5 governance sub-schemas are typed Pydantic v2 models &mdash; parse-time validation catches misconfigurations at compile time.

Governance travels with the agent. The `--governed` export flag embeds governance directly into LangGraph, CrewAI, AutoGen, and Haystack exports &mdash; `@governed` decorator, compliance JSONL logging, kill switch, autonomy ceiling.

### Compliance Engine &mdash; 18 Regulatory Frameworks

| Framework | What Castellan Does |
|:--|:--|
| **EU AI Act** | Risk tier classification, article-by-article compliance assessment |
| **HIPAA** | Administrative, Physical, Technical safeguard mapping |
| **PCI-DSS v4.0** | 6-goal compliance mapping with AI/ML supplement |
| **SOC 2 Type II** | Dual-mode evidence generation |
| **NIST AI RMF** | Governance-to-function/category alignment |
| **NIST 800-53** | 30+ federal security control patterns |
| **NIST CSF 2.0 (CAISI)** | 6-function structure, AI Agent Standards Initiative |
| **ISO 42001 / 27001** | AI management system + information security |
| **GDPR Article 22** | Automated decision-making rights, PII redaction |
| **FedRAMP** | Federal risk authorization (Low/Moderate/High) |
| **DoD IL4/IL5** | Impact level controls for defense |
| **CNSSP-12** | Classified environment compliance |
| **FINRA 2026** | Financial regulatory compliance |
| **OWASP Agentic** | Full Top 10 vulnerability mapping |
| **COPPA** | Children's privacy protection |

### Runtime Guardrails

Every LLM response runs through an inline guardrail pipeline before it reaches the user:

- **PII Redaction** &mdash; emails, SSNs, credit cards, phone numbers, custom patterns
- **Prompt Injection Filtering** &mdash; injection attacks, exfiltration attempts, privilege escalation
- **Hallucination Detection** &mdash; quoted facts verified against tool results and conversation context
- **Most-restrictive-wins semantics** &mdash; strictest action (BLOCK > REDACT > WARN > PASS) applied

### Execution Engine

Async-first ReAct runtime: **Observe &rarr; Think &rarr; Act &rarr; Validate** with 4 LLM providers (Anthropic, OpenAI, Google, Ollama), MCP client, A2A protocol, RAG pipeline, sliding-window memory with working memory slots, cost-aware model routing with budget enforcement, circuit breaker with fallback provider chain, and LRU + TTL response caching.

### Multi-Agent Orchestration

| Pattern | How It Works |
|:--|:--|
| **Supervisor** | Master agent routes tasks to specialists via regex/keyword rules |
| **Pipeline** | Sequential chain with stage transforms, stops on error |
| **Broadcast** | Parallel fan-out with aggregation (concat, first, vote) |
| **Peer** | Turn-based collaboration with configurable max rounds |

### Production Deployment &mdash; 12 Targets, Governance Embedded

Python package, Docker, FastAPI server, Claude Code skill, Kubernetes (Deployment/Service/ConfigMap/Secret/Kustomization/Helm), Temporal workflow, client delivery package, and **Level 6 hardened Rust binaries** (FROM scratch, static musl, panic=abort, LTO, stripped) for DoD deployments.

### CI/CD Governance Gate

`castellan ci-diff` compiles both base and head spec versions, runs governance scoring on both, produces a `GovernanceImpactReport` with verdict **APPROVE / REVIEW / BLOCK**. GitHub Action and GitLab CI templates included. Governance regression doesn't slip through code review &mdash; it blocks the merge.

<div align="center">

`CLI + Rust target generation` · `531 modules` · `8,600+ tests`

</div>

<br>

---

## 2. Charlotte &mdash; Context Engineering Compiler

**The context compiler. 103-block template catalog, defense-grade security scanning, MCP server generation in Python and Rust.**

> The problem: prompts are the source code of AI applications, but they have no SDLC. No compilation. No type system. No testing framework. No security scanning. No version control semantics. No CI/CD. For any artifact this critical, that's engineering malpractice.

Charlotte transforms prompt engineering into **structured, validated, composable software engineering** through a 5-stage deterministic pipeline. Write a YAML spec. Charlotte compiles it into a validated, optimized, deployment-ready prompt or complete MCP server with security scanning, testing, and multi-provider rendering.

### The Compilation Pipeline

| Stage | What It Does |
|:--|:--|
| **Parse** | Validates YAML, resolves references from 103-block catalog across 20 types |
| **Compose** | Assembles blocks in priority order, resolves variables with Jinja2, applies composition rules |
| **Optimize** | Token budget analysis per provider model, prompt compression, cost estimation |
| **Validate** | 30 assertion types, output format verification, quality threshold checks |
| **Render** | Multi-provider output, Claude Code skills, MCP servers, GitHub Actions CI |

### Defense & Federal Compliance Scanning

Charlotte implements **89 security patterns across 22 categories**:

| Capability | Implementation |
|:--|:--|
| **DoD Patterns** | 35+ detection patterns aligned to NIST 800-53 families (AC, AU, IA, SC, SI, CM, CP, IR, RA, SA) |
| **STIG Export** | Checklist generation with vulnerability IDs (V-222400 format), CAT I&ndash;III |
| **FIPS 140-3** | Non-FIPS algorithm detection, FIPS transport requirement validation |
| **mTLS / CAC** | Mutual TLS enforcement, Common Access Card / PKI authentication |
| **Classification Banners** | CUI, UNCLASSIFIED//FOUO, SECRET, TOP SECRET display enforcement |
| **MCP DoD Hardening** | TLS 1.2+, AES-256, non-root containers, capability dropping |
| **CoSAI Threat Model** | MCP-T1/T2/T6/T9 coverage |
| **Audit Format** | JSON, CEF (ArcSight/SIEM), Syslog RFC 5424 |

### 103-Block Catalog Across 20 Types

The block catalog is the substrate. Specs assemble blocks; blocks compose into prompts under composition rules (singletons, mutual exclusions, co-requirements, precedence). 12 domain cards, tier requirements, MCP sizing tiers, calibration benchmarks. Plugin system allows custom block auto-discovery.

| Block category (selected) | Examples |
|:--|:--|
| **Identity & role** | role, persona, expertise, voice, audience |
| **Methodology** | methodology, decision_framework, evaluation_criteria |
| **Constraints** | constraints, anti_patterns, prohibitions, scope_limits |
| **Knowledge bundles** | glossary, standards, api_schema, examples, policy |
| **Output structuring** | format, schema, examples, anti_examples |
| **Tool & MCP** | tools, mcp_servers, capabilities, surface_definitions |
| **Reasoning** | thinking_strategy, self_critique, verification |
| **Compliance** | governance, classification, attestation, audit_trail |

Three tier floors enforce structural depth: **single-turn (18K tokens)**, **multi-phase (35K tokens)**, **agent-orchestrating (55K tokens)**. A 10-factor quality scorer + 12 red-flag checks + variable-density minimums + calibration benchmarks reject thin prompts at compile time.

### 8-Pass Optimizer

| Pass | What It Does |
|:--|:--|
| **Dedup** | Removes redundant block content |
| **Merge** | Combines compatible blocks under composition rules |
| **Strip** | Removes empty / placeholder content |
| **Normalize** | Standardizes formatting, whitespace, headings |
| **Reorder** | Applies precedence ordering (20-type precedence) |
| **Compress** | Token-aware compression where safe |
| **Budget** | Per-provider model token budget enforcement |
| **Provider hints** | Inserts provider-specific optimizations |

### MCP Server Generation &mdash; Python and Rust

Charlotte compiles prompt specs into complete MCP servers in two targets:

| Target | Description |
|:--|:--|
| **Python (FastMCP)** | Python MCP servers with governance spec integration |
| **Rust (Level 6)** | Level 6 hardened Rust MCP binaries &mdash; FROM scratch, static musl, rustls, panic=abort |

Additional quantized MCP renderers for air-gapped Ollama deployments.

### 23 Export Formats, Multi-Provider Rendering

Provider-aware rendering for **Anthropic, OpenAI, Google Gemini**, and Ollama. Export formats include Claude Code skills (`SKILL.md`), Cursor / OpenCode IDE skills, MCP servers (Python + Rust), HTML + README export, eval trend dashboards, and GitHub Actions CI integrations.

### 6-Stage Block Builder

LLM-assisted block authoring pipeline: **brief &rarr; draft &rarr; critique &rarr; refine &rarr; validate &rarr; emit**. Drafts new blocks against existing catalog patterns, runs the 10-factor quality scorer, applies red-flag checks, and produces calibrated output that passes Charlotte's own validation gates.

<div align="center">

`CLI + MCP Server Generator` · `135 modules` · `3,700+ tests`

</div>

<br>

---

## 3. Chronicle &mdash; Runtime Attestation & Compliance Observability

**The evidence substrate. Agents emit events; Chronicle signs, verifies, Merkle-chains, persists, maps to controls, and produces auditor-shippable OSCAL packages and ATO bundles.**

> The problem: agents pass their own tests, but compliance auditors need *evidence* &mdash; cryptographically signed, tamper-evident, framework-mapped proof of what the agent actually did at runtime. Most observability stacks produce logs that any operator can edit. Auditors don't trust them. Without an attestation substrate, a compliance claim is an assertion, not evidence.

Chronicle is the **runtime-attestation and compliance-observability substrate** for agent fleets. The fifth "C" in the Castellan / Charlotte / Chancery / Citadel / Chronicle stack. Chronicle itself is **zero-LLM in the compliance-critical path** &mdash; signing, verification, transition gates, and build gates are all deterministic Rust. LLM assistance exists only in the advisory pack-authoring drafter layer; LLM output cannot produce a valid attestation.

### Hybrid Post-Quantum Signing from v0

Every event, every OSCAL package, every ATO bundle is signed with **both Ed25519 and ML-DSA-65 (FIPS 204)** &mdash; the post-quantum lattice signature standardized by NIST. `verify_hybrid` requires BOTH halves to verify. This is the cryptographic floor that lets a 3PAO verify any artifact on a separate machine in 2026 *or* 2036, when a cryptographically-relevant quantum computer would have rendered Ed25519 alone forgeable.

### Deterministic Attestation Substrate

| Layer | Implementation |
|:--|:--|
| **Canonicalization** | RFC 8785 JSON Canonicalization Scheme &mdash; identical events serialize byte-identically |
| **Hash chain** | SHA-256 Merkle tree, O(log N) inclusion proofs |
| **Signing** | Hybrid Ed25519 + ML-DSA-65 keyring; FIPS-only build feature substitutes AES-GCM for ChaCha20-Poly1305 |
| **Reproducible build** | `lto = true`, `codegen-units = 1`, `strip = "symbols"`, `SOURCE_DATE_EPOCH` pinned &mdash; same commit produces byte-identical binary |
| **Persistence** | PostgreSQL store with tenant isolation; in-memory store for tests |
| **Witness** | Internal log + external witness adapters (Mock, Rekor) for transparency |

### 18-Crate Rust Workspace

| Crate | Function |
|:--|:--|
| **chronicle-core** | RFC 8785 JCS canonicalization, SHA-256, ID types |
| **chronicle-crypto** | Ed25519 + ML-DSA-65 hybrid signing keyring |
| **chronicle-events** | 6 event classes + common envelope + canonical-unsigned-bytes helper |
| **chronicle-chain** | Merkle tree + inclusion proofs (O(log N)) |
| **chronicle-store** | Store trait + MemStore + PgStore + tenant_configs |
| **chronicle-verifier** | 9 core governance rules (deterministic, zero-LLM) |
| **chronicle-packs** | 4 framework packs (SOC 2, HIPAA, EU AI Act, NIST 800-53 Moderate subset) |
| **chronicle-mapping** | Control Mapping Engine + 92 mapping rules |
| **chronicle-pipeline** | Ingestor &mdash; sign &rarr; verify &rarr; persist &rarr; Merkle-commit &rarr; inclusion proofs |
| **chronicle-shred** | Crypto-shred + retention + shred-authorization + ShredAttribution |
| **chronicle-witness** | Transparency log adapters (internal + MockExternalWitness + Rekor) |
| **chronicle-oscal** | OSCAL evidence-package export + signed packages + cross-reference table |
| **chronicle-admin** | Admin plane domain (AdminPlane, two-person integrity) |
| **chronicle-server** | gRPC ingest (tonic) + admin HTTP (axum) + Bearer-token auth |
| **chronicle-ingest** | Main demo binary + regulated-dry-run + e2e-validation binaries |
| **chronicle-otel-bridge** | OTLP span &rarr; ChronicleEvent translator + Langfuse / Arize / Grafana adapters |
| **chronicle-pack-authoring** | Reviewer-attestation pipeline + advisory drafter (zero-LLM in critical path) |
| **chronicle-ato** | System Security Plan + ConMon plan + pen-test scope + signed bundle |

### Framework Packs &mdash; 92 Control Mapping Rules

Chronicle ships with 4 framework packs. Each pack carries article/clause text (skeletons or transcribed public-domain excerpts), evidence schemas, and the 92 mapping rules that bind agent events to control families.

| Pack | Coverage |
|:--|:--|
| **SOC 2** | Trust Services Criteria, dual-mode evidence |
| **HIPAA** | Administrative / Physical / Technical safeguards (&sect;164.312 transcribed) |
| **EU AI Act** | High-risk system controls, Annex IV references |
| **NIST 800-53 Moderate** | Federal Moderate baseline subset |

Pack-authoring uses a controlled transition pipeline: (a) complete checklist with all items `Pass` or `PassWithCaveat`, (b) hybrid-signed `ReviewerAttestation` binding the checklist SHA-256, (c) reviewer in the authorized registry, (d) `pack_version` + `control_scope` match. Failures refuse with structured reason. Pack skeletons never auto-cite &mdash; real licensing flows through reviewer attestation before production citation.

### One Codebase, Three Deployment Tiers

`DeploymentTier::{Commercial, Regulated, Sovereign}` parameterizes witness policy, ConMon cadence, and pen-test scope &mdash; **not forked code**. Sovereign adds cross-jurisdictional witness quorum + HSM-backed keys.

| Tier | Witness | ConMon | Pen-test |
|:--|:--|:--|:--|
| **Commercial** | Internal log | Annual | Optional |
| **Regulated** | External witness (Rekor) | Quarterly | Annual scoped |
| **Sovereign** | Cross-jurisdiction quorum | Continuous | Continuous w/ red team |

### OSCAL & ATO Export

Chronicle produces auditor-independent artifacts:

- **OSCAL evidence packages** &mdash; signed, cross-referenced control evidence
- **System Security Plan** (SSP)
- **Continuous Monitoring (ConMon)** plan
- **Pen-test scope** specification
- **Signed ATO bundle** &mdash; full package binding all artifacts under hybrid signature

Every signed artifact can be verified by a 3PAO on a separate machine using only the signer's public-key bundle. No Chronicle install, no tenant trust assumption, no in-process state.

<div align="center">

`Rust Binary + gRPC + Postgres` · `18 crates` · `394+ tests` · `Hybrid Ed25519 + ML-DSA-65`

</div>

<br>

---

## 4. Citadel &mdash; Compliance-Aware Design Intelligence

**The design front end and compliance engine. Compiler-ready specs in, governed fleet architectures and regulatory documents out.**

Citadel is the compliance-aware design intelligence platform. It generates compiler-ready YAML specs with governance fields that become runtime enforcement rules, compiles behavioral intent into enforceable policy, and runs a full compliance engine for regulatory documentation and live codebase scanning.

### Three Operating Modes, 43 Tools

| Mode | Description |
|:--|:--|
| **`citadel design`** | Interactive CLI via Anthropic API (user-driven, reactive) |
| **`citadel forge`** | Voice-first automated pipeline (4 stages, 3 approval gates) |
| **`citadel serve`** | FastMCP server (stdio/SSE) for MCP clients |

### Fleet-Level Artifact Generation

`gen_fleet_specs` produces coordinated artifacts for multi-agent deployments:

- Castellan agent specs + Charlotte MCP server specs (compliance + behavioral aware)
- A2A trust policy (bilateral pairs with delegation types)
- Runtime registration config with spec hashes and hierarchy
- Herald C2 config (protected fields, HMAC signing)
- Behavioral baseline (per-agent expected behaviors)
- HMAC manifest (design-time placeholders)
- Provenance manifest (Merkle root)
- Tool description scan (poisoning detection)
- Tool integrity manifest (SHA-384 description hashes)
- Call stack policy (chain depth, circular detection, sequence rules)
- Autonomy progression (tier-based promotion/demotion)
- Crossing policy (territory allowlists, crypto suite selection)
- Redundancy protocol policy &mdash; governed failover
- MCP topology policy (expected interaction graph, undeclared edge detection)
- Trust scoring policy (behavioral trust decay)
- SR 11-7 model cards (per-agent risk documentation)

### Compliance Engine &mdash; 26 Frameworks

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

### MCP Security Pipeline

Design-time defense against MCP attack vectors (tool poisoning, rug pulls, preference manipulation, call chain abuse). All modules are regex-based, deterministic, air-gap safe:

- **`scan_tool_descriptions(tools)`** &mdash; 20 patterns, 4 severity levels
- **`verify_tool_integrity(tools, manifest)`** &mdash; SHA-384 hashes for rug-pull detection
- **`compile_call_stack_policy(prompt, framework)`** &mdash; depth limits, circular detection
- **`compile_topology_policy(prompt, framework)`** &mdash; MCP interaction graph, drift detection
- **`compile_trust_scoring_policy(prompt, framework)`** &mdash; zero trust with memory

<div align="center">

`CLI + MCP Server` · `88 modules` · `1,000+ tests` · `43 FastMCP Tools` · `27 Framework Profiles`

</div>

<br>

---

<br>

---

## 5. Recon &mdash; AI Agent Inspector

**Point Recon at someone else's AI agent &mdash; their source, their MCP servers, their A2A agent cards &mdash; and it produces a signed, compliance-aware certificate naming exactly what's broken and exactly how to fix it.**

Recon is the **inbound** half of the platform. Castellan, Charlotte, and Citadel emit governed agents *outward* from specifications. Recon reverses the arrow: take any already-built agent artifact and reverse-engineer the compliance contract it should have had. Customer hands over a repository, a LangChain chain, a YAML spec, an MCP manifest, or an A2A agent card; Recon hands back a forensic verdict with verbatim citations.

### The Headline

| | |
|:--|:--|
| **Compliance frameworks** | 10 &mdash; PCI-DSS 4.0, HIPAA, SOC 2, FedRAMP, NIST 800-53 Rev. 5, NIST AI RMF, ISO 27001:2022, GDPR, EU AI Act, OWASP LLM Top 10 (2026) |
| **Check identifiers** | 48 distinct &mdash; 25 MCP + 24 A2A across 16 check families |
| **Compliance citations** | 272 individually priority-tagged (blocker / elevated / advisory) |
| **Built-in policy presets** | 7 &mdash; strict / relaxed / PCI-tuned / HIPAA-tuned per target |
| **Framework adapters** | 21 &mdash; LangChain, LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, Amazon Bedrock, Semantic Kernel, DSPy, Python AST, JS/TS, Java, Go, etc. |
| **Output formats** | 4 &mdash; JSON certificate, Markdown report, HTML stakeholder page, SARIF 2.1.0 |
| **Verdict tiers** | 3 &mdash; CERTIFIED / CONDITIONAL / REJECTED (deterministic) |
| **Tests** | 2,917 passing / 64 skipped / 0 failed / 0 warnings |

### The Three-Stage Pipeline

| Stage | What Happens |
|:--|:--|
| **Extract** | ReconScanner walks every artifact via 21 framework-specific adapters. AST parsing for source code; YAML/JSON schema introspection for specs; declarative parsing for MCP manifests and A2A agent cards. Produces a 42-field `ExtractionResult` &mdash; the structured fingerprint of what the artifact actually declares versus what governance demands. |
| **Reconstruct** | Gap detection between declared behavior and framework requirements. Mismatch detection between MCP tool descriptions and observed code paths. Generates the agent.yaml that the artifact *should* have shipped with, plus a gap list and a mismatch list keyed to source line numbers. |
| **Report** | Verdict assembled across 48 checks with 272 citations. Output emitted to all four formats simultaneously. SARIF 2.1.0 means findings land directly in GitHub code-scanning, GitLab security dashboard, Azure DevOps, and any IDE that speaks the standard. |

### The Verdict Model

Three deterministic tiers, no LLM in the decision path:

| Verdict | What It Means |
|:--|:--|
| **CERTIFIED** | Zero blockers, advisory findings only. Safe to deploy under the selected framework. |
| **CONDITIONAL** | Elevated findings present but no blockers. Deployment permitted with named remediation work. |
| **REJECTED** | One or more blocker findings. Not deployable under the selected framework until remediated. |

Every finding carries: priority tag, source span (file + line + column), framework citation (specific clause / control / requirement), suggested remediation, and a verbatim quote from the source artifact.

### Why Recon Is the Inbound Compiler

The platform's outbound stack (Castellan emits governed agents, Charlotte emits governed MCP servers, Citadel orchestrates compliance) assumes the customer is building new. Recon serves the customer who already has something running and needs to know whether it survives the framework they're suddenly required to meet. The flow is symmetric:

- **Outbound**: spec &rarr; Citadel &rarr; Charlotte/Castellan &rarr; governed binary
- **Inbound**: governed-or-not binary &rarr; Recon &rarr; certificate + reconstructed spec + remediation patches

The reconstructed spec is itself Castellan/Charlotte-conformant &mdash; meaning the customer can take Recon's output, drop it back into the outbound stack, and recompile their existing agent into a governed binary. The two halves of the platform meet at the reconstructed spec.

### Used By Audit Pro

Recon is the inbound governance-extraction stage of [Audit Pro](#13-audit-pro--productized-governance-audit)'s customer scan pipeline. Customers don't need to interact with Recon directly &mdash; Audit Pro orchestrates it, then signs the outputs into a Chronicle evidence bundle.

<div align="center">

`pip install stratum-recon` · `3-Stage Pipeline` · `21 Framework Adapters` · `48 Checks` · `272 Citations` · `2,917 Tests`

</div>

<br>

---

<div align="center">

# Runtime Substrate

*Seven systems. Pre-deployment audit gate, policy authority, customer shell, governed transport, observability, Rust runtime, licensing. The enforcement layer that decides what runs and keeps it honest while it does.*

</div>

<br>

---

## 6. Aegis &mdash; Pre-Deployment Audit Gate

**The ship/block decision point. Every governed binary that reaches Garrison's allowlist passed through here. BLOCK verdicts carry remediation pointers back into the originating spec; nothing reaches runtime substrate until Aegis says SHIP.**

Aegis is the gate between compile-time and runtime. Castellan, Charlotte, and Citadel produce the binaries and the governance specification; Aegis is what audits the resulting bundle end-to-end before a single byte reaches Garrison or any other deployment substrate. Its output is the attestation artifact required for FedRAMP authorization-to-operate packages, DoD ATO submissions, and CMMC pre-deployment evidence.

### What Aegis Validates

| Dimension | Check |
|:--|:--|
| **Tool description integrity** | Scans for poisoning indicators (exfiltration URLs, hidden directives, embedded prompt-injection patterns) across every MCP tool description |
| **Integrity manifest coverage** | Verifies SHA-384 hash agreement between declared tool manifest and compiled artifact; no rug-pull surface |
| **MCP topology** | Compares declared-versus-expected interaction graph; flags undeclared fan-out, cross-domain calls, hop-depth violations |
| **Behavioral policy completeness** | Confirms compiled policy meets framework floor (DoD IL5, FedRAMP High, HIPAA, etc.) on every required dimension |
| **Attestation provenance chain** | Walks the Merkle-anchored provenance chain from spec back to compiler version; flags broken anchors |
| **License-token presence** | Confirms a valid Key Server license token is present for every deployable binary in the bundle |

### Binary Verdict

| Verdict | Meaning |
|:--|:--|
| **SHIP** | All dimensions pass; bundle proceeds to Garrison ingest and runtime activation |
| **BLOCK** | One or more dimensions fail; verdict carries remediation pointers naming exact spec locations to fix; bundle does not reach runtime |

### Compliance Posture

Produces the pre-deployment attestation artifact required for **FedRAMP** authorization-to-operate packages, **DoD ATO** submissions, **CMMC** pre-deployment evidence, and **ISO/IEC 42001** management-system audits. Aegis output is consumed directly by Audit Pro as part of customer-facing audit deliverables.

<div align="center">

`Pre-Deployment Gate` · `6-Dimension Spec Validation` · `Binary SHIP / BLOCK Verdict` · `716 tests` · `FedRAMP ATO + DoD ATO + CMMC Evidence Artifact`

</div>

<br>

---

## 7. Seneschal &mdash; Runtime Policy Authority

**The on-premises Rust authority that turns Citadel's compiled policy into runtime enforcement. Every agent action passes through it. Every decision is signed.**

Seneschal is the keystone of the runtime stack. Castellan compiles agents; Charlotte compiles MCP servers; Citadel compiles the governance specification &mdash; Seneschal is what enforces all of it at runtime. Built as a 23K+ line Rust authority with FIPS 140-3 cryptography throughout, it sits between every agent and every tool call, evaluating policy in a 30-check gate before a single byte crosses the boundary.

### The 30-Check Policy Gate

| Check Family | What Gets Validated |
|:--|:--|
| **Autonomy ceiling** | Max tool chain depth, unsupervised turns, actions per session &mdash; framework-derived from the compliance spec |
| **Call stack integrity** | Depth limits, circular-call detection, privilege-escalation prevention, sequence authorization |
| **Cost limits** | Per-call / per-session / per-day ceilings with hard cutoff |
| **Tool integrity** | Re-hashes tool descriptions at every call against the signed integrity manifest &mdash; rug-pull detection |
| **MCP topology** | Declared-versus-actual interaction graph; fan-out / fan-in limits; hop depth; cross-domain restrictions |
| **Behavioral trust** | Zero-trust-with-memory: per-server trust score with decay and penalty weights |
| **Crossing policy** | Inter-territory message authorization against Drawbridge-bound policy |
| **Framework floor** | Compliance-derived minimums (DoD IL5, FedRAMP High, HIPAA, etc.) checked at every action |

### Attestation Surface

- **80 distinct attestation event types** emitted on every policy decision, tool call, A2A message, and governance amendment
- **83 violation classifications** with framework-mapped severity grading
- **HMAC-SHA384 signing** on every emitted event; SHA-384 spec-hash anchoring
- **Chain.Append** with `CnsaHash = Sha384` record_hash + previous_hash for tamper-evident integrity
- **Kill-switch surface** invokable by Herald amendments to halt agent execution mid-action

### Closed-Loop Governance

The behavioral-governance loop runs continuously: Citadel compiles policy &rarr; Seneschal enforces &rarr; Vigil / Vigil-Edge observe deviations &rarr; Vigil issues amendments &rarr; Herald carries the amendment &rarr; Seneschal adapts at runtime without redeploy. No restart. No recompile. Audit trail signed end-to-end.

### Crypto Posture

- **FIPS 140-3** module-verified at startup
- **CNSA 2.0** alignment: SHA-384 + HMAC-SHA384 throughout (CnsaHash = Sha384, HKDF-SHA384, no SHA-256 in any cryptographically-critical path)
- **Hash-prefix migration support**: accepts both `SHA384:` (current) and legacy `SHA256:` formats during fleet upgrade windows

<div align="center">

`FIPS 140-3 Module` · `30-Check Gate` · `80 Event Types` · `83 Violation Classifications` · `179+ Tests`

</div>

<br>

---

## 8. Garrison &mdash; Hardened Operator Console

**The customer-facing shell. Closed-allowlist runtime that hosts the agents and MCP servers Castellan and Charlotte produce. No third-party plugins. No unsigned binaries. Ever.**

Garrison is what the customer actually buys and runs. The compilers (Castellan / Charlotte / Citadel) produce the binaries; Garrison is the hardened operator console that hosts them. It's deliberately a **closed-allowlist runtime** &mdash; only Charlotte/Castellan-compiled binaries that have been Aegis-attested and Key-Server-licensed will load. There is no plugin marketplace. There is no "BYO agent." Sovereign deployment requires sovereign control of the boundary.

### Four SKU Tiers

| Tier | Boundary | Workload Set |
|:--|:--|:--|
| **Hosted** | Public CSP allowed | Full platform, hosted Claude models |
| **Stronghold** | Customer VPC | Same workload set, customer-controlled tenancy |
| **Enclave** | On-prem, FIPS module mandatory | DoD IL4 / IL5 baseline, mTLS throughout |
| **Sovereign** | SCIF / air-gap, no egress | DoD IL5 / CNSSP-12, local Ollama, Citadel-Edge policy bundles |

The SKU is carried in the signed license token issued by Key Server; downstream feature activation gates against it.

### Architectural Split

- **Gateway** &mdash; operator + agent ingress with auth, body limits, rate limiting, graceful shutdown
- **Executor** &mdash; runs the customer's Castellan-compiled agent binaries
- **Bootstrap orchestrator** &mdash; calls Key Server license check as bootstrap step zero
- **Provider routing** &mdash; Anthropic / OpenAI / Ollama; air-gap tiers route to local quantized models
- **Persistence** &mdash; SQLite-backed conversation state with CNSA 2.0 cryptography
- **Internal MCP allowlist** &mdash; small closed set (sandbox, file manager, command-line adapter); no third-party MCP loading

### Hardening Profile

Level 6 release build throughout: **LTO**, **strip**, **panic=abort**, **overflow checks**, **opt-level=z**. Stripped PIE binaries. **FROM scratch** containers, static **musl**, **RELRO+NX**, **mTLS**, **STIG-aligned**.

<div align="center">

`16 Rust Crates` · `Level 6 Hardened` · `4 SKU Tiers` · `Closed Allowlist` · `Sovereign Deployable`

</div>

<br>

---

## 9. Drawbridge &mdash; Governed A2A Transport Stack

**Per-message signed, encrypted, attested, policy-gated inter-territory messaging. Most AI platforms don't have governed inter-agent comms at all. This one does &mdash; with FIPS 140-3 today and a post-quantum tier for TS/SCI tomorrow.**

Drawbridge defines a **"territory"** as a governance boundary compiled by Citadel &mdash; a set of agents and MCP servers operating under a shared governance specification. Every cross-territory message is treated as a first-class governance event: signed at the sender, encrypted in transit, attested into Chronicle, policy-gated at the receiving Seneschal instance against the recipient territory's compiled spec.

### Four-Component Stack

| Component | Role |
|:--|:--|
| **Drawbridge** | The transport. Classical FIPS 140-3 primitives: HMAC-SHA384 message integrity, ChaCha20-Poly1305 (RFC 8439) authenticated encryption, ephemeral Diffie-Hellman session keying with HKDF-SHA384 (NIST SP 800-56C) key derivation. Every message bound to a Chronicle-anchored provenance chain |
| **Drawbridge Console** | Sovereign in-territory operator command channel. Operator actions carried as policy-gated Drawbridge messages &mdash; every operator command subject to the same governance evaluation as agent traffic |
| **Outpost** | Remote-operator client establishing an authenticated Drawbridge session into the in-territory Console from outside the protected territory boundary. Cross-boundary mutual authentication and identity binding |
| **Portcullis** | Standalone hardened Rust CLI for the cryptographic operations supporting the stack: key management, message signing/verification, attestation construction, operator credential issuance, key-ceremony orchestration, offline signed-bundle verification. Statically linked, no runtime dependencies |

### Compliance Posture

Built against **FIPS 140-3** cryptographic requirements. Deployable in HIPAA, PCI-DSS, SOC 2, FedRAMP Moderate / High, and DoD IL4 / IL5 environments. Operator-action auditability sufficient for **DoD privileged-user monitoring** and **STIG operator-control** requirements. A post-quantum variant exists for higher-tier deployments; specifics reserved under NDA.

<div align="center">

`FIPS 140-3` · `4 Components` · `Classical + Post-Quantum Tiers` · `Hardened Rust` · `Territory-Bound Policy Gating`

</div>

<br>

---

## 10. Vigil + Vigil-Edge &mdash; Fleet Behavioral Monitoring

**Compiled policy alone doesn't prove an agent is behaving. Vigil and Vigil-Edge ingest Seneschal's attestation stream, compare it against the behavioral baseline Citadel compiled, and synthesize amendment proposals that flow back through Herald to Seneschal &mdash; closed loop, no redeploy, full audit trail.**

Two deployment shapes share one evidence model: **Vigil** is the hosted multi-tenant FastAPI + Next.js portal; **Vigil-Edge** is the per-node Level 6 hardened Rust observer for SCIF / air-gap environments where the central portal is unreachable. Both produce the evidence shape required for **FedRAMP Continuous Monitoring**, **SOC 2 Type II**, **ISO/IEC 42001**, **EU AI Act post-market monitoring**, and **FDA PCCP change-tracking**.

The amendment loop is the part most monitoring stacks don't have: drift detected &rarr; amendment proposal generated &rarr; Herald carries the signed amendment &rarr; Seneschal adapts mid-flight. Governance becomes a feedback system, not a deploy-time checkpoint.

<div align="center">

`Vigil: FastAPI + Next.js` · `Vigil-Edge: Hardened Rust` · `FedRAMP ConMon · SOC 2 Type II · ISO 42001 · EU AI Act post-market · FDA PCCP`

</div>

<br>

---

## 11. Bailiff &mdash; Rust Agent Runtime

**Castellan compiles agents to Python or Rust. The Rust target needs a Rust runtime to execute it &mdash; one that has no Python anywhere in the execution path. Bailiff is that runtime.**

DoD IL5 and CNSSP-12 sovereign environments routinely exclude managed-runtime languages (Python, Node, Java) by policy. Without Bailiff, a Rust-target Castellan agent would have no runtime that meets the deployment-tier requirements. With Bailiff, the entire chain &mdash; spec compile through agent execution &mdash; stays in Rust: ReAct reasoning loop, multi-provider model client (Ollama / on-prem / quantized-local routing), structured tool invocation with per-call Seneschal evaluation, Chronicle attestation-event emission signed and chained inline. Level 6 release profile throughout (LTO, strip, panic=abort, overflow checks, opt-level=z, FROM scratch, static musl, RELRO+NX, mTLS, STIG-aligned).

<div align="center">

`Level 6 Hardened Rust` · `Zero Python in Execution Path` · `DoD IL5 / CNSSP-12 Ready` · `mTLS + STIG-aligned`

</div>

<br>

---

## 12. Key Server &mdash; Fleet Licensing Backbone

**Bootstrap step zero. Every governed binary in the fleet validates a license before it will start &mdash; or refuses to start.**

axum REST service on PostgreSQL + Redis with **HSM-backed token signing** carrying SKU tier (Hosted / Stronghold / Enclave / Sovereign), expiry, and customer ID. **AWS SNS cross-region revocation** propagates within seconds. **Sovereign offline tokens** support SCIF / air-gap operation where outbound network access is impossible. The Governance-Integration SDK in every binary calls Key Server before any other initialization &mdash; no license, no startup.

Three license behaviors most fleet licensing systems don't handle: (1) offline tokens for air-gap, (2) sovereign-territory issuance under customer control, (3) cross-region revocation that survives partition. Key Server implements all three.

<div align="center">

`axum + PostgreSQL + Redis` · `HSM-Backed Signing` · `Sovereign Offline Tokens` · `AWS SNS Cross-Region Revocation` · `Bootstrap Step Zero`

</div>

<br>

---

<div align="center">

# Production Products

*Four customer-facing products deploying the platform in specific domains.*

</div>

<br>

---

## 13. Audit Pro &mdash; Productized Governance Audit

**The customer-facing audit product. Third-party AI agents in, Chronicle-signed evidence bundles out. Independent verification by any 3PAO.**

> The problem: enterprises shipping AI agents face a verification gap. Drata and Vanta automate SOC 2 evidence collection but don't read agent specs. Big 4 advisory practices charge six figures and produce PDF assessments that can't be cryptographically verified. The customer needs a productized audit that produces machine-verifiable evidence and concrete remediation &mdash; not a slide deck.

Audit Pro is the **productized governance audit** for third-party AI agents. The architecture matches the platform's own self-hosting principle: Audit Pro's analytical layer is itself **seven Castellan-compiled agents and seven Charlotte-compiled MCP servers** &mdash; auditing customer agents while itself being a hand-rolled bag of Rust functions would be hypocrisy that auditors smell. The Rust outer shell is the *delivery vehicle*: CLI, orchestrator state machine, deliverable assembly, verify pipeline, remediation patch emit/apply, retirement + redaction.

### What Customers Hand Over, What Audit Pro Returns

| Customer hands over | Audit Pro returns |
|:--|:--|
| Agent code, specs, configs | Premium HTML deliverable with verbatim citations |
| Optional runtime logs | Behavioral baseline (when logs provided) |
| Framework selection | Framework-mapped findings, severity-graded |
| Authorized signer | Signed scope attestation |
| | **Drop-in recompiled Castellan/Charlotte spec** that closes the priority-1 findings |
| | **Chronicle-signed evidence bundle** (hybrid Ed25519 + ML-DSA-65) |
| | OSCAL package + SR 11-7 model card per agent |
| | Auditor handoff document (12+ pages) |

### Frameworks Supported

| Framework | What Audit Pro Maps |
|:--|:--|
| **NIST AI Risk Management Framework** | Govern / Map / Measure / Manage functions; full risk-tier classification |
| **EU AI Act (High-Risk)** | Annex III system classification, Annex IV technical documentation |
| **SR 11-7** | Federal Reserve Model Risk Management; per-agent model card |
| **SOC 2 Common Criteria 6** | CC6 logical access, CC7 system operations evidence |
| **NIST SP 800-53 Moderate** | Federal Moderate baseline control mapping |
| **CMMC Level 2** | DoD Cybersecurity Maturity Model Certification |
| **HIPAA** | Administrative / Physical / Technical safeguard mapping |
| **PCI-DSS v4.0** | 12-requirement mapping, SAQ determination |

### The Engagement Pipeline

| Phase | What Happens |
|:--|:--|
| **Init** | `audit-pro init` opens a content-addressable engagement workdir, validates intake YAML, signs scope attestation |
| **Scan** | Citadel compliance scanner + description scanner + integrity manifest + topology observer + trust scorer run against customer artifacts. Forge intake/Recon/Aegis run optional governance scoring |
| **Analyze** | Seven Castellan-compiled audit agents map raw findings to chosen framework; severity grading; recompiled-spec generation |
| **Evidence pack** | Chronicle signs the bundle (hybrid ML-DSA-65 + Ed25519); OSCAL output assembled; SR 11-7 model card per agent emitted |
| **Finalize** | HMAC-bound bundle sealed; tar.gz produced; verification key bundle exported |
| **Verify** | Anyone, anywhere: `audit-pro verify <bundle.tar.gz> --hmac-secret <key>` &mdash; CI mode supports `--strict-warnings` and `--json` |
| **Diff** | `audit-pro diff <bundle-a> <bundle-b>` &mdash; re-engagement comparison shows posture drift over time |
| **Remediate** | `audit-pro apply-patch <patch.yaml> <target-spec.yaml>` &mdash; remediation patches emitted as YAML, apply directly to customer specs |
| **Retire** | `audit-pro retire --purge` &mdash; GDPR right-to-erasure on customer data |

### Architectural Invariants

1. **Audit Pro never re-implements engine logic.** It composes existing engines (Citadel, Forge, Castellan, Charlotte, Bailiff, Chronicle).
2. **Intelligence lives in compiled artifacts.** Same Charlotte / Castellan quality floors and governance posture as everything else in the fleet.
3. **The Rust shell is the outer wrapper.** CLI, state machine, subprocess coordination, Chronicle linkage, deliverable assembly. No LLM-calling logic in the shell &mdash; that lives in the compiled agents.
4. **Auditor-independent verification.** Every signed artifact verifies on a separate machine using only the signer's public-key bundle. No Audit Pro install, no tenant trust assumption.
5. **Customer-facing product is Rust.** Single Level 6 hardened binary. No Python runtime in customer environments at delivery time.

### Three-Year Product Line

| Year | Form | Buyer |
|:--|:--|:--|
| **Year 1** | Productized 4-week service engagement | Direct CISO / GRC lead |
| **Year 2** | Licensed on-prem tool | Consultancies, MSSPs, Big 4 advisory |
| **Year 3** | Attestation gateway SaaS | Platform engineering / CISO |

The shell is the same across all three years. Year-by-year, more of the loop becomes self-service; the cryptographic-attestation core is constant.

<div align="center">

`Rust CLI + Compiled Agents + MCP Servers` · `5 Rust crates · 89 modules` · `215+ tests` · `Chronicle-Signed Evidence Bundles`

</div>

<br>

---

## 14. Chancery &mdash; AI Chief Product Officer

**The PRD compiler and design front door. Unstructured product input in, compliance-aware PRDs and per-component SDD bundles out.**

> The problem: product requirements start as chaos &mdash; voice transcripts, Slack threads, meeting notes, emails. Turning that into a structured, compliance-aware PRD takes days. Most PRD tools produce generic documents with no regulatory awareness.

Chancery is an **AI Chief Product Officer** that normalizes unstructured product input and compiles it through a disciplined 4-phase, 3-gate workflow into production-quality PRDs and agent/MCP fleet architectures.

### 4-Phase Workflow

| Phase | Gate | Output |
|:--|:--|:--|
| **Assessment** | Structured input | Normalized problem statement |
| **Discovery** | Domain interrogation | Branch-adapted discovery (5 branches) |
| **Spec** | Quality gates (30-item checklist) | Compliance-annotated PRD |
| **SDD** | Per-component validation | SDD bundles for Charlotte + Castellan |

### Architect Mode

Chancery's architect mode deploys as a **Claude Desktop Project** and **Claude Code skill** (`/chancery-architect`). Embeds V1 Agent Architecture Design methodology: conversational decomposition into min-correct agent/MCP architectures with per-component SDD bundles validated by Charlotte + Castellan. Ships with 7 dense knowledge files (~89K tokens), QA'd on 4 synthetic scenarios &mdash; all pass with strong discipline signals (caught HIPAA-doesn't-apply-to-vets, PCI SAQ scoping, FIPS 140-2/140-3 transition; collapsed a 5-agent legal fleet to 2 with rationale).

### Per-Component SDD Bundle Generation

The architect mode writer produces per-component artifacts that pass `charlotte validate` and `castellan validate` cleanly:

- **At fleet root** &mdash; `GOVERNANCE.md`, `ARCHITECTURE.md`, `README.md`
- **Per component** &mdash; `CONSTITUTION`, `SPEC`, `PLAN`, `TASKS`, `HANDOFF`, `spec.yaml`, `QUALITY_SUMMARY`
- **Per MCP server** &mdash; 6 knowledge placeholders (~14K chars / ~2,600 tokens each to clear Charlotte's 2,500-token per-file floor)

Auto-tier selection, auto-knowledge-ref generation, ceiling validator that runs Charlotte and Castellan tier-floor checks at design time.

### Stateful FastMCP Server &mdash; 21 Tools

| Tool category | Count | Purpose |
|:--|:--:|:--|
| **Legacy PRD tools** | 12 | normalize_input, compliance_check, web_search, conflict_detector, confirm_product_definition, compile_prd, generate_artifacts, record_assumption, update_assumption, issue_challenge, record_interrogation, score_prd |
| **Architect-mode actions** | 7 | record_component, record_policy_gate, record_hitl_point, record_compliance_boundary, record_a2a_relationship, set_topology, lock_architecture |
| **Artifact tools** | 2 | Claude Desktop artifact design path |

`AppState` dataclass holds per-client `PRDSession` via lifespan context. All tools dispatch through `TOOL_DISPATCH` handlers &mdash; same logic as the CLI path.

### Compliance Framework Detection

Automatically detects **10 compliance frameworks**: PCI-DSS, HIPAA, GDPR, EU AI Act, NIST 800-53, COPPA, SOC 2, FedRAMP, HL7 FHIR, FINRA. Citadel bridge surfaces compliance gaps as PRD NFRs and risks.

### 7 Cognitive Bias Detectors

Deterministic regex patterns + LLM-assisted reframing challenges. The detectors catch product-design pathologies before they become PRD content:

| Bias | What It Catches |
|:--|:--|
| **Sunk cost** | "We've already invested..." reasoning preserved over fresh evaluation |
| **Confirmation** | Selecting evidence that supports the desired conclusion |
| **IKEA effect** | Overvaluing self-built artifacts vs. evaluating fit |
| **Planning fallacy** | Optimistic estimates absent base-rate calibration |
| **Survivorship** | Patterns drawn only from successful comparators |
| **Anchoring** | First-mentioned number / scope dominating subsequent reasoning |
| **Scope creep** | Stakeholder asks expanding the canonical problem statement |

### Quality Infrastructure

- **30-item quality checklist** &mdash; 21 deterministic regex/structural + 9 LLM-assisted semantic
- **9-enum / 17-dataclass state machine** &mdash; `pipeline/state.py`, gate enforcement absolute (`GateNotApprovedError` raised if tools called without gate approval)
- **Small-agents philosophy** &mdash; code-enforced &lt;6 agents per fleet
- **Subprocess-based LLM orchestration** &mdash; no SDK lock-in
- **15 knowledge files** (~140K tokens, knowledge budget ratio raised to 0.80)
- **18-archetype catalog** &mdash; deterministic artifact interrogation pipeline (13-step flow with regex/keyword fit gate, archetype selection, taste extractor, bias detector, compliance lens, 10-factor quality scorer)

<div align="center">

`CLI + MCP Server + Claude Desktop Project` · `70 modules` · `822+ tests` · `4-Phase / 3-Gate Workflow`

</div>

<br>

---

## 15. Quaestor &mdash; RFP Intelligence Engine

**Reads federal solicitations, judges every offeror response against the question it claims to address, returns a forensic verdict with byte-level provenance.**

Quaestor is the procurement-response validation engine. Roman quaestors audited state procurement contracts; this binary does the same job two thousand years later, faster. V0 ships as a single Rust binary (7-crate workspace). Reads `.docx` and `.pdf` solicitation responses, judges each (requirement, response) pair via `claude -p` subprocess, and emits a dark-themed dual HTML+PDF verdict report plus structured JSON with full source provenance. **V1 9-component fleet** (4 agents + 9 MCP servers + Chronicle + Drawbridge clients) is on disk as design reference; activated when an engagement justifies it.

### The Judging Philosophy &mdash; Demonstrate vs Name-Drop

Federal solicitation responses live or die on this distinction. Mentioning FedRAMP is name-drop; citing an ATO date, level, and authorizing officer is demonstration. Mentioning past performance is name-drop; supplying a contract number, period of performance, contract value, and CPARS rating is demonstration. Quaestor scores against the demonstration bar, calibrated by a Federal Procurement domain pack auto-loaded at judgment time.

### Verdict Schema

Three-state verdict (`pass` / `weak` / `miss`) with 0&ndash;100 confidence, five sub-scores, surfaced risk signals, framework attestations, missing demonstrations, and verbatim supporting quotes.

| Sub-score | Scale | What It Measures |
|:--|:--:|:--|
| **Completeness** | 0&ndash;100 | Does the response address every sub-ask in the requirement? |
| **Specificity** | 0&ndash;100 | Concrete tools, dates, contracts, evidence vs generic capability claims |
| **Evidence Quality** | 0&ndash;100 | Are claims corroborable from the response itself? |
| **Framework Demonstration** | 0&ndash;100 | When NIST/FAR/DFARS clauses are invoked, are controls demonstrated or just named? |
| **Fluff** | 0&ndash;100 | Fraction of hand-wave language. **Lower is better.** |

### Risk Signal Taxonomy

| `type` | Meaning |
|:--|:--|
| **false_claim_signal** | Certification/ATO/contract claimed without offered corroboration |
| **oci_signal** | Organizational Conflict of Interest &mdash; impaired objectivity or unequal access |
| **ceiling_above_signal** | Framework invoked above what a reasonable offeror would carry (e.g. FedRAMP High but no ATO) |
| **date_inconsistency** | Internal date conflicts (period of performance vs completion vs award) |
| **fabricated_quote** | **Quaestor-injected**: model returned a supporting quote not present in source. Each fabricated quote downgrades evidence_quality by 20; auto-detected via verbatim source round-trip |

### V0 Architecture

| Crate | Role |
|:--|:--|
| **qsr-core** | IDs, errors, provenance, verdict, classification |
| **qsr-crypto** | CNSA 2.0 wrappers (SHA-384, HMAC-SHA384, FIPS module verify) |
| **qsr-cui** | DoDM 5200.01 V4 banner injection trait + classification scanner |
| **qsr-judge** | docx/pdf extract &rarr; `claude -p` subprocess &rarr; HTML render &rarr; PDF post-process |
| **qsr-cli** | binary `quaestor` with `judge`/`render`/`pdf`/`selftest` subcommands |
| **qsr-chronicle-client** | Attestation event emission (V0 stub, V1 substrate) |
| **qsr-drawbridge-client** | A2A signed messaging (V0 stub, V1 substrate) |

### Three-Stage PDF Rendering Pipeline

wkhtmltopdf alone can't produce a viewer-portable dark PDF; Quaestor stitches three tools:

1. **wkhtmltopdf** renders the dark-themed HTML to PDF
2. **pdftocairo** (poppler-utils) normalizes the malformed xref table so a strict PDF parser can read it
3. **`qsr_judge::pdf_post::add_page_background`** opens the PDF with `lopdf`, prepends `q  R G B rg  llx lly w h re  f  Q` to every page's content stream &mdash; a save-state, set-non-stroke-RGB, fill-rect-covering-MediaBox, restore-state. Universal PDF op codes; every viewer (Chrome PDFium, Safari, Adobe Reader, Preview) honors them.

### Three Skews, One Binary

| Skew | Boundary | Model Provider |
|:--|:--|:--|
| **Hosted** | Public CSPs allowed | Claude API hosted |
| **On-prem IL4/IL5** | Tenant VPC | Claude on customer VPC, FIPS module mandatory |
| **Air-gap SCIF** | No network | Local model (Ollama-class) via redirected `claude -p` |

### Compliance & Provenance

- **CNSA 2.0 alignment** &mdash; SHA-384 + HMAC-SHA384 only, FIPS module verified at startup
- **DoDM 5200.01 V4 banner discipline** &mdash; classification detection requires standalone uppercase lines, ≤100 chars, no sentence-ending punctuation; body prose containing "CUI" is correctly rejected
- **Reproducibility envelope** &mdash; every artifact carries source SHA-384, run timestamp (RFC 3339 UTC), model identifier, and per-quote verification
- **Domain-pack-aware** &mdash; auto-loads `/projects/fleet/governance/federal-procurement-pack/` when present; demonstrate-vs-namedrop YAMLs inject into the judgment prompt for per-framework calibration
- **Resumable runs** &mdash; `--resume` skips sections with prior verdicts, no double-billing for `claude` tokens

### Customer Delivery Convention

Output bundle lands in `<given-dir>/quaestor/`; tar.gz sibling at `<given-dir>/<source-stem>.quaestor.final.tar.gz`. The archive contains analysis only &mdash; never the client's source DOCX/PDF.

### Sample Run Benchmark

EPA Cloud Engineering Enhanced v4 (3.1 MB DOCX, 9 sections): **0 pass · 3 weak · 6 miss** at 83% mean confidence. Frameworks invoked: CJIS, FedRAMP, HIPAA, IRS Pub 1075, NIST SP 800-53. Risk signals surfaced: false_claim (FedRAMP "alignment" without ATO), ceiling_above (5 compliance regimes claimed without proof), date_inconsistency (referenceable case study with no dates), fabricated_quote (multiple sections). Representative federal-procurement work in 2026 &mdash; heavy on framework name-drops, light on demonstrated controls.

<div align="center">

`7 Rust Crates` · `83 tests` · `CNSA 2.0 + DoDM 5200.01 V4 Banner Discipline`

</div>

<br>

---

## 16. Augur &mdash; AI Strategy & Center-of-Excellence Advisor

**The CoE function on tap. A consultant walks into a company and *is* the AI Center of Excellence for the engagement &mdash; with an auditable model catalog, framework catalog, CoE playbook, and use-case library doing the institutional work.**

Augur is a CoE-as-a-Service consulting product and the **evidence layer underneath Citadel and Chancery's spec generators**. Mid-size companies (500&ndash;5,000 employees) face board pressure to "have an AI strategy" but lack the institutional muscle &mdash; a permanent 5-person CoE staff over 18 months is the alternative they're trying to avoid. Augur replaces years of accumulated CoE knowledge with an auditable, score-justified, audit-replayable catalog. **One agent, four MCP servers, six wired bridges, two refresh sources, one portable skill.**

### The Five-Mode Engagement Workflow

| Mode | What Happens |
|:--|:--|
| **Discovery** | Stakeholder intake interview, candidate use cases identified, data requirements extracted from voice or text input |
| **Shortlist** | Model and Framework Catalogs queried, candidates ranked under defensible scoring rubric, optionally Forge-eval'd, adopt-or-reject recommendation with full evidence trail |
| **Translate** | BRDs, FRDs, user stories, and data mapping documents from the locked use case definition |
| **Govern** | Model cards, risk register, ROI scorecards, governance gate checklists generated by calling the Citadel compliance engine through its Python bridge |
| **Present** | Workshop deck, POC scaffold, executive presentation; rendered live through Folio so stakeholders see governance scorecards as PDFs in seconds |

### Four MCP Servers

| MCP Server | Substance |
|:--|:--|
| **Model Catalog** | 12 cataloged agentic-capable models (frontier + open-weights + small-local) scored across 8 dimensions: tool-use, multi-turn reliability, MCP support, RAG fit, cost-per-decision, deployment surface, license posture, agentic loop behavior. Hardware envelope filtering (VRAM, RAM, quantization). Refresh from HuggingFace + vendor docs + curated seed; every entry SHA-384 hashed with fetch timestamp + source URL + scorer version |
| **Framework Catalog** | 10 reference frameworks (LangChain, LangGraph, LlamaIndex, AutoGen, CrewAI, Anthropic Agents SDK, OpenAI Agents SDK, Google ADK, MCP, A2A) with governance posture overlays: audit trail, lock-in risk, compliance friendliness, deployment portability, MLOps fit |
| **CoE Playbook** | AI Center of Excellence adoption patterns: intake gates, ROI scoring rubrics, governance scorecards, model risk classification, change management workflows, autonomy progression tier ceilings. Sourced from public CoE writeups, ISO 42005, EU AI Act high-risk obligations, NIST AI RMF, OCC SR 11-7, plus the Citadel compliance engine itself |
| **Use Case Library** | 19 patterns (12 synthetic_seed + 7 pilot_validated, mined from real-world AI agent deployments). Tagged with outcome data &mdash; what shipped, what flopped, why, ROI realized, governance overhead actually incurred. Keyed by industry and business unit |

### Anti-Hallucination Guardrails

Six structural verifiers run before every recommendation returns. Tamper-evident audit log writes per call.

| Verifier | Enforces |
|:--|:--|
| **CatalogIntegrityVerifier** | All cited models/frameworks exist in catalog at the cited version; no fabricated entries |
| **CatalogResidenceVerifier** | Score values in recommendations match catalog values exactly &mdash; no model invented its own scoring |
| **ScoreVerifier** | Composite scoring math is reproducible from cataloged sub-scores |
| **CitationVerifier** | Citation byte-ranges round-trip against source documents |
| **ROIVerifier** | ROI claims trace to use-case-library outcome data, not generated narrative |
| **ComplianceVerifier** | Framework attestations align with the Citadel compliance engine, not free-form text |

### Six Wired Bridges

Augur calls into and is called by the rest of the platform:

- **Citadel bridge** &mdash; Augur's recommendations replace hardcoded defaults in `castellan_gen` (model + provider), `charlotte_gen` (MCP target model), and `fleet_gen` (runtime tier + local-quantized open-weights model with vendor-id-to-Ollama-tag translation)
- **Chancery bridge** &mdash; Same pattern for PRD-driven spec generation
- **Folio bridge** &mdash; Live PDF rendering during workshops
- **Forge bridge** &mdash; Real eval harness fired during Shortlist mode
- **Refresh source: HuggingFace** &mdash; Catalog refresh from model card metadata
- **Refresh source: vendor docs** &mdash; Catalog refresh from API documentation

Behavior contract: when Augur is installed in the venv, recommendations carry catalog provenance (composite score, runner-up, rationale, scorer version, sources) recorded as `augur_recommendation` blocks in spec output. When absent, hardcoded defaults are used exactly as before. **Graceful, optional, additive &mdash; never a hard dependency.**

### Compliance Posture

EU AI Act High-Risk as the primary framework, with ISO 42005 AI risk management and OCC SR 11-7 model risk available as overlays. Two runtime tiers from day one: **frontier** (Claude via passthrough) for fast iteration on commercial engagements, and **local_quantized** (Ollama llama 3.1 8B class) for air-gap or sovereign engagements where customer AI strategy data cannot leave the boundary. Selected per engagement, not baked in.

### Conductor Tier

Regulated Conductor tier: full governance layers (A2A, Seneschal registration, Herald, Vigil baseline, tool integrity, call stack, autonomy progression, behavioral, topology, trust scoring, crossing policy, SRP), HMAC-SHA384 manifests, single-tenant Chronicle, software HSM, 7-year retention, five gates. Sovereign tier reserved for DoD-adjacent CoE engagements.

### Hero Use Case &mdash; Day-Zero Domination

Walk into a CoE engagement having already cataloged the relevant agentic model landscape against the customer's stack, with governance artifacts pre-templated for their compliance posture, with workshop scripts and POC scaffolds ready, and with the eval harness primed to fire real benchmarks during the first stakeholder session. By the end of week one the customer believes the consultant has been doing AI CoE work for a decade. The tool is the difference.

<div align="center">

`Python 3.10+` · `209 tests` · `1 Agent + 4 MCPs` · `12 models · 10 frameworks · 19 use-case patterns`

</div>

<br>

---


<br>

<div align="center">

# Operator Loop

*The daily loop I use to do my own job — built on top of Castellan, Charlotte, Chronicle, and Citadel. Not part of the IP-protected core platform; the practitioner-side complement.*

[Verity](#17-verity--smpm-intelligence-platform) · [Steward](#18-steward--popm-intelligence-platform) · [Reeve](#19-reeve--governed-atlassian-administration) · [Author](#20-author--storyepic-coaching-tool)

</div>

<br>

---

## 17. Verity &mdash; SM/PM Intelligence Platform

**The Scrum Master / Project Manager survival weapon. Reads Jira, Confluence, GitHub, Bitbucket, Slack, Teams — surfaces the conversations you need to have today.**

Verity is the Scrum Master / Project Manager intelligence platform. 33 workspace crates, 58 CLI subcommands, **17 MCP servers**, **8 governed agents**. SOC 2 compliant fleet artifacts generated by Citadel. **Read-only by compile-time construction** &mdash; the HTTP client is GET-only, enforced at the type level.

### 17 MCP Servers Across 6 Data Sources

Verity reads from Jira, Confluence, GitHub, Bitbucket, Slack, and Teams. The MCP layer wraps each source with governed tools that respect rate limits, scope restrictions, and read-only enforcement. Each MCP server has both stub and live handlers; live handlers ship as parallel implementations behind a trait, never replacing the stubs.

### 23 Antipattern Detectors

| Methodology | Count | Examples |
|:--|:--:|:--|
| **Scrum** | 12 | sprint_goal_drift, standup_status_only, retro_no_action, planning_overcommit, demo_skipped, ceremony_decay, dependency_silence |
| **Review Quality** | 3 | review_summary_thin, action_items_missing, decision_unmoored |
| **Kanban** | 8 | wip_runaway, age_drift, blocker_silent, swimlane_collapse, policy_decay |

### 8 Governed Agents

Sprint intelligence, antipattern detector, ceremony brief composer, review quality analyst, GitHub intel, signal correlator, delivery dispatcher, report writer. Each compiled by Castellan, every prompt by Charlotte, every fleet spec by Citadel under SOC 2.

### 5 Ceremony Pipelines

| Pipeline | Cadence | Output |
|:--|:--|:--|
| **Standup** | Daily | Surfaces blockers, drift signals, talk-track for the SM |
| **Planning** | Per-sprint | Capacity check, dependency map, scope warnings |
| **Review** | Per-sprint | Structured demo recap, decision capture |
| **Retro** | Per-sprint | Pattern continuity from prior retros, action-item carryover |
| **Refine** | Weekly | Backlog readiness, story-quality scoring |

### 5-Layer Signal Observability

| Layer | What Lives Here |
|:--|:--|
| **Raw** | Unmodified source events (Jira webhooks, Slack messages, GitHub PR events) |
| **Feature** | Extracted facts: sprint goal text, PR review counts, ceremony attendance |
| **Correlation** | Cross-source links (PR &harr; Jira ticket &harr; Slack thread) |
| **Pattern** | Detector matches: antipattern hits, ceremony drift, dependency silences |
| **Insight** | Framed talk-tracks for the SM, ranked by impact |

### Methodology System

Profile-driven configuration covering **Scrum, Kanban, Scrumban, PM**. Per-profile cadence schedules, sprint anchor source (Jira / GitHub / manual), bindings (Jira project, GitHub repo, Slack channel). Daemon mode (`verity daemon`) reads `cadence_json` per profile, computes next firings, fires when `ready_at` arrives. Briefs land with status `ready`. Nothing auto-delivers.

### Day-Zero Scan Pipeline

24-hour intelligence onboarding for new SM/PM roles. Walk in, run the scan, sit Day 1's standup with team history compounded into the talk-track.

### Delivery & Reporting

- **9 report kinds** with voice-initiated publish
- **Multi-channel delivery** &mdash; SMTP / Slack / Teams with audience fan-out
- **Slack/Teams bot** &mdash; click = request only; Verity-side confirmation is the governed event (all skews)
- **Voice-initiated publish** &mdash; primary delivery path; auto-fired findings are secondary
- **Career log** &mdash; ChaCha20-Poly1305 + Argon2id encrypted personal history
- **Web UI** &mdash; axum + rustls, full route coverage

### Governance Posture

- Citadel-generated fleet specs (SOC 2 compliant)
- Every component passes Castellan + Charlotte compliance floors
- Read-only by construction &mdash; compile-time GET-only HTTP client (the type system rejects POST / PUT / PATCH / DELETE at compile time)

<div align="center">

`33 Rust Crates` · `17 MCP Servers` · `8 Governed Agents` · `3,900+ tests`

</div>

<br>

---

## 18. Steward &mdash; PO/PM Intelligence Platform

**The Product Owner / Product Manager survival weapon. Same architecture as Verity, tuned for product intelligence cadences.**

Steward is the Product Owner / Product Manager intelligence platform &mdash; sibling to Verity, same read-only architecture. 21 workspace crates, 50 CLI subcommands, **5 MCP servers**, **8 PO-specific agents**. SOC 2 compliant fleet artifacts generated by Citadel. **62 knowledge bundles** (1.1 MB total, 59 wired to MCP server specs).

### 8 PO-Specific Agents

| Agent | Domain | Autonomy |
|:--|:--|:--|
| **roadmap-intelligence-agent** | Roadmap health, epic correlation, drift detection | supervised |
| **backlog-quality-agent** | Story readiness, AC quality, refinement scoring | supervised |
| **stakeholder-dynamics-agent** | Engagement patterns, priority conflicts, silent vetoes | supervised |
| **product-drift-agent** | Scope vs vision, feature factory detection | supervised |
| **outcome-intelligence-agent** | Post-release value, adoption signals | supervised |
| **decision-archaeology-agent** | Decision history, trade-off replay | supervised |
| **communication-agent** | Drafts external sends, never auto-sends | human-in-loop |
| **individual-mirror-agent** | Self-reflection, career log (one-way data firewall) | supervised |

### 5 PO Intelligence Cadences

| Cadence | Frequency | Purpose |
|:--|:--|:--|
| **roadmap_review** | Weekly | Roadmap drift, epic health, milestone risk |
| **backlog_health** | Daily | Story readiness, refinement debt, stale-ticket pruning |
| **stakeholder_pulse** | Biweekly | Engagement patterns, silent-veto detection, alignment scoring |
| **release_readiness** | Per-release | Scope-vs-promise diff, defect risk, rollout gating |
| **outcome_review** | Monthly | Post-release adoption signals, value-delivered audit |

### 16 PO Antipattern Detectors

roadmap_drift · backlog_bloat · refinement_desert · stakeholder_silent_veto · scope_vs_vision_drift · feature_factory · acceptance_criteria_thin · story_breakdown_horizontal_only · release_promise_overrun · adoption_signal_unmonitored · decision_unrecorded · priority_conflict_unsurfaced · stakeholder_engagement_decay · backlog_age_skew · epic_correlation_missing · outcome_review_skipped &mdash; all with real detection logic over the data store, not stubs.

### Day-Zero Scan Pipeline

`steward scan` Phase 4 invokes 4 PO agents (roadmap-intelligence, backlog-quality, stakeholder-dynamics, decision-archaeology) for fast onboarding into a new PO role. Skippable with `--no-agents` for air-gap mode.

### Authoring Knowledge

4 dedicated authoring knowledge bundles (~80.6 KB): `user_story_writing_patterns.md`, `vertical_slicing_methodology.md`, `invest_criteria_reference.md`, `acceptance_criteria_advanced.md`. Powers the `communication-agent` draft pipeline.

### Delivery & Web UI

- **9 PO-specific report kinds** with voice-initiated publish
- **Multi-channel delivery** &mdash; SMTP / Slack / Teams with audience fan-out
- **Web UI** &mdash; 20 routes + 5 SVG visualizations: `/today`, `/roadmap`, `/backlog`, `/stakeholders`, `/releases`, `/outcomes`, `/decisions`, `/brief`, `/findings`, `/drafts`, `/cadences`, `/reports`, `/profiles`, `/settings/connections`, `/settings/audiences`, `/settings/cadence`, `/settings/delivery`, `/observability`, `/author`, `/audit`
- **5 synthetic test scenarios** &mdash; deterministic validation
- **Individual mirror as one-way firewall** &mdash; `individual-mirror-agent` accepts data IN (with consent), nothing flows OUT. Hard architectural rule.

<div align="center">

`21 Rust Crates` · `5 MCP Servers · 8 PO Agents` · `145+ tests`

</div>

<br>

---

## 19. Reeve &mdash; Governed Atlassian Administration

**The Atlassian writer where Verity and Steward are readers. Governed configuration, approval gates, state snapshots + rollback.**

Reeve is the governed Atlassian administration platform. It exposes 5 MCP servers for governed project/workflow/permission updates, with compliance-aware fleet artifacts generated by Citadel when the framework demands traceable Atlassian admin actions (SOX change control, HIPAA access review, SOC 2 privilege separation).

### 5 Governed MCP Servers &mdash; 102 Atlassian Tools

| Server | Domain | Tool surface |
|:--|:--|:--|
| **jira-config** | Projects, workflows, schemes, permissions | Project lifecycle, workflow CRUD, permission scheme bind/unbind, role assignment, custom field management |
| **jira-reporting** | Dashboards, filters, custom fields | Dashboard CRUD, JQL filter authoring, gadget configuration, sprint reports |
| **jsm** | Service desk configuration | Request type CRUD, SLA configuration, queue management, automation rules, customer portal config |
| **confluence-admin** | Spaces, permissions, page templates | Space CRUD, permission inheritance, template authoring, page restrictions, label governance |
| **plugin-governance** | Plugin lifecycle | Marketplace allowlists, version pinning, license attestation, security review tracking, deprecation handling |

### 4 Governed Agents

| Agent | Function |
|:--|:--|
| **config architect** | Reasons over configuration intent, proposes changes, surfaces conflicts before write |
| **reporting analyst** | Builds JQL filters and dashboards from plain-language asks |
| **hygiene enforcer** | Detects drift from declared configuration baselines, proposes corrective changes |
| **process optimizer** | Surfaces workflow inefficiencies, suggests structural improvements |

### Governed Write Architecture

- **7 CLI subcommands** for governed Atlassian admin
- **Plain-language intent** &mdash; describe configuration in natural language; the agent decomposes into typed tool calls
- **Approval gates** &mdash; HITL checkpoints for regulated changes (SOX change control, HIPAA access review, SOC 2 privilege separation)
- **State snapshots + rollback** &mdash; every change captured as a pre-state snapshot; rollback is a one-command revert
- **Read-write-http client** &mdash; governed write access (contrasts with Verity/Steward read-only). Type system distinguishes read vs. write operations
- **Compliance-aware fleet specs** &mdash; Citadel generates the agent + MCP fleet under the framework demanded by the customer's regulatory posture

### Knowledge Architecture

12 knowledge files (20,982 words) covering Atlassian admin patterns: workflow design, permission scheme inheritance, JSM SLA configuration, Confluence space governance, plugin lifecycle management, and audit-trail requirements per framework.

<div align="center">

`17 Rust Crates` · `5 MCP Servers · 102 Atlassian Admin Tools` · `532+ tests`

</div>

<br>

---

## 20. Author &mdash; Story/Epic Coaching Tool

**The authoring discipline tool. Generates epics and stories on command; deterministic refusal layer catches shallow authoring.**

Author generates epics and stories on command and enforces authoring discipline through a deterministic refusal layer that catches shallow authoring before it reaches Jira. The primary function is **generation** &mdash; building world-class epics and stories on command. The refusal layer is the safety net that prevents bad authoring from leaving the tool, not the headline feature.

### 6-Crate Workspace

| Crate | Role |
|:--|:--|
| **author-core** | Domain types, INVEST scoring, anti-pattern detection, refusal evaluator, gold-signature matcher |
| **author-store** | SQLite persistence for stories, drafts, gold signatures, adaptive tuning state |
| **author-llm** | LLM provider abstraction (Anthropic, OpenAI, Ollama) + keyword-skeleton fallback for air-gap |
| **author-control** | Workflow state machine: draft &rarr; coach &rarr; refusal-eval &rarr; accept/reject |
| **author-mcp** | MCP stdio server exposing authoring tools to other agents |
| **author-web** | axum web UI with story browser, draft authoring surface, refusal explanations |

### The Deterministic Refusal Layer

The refusal layer is structural quality enforcement that runs before any LLM output ships:

| Gate | What It Enforces |
|:--|:--|
| **INVEST scoring** | Independent, Negotiable, Valuable, Estimable, Small, Testable &mdash; numeric scoring with per-dimension thresholds |
| **DoR gates** | Definition of Ready compliance &mdash; acceptance criteria present, dependencies named, scope bounded |
| **15 anti-pattern detectors** | Shallow authoring patterns caught before submission &mdash; vague_value, role_missing_user_type, ac_implementation_detail, scope_horizontal_slice, dependency_silent, estimate_unmoored, story_disguised_epic, technical_task_as_story, etc. |
| **Gold-signature matcher** | Auto-anchoring against validated exemplars &mdash; the user has seen exactly one good epic/story set in his career; gold signatures encode that bar |
| **Adaptive tuning state** | Coach learns from accepted/rejected outputs &mdash; threshold weights adjust over time per user |

A draft that fails the refusal layer is rejected with structured reason; the user gets specific guidance on what to fix, not a generic "try again." Most real-world stories should fail, not pass &mdash; the refusal layer is calibrated against the user's authoring bar, not against the median.

### Capabilities

- **5 domain packs** &mdash; Domain-specific authoring templates and patterns
- **Scan + rewrite** &mdash; Bulk analysis of existing Jira stories with suggested rewrites
- **Live Jira JQL read + push** &mdash; Optional integration; pulls existing stories, pushes accepted drafts back
- **Confluence export** &mdash; Epic-level export to Confluence pages with structured layout
- **MCP stdio server + axum web UI** &mdash; Multi-surface access (terminal, browser, agent integration)
- **LLM coaching with keyword-skeleton fallback** &mdash; Works with or without LLM access; the keyword skeleton produces structurally valid drafts even air-gapped

### Quality Metrics

| Metric | Value | Meaning |
|:--|:--|:--|
| **MAE** | 0.109 | Mean absolute error between predicted and human-graded scores on reference corpus |
| **F1** | 0.97 | Anti-pattern detector precision/recall balance |
| **one-shot-good** | 10/10 | Reference corpus pass rate on first generation |

<div align="center">


---

## How They Connect

```
┌──────────────────────────────────────────────────────────────────────┐
│              DESIGN-TIME COMPILERS — the four Cs + Recon              │
│                                                                      │
│  ┌────────────┐                                                      │
│  │  Citadel   │──> compliance-aware design intelligence              │
│  │ (design)   │    (fleet specs, compliance docs, behavioral policy) │
│  └─────┬──────┘                                                      │
│        │                                                             │
│        v                                                             │
│  ┌────────────┐      ┌────────────┐      ┌────────────┐              │
│  │ Castellan  │─────>│  Charlotte │      │   Recon    │              │
│  │ (agents)   │      │  (context) │      │  (inbound) │              │
│  └─────┬──────┘      └─────┬──────┘      └─────┬──────┘              │
│        │                    │                    │                    │
│        │  (outbound:        │  (outbound:        │  (inbound: scans   │
│        │   compiled         │   compiled         │   already-built    │
│        │   agents)          │   MCP servers)     │   artifacts)       │
│        v                    v                    v                    │
│  ┌────────────────────────────────────────────────────┐              │
│  │       Chronicle (attestation substrate)            │              │
│  │   hybrid Ed25519 + ML-DSA-65 · OSCAL · ATO bundles │              │
│  └────────────────────────────────────────────────────┘              │
│                                                                      │
├──────────────────────────────────────────────────────────────────────┤
│                       RUNTIME SUBSTRATE                               │
│                                                                      │
│   Aegis ───────────> Pre-deployment audit gate. SHIP / BLOCK verdict │
│                      6-dimension spec validation. ATO + CMMC evidence│
│                                                                      │
│   Seneschal ───────> 30-check policy gate, 80 event types,           │
│                      83 violation classes, kill switch, FIPS 140-3   │
│                                                                      │
│   Garrison ────────> Customer shell (closed allowlist, 4 SKU tiers   │
│                      Hosted/Stronghold/Enclave/Sovereign, Level 6)   │
│                                                                      │
│   Drawbridge ──────> Governed A2A transport: Drawbridge + Console    │
│                      + Outpost + Portcullis. Classical + PQ tiers    │
│                                                                      │
│   Vigil + Edge ────> Behavioral telemetry, drift, amendment proposals│
│                      → Herald → Seneschal (closed-loop adaptation)   │
│                                                                      │
│   Bailiff ─────────> Rust agent runtime for Castellan Rust-target    │
│                      binaries. Closes Python gap for DoD IL5 / SCIF  │
│                                                                      │
│   Key Server ──────> Bootstrap step zero. License check before any   │
│                      binary will start. Sovereign offline tokens     │
│                                                                      │
├──────────────────────────────────────────────────────────────────────┤
│                            PRODUCTS                                   │
│                                                                      │
│   Audit Pro ───────> Productized audit of third-party agents.        │
│                      Recon scans → Chronicle-signed evidence bundle  │
│                                                                      │
│   Chancery ────────> AI CPO. PRDs + SDD bundles feed                 │
│   (AI CPO)           Charlotte + Castellan                           │
│                                                                      │
│   Quaestor ────────> RFP intelligence — judge offeror responses,     │
│                      surface fabricated quotes, three-skew binary    │
│                                                                      │
│   Augur ───────────> AI Strategy + CoE advisor; evidence layer       │
│                      under Citadel/Chancery spec generators          │
│                                                                      │
├──────────────────────────────────────────────────────────────────────┤
│                          OPERATOR LOOP                                │
│                                                                      │
│   Verity + Steward ──> Read Jira/Confluence/GitHub/Slack/Teams       │
│   (SM/PM)  (PO/PM)     surface intelligence, deliver reports         │
│                                                                      │
│   Reeve ───────────> Write Atlassian admin (governed, approval-gated)│
│                                                                      │
│   Author ──────────> Story/epic coaching with refusal layer          │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘

Outbound Build Loop:
Spec YAML → Citadel (compliance) → Castellan/Charlotte (compile binaries)
         → Aegis (SHIP/BLOCK verdict on bundle) → Key Server (license)
         → Garrison (host) → Seneschal (enforce) → Chronicle (sign)
         → Vigil (observe) → Herald (amend) → loop

Inbound Audit Loop (third-party customer agents):
Customer artifacts → Recon (extract + reconstruct) → Audit Pro (orchestrate)
                  → Castellan/Charlotte recompile → Chronicle sign
                  → 3PAO-verifiable evidence bundle

A2A Transport Loop:
Agent A (Territory T1) → Drawbridge sign + encrypt → Drawbridge transit
                       → Seneschal T2 policy gate → Agent B (Territory T2)
                       → Chronicle attest both sides

RFP Loop:
Federal solicitation .docx/.pdf → Quaestor judge → forensic verdict report
                                                  + Chronicle-signed evidence

CoE Engagement Loop:
Stakeholder intake → Augur Discovery → Shortlist → Translate → Govern → Present
              (catalogs feed Citadel + Chancery for governed spec generation)

Operator Lifecycle Loop:
Chancery (discover) → Author (write) → Jira → Verity + Steward (read) → Reeve (admin)
                                              SM / PM      PO / PM       Atlassian
```

### The Governance Loop

1. **Design** &mdash; Chancery compiles PRDs and SDD bundles. Citadel generates governance-aware fleet specs and regulatory documentation
2. **Build** &mdash; Charlotte compiles context/prompts/MCP servers. Castellan compiles agents. Both enforce compliance floors
3. **Audit Inbound** &mdash; Recon reverse-engineers compliance contracts from already-built customer artifacts. Inbound complement to outbound compilation
4. **Gate** &mdash; Aegis runs the pre-deployment audit across six dimensions (tool description poisoning, integrity-manifest agreement, MCP topology, behavioral policy floor, attestation provenance, license-token presence). SHIP / BLOCK verdict. Nothing reaches Garrison until Aegis says SHIP
5. **Host** &mdash; Garrison loads only Aegis-attested, Key-Server-licensed binaries. Closed allowlist. Four SKU tiers from Hosted to Sovereign
6. **Enforce** &mdash; Seneschal evaluates every agent action through a 30-check policy gate. 80 attestation events, 83 violation classes, kill switch, HMAC-SHA384 signing
7. **Transport** &mdash; Drawbridge carries every cross-territory agent message under per-message signing, encryption, attestation, and policy gating. Classical FIPS 140-3 + post-quantum tier
8. **Attest** &mdash; Chronicle signs runtime events with hybrid Ed25519 + ML-DSA-65; produces OSCAL packages and signed ATO bundles
9. **Observe + Amend** &mdash; Vigil and Vigil-Edge compare runtime behavior against the compiled baseline; synthesize amendments; Herald carries them back to Seneschal for mid-flight adaptation
10. **Audit Productized** &mdash; Audit Pro composes the engines into a customer-facing productized audit; emits Chronicle-signed evidence + drop-in recompiled specs
11. **Operate** &mdash; Chancery for conversational design. Quaestor for federal RFP judging. Augur for CoE engagement. Verity / Steward / Reeve / Author for the practitioner-side lifecycle &mdash; eating the platform's own dogfood

Every system is standalone. Together they close the loop.

---

## Platform Totals

<div align="center">

<br>

![Total Tests](https://img.shields.io/badge/24%2C000%2B-Tests_Passing-16A34A?style=for-the-badge)
![Total Systems](https://img.shields.io/badge/20-Production_Systems-7C3AED?style=for-the-badge)
![Total Standards](https://img.shields.io/badge/20%2B-Compliance_Standards-DC2626?style=for-the-badge)

<br>

### Design-Time Compilers

| | Castellan | Charlotte | Chronicle | Citadel | Recon | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|
| **Tests** | 8,600+ | 3,700+ | 394+ | 1,000+ | 2,917 | **16,611+** |

### Runtime Substrate

| | Aegis | Seneschal | Garrison | Drawbridge | Vigil + Edge | Bailiff | Key Server | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Tests** | 700+ | 179+ | 200+ | 100+ | 250+ | 50+ | 50+ | **1,500+** |

### Products

| | Audit Pro | Chancery | Quaestor | Augur | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|
| **Tests** | 215+ | 822+ | 83 | 209 | **1,329+** |

### Operator Loop

| | Verity | Steward | Reeve | Author | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|
| **Tests** | 3,900+ | 145+ | 532+ | 181+ | **4,758+** |

### Combined

| Metric | Value |
|:--|:--|
| **Total Systems** | **20** |
| **Total Tests (passing)** | **~24,000+** |
| **Compliance Standards** | **20+** (EU AI Act, NIST AI RMF, NIST 800-53, NIST 800-171 Rev 2, NIST CSF 2.0/CAISI, NIST IR 8596, FedRAMP Low/Moderate/High, DoD IL4/IL5, CMMC L1/L2/L3, CNSSP-12, CNSA 2.0, FIPS 140-3, FIPS 204 (ML-DSA), DoD STIG, HIPAA, PCI-DSS v4.0, SOC 2 Type II, ISO 42001, ISO 27001, ISO 42005, GDPR, GLBA Safeguards, FFIEC IT Handbook, SOX ITGC, OCC SR 11-7, FINRA 2026, MAS AI RM, Singapore IMDA, OWASP Top 10, CoSAI, COPPA) |
| **Languages** | Python, Rust, TypeScript |

<br>

**Stack**

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-2021-DEA584?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Axum](https://img.shields.io/badge/Axum-Rust-000000?style=flat-square)
![Tokio](https://img.shields.io/badge/Tokio-Async-000000?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-v2-E92063?style=flat-square&logo=pydantic&logoColor=white)
![rustls](https://img.shields.io/badge/rustls-mTLS-orange?style=flat-square)
![aws--lc--rs](https://img.shields.io/badge/aws--lc--rs-FIPS_140--3-yellow?style=flat-square)
![ML-DSA](https://img.shields.io/badge/ML--DSA--65-FIPS_204-purple?style=flat-square)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

![Claude](https://img.shields.io/badge/Claude_API-D4A574?style=flat-square&logo=anthropic&logoColor=black)
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-4285F4?style=flat-square&logo=google&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-Local-000000?style=flat-square)
![MCP](https://img.shields.io/badge/MCP-2025--11--25-8A2BE2?style=flat-square)
![OSCAL](https://img.shields.io/badge/OSCAL-NIST-blue?style=flat-square)
![Rekor](https://img.shields.io/badge/Rekor-Transparency-green?style=flat-square)

</div>

---

<br>

<div align="center">

## Let's Talk

</div>

If your team is shipping production AI agents and needs them **governed, compiled, attested, and audited** &mdash; not hand-assembled and hoped for &mdash; I built the platform that makes that possible.

**Currently open to**: Principal / Staff / Chief Architect roles building AI infrastructure for regulated-industry, federal, or defense-tier environments. Strongest fit for teams that need someone who can build the *entire stack* &mdash; design-time compilers, runtime enforcement, governed transport, observability, and customer-facing product surface &mdash; rather than one layer in isolation.

**Domain depth, in case it's useful**:

> **Agent governance platforms** · **Agent compilation** · **Runtime attestation & cryptographic evidence** · **Productized AI governance audits** · **Defense & federal compliance** (FIPS 140-3, FIPS 204 ML-DSA, CNSA 2.0, CNSSP-12, STIG, FedRAMP, DoD IL4/IL5, CMMC) · **Compliance evidence automation** (OSCAL, ATO bundles) · **SDLC automation** · **Rapid prototyping** from spec to production · Pre-deployment security auditing · Fleet governance monitoring · Context engineering and MCP server compilation · Test generation pipelines · OWASP security auditing · Federal RFP intelligence · AI Center-of-Excellence advisory · Product intelligence platforms for SM / PM / PO teams

<div align="center">

<br>

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

*20+ years enterprise ops · 2 IPOs · 4 acquisitions · Salesforce · IBM · Oracle · iHeartMedia*

<br>

</div>

