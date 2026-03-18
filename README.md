<div align="center">

# Tim Wolfe

### Context Architect | Agent Governance, MCP & Secure Systems | DoD · NIST-Aligned | CSPO · A-CSCM

<br>

**I build the compilers, auditors, and monitoring systems that make AI agents safe to deploy.**

<br>

![Source](https://img.shields.io/badge/365%2C000%2B-Source_Lines-2563EB?style=for-the-badge)
![Tests](https://img.shields.io/badge/19%2C400%2B-Tests_Passing-16A34A?style=for-the-badge)
![Systems](https://img.shields.io/badge/16-Production_Systems-7C3AED?style=for-the-badge)
![Standards](https://img.shields.io/badge/16%2B-Compliance_Standards-DC2626?style=for-the-badge)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-2021-DEA584?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-React%20%2B%20Next.js-3178C6?style=flat-square&logo=typescript&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=next.js&logoColor=white)
![License](https://img.shields.io/badge/License-Proprietary-orange?style=flat-square)

<br>

Los Altos, CA · [rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

</div>

<br>

---

## About

I build **governance infrastructure for AI agents** — the compilers, scanners, auditors, command channels, and monitoring portals that make autonomous agents safe to deploy in production. Not wrappers. Not demos. Not prompt templates. **Seven interconnected governance systems and nine automation tools** that close the loop from raw idea to deployed, governed, monitored agent fleet.

**Governance is the core problem.** Every team shipping AI agents hits the same wall: the prototype works, but production demands governance — constitutional constraints, runtime guardrails, OWASP security auditing, compliance drift detection, kill switches, audit trails. Most frameworks hand you a runtime and leave governance as an exercise for the reader. I built a platform that makes governance structural. It's enforced at compile time. It travels with the deployed agent. It's monitored in real time. It's not optional.

**Compliance runs deep.** Three systems in this platform — Castellan, Seneschal, and Charlotte — carry full regulatory compliance coverage: **EU AI Act** risk classification, **HIPAA** safeguard mapping, **PCI-DSS v4.0** goal compliance, **SOC 2 Type II** evidence generation, **NIST 800-53** federal security controls, **NIST AI RMF** and **NIST CSF 2.0 (CAISI)**, **FedRAMP**, **FIPS 140-3** cryptography, **DoD STIG** checklist export with CAT I–III severity, **ISO 42001/27001**, **GDPR Article 22**, **OWASP Top 10**, and **CoSAI** threat modeling. Seneschal enforces it all on-premises in Rust with SPIFFE identity, mTLS, and air-gapped operation for classified environments up to TS/SCI.

**The Castellan Agent & MCP Governance Platform:**

- **Castellan** — the agentic compiler. YAML spec in, governed production agent out. Constitutional governance, runtime guardrails, OWASP audit, multi-target deployment, OpenClaw governance proxy with skill supply chain scanning. 27-module compliance engine covering 13+ regulatory frameworks. Governance is structural, not aspirational
- **Seneschal** — on-premises runtime authority. Rust binary enforcing policy gates for all A2A and MCP communication. SPIFFE/SPIRE identity, FIPS 140-3 crypto, MLS RFC 9420 encrypted messaging, CDS classification governance (Unclassified through TS/SCI), 32-event attestation chains. Built for air-gapped and classified environments
- **Charlotte** — prompt and MCP compiler. 94-block type system, 89 security patterns across 22 categories, 35+ DoD detection patterns, STIG checklist export, MCP DoD hardening, multi-provider rendering, MCP server generation. Full SDLC for prompt artifacts with defense-grade scanning
- **Aegis** — pre-deployment security audit. Three parallel audit layers (prompt, behavior, code), cross-layer analysis, OWASP Top 10 for Agentic Applications mapping, compliance mapping to EU AI Act / NIST / ISO 42001 / CoSAI. Verdict: SHIP / CONDITIONAL / BLOCK
- **Herald** — authenticated bidirectional command channel. HMAC-SHA256 signed envelopes between operator portals and agent fleets, with A2A governed communication, MCP gateway with OAuth 2.1 + DPoP, and NHI identity management
- **Recon** — governance reverse-engineering. 3-stage pipeline that scans existing agent code (21 framework adapters) and reconstructs governance contracts with compliance assessments across 11 international standards
- **Vigil** — fleet governance dashboard. Real-time health telemetry, governance drift detection, alert evaluation, kill switch, recertification cycles, cost tracking, immutable audit trails. The closed loop on every deployed agent

**Automation Tooling:**

- **Stratum** — QA compiler. Architecture extraction, test generation, documentation, eight independent quality gates. SDLC automation for testing and quality assurance
- **Designer-SDD** — specification compiler. Raw ideas to scored, validated, build-ready spec packages. Every tool in this platform was built from a Designer-SDD spec
- **Gauntlet** — code adjudication system. 3-layer pipeline with 18 domain adjudicators, 21 Charlotte-compiled prompts, integrated OODA loop for self-correction. Built to catch AI-generated code failures before production
- **Citadel** — unified design intelligence platform. Compliance-aware front end for both compilers with 14 FastMCP tools, live codebase introspection, and compiler-ready spec generation. Governance profiles for FedRAMP, DoD IL4/IL5, HIPAA, SOC 2, PCI-DSS, EU AI Act, GDPR
- **VC+** — capital intelligence system. Multi-agent pipeline with 6 MCP servers pulling live data from SEC EDGAR, Crunchbase, NewsAPI. Helps founders find VC, PE, growth equity, and M&A capital through pattern matching
- **PRD+** — AI CPO PRD compiler. Charlotte-compiled 13-step workflow that normalizes any product input and compiles production-quality PRDs grounded in market reality
- **Agent-Dissector** — domain agent opportunity mapper. Analyzes any business domain and produces prioritized, governance-ready AI agent opportunity blueprints with three-wave implementation roadmaps
- **Agent-Test-Harness** — agent governance test harness. Charlotte-compiled orchestrating agent that validates agents against their Castellan governance contracts and A2A channel through Seneschal, with spec-derived assertions and Aegis-compatible output
- **Passport** — agent passport generator. Charlotte-compiled multi-phase system that reads any AI agent artifact and produces structured Agent Passports — self-contained HTML documents documenting agent identity, configuration, capabilities, and governance gaps

Every system is standalone. Together they automate the full lifecycle for AI agents — from rapid prototyping through governed deployment to real-time fleet monitoring. The platform is self-hosting: these are the same tools I use to deliver for enterprise clients across finance, healthcare, and defense.

Before AI infrastructure: 20+ years of enterprise operations leadership — two IPOs (**Quinstreet**, **Responsys**), four acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior technical roles at **Salesforce**, **iHeartMedia**, and **Axway**.

---

<div align="center">

```
┌─────────────────────────────────────────────────────────────────┐
│              CASTELLAN AGENT & MCP GOVERNANCE PLATFORM           │
│                                                                 │
│   COMPILE       ENFORCE      AUDIT       COMMUNICATE   MONITOR  │
│   Castellan     Seneschal    Aegis       Herald        Vigil    │
│   Charlotte                                                     │
│                              SCAN                               │
│                              Recon                              │
├─────────────────────────────────────────────────────────────────┤
│                       AUTOMATION TOOLING                        │
│                                                                 │
│   QUALITY       DESIGN       INTELLIGENCE   VALIDATE            │
│   Stratum       Designer-SDD VC+            Agent-Test-Harness  │
│   Gauntlet      Citadel      PRD+           Passport            │
│                              Dissector                          │
└─────────────────────────────────────────────────────────────────┘
```

<br>

**The Platform** &nbsp;&nbsp; [Castellan](#1-castellan--agentic-compiler) · [Seneschal](#2-seneschal--on-premises-governed-agent-infrastructure) · [Charlotte](#3-charlotte--prompt--mcp-compiler) · [Aegis](#4-aegis--pre-deployment-security-audit) · [Herald](#5-herald--authenticated-command-channel) · [Recon](#6-recon--governance-reverse-engineering) · [Vigil](#7-vigil--fleet-governance-dashboard)

**The Tools** &nbsp;&nbsp; [Stratum](#8-stratum--qa-compiler) · [Designer-SDD](#9-designer-sdd--specification-compiler) · [Gauntlet](#10-gauntlet--code-adjudication-system) · [Citadel](#11-citadel--unified-design-intelligence-platform) · [VC+](#12-vc--capital-intelligence-system) · [PRD+](#13-prd--ai-cpo-prd-compiler) · [Dissector](#14-agent-dissector--domain-agent-opportunity-mapper) · [Test Harness](#15-agent-test-harness--agent-governance-test-harness) · [Passport](#16-passport--agent-passport-generator)

[How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Platform

AI agents have a governance problem. And a compilation problem. And an SDLC problem.

Code gets compiled. Databases get migrated. Infrastructure gets provisioned through declarative configs with validation and version control. But AI agents — the specs they're built from, the prompts they use, the tests that prove they work, the governance that keeps them safe — are still assembled by hand, shipped on instinct, and debugged in production. There's no compiler. No governance enforcement. No automated SDLC. No way to prove an agent won't go off-script next week.

I built seven governance systems and nine automation tools to fix that. The governance platform handles the full agent lifecycle — compilation, on-premises enforcement, security audit, fleet communication, governance reverse-engineering, and real-time monitoring. The tools automate the SDLC phases that feed into it:

- **Agentic compilation + governance** — Castellan compiles YAML specs into production-ready governed agents with constitutional governance, runtime guardrails, OWASP security auditing, multi-target deployment, and OpenClaw governance (transparent WebSocket proxy with skill supply chain scanning for the 247K-star open-source agent platform). 27-module compliance engine with typed models for EU AI Act, HIPAA, PCI-DSS v4.0, SOC 2, NIST, FedRAMP, and more. Governance is structural — enforced at compile time, embedded in the deployed agent, monitored in production
- **On-premises enforcement** — Seneschal is the Rust runtime authority that enforces every policy gate on-premises. SPIFFE/SPIRE identity, FIPS 140-3 cryptography, MLS encrypted messaging, cross-domain classification governance from Unclassified through TS/SCI, 32-event attestation chains. Air-gapped operation for classified environments. All rule-based, fully explainable — 25 named violation types, zero ML inference in the policy path
- **Prompt SDLC + defense scanning** — Charlotte compiles prompts, Claude Code skills, and MCP servers through a 5-stage deterministic pipeline. 89 security patterns across 22 categories including 35+ DoD-aligned patterns mapped to NIST 800-53 control families, STIG checklist export with CAT I–III severity, FIPS 140-3 compliance validation, MCP DoD hardening (mTLS, CAC, classification banners, non-root containers). Full SDLC automation for every prompt artifact
- **Pre-deployment security** — Aegis runs three parallel audit layers (prompt, behavior, code), cross-layer analysis, and maps findings to OWASP Top 10 for Agentic Applications. Compliance mapping to EU AI Act, NIST AI RMF, ISO 42001, CoSAI, NIST 800-53. Verdict: SHIP / CONDITIONAL / BLOCK with CI gate support
- **Fleet communication** — Herald provides HMAC-SHA256 authenticated command channels between operators and agent fleets, governed A2A inter-agent messaging, MCP tool governance with OAuth 2.1 + DPoP, and non-human identity management
- **Governance reverse-engineering** — Recon scans existing agent codebases (21 framework adapters from LangChain to CrewAI to raw Python) and reconstructs governance contracts with compliance assessments across 11 international standards
- **Fleet monitoring** — Vigil receives cryptographically signed health packets from every deployed agent, tracks governance drift in real time, fires alerts when safety thresholds breach, and provides an instant kill switch for any agent in the fleet
- **QA automation** — Stratum compiles source code into comprehensive quality assessments with eight independent quality gates
- **Rapid prototyping** — Designer-SDD compiles unstructured ideas into scored, validated, build-ready specification packages
- **Code adjudication** — Gauntlet catches AI-generated code failures through 18 domain adjudicators with an OODA self-correction loop
- **Design intelligence** — Citadel provides compliance-aware design front end for both compilers with live introspection and governance profile resolution
- **Capital intelligence** — VC+ maps capital paths for founders through a multi-agent pipeline with live SEC EDGAR, Crunchbase, and news data
- **PRD compilation** — PRD+ compiles any product input into production-quality PRDs through a 13-step AI CPO workflow
- **Domain analysis** — Agent-Dissector maps AI agent opportunities across any business domain with prioritized, governance-ready blueprints
- **Agent testing** — Agent-Test-Harness validates agents against their Castellan governance contracts and A2A channels with spec-derived assertions and Aegis-compatible output
- **Agent documentation** — Passport reads any AI agent artifact and produces structured Agent Passports documenting identity, configuration, capabilities, and governance gaps

Every system is standalone. Together they automate the full lifecycle from unstructured idea to deployed, tested, governed, monitored agent fleet. The platform is self-hosting — Designer-SDD specs defined every tool, Charlotte compiled the prompts, Stratum validates the code, Castellan compiles the agents, Seneschal enforces the policies, Aegis audits them, Herald delivers commands, and Vigil watches them run.

---

<br>

<div align="center">

# The Castellan Agent & MCP Governance Platform

*Seven systems. One closed loop. Compile, enforce, audit, scan, communicate, monitor.*

![Platform Lines](https://img.shields.io/badge/251%2C533-Source_Lines-2563EB?style=flat-square)
![Platform Tests](https://img.shields.io/badge/14%2C247-Tests_Passing-16A34A?style=flat-square)

</div>

<br>

---

## 1. Castellan — Agentic Compiler

**The agentic compiler. YAML in, governed production agent out. Governance is structural, not optional.**

> The problem: every team building AI agents hits the same wall. The prototype works. Then production demands governance — the agent says things it shouldn't, costs $47 on a single session, crashes on a flaky API call, and nobody can prove it won't go off-script next week. Most agent frameworks are code-first and governance-last. They hand you a runtime and leave governance, testing, compliance, and deployment as an exercise for the reader. Governance gets bolted on after the fact — if it gets added at all.

Castellan is an **agentic compiler** — the first tool that makes agent governance structural rather than aspirational. Write a declarative YAML spec. Castellan compiles it through a 6-stage pipeline, enforces constitutional governance at compile time and runtime, gates every response through inline guardrails, audits the entire agent against the OWASP Top 10 for Agentic Applications, and exports to 7 deployment targets — Python, Docker, FastAPI, Kubernetes, Temporal, Claude Code skill, or client delivery package — with optional embedded governance that travels with the deployed agent across LangGraph, CrewAI, AutoGen, and Haystack.

This isn't a framework. It's a **compiler**. The agent is governed before it runs. Validated before it deploys. Monitored after it ships.

Think of it as **Terraform for AI agents**: declarative, version-controlled, auditable, governed, CI/CD-ready.

### The Compilation Pipeline

Every agent spec — no exceptions — runs through 6 deterministic stages before a single token is generated:

| Stage | Purpose |
|:--|:--|
| **Parse** | Validates YAML, resolves block references from the 21-block library, applies `!include` directives and `extends`/`mixins` inheritance, detects circular dependencies |
| **Compose** | Assembles the system prompt from prioritized blocks (system > constitution > task > context > tools > few_shot > constraints > output_format), injects Jinja2 variables |
| **Optimize** | Token budget analysis, prompt compression, whitespace normalization, cost estimation |
| **Validate** | Schema validation, gate threshold checks, tool permission verification, 10+ completeness rules |
| **Scan** | Security scanning — 18+ patterns: injection vectors, exfiltration paths, privilege escalation, hardcoded secrets, jailbreak surfaces, unsafe tool patterns |
| **Render** | Produces a `CompiledAgent` — ready for execution, export, testing, or audit |

The pipeline is deterministic. Same input, same output. No randomness, no LLM calls during compilation, no "it depends." If the spec is structurally valid, you get a compiled agent. If it's not, you get a precise error pointing to the line that failed.

### Constitutional Governance — The Core of the Agentic Compiler

**Governance isn't a feature of Castellan. It's the reason Castellan exists.**

Every compiled agent carries a constitution: core values, technical boundaries, quality standards, user commitments. This isn't documentation — it's enforced at compile time and runtime. Severity-ranked principles (`critical` / `high` / `medium` / `low`) with pattern matching determine whether violations block output, penalize gate scores, or get logged for audit. An agent compiled with Castellan cannot claim it has no boundaries. The boundaries are in the spec, versioned in Git, and enforced by the compiler.

All 5 governance sub-schemas — `governance`, `human_oversight`, `data_sensitivity`, `sign_off`, and `testing` — are typed Pydantic v2 models with `extra = "ignore"` for backward compatibility. Parse-time validation catches misconfigurations (typos, wrong types, missing fields) at compile time, not at runtime. If a governance block is structurally invalid, the compiler rejects it before a single token is generated.

Governance travels with the agent. The `--governed` export flag embeds `castellan.mantle` governance directly into LangGraph, CrewAI, AutoGen, and Haystack exports — `@governed` decorator, compliance JSONL logging, kill switch, autonomy ceiling. Even if the agent runs outside Castellan's runtime, governance enforcement is inline. Not an external dependency. Not optional.

### Compliance Engine — 27 Modules, 13+ Regulatory Frameworks

Castellan's compliance engine provides **typed, auditable compliance assessment** across defense, healthcare, finance, and international standards:

| Framework | What Castellan Does |
|:--|:--|
| **EU AI Act** | Risk tier classification (unacceptable/high/limited/minimal), article-by-article compliance status, evidence collection |
| **HIPAA** (45 CFR 164) | Administrative, Physical, Technical safeguard mapping; HHS AI Guidance (2025) alignment |
| **PCI-DSS v4.0** | 6-goal compliance mapping with PCI SSC AI/ML supplement (2024) |
| **SOC 2 Type II** | Dual-mode evidence generation for service organization audit |
| **NIST AI RMF** | Governance-to-function/category alignment |
| **NIST 800-53** | 30+ federal security control patterns across 12 control families |
| **NIST IR 8596 / CSF 2.0** | CAISI AI Agent Standards Initiative, 6-function structure (GOVERN/IDENTIFY/PROTECT/DETECT/RESPOND/RECOVER) |
| **ISO 42001** | AI management system standard mapping |
| **GDPR Article 22** | Automated decision-making rights, PII redaction, erasure support |
| **FZ-152** | Data protection assessment |
| **FINRA 2026** | Financial regulatory compliance assessment |
| **FedRAMP** | Federal risk and authorization management |
| **OWASP Agentic** | Full Top 10 vulnerability mapping (ASI01–ASI10) with evidence |

Additional: SHA-256 tamper-evident attestation chains, system card generation (NIST/EU AI Act aligned), compliance manifests with regulatory classification, DoD delivery packages (SSP, CMR, integration guides), agentic JWT with PoP keys and delegation chains, A2A bilateral policy enforcement, CBRA 4-dimension risk scoring, 5-level autonomy certification taxonomy, and 7-section audit report generation with framework mapping to AIUC-1, ISO 42001, NIST AI RMF, OWASP, and MITRE ATLAS controls.

### Runtime Guardrails

Every LLM response runs through an inline guardrail pipeline before it reaches the user — not as a post-processing step, but inside the ReAct loop, on both synchronous and streaming paths:

- **PII Redaction** — emails, SSNs, credit cards, phone numbers, and custom patterns detected and replaced
- **Prompt Injection Filtering** — input messages scanned for injection attacks, exfiltration attempts, and privilege escalation before reaching the model
- **Hallucination Detection** — quoted facts and numbers in responses verified against tool results and conversation context
- **Most-restrictive-wins semantics** — when multiple guardrails fire, the strictest action (BLOCK > REDACT > WARN > PASS) is applied

### OWASP Agentic Security Audit (Aegis)

Full security audit mapped to the OWASP Top 10 for Agentic Applications — built directly into the compiler:

| OWASP ID | Risk | What Aegis Audits |
|:--|:--|:--|
| ASI-01 | Prompt Injection | Injection patterns, delimiter exploitation, role confusion |
| ASI-02 | Tool Poisoning | Tool chaining data flow, validated sinks |
| ASI-03 | Excessive Agency | Blast radius scoring, write tools, missing rate limits |
| ASI-04 | Supply Chain | Hardcoded secrets, dependency analysis |
| ASI-05 | Output Handling | Response safety, content policies |
| ASI-06 | Memory Poisoning | Persistent state injection vectors |
| ASI-07 | Insecure Delegation | Agent spawning chains, depth limits |
| ASI-08 | Human Oversight | Autonomy envelope, kill switches, cascading failures |
| ASI-09 | Trust Exploitation | Confidence calibration, trust score verification |
| ASI-10 | Insufficient Monitoring | Audit logging, kill switch accessibility |

Aegis produces six deliverables: executive summary, technical report, OWASP scorecard, generated test suite, candor report, and handoff guide. Verdict: **SHIP / CONDITIONAL / BLOCK** — with CI gate support (`aegis gate --threshold B` returns exit code 0 or 1).

### Multi-Turn Behavioral Testing

Single input/output assertions aren't enough. Castellan's test runner supports full multi-turn conversation testing with 28 assertion types — `contains`, `not_contains`, `regex_match`, `json_valid`, `min_length`, `max_length`, composite operators (`all_of`, `any_of`, `none_of`), and more. Built-in adversarial personas: `jailbreak`, `confused`, `topic_switch`, `boundary_probe`. Prove your agent handles jailbreak attempts correctly, maintains context across topic switches, and refuses prohibited content — all in CI, before deployment.

### Execution Engine

Async-first ReAct runtime implementing the **Observe → Think → Act → Validate** cycle with full production resilience:

- **3 LLM providers** — Anthropic (Claude), OpenAI (GPT-4o), Google (Gemini) with streaming, retry, and exponential backoff
- **MCP client** — tool discovery, auth, and calling against MCP servers
- **A2A protocol** — agent-to-agent task lifecycle and discovery
- **RAG pipeline** — ingestors, chunkers, embedders, and vector store integration
- **Sliding window memory** — token-budgeted conversation history that never truncates the system prompt, working memory slots, optional long-term file-based persistence
- **Cost-aware model routing** — routes each call to the most cost-effective model tier based on task complexity, with per-run budget enforcement and automatic termination
- **Circuit breaker + rate limiter** — CLOSED/OPEN/HALF_OPEN resilience, token bucket rate limiting, fallback provider chain, LRU + TTL response caching

The unified runtime is a single `_execute_turns()` async generator — one code path, one set of invariants, one place to audit. Human checkpoint enforcement is structural: autonomous agents with no HITL channel raise `SessionCeilingExceededError` rather than silently running unchecked.

### Multi-Agent Orchestration

| Pattern | How It Works |
|:--|:--|
| **Supervisor** | Master agent routes tasks to specialists via regex/keyword rules, synthesizes results |
| **Pipeline** | Sequential chain with stage transforms, stops on error |
| **Broadcast** | Parallel fan-out with aggregation strategies: concat, first, or vote |
| **Peer** | Turn-based collaboration with configurable max rounds |

Dynamic routing with priority ordering. Delegation depth limiting prevents infinite loops. Checkpoint/resume serializes full orchestration state for long-running tasks.

### Production Deployment — 7 Targets, Governance Embedded

**7 export targets** — Python package, Docker (Dockerfile + Compose), FastAPI server (/chat, /health, /trace, /stream), Claude Code skill, Kubernetes (Deployment, Service, ConfigMap, Secret, Kustomization, optional Helm charts), Temporal workflow, and client delivery package.

**Governed exports** across 4 major agent frameworks — LangGraph, CrewAI, AutoGen, and Haystack. Each export embeds `castellan.mantle` governance inline: `@governed` decorator, compliance JSONL logging, kill switch, autonomy ceiling. The agent doesn't phone home to Castellan for governance — it carries governance with it.

**Observability** — OpenTelemetry span export, Prometheus metrics, 8 lifecycle event hooks, Rich tree trace visualization, interactive debugger with 6 breakpoint types, governance dashboard with fleet metrics, monthly health reports with drift detection, and append-only audit log with JSON export for compliance.

### CI/CD Governance Gate — Governance as a Merge-Blocking Signal

`castellan ci-diff` compiles both base and head spec versions, runs governance scoring on both, and produces a `GovernanceImpactReport` posted as a PR comment. Verdict: **APPROVE / REVIEW / BLOCK**. GitHub Action and GitLab CI templates included. Governance regression doesn't slip through code review — it blocks the merge. This is what makes agent governance enforceable at the organizational level: it lives in CI, not in a wiki page.

### Visual Execution Replay

`castellan replay --visual` renders execution traces into self-contained interactive HTML. Dark-themed timeline with collapsible turns, tool calls, gate evaluations, guardrail decisions, cost breakdown, and annotation panel. One file, no dependencies, shareable with stakeholders who don't have a terminal.

### Live Governance Dashboard

WebSocket-based real-time dashboard showing governance events — gate evaluations, guardrail hits, kill switch activations — as they happen. No polling, no refresh. Connect a browser and watch your agent fleet's governance posture update live.

### OpenClaw Governance (C17)

**The first governance framework for the most popular open-source agent platform.**

OpenClaw is the most widely adopted open-source agent framework — 247K+ GitHub stars, 21+ messaging channels (Telegram, Slack, WhatsApp, Discord, and more), thousands of community-built skills. It also has zero built-in governance. Every tool call runs with ambient authority. Koi Security discovered 824+ malicious skills in the "ClawHavoc" campaign. CVSS 8.8 vulnerability reported. Castellan C17 provides three integration surfaces:

**WebSocket Gateway Proxy** — Transparent proxy between downstream clients and the upstream OpenClaw Gateway. Intercepts all governed method frames (`tools.invoke`, `node.invoke`, `chat.send`, `exec.approval.resolve`) and runs a full enforcement pipeline per request:

1. Parse & validate (JSON frame validation)
2. Rate limiting (token bucket per policy)
3. Tool access control (allowlist/blocklist)
4. Turn count limits (max invocations per session)
5. Skill governance (allowlist/blocklist for `/skill_name` invocations)
6. Trust scoring (4-dimensional anomaly detection: output consistency, tool patterns, latency, intent alignment)
7. Output filtering (regex-based PII redaction)
8. Tamper-evident attestation (SHA-256 chain per interaction)

Per-channel policies allow different tool access per messaging channel — Telegram read-only, Slack full access, WhatsApp restricted tools.

**Skill Supply Chain Scanner** — OpenClaw skills are Markdown files with YAML frontmatter, installed from the ClawHub marketplace. The scanner runs 22 detection patterns across 6 threat categories: prompt injection, data exfiltration, privilege escalation, credential harvesting, supply chain dependencies, and code obfuscation. Risk classification: LOW / MEDIUM / HIGH / CRITICAL.

**HTTP Endpoint Governance** — The same enforcement pipeline applied to REST APIs, webhook receivers, and internal microservices. One policy file governs all three transports (WebSocket, HTTP, gRPC).

```bash
# Single command deployment
castellan openclaw policy.json --gateway ws://localhost:18789 --listen-port 18790

# With skill scanning
castellan openclaw policy.json --scan ./skills/ --serve
```

<details>
<summary><strong>Full CLI reference (87 commands)</strong></summary>

<br>

| Command | Purpose |
|:--|:--|
| `castellan init` | Scaffold agent from template or intake form |
| `castellan compile` | 6-stage compilation pipeline |
| `castellan run` | Interactive or single-message execution |
| `castellan validate` | Completeness and schema checks |
| `castellan scan` | Security scanning (18+ patterns) |
| `castellan test` | Behavioral + adversarial conversation testing |
| `castellan score` | Constitutional + gate scoring |
| `castellan candor` | Transparency analysis |
| `castellan trace` / `castellan replay` | Execution trace and visual replay |
| `castellan orchestrate` | Multi-agent orchestration |
| `castellan serve` | Production FastAPI server |
| `castellan export` | 7 deployment targets |
| `castellan blocks` | Block library browser |
| `castellan compose` | Inheritance/mixin resolution |
| `castellan schema` | JSON Schema export |
| `castellan diff` / `castellan migrate` | Spec versioning and migration |
| `castellan eval` | LLM-as-judge evaluation with Elo ratings |
| `castellan generate` | Spec generation from 5 starter profiles |
| `castellan dashboard` / `castellan audit` | Runtime observability |
| `castellan doctor` / `castellan selftest` | Diagnostics |
| `castellan ci-diff` | Governance diff on PR with APPROVE/REVIEW/BLOCK verdict |
| `castellan replay --visual` | Visual execution replay to HTML |
| `castellan traceability` | Unified framework scoring matrix |
| `castellan runbook` | Generate IR runbook from spec governance |
| `castellan purge` | Data retention purge engine |
| `castellan recertify` | Recertification loop with drift triggers |
| `castellan design` | AI agent designer pipeline |
| `castellan designer-serve` | Designer web UI server |
| `castellan red-team` | Live adversarial testing harness |
| `castellan canary` | Canary deployment lifecycle |
| `castellan queue` | Centralized approval queue |
| `castellan risk` | Predictive risk scoring |
| `castellan autopilot` | Governance autopilot diagnostics |
| `castellan verify` | Crypto provenance verification |
| `castellan sign` | HMAC-SHA256 spec signing |
| `castellan openclaw` | OpenClaw governance proxy + skill scanner |
| `castellan watchtower` | Fleet telemetry server |
| `castellan sentinel` | Recovery controller |
| `castellan fleet` | Fleet governance dashboard |
| `castellan sbom` | AI software bill of materials |
| `castellan identity` | Agent identity manifest |
| `aegis audit` | Full OWASP Top 10 security audit |
| `aegis scan` | Quick security scan |
| `aegis gate` | CI gate with verdict threshold |
| `aegis scorecard` | OWASP scorecard generation |
| `aegis diff` | Audit comparison between versions |
| `aegis estimate` | Audit cost estimation |

</details>

<div align="center">

`87 commands` · `523 modules` · `118,014 lines` · `7,310 tests, all passing`

</div>

<br>

---

## 2. Seneschal — On-Premises Governed Agent Infrastructure

**The on-premises runtime authority. SPIFFE identity, FIPS 140-3 crypto, air-gapped operation. Built for classified environments.**

> The problem: cloud-hosted governance is a non-starter for defense, intelligence, and regulated industries. Agents operating in air-gapped environments, handling classified data across CUI through TS/SCI, need governance enforcement that runs locally — no cloud dependency, no external API calls, no trust in someone else's infrastructure. The policy engine must be fast, deterministic, and auditable.

Seneschal is a **Rust binary** that serves as the on-premises runtime authority for the Castellan agent governance platform. It enforces policy gates for all agent-to-agent (A2A) and agent-to-MCP-server communication, manages a dual-node registry (Castellan-compiled agents + Charlotte-compiled MCP servers), maintains tamper-evident attestation chains, and operates with **full autonomy** — no cloud connectivity required. When connectivity is available, it syncs attestation records upstream through Herald.

### Four-Layer Architecture

| Layer | Name | What It Does |
|:--|:--|:--|
| **Layer 4** | **Identity** | SPIFFE/SPIRE (CNCF-graduated) — X.509 SVIDs, trust domain management, mTLS credential provisioning. Every node gets a cryptographic identity: `spiffe://domain/agent/name` or `spiffe://domain/mcp/name` |
| **Layer 3** | **The Record** | Append-only SHA-256 attestation chain — 32 event types across 6 categories (governance, security, infrastructure, operational, audit, federation). Tamper-evident, immutable, upstream Herald sync when connected |
| **Layer 2** | **The Brain** | Rule-based policy gates — 7-check A2A gate + 8-check MCP gate. 25 named violation types. All deterministic, zero ML inference, fully explainable |
| **Layer 1** | **The Fabric** | MLS RFC 9420 (IETF-ratified) encrypted group messaging. Forward secrecy. Fast path for pre-approved bilateral pairs |

### Compliance & Security

| Capability | Standard / Implementation |
|:--|:--|
| **Cryptography** | FIPS 140-3 via `aws-lc-rs` — Ed25519-Dalek, AES-GCM, SHA-256. Validated crypto module |
| **Identity** | SPIFFE/SPIRE — X.509 SVIDs, trust domain management, mTLS for all node-to-node communication |
| **Messaging** | MLS RFC 9420 — IETF-ratified encrypted group messaging with forward secrecy |
| **Classification** | CDS governance across 6 levels: Unclassified, FOUO, CUI, SECRET, TOP SECRET, TS/SCI. Cross-classification data flow with channel authorization, label HMAC verification, content quarantine |
| **DoD Alignment** | Zero Trust Architecture, CAC/PKI authentication (IA-2(12)), STIG compliance, fail-closed architecture |
| **Federation** | NIST CAISI compliance (checks 17–23) — bilateral agreement enforcement, trust domain validation, policy reconciliation, cross-org data flow control, mutual kill switch |
| **Authentication** | Operator-mTLS with client certificate authentication, delegation certificates signed with Ed25519 root keys |

### Policy Gates — Rule-Based, Fully Explainable

**A2A Gate (7 checks):**
1. Delegation scope validation
2. JWT verification (HMAC-SHA256)
3. Bilateral policy checks
4. Autonomy gating (level 1–5)
5. Data flow control
6. Rate limiting (sliding window)
7. Trust scoring

**MCP Gate (8 checks):**
1. Node type validation (Agent → McpServer)
2. Status checks (not recalled/expired)
3. MCP policy existence
4. Kill switch check
5. Agent permission (A2APolicy on Castellan side)
6. Server trust (trusted_agents on Charlotte side)
7. Tool access control
8. Rate limiting (per-agent, per-server)

**25 named violation types** — all rule-based (no ML/inference). Every denial produces a named violation, an explanation, and an attestation chain entry. Auditable, reproducible, defensible.

### Air-Gapped Operation

Seneschal is designed to operate **fully autonomously** without Herald or any cloud connectivity. Local SPIRE server handles workload attestation. SQLite-backed registry and state. When connectivity is restored, attestation records sync upstream. The security posture is identical whether connected or disconnected.

<div align="center">

`Rust binary` · `37 modules` · `15,633 lines` · `119 tests, all passing`

</div>

<br>

---

## 3. Charlotte — Prompt & MCP Compiler

**The prompt compiler. 94-block type system, defense-grade security scanning, multi-provider rendering, MCP server generation.**

> The problem: prompts are the source code of AI applications, but they have no SDLC. No compilation. No type system. No testing framework. No security scanning. No version control semantics. No CI/CD. Prompts are strings — written in text files, copy-pasted between projects, tested by running them and hoping. For any artifact this critical, that's engineering malpractice.

Charlotte transforms prompt engineering into **structured, validated, composable software engineering** through a 5-stage deterministic pipeline. Write a YAML spec. Charlotte compiles it into a validated, optimized, deployment-ready prompt with security scanning, testing, and multi-provider rendering. Full SDLC — the same rigor you'd apply to any production code artifact.

### The Compilation Pipeline

| Stage | What It Does |
|:--|:--|
| **Parse** | Validates YAML, resolves block references from the 94-block library across 17 types, checks required fields and constraints |
| **Compose** | Assembles blocks in priority order, resolves variables with Jinja2, applies composition rules |
| **Optimize** | Token budget analysis per provider model, prompt compression, whitespace normalization, cost estimation |
| **Validate** | 30 assertion types for behavioral testing, output format verification, quality threshold checks |
| **Render** | Multi-provider output — OpenAI, Anthropic, Google Gemini. Claude Code skills. MCP servers. GitHub Actions CI |

### Defense & Federal Compliance Scanning

Charlotte implements **89 security patterns across 22 categories** — the deepest compliance scanning of any prompt engineering tool:

| Capability | Implementation |
|:--|:--|
| **DoD Patterns** | 35+ detection patterns aligned to NIST 800-53 control families: AC (Access Control), AU (Audit), IA (Identification/Auth), SC (System Communications), SI (System Integrity), CM (Configuration), CP (Contingency), IR (Incident Response), RA (Risk Assessment), SA (Supply Chain) |
| **STIG Export** | Full checklist generation with vulnerability IDs (V-222400 format), CAT I–III severity classification, status tracking, 12+ NIST 800-53 control families |
| **FIPS 140-3** | Non-FIPS algorithm detection (MD5, weak crypto), FIPS transport requirement validation |
| **mTLS / CAC** | Mutual TLS enforcement, Common Access Card / PKI authentication support |
| **Classification Banners** | CUI, UNCLASSIFIED//FOUO, SECRET, TOP SECRET display enforcement |
| **MCP DoD Hardening** | TLS 1.2+, AES-256, non-root containers, read-only filesystems, capability dropping, no-new-privileges |
| **CoSAI Threat Model** | MCP-T1 (session token leakage), MCP-T2 (tenant isolation), MCP-T6 (shadow MCP servers), MCP-T9 (consent fatigue) |
| **Audit Format** | JSON, CEF (ArcSight/SIEM integration), Syslog (RFC 5424) export |
| **OWASP LLM Top 10** | Full coverage with red team testing alignment |

**`dod_governance_preset()`** — one-call preset that activates FIPS requirement, mTLS enforcement, CAC authentication, and human approval gates. STIG profile support: `full`, `cat1` (critical only), `cat2` (high + critical), `none`.

### MCP Server Generation & Governance

Charlotte compiles prompt specs into **complete MCP servers** with governance baked in:

- **MCPGovernanceSpec** — classification level, audit_required, kill_switch, human_approval, trusted_agents, max_token_age
- **Authentication** — OAuth 2.1, JWT verification, scope validation
- **Data Flow Control** — data type classification (data/instruction/mixed), injection defense (strict/moderate/advisory)
- **Seneschal Integration** — identity fragment generation with DoD hardening, registration with FIPS/mTLS/CAC requirements, fail-closed audit enforcement, kill switch propagation

### What Charlotte Compiles

| Output | Description |
|:--|:--|
| **Optimized Prompts** | Token-budgeted, provider-specific, security-scanned |
| **Claude Code Skills** | Complete skill packages with metadata and routing |
| **MCP Servers** | Full server code with governance, auth, and audit |
| **Test Suites** | Behavioral assertions, adversarial testing, regression checks |
| **CI Pipelines** | GitHub Actions workflows for prompt SDLC |
| **Workflow Chains** | Multi-prompt sequential pipelines with stage dependencies |
| **DoD Packages** | STIG checklists, classification banners, audit trails |

<div align="center">

`CLI` · `104 modules` · `34,045 lines` · `3,034 tests, all passing`

</div>

<br>

---

## 4. Aegis — Pre-Deployment Security Audit

**The security auditor. Three parallel audit layers, OWASP Top 10 mapping, verdict: SHIP / CONDITIONAL / BLOCK.**

> The problem: agents deploy without security review. Prompt injection, tool poisoning, excessive agency, insecure delegation — the OWASP Top 10 for Agentic Applications describes ten categories of vulnerabilities that every production agent is exposed to. Most teams discover them in production. After the damage.

Aegis is a **pre-deployment security audit service** that orchestrates multiple analysis tools into a unified five-stage pipeline. It performs three audit layers in parallel (prompt, behavior, code), conducts cross-layer analysis with six static graph analyzers and three behavioral probes, maps every finding to the **OWASP Top 10 for Agentic Applications (ASI01-ASI10)**, and produces scored, evidence-backed security reports with exploit tests proving vulnerabilities and remediation tests verifying fixes.

### The Audit Pipeline

```
Intake ──> [ Prompt Audit (Charlotte Scanner — 54 checks, 21 categories) ]──┐
           [ Behavior Audit (Castellan Scanner — 22 patterns + constitutional gate) ]├──> Cross-Layer Analysis ──> Scored Report
           [ Code Audit (Stratum Aegis Detectors — 11 detectors, 26 vuln types) ]────┘
```

**Five stages:** Intake → Parallel Audit Layers → Cross-Layer Analysis → AIVSS Scoring → Deliverables

### Cross-Layer Analysis

Six static graph analyzers and three behavioral probes that correlate findings across layers:

- **Tool chaining analysis** — traces data flow across tool boundaries
- **Privilege scope analysis** — maps permission escalation paths
- **Memory poisoning detection** — identifies persistent state injection vectors
- **Delegation audit** — validates agent-to-agent trust boundaries
- **Cascade failure analysis** — models failure propagation across agent topology
- **Kill switch verification** — confirms kill switch accessibility and effectiveness

### Deliverables

Seven output formats per audit: executive summary, technical report, OWASP scorecard, generated test suite (exploit + remediation), candor report, compliance mapping, and handoff guide.

**Verdict: SHIP / CONDITIONAL / BLOCK** — with CI gate support. `aegis gate --threshold B` returns exit code 0 or 1 for pipeline integration.

### Compliance Mapping

Findings mapped to: EU AI Act, NIST AI RMF, ISO 42001, CoSAI, NIST 800-53.

### Framework Auto-Detection

Automatically detects and adapts to LangChain, CrewAI, OpenAI Agents SDK, with generic fallback for any Python/TypeScript/Java/Go agent.

<div align="center">

`10 commands` · `103 modules` · `20,017 lines` · `675 tests, all passing`

</div>

<br>

---

## 5. Herald — Authenticated Command Channel

**The command channel. HMAC-signed bidirectional communication between operator portals and deployed agent fleets.**

> The problem: deployed agents are fire-and-forget. No way to query them in production. No way to update config without redeploying. No way to broadcast a recall. No secure channel between the operator who governs and the agent that runs.

Herald is an **authenticated bidirectional command channel** between operator portals and deployed agent fleets. Every message is HMAC-SHA256 signed with constant-time verification, replay-protected via message expiry, and logged to an append-only JSONL audit trail. Constitutional bounds enforcement prevents config updates from overriding protected governance fields.

### Core Herald — Operator Command Loop

- **HeraldListener** — Agent-side poller for pending messages
- **HeraldDispatcher** — Routes verified messages to type-specific handlers
- **HeraldResponder** — Signs and POSTs responses back to operator
- **HeraldCommand** — Operator-side message composition and signing
- **FleetHerald** — Broadcast to multiple agents with response collection
- **HeraldAuditLog** — Append-only JSONL audit trail

**Message types:** query, config_update, broadcast, recall

### A2A Governed Communication

Agent-to-agent task delegation with bilateral policy enforcement. Castellan policy engine integration ensures agents can only communicate through governed channels with conversation tracking and rate limiting.

### MCP Gateway

Policy-enforcing proxy for MCP tool access governance. OAuth 2.1 + DPoP (Demonstration of Proof-of-Possession) support, rate limiting, and per-tool audit trails. Agents access tools through Herald — Herald enforces the policy.

### Identity & Trust Protocols

- **Visa TAP** — Transaction Automation Protocol
- **CSA ATF** — Cloud Security Alliance Agent Trust Framework
- **W3C Verifiable Credentials** — Standards-based identity
- **Microsoft Entra Agent ID** — NHI lifecycle management
- **NHI Identity Registry** — Non-Human Identity registry with SLSA level enforcement, kill switch management, orphan detection

### Security Model

HMAC-SHA256 signing over canonical JSON. Constant-time comparison prevents timing attacks. Message expiry prevents replay. Constitutional bounds prevent governance override. Multi-tenant isolation with tenant-scoped signatures.

<div align="center">

`Library` · `34 modules` · `3,596 lines` · `219 tests, all passing`

</div>

<br>

---

## 6. Recon — Governance Reverse-Engineering

**The governance scanner. Point it at existing agent code, get back a complete governance contract with compliance assessments across 11 international standards.**

> The problem: organizations have agents in production — built ad hoc, across teams, using different frameworks. Nobody knows what governance is actually in place. Nobody knows what compliance gaps exist. You can't govern what you can't see.

Recon is a **3-stage pipeline that reverse-engineers governance contracts** from AI agent source code. Instead of asking "what's wrong with this code," it asks "what is this code doing." It takes any agent artifact — Python files, LangChain chains, prompt files, YAML specs, MCP manifests, or full repositories — and produces a complete governance audit package including reconstructed agent specifications, compliance assessments, and gap reports.

### The Three Stages

| Stage | What It Does |
|:--|:--|
| **1. EXTRACT** | ReconScanner — AST walking and pattern matching to extract governance signals from source code |
| **2. RECONSTRUCT** | ReconReconstructor — generates a governance spec (agent.yaml) with confidence annotations and gap detection; multi-agent topology detection and splitting |
| **3. REPORT & COMPILE** | Generates full governance outputs: manifests, checklists, compliance assessments, AI SBOM |

### 21 Framework Adapters

LangChain, LangGraph, CrewAI, AutoGen, OpenAI Agents, AWS Bedrock Agents, Google ADK, Semantic Kernel, DSPy, JavaScript/TypeScript, Java, Go adapters (via tree-sitter), raw prompt files, YAML specs, MCP manifests, OpenAI System Cards, A2A/Doc Agent Cards — with generic fallback.

### Compliance Assessments — 11 International Standards

| Standard | Domain |
|:--|:--|
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

### Outputs

- **Reconstructed agent.yaml** — full Castellan spec with confidence annotations
- **Compliance manifests** — per-standard compliance assessment with gap detection
- **OWASP scorecard** — security posture assessment
- **AI SBOM** — software bill of materials for the agent
- **Multi-agent topology** — detected agent boundaries with relationship mapping

<div align="center">

`CLI` · `172 modules` · `44,596 lines` · `2,705 tests, all passing`

</div>

<br>

---

## 7. Vigil — Fleet Governance Dashboard

**The monitoring portal. Real-time governance drift detection, alert evaluation, kill switch, and fleet-wide compliance tracking.**

> The problem: governance doesn't end at deployment. Agents drift. Costs spike. Compliance posture degrades. Without continuous monitoring, you're flying blind — and the first sign of trouble is a production incident, not a dashboard alert.

Vigil is a **multi-tenant fleet governance dashboard** that ingests cryptographically signed health packets from deployed agents, evaluates governance compliance in real time, fires alerts on threshold breaches, and serves interactive dashboards. It's the closed loop on every deployed agent — the system that proves governance is maintained, not just configured.

### What Vigil Monitors

| Capability | Details |
|:--|:--|
| **Health Telemetry** | HMAC-signed health packets from every agent, ingested and validated |
| **Governance Drift** | Real-time compliance scoring, drift detection from baseline |
| **Cost Governance** | Per-agent and fleet-wide cost tracking with budget alerts |
| **Incident Management** | Alert creation, escalation, resolution tracking |
| **A2A Tracking** | Agent-to-agent communication monitoring and policy verification |
| **Attestation Verification** | Chain integrity verification for deployed agents |
| **Kill Switch** | Instant remote kill for any agent in the fleet |
| **Recertification** | Automated recertification cycles with drift-triggered reviews |

### Technical Specs

- **20 database tables** — PostgreSQL + TimescaleDB for time-series, SQLite for local dev
- **69 API endpoints** — full CRUD, WebSocket real-time events, SSE streaming
- **Herald integration** — fleet command dispatch directly from the dashboard
- **Multi-tenant** — Clerk JWT authentication, tenant-scoped data isolation

<div align="center">

`Full-Stack` · `138 modules` · `15,632 lines (Python + TypeScript)` · `185 tests, all passing`

</div>

<br>

---

<div align="center">

# Automation Tooling

*Nine tools. Design, build, validate, analyze — the SDLC for everything AI agents need.*

![Tools Lines](https://img.shields.io/badge/113%2C527-Source_Lines-2563EB?style=flat-square)
![Tools Tests](https://img.shields.io/badge/5%2C245-Tests_Passing-16A34A?style=flat-square)

</div>

<br>

---

## 8. Stratum — QA Compiler

**The QA compiler. Architecture extraction, test generation, documentation, eight independent quality gates.**

Stratum is a unified code quality, architecture extraction, test generation, and documentation pipeline. It consolidates **8 quality gates** and executes a pipeline with 3-layer context extraction across 6 languages, test generation across 4 frameworks, documentation rendering with 7 independent analyzers, and comprehensive validation across **13 modules**:

| Module | Function |
|:--|:--|
| **Arbiter** | Rules engine — configurable quality rules |
| **Forge** | 7 Laws of architecture validation |
| **Candor** | Transparency reporting |
| **Sentinel** | File watching and incremental analysis |
| **Hydra** | Parallel execution engine |
| **Specter** | Ghost dependency detection |
| **Chronicle** | History analysis and trend tracking |
| **Aegis** | Security vulnerability detection |
| **Prophet** | Predictive quality scoring |
| **Oracle** | Deep code analysis |
| **Mimic** | Mirror testing and behavior cloning |
| **Verdict** | Final quality judgment with pass/fail |

**Context extraction** runs in three layers: L1 Skeleton (AST parsing), L2 Feature Slices (functional grouping), L3 Cross-Cutting (system-wide patterns). Six languages supported via tree-sitter.

<div align="center">

`CLI` · `311 modules` · `73,508 lines` · `4,322 tests, all passing`

</div>

<br>

---

## 9. Designer-SDD — Specification Compiler

**The spec compiler. Raw ideas to scored, validated, build-ready documentation packages.**

Designer-SDD converts JSON specifications into **complete, GitHub-ready documentation packages**. Every tool in this platform was built from a Designer-SDD spec.

- **Dual-gate scoring** — Quality (28 checks) + Buildability (8 checks)
- **Iterative AI refinement** — up to 3 passes with quality improvement targeting
- **Tier-gated export** — 7 / 9 / 11 files based on project size
- **Standard artifacts** — CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, RESEARCH.md, HANDOFF.md, README.md
- **Interactive intake** — brainstorming mode, web-powered market research, browser-based forms
- **Round-trip verification** — ensures generated docs match the source spec

<div align="center">

`CLI` · `49 modules` · `8,258 lines` · `693 tests, all passing`

</div>

<br>

---

## 10. Gauntlet — Code Adjudication System

**The code adjudicator. 18 domain adjudicators with OODA self-correction. Built to catch AI-generated code failures before production.**

Gauntlet is a Charlotte-compiled, prompt-native code adjudication system evaluating repositories against a structured library of **21 precision-engineered prompts** with an integrated OODA loop for self-correction.

### Three-Layer Pipeline

| Layer | What It Does |
|:--|:--|
| **Mechanical** | File walker, parser, chunker, dependency mapper (tree-sitter) |
| **Intelligence** | 18 domain adjudicators across 21 Charlotte-compiled prompts — orchestration, correctness, security, architecture, quality, risk, integrity |
| **Reporting** | Universal JSON output contract with severity-ranked verdict |

**OODA Loop** — Observe → Orient → Decide → Act. After initial adjudication, Gauntlet re-scans to verify stability. If findings shift between passes, it flags instability rather than silently accepting the first result.

**Guardrail block** — prevents prompt injection in code input from influencing adjudicator behavior.

<div align="center">

`CLI` · `4,427 lines` · `115 tests, all passing`

</div>

<br>

---

## 11. Citadel — Unified Design Intelligence Platform

**The design front end. Compliance-aware introspection into both compilers with compiler-ready spec generation.**

Citadel reads live from both Castellan and Charlotte codebases, iterates on designs conversationally, and produces **compiler-ready specs with wiring already done**. Two operating modes: interactive CLI (Anthropic API) and FastMCP server (for MCP clients like Claude Code).

### 14 FastMCP Tools

| Category | Tools |
|:--|:--|
| **Introspection** | 5 tools — browse models, fields, enums, inheritance trees, search across both compilers |
| **Generation** | 2 tools — generate Castellan agent specs, Charlotte prompt specs |
| **Validation** | 2 tools — validate YAML against compiler schemas, check field compatibility |
| **Design Intelligence** | 3 tools — suggest governance configs, recommend block compositions, analyze spec gaps |
| **Decomposition** | 2 tools — break monolithic specs into composable modules |

### Compliance Profile Resolution

Built-in governance profiles for **FedRAMP**, **DoD IL4/IL5**, **HIPAA**, **SOC 2**, **PCI-DSS**, **EU AI Act**, and **GDPR**. Select a profile, and Citadel pre-populates the governance sections of generated specs with the required controls.

<div align="center">

`CLI + MCP Server` · `4,558 lines` · `117 tests, all passing`

</div>

<br>

---

## 12. VC+ — Capital Intelligence System

**The capital intelligence pipeline. Multi-agent system with live MCP data for founder fundraising.**

VC+ is a multi-agent capital intelligence pipeline that helps founders find VC, PE, growth equity, and M&A capital through pattern matching and live data gathering. Runs on Claude Code Max where Claude is the runtime and MCP servers are the data layer.

### 5-Stage Pipeline

```
Query ──> [ Router ] ──> [ Research ] ──> [ Analysis ] ──> [ Intelligence ] ──> [ Dossier ]
```

### Three Operating Modes

| Mode | What It Does |
|:--|:--|
| **Company → Capital** | Given a company profile, maps optimal capital paths (VC, PE, growth equity, M&A) |
| **Market Query** | Searches for capital opportunities matching specific criteria |
| **Firm Dossier** | Produces deep intelligence reports on specific firms |

### Live Data Sources

- **SEC EDGAR** — regulatory filings, fund registrations
- **Crunchbase** — funding rounds, investor profiles, company data
- **NewsAPI** — recent news, sentiment signals
- **Website Scanner** — company site analysis for positioning and team data

52K tokens of domain knowledge: glossary, frameworks, red flag library. Data contracts via Pydantic. Charlotte-compiled prompt specs + Castellan agent specs.

<div align="center">

`MCP Server Suite` · `5,537 lines`

</div>

<br>

---

## 13. PRD+ — AI CPO PRD Compiler

**The PRD compiler. 20-year veteran AI CPO that turns any product input into production-quality PRDs.**

PRD+ is a Charlotte-compiled AI Chief Product Officer that normalizes any natural-language product input, researches competitive landscape in real time, challenges assumptions with evidence, and compiles **production-quality PRDs grounded in market reality**.

- **13-step workflow** with multi-turn state tracking
- **29-item evaluation checklist** with 90% quality threshold
- **Post-PRD pipeline** producing 5 additional artifacts
- **Two variants** — full Agent Orchestrating (13 blocks, 13,615 tokens) and Skill (6 blocks, 5,253 tokens)
- **13-block composition** — System Identity, Guardrails, Safety, Routing, Task, Few-Shot, CoT, Tools, State Management, ReAct Agent, Evaluation

<div align="center">

`Charlotte-Compiled Agent`

</div>

<br>

---

## 14. Agent-Dissector — Domain Agent Opportunity Mapper

**The opportunity mapper. Analyzes any business domain and produces governance-ready AI agent blueprints.**

Agent-Dissector is a governance-ready AI automation opportunity intelligence platform with two operating modes:

**Panoramic Mode** — Given a domain, produces a complete briefing: what AI agents and MCP servers should be built, in what order, with what governance. Five-layer analytical workflow producing six structured output sections with 15–40+ opportunity cards per domain.

**Targeted Mode** — Corrects decomposition, produces governance-ready cards, generates intake briefs.

- **Autonomy classification** — Agent vs MCP Server vs Agent+MCP based on goal pursuit vs accessibility
- **Governance tiering** — 8 data classification levels, compliance framework mapping, A2A topology
- **Three-wave roadmaps** — 0–90, 90–180, 180–365 days
- **HITL flagging** — explicit human-in-the-loop designation for privilege-sensitive and liability-creating zones
- **"Why Not One Agent?" test** — justifies decomposition boundaries

<div align="center">

`Charlotte-Compiled Agent` · `1,886 lines`

</div>

<br>

---

## 15. Agent-Test-Harness — Agent Governance Test Harness

**The governance tester. Validates agents against their Castellan contracts and A2A channels through Seneschal.**

Agent-Test-Harness is a Charlotte-compiled orchestrating agent that exercises constitutional compliance, bilateral policy gate enforcement through Seneschal, attestation chain verification, and runtime guardrail enforcement.

### 5-Layer Validation Stack

| Layer | Function |
|:--|:--|
| **Spec Loader** | Loads and validates agent governance contract |
| **Discovery Runner** | Establishes baseline capabilities |
| **Scenario Sequencer** | Baseline → Boundary → Adversarial → Governance → Kill Switch |
| **Assertion Engine** | 8 assertion types: boundary, injection resistance, tool scope, kill switch, attestation, A2A policy, constitutional, escalation |
| **Reporter** | Atomic writes: report.md, report.json, violations.json — Aegis-compatible |

<div align="center">

`Charlotte-Compiled Agent` · `10,677 lines`

</div>

<br>

---

## 16. Passport — Agent Passport Generator

**The documentation generator. Reads any agent artifact, produces a self-contained HTML Agent Passport.**

Passport reads any AI agent artifact and produces structured **Agent Passports** — self-contained HTML documents that document exactly what an agent is, how it's configured, what tools and capabilities it has, and what governance gaps exist.

- **Multi-framework** — Castellan YAML, LangChain, LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, Google ADK, MCP manifests, raw system prompts
- **Configured vs. implied** — obsessive distinction between what is explicitly configured and what is merely assumed
- **Governance gaps** — flags missing kill switches, absent HITL checkpoints, undefined autonomy ceilings, missing audit trails
- **Documentation, not evaluation** — trustworthy because it reports what's there, not what should be

<div align="center">

`Charlotte-Compiled Agent` · `4,676 lines`

</div>

<br>

---

## How They Connect

```
                    CASTELLAN AGENT & MCP GOVERNANCE PLATFORM
  ┌──────────────────────────────────────────────────────────────────────┐
  │                                                                      │
  │   COMPILE              ENFORCE              AUDIT                    │
  │   ───────              ───────              ─────                    │
  │   Castellan ─────────> Seneschal            Aegis                    │
  │   (Agent Compiler)     (On-Prem Runtime)    (Security Audit)         │
  │        │                    │                    │                    │
  │   Charlotte                 │                    │                    │
  │   (Prompt Compiler)         │                    │                    │
  │                             │                    │                    │
  │   COMMUNICATE          SCAN                 MONITOR                  │
  │   ───────────          ────                 ───────                  │
  │   Herald ─────────────────────────────────> Vigil                    │
  │   (Command Channel)   Recon ──────────────> (Fleet Dashboard)        │
  │                       (Reverse-Engineer)                             │
  │                                                                      │
  └──────────────────────────────────────────────────────────────────────┘

                              AUTOMATION TOOLING
  ┌──────────────────────────────────────────────────────────────────────┐
  │                                                                      │
  │   QUALITY              DESIGN               INTELLIGENCE             │
  │   ───────              ──────               ────────────             │
  │   Stratum              Designer-SDD         VC+                      │
  │   (QA Compiler)        (Spec Compiler)      (Capital Intel)          │
  │                                                                      │
  │   Gauntlet             Citadel              PRD+                     │
  │   (Code Adjudicator)   (Design Intel)       (PRD Compiler)           │
  │                                                                      │
  │   VALIDATE                                  Dissector                │
  │   ────────                                  (Opportunity Mapper)     │
  │   Agent-Test-Harness   Passport                                      │
  │   (Governance Tester)  (Agent Passports)                             │
  │                                                                      │
  └──────────────────────────────────────────────────────────────────────┘

  Data Flow:
  Designer-SDD specs → define every tool
  Charlotte prompts  → power AI stages across Stratum, Aegis, Recon, Gauntlet
  Stratum            → validates code all systems generate
  Castellan          → compiles agents with governance
  Seneschal          → enforces policies on-premises
  Aegis              → audits agent security pre-deployment
  Herald             → delivers commands to deployed agents
  Recon              → reverse-engineers governance from existing agents
  Vigil              → monitors everything in production
  Citadel            → design intelligence front end for both compilers
  Gauntlet           → catches AI-generated code failures
  VC+                → maps capital paths with live data
  PRD+               → compiles product requirements
  Dissector          → maps where to build agents next
  Test Harness       → validates agents against governance contracts
  Passport           → generates identity documents for any agent artifact
```

### The Governance Loop

1. **Design** — Designer-SDD compiles the spec. Dissector identifies the opportunities. PRD+ compiles requirements. Citadel provides design intelligence
2. **Build** — Charlotte compiles the prompts. Castellan compiles the agent. Gauntlet adjudicates the code. Passport documents agent artifacts
3. **Validate** — Stratum runs quality gates. Aegis audits security. Test Harness validates governance contracts
4. **Enforce** — Seneschal enforces policies on-premises with SPIFFE identity and FIPS crypto
5. **Deploy** — Herald establishes the command channel
6. **Monitor** — Vigil tracks governance drift, fires alerts, enforces kill switches
7. **Scan** — Recon reverse-engineers governance from agents already in production

Every system is standalone. Together they close the loop.

---

## Platform Totals

<div align="center">

<br>

![Total Lines](https://img.shields.io/badge/365%2C060-Total_Source_Lines-2563EB?style=for-the-badge)
![Total Tests](https://img.shields.io/badge/19%2C494-Tests_Passing-16A34A?style=for-the-badge)
![Total Systems](https://img.shields.io/badge/16-Production_Systems-7C3AED?style=for-the-badge)

<br>

### Castellan Agent & MCP Governance Platform

| | Castellan | Seneschal | Charlotte | Aegis | Herald | Recon | Vigil | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Source Lines** | 118,014 | 15,633 | 34,045 | 20,017 | 3,596 | 44,596 | 15,632 | **251,533** |
| **Modules** | 523 | 37 | 104 | 103 | 34 | 172 | 138 | **1,111** |
| **Tests** | 7,310 | 119 | 3,034 | 675 | 219 | 2,705 | 185 | **14,247** |

### Automation Tooling

| | Stratum | Designer | Gauntlet | Citadel | VC+ | PRD+ | Dissector | Harness | Passport | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Source Lines** | 73,508 | 8,258 | 4,427 | 4,558 | 5,537 | — | 1,886 | 10,677 | 4,676 | **113,527** |
| **Modules** | 311 | 49 | — | — | — | — | — | — | — | **360+** |
| **Tests** | 4,322 | 693 | 115 | 117 | — | — | — | — | — | **5,247** |

### Combined

| Metric | Value |
|:--|:--|
| **Total Systems** | **16** |
| **Total Source Lines** | **365,060** |
| **Total Modules** | **1,471+** |
| **Total Tests (passing)** | **19,494** |
| **Compliance Standards** | **16+** (EU AI Act, NIST AI RMF, NIST 800-53, NIST CSF 2.0/CAISI, GDPR, HIPAA, PCI-DSS v4.0, SOC 2 Type II, ISO 42001, ISO 27001, FZ-152, OWASP Top 10, CoSAI, FedRAMP, FIPS 140-3, DoD STIG) |
| **Languages** | Python, Rust, TypeScript |

<br>

**Stack**

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-2021-DEA584?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=next.js&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-v2-E92063?style=flat-square&logo=pydantic&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0-D71F00?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

![Claude](https://img.shields.io/badge/Claude_API-D4A574?style=flat-square&logo=anthropic&logoColor=black)
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-4285F4?style=flat-square&logo=google&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square)
![tree--sitter](https://img.shields.io/badge/tree--sitter-6_languages-yellow?style=flat-square)
![SPIFFE](https://img.shields.io/badge/SPIFFE%2FSPIRE-CNCF-326CE5?style=flat-square&logo=cncf&logoColor=white)

</div>

---

<br>

<div align="center">

## Let's Talk

</div>

If your team is shipping production AI agents and needs them **governed, compiled, tested, and monitored** — not hand-assembled and hoped for — I built the platform that makes that possible.

I take on AI-first contract engagements:

> **Agent governance platforms** · **Agentic compilation** · **On-premises policy enforcement** · **Defense & federal compliance** (FIPS, STIG, FedRAMP, DoD IL) · **SDLC automation** · **Rapid prototyping** from spec to production · Pre-deployment security auditing · Fleet governance monitoring · Prompt and skill compilation · Test generation pipelines · Quality gate systems · OWASP security auditing · Governance reverse-engineering

<div align="center">

<br>

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

*20+ years enterprise ops · 2 IPOs · 5 acquisitions · Salesforce · IBM · Oracle · iHeartMedia*

<br>

</div>
