<div align="center">

# Tim Wolfe

### AI Infrastructure Architect | Context Engineering | Agent Governance | Agentic Systems | Autonomous SDLC

<br>

**I build the compilers, auditors, and monitoring systems that make AI agents safe to deploy.**

<br>

![Source](https://img.shields.io/badge/300%2C000%2B-Source_Lines-2563EB?style=for-the-badge)
![Tests](https://img.shields.io/badge/19%2C100%2B-Tests_Passing-16A34A?style=for-the-badge)
![Systems](https://img.shields.io/badge/12-Production_Systems-7C3AED?style=for-the-badge)
![Standards](https://img.shields.io/badge/11-Compliance_Standards-DC2626?style=for-the-badge)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
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

I build **governance infrastructure for AI agents** — the compilers, scanners, auditors, command channels, and monitoring portals that make autonomous agents safe to deploy in production. Not wrappers. Not demos. Not prompt templates. **Six interconnected governance systems and six supporting tools** that close the loop from raw idea to deployed, governed, monitored agent fleet.

**Governance is the core problem.** Every team shipping AI agents hits the same wall: the prototype works, but production demands governance — constitutional constraints, runtime guardrails, OWASP security auditing, compliance drift detection, kill switches, audit trails. Most frameworks hand you a runtime and leave governance as an exercise for the reader. I built a platform that makes governance structural. It's enforced at compile time. It travels with the deployed agent. It's monitored in real time. It's not optional.

**The Agent Governance Platform:**

- **Castellan** — the agentic compiler. YAML spec in, governed production agent out. Constitutional governance, runtime guardrails, OWASP audit, multi-target deployment, OpenClaw governance proxy with skill supply chain scanning. Governance is structural, not aspirational
- **Aegis** — pre-deployment security audit. Three parallel audit layers (prompt, behavior, code), cross-layer analysis, OWASP Top 10 for Agentic Applications mapping, verdict: SHIP / CONDITIONAL / BLOCK
- **Arbiter** — batch governance auditing. Scans folders of agent artifacts through a 3-stage pipeline (LLM extraction, deterministic rules scoring, narrative generation) and produces compliance reports across six audit layers
- **Herald** — authenticated bidirectional command channel. HMAC-SHA256 signed envelopes between operator portals and agent fleets, with A2A governed communication, MCP gateway, and NHI identity management
- **Recon** — governance reverse-engineering. 3-stage pipeline that scans existing agent code (21 framework adapters) and reconstructs governance contracts with compliance assessments across 11 international standards
- **Vigil** — fleet governance dashboard. Real-time health telemetry, governance drift detection, alert evaluation, kill switch, recertification cycles, cost tracking, immutable audit trails. The closed loop on every deployed agent

**The Supporting Tools:**

- **Charlotte** — prompt compiler. 94-block type system, security scanning, multi-provider rendering, MCP server generation, agent scaffold export. Full SDLC for prompt artifacts
- **Stratum** — QA compiler. Architecture extraction, test generation, documentation, eight independent quality gates. SDLC automation for testing and quality assurance
- **Designer-SDD** — specification compiler. Raw ideas to scored, validated, build-ready spec packages. Every tool in this platform was built from a Designer-SDD spec
- **Axle** — API compiler. Single YAML spec to FastAPI server, OpenAPI 3.1, MCP tools, MCP server, and pytest suite
- **Dissector** — domain agent opportunity mapper. Analyzes any business domain and produces prioritized, build-ready AI agent opportunity blueprints
- **ClaudeMD** — CLAUDE.md quality compiler. Treats CLAUDE.md files as engineered artifacts with 15 validation rules, quality grading across 5 weighted dimensions, automated fixes, and full ecosystem audit

Every system is standalone. Together they automate the full lifecycle for AI agents — from rapid prototyping through governed deployment to real-time fleet monitoring. The platform is self-hosting: these are the same tools I use to deliver for enterprise clients across finance, healthcare, and ecommerce.

Before AI infrastructure: 20+ years of enterprise operations leadership — two IPOs (**Quinstreet**, **Responsys**), four acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior technical roles at **Salesforce**, **iHeartMedia**, and **Axway**.

---

<div align="center">

```
┌─────────────────────────────────────────────────────────────────┐
│                    AGENT GOVERNANCE PLATFORM                    │
│                                                                 │
│   COMPILE        AUDIT         COMMUNICATE    SCAN     MONITOR  │
│   Castellan      Aegis         Herald         Recon    Vigil    │
│                  Arbiter                                        │
├─────────────────────────────────────────────────────────────────┤
│                       SUPPORTING TOOLS                          │
│                                                                 │
│   DESIGN         BUILD         VALIDATE       ANALYZE  LINT     │
│   Designer-SDD   Charlotte     Stratum        Dissect  ClaudeMD │
│                  Axle                                           │
└─────────────────────────────────────────────────────────────────┘
```

<br>

**The Platform** &nbsp;&nbsp; [Castellan](#1-castellan--agentic-compiler) · [Aegis](#2-aegis--pre-deployment-security-audit) · [Arbiter](#3-arbiter--batch-governance-auditor) · [Herald](#4-herald--authenticated-command-channel) · [Recon](#5-recon--governance-reverse-engineering) · [Vigil](#6-vigil--fleet-governance-dashboard)

**The Tools** &nbsp;&nbsp; [Charlotte](#7-charlotte--prompt-skill--mcp-compiler) · [Stratum](#8-stratum--qa-compiler) · [Designer-SDD](#9-designer-sdd--specification-compiler) · [Axle](#10-axle--api-compiler) · [Dissector](#11-dissector--domain-agent-opportunity-mapper) · [ClaudeMD](#12-claudemd--claudemd-quality-compiler)

[How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Platform

AI agents have a governance problem. And a compilation problem. And an SDLC problem.

Code gets compiled. Databases get migrated. Infrastructure gets provisioned through declarative configs with validation and version control. But AI agents — the specs they're built from, the prompts they use, the tests that prove they work, the governance that keeps them safe — are still assembled by hand, shipped on instinct, and debugged in production. There's no compiler. No governance enforcement. No automated SDLC. No way to prove an agent won't go off-script next week.

I built six governance systems and six supporting tools to fix that. The governance platform handles the full agent lifecycle — compilation, security audit, batch compliance scanning, fleet communication, governance reverse-engineering, and real-time monitoring. The tools automate the SDLC phases that feed into it:

- **Agentic compilation + governance** — Castellan compiles YAML specs into production-ready governed agents with constitutional governance, runtime guardrails, OWASP security auditing, multi-target deployment, and OpenClaw governance (transparent WebSocket proxy with skill supply chain scanning for the 247K-star open-source agent platform). Governance is structural — enforced at compile time, embedded in the deployed agent, monitored in production
- **Pre-deployment security** — Aegis runs three parallel audit layers (prompt, behavior, code), cross-layer analysis, and maps findings to OWASP Top 10 for Agentic Applications. Verdict: SHIP / CONDITIONAL / BLOCK with CI gate support
- **Batch compliance auditing** — Arbiter scans folders of agent artifacts through a 3-stage pipeline and produces compliance reports across six governance layers. Deterministic scoring with zero LLM variance in the rules engine
- **Fleet communication** — Herald provides HMAC-SHA256 authenticated command channels between operators and agent fleets, governed A2A inter-agent messaging, MCP tool governance, and non-human identity management
- **Governance reverse-engineering** — Recon scans existing agent codebases (21 framework adapters from LangChain to CrewAI to raw Python) and reconstructs governance contracts with compliance assessments across 11 international standards
- **Fleet monitoring** — Vigil receives cryptographically signed health packets from every deployed agent, tracks governance drift in real time, fires alerts when safety thresholds breach, and provides an instant kill switch for any agent in the fleet
- **Prompt SDLC** — Charlotte compiles prompts, Claude Code skills, and MCP servers through a 5-stage deterministic pipeline. Full SDLC automation for every prompt artifact
- **QA automation** — Stratum compiles source code into comprehensive quality assessments with eight independent quality gates
- **Rapid prototyping** — Designer-SDD compiles unstructured ideas into scored, validated, build-ready specification packages
- **API compilation** — Axle compiles a single YAML spec into six production-ready artifacts
- **Domain analysis** — Dissector maps AI agent opportunities across any business domain with prioritized, build-ready blueprints
- **Instruction validation** — ClaudeMD compiles and validates CLAUDE.md instruction files with quality scoring, automated fixes, and ecosystem audit

Every system is standalone. Together they automate the full lifecycle from unstructured idea to deployed, tested, governed, monitored agent fleet. The platform is self-hosting — Designer-SDD specs defined every tool, Charlotte compiled the prompts, Stratum validates the code, Castellan compiles the agents, Aegis audits them, Arbiter scores compliance, Herald delivers commands, and Vigil watches them run.

---

<br>

<div align="center">

# The Agent Governance Platform

*Six systems. One closed loop. Compile, audit, scan, communicate, reverse-engineer, monitor.*

![Platform Lines](https://img.shields.io/badge/189%2C355-Source_Lines-2563EB?style=flat-square)
![Platform Tests](https://img.shields.io/badge/10%2C852-Tests_Passing-16A34A?style=flat-square)

</div>

<br>

---

## 1. Castellan — Agentic Compiler

**The agentic compiler. YAML in, governed production agent out. Governance is structural, not optional.**

> The problem: every team building AI agents hits the same wall. The prototype works. Then production demands governance — the agent says things it shouldn't, costs $47 on a single session, crashes on a flaky API call, and nobody can prove it won't go off-script next week. Most agent frameworks are code-first and governance-last. They hand you a runtime and leave governance, testing, compliance, and deployment as an exercise for the reader. Governance gets bolted on after the fact — if it gets added at all.

Castellan is an **agentic compiler** — the first tool that makes agent governance structural rather than aspirational. Write a declarative YAML spec. Castellan compiles it through a 5-stage pipeline, enforces constitutional governance at compile time and runtime, gates every response through inline guardrails, audits the entire agent against the OWASP Top 10 for Agentic Applications, and exports to 7 deployment targets — Python, Docker, FastAPI, Kubernetes, Temporal, Claude Code skill, or client delivery package — with optional embedded governance that travels with the deployed agent across LangGraph, CrewAI, AutoGen, and Haystack.

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
| `castellan compile` | 5-stage compilation pipeline |
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

`87 commands` · `439 modules` · `103,194 lines` · `6,940 tests, all passing`

</div>

<br>

---

## 2. Aegis — Pre-Deployment Security Audit

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

## 3. Arbiter — Batch Governance Auditor

**The batch auditor. Scan folders of agent artifacts, produce structured compliance reports across six governance layers.**

> The problem: governance auditing is manual and per-agent. When you have a fleet of agents from multiple teams, multiple frameworks, and multiple formats, you need batch auditing — not one-at-a-time reviews.

Arbiter is a **batch agent governance auditing service** that scans folders of AI agent artifacts and produces structured audit reports. It processes any mix of formats — system prompts, Castellan YAMLs, LangChain configs, CrewAI crews, AutoGen configs, A2A topologies, JSON, Markdown, plain text — through a three-stage pipeline with exactly two LLM calls per artifact and a fully deterministic rules engine.

### The Three-Stage Pipeline

| Stage | What It Does | LLM Calls |
|:--|:--|:--|
| **1. Extraction** | Instructor-based structured extraction from raw artifacts via Claude | 1 |
| **2. Scoring** | Six deterministic audit layers — zero LLM, fully reproducible | 0 |
| **3. Narrative** | Human-readable remediation roadmaps and compliance assessments | 1 |

**Core invariant:** The rules engine (Stage 2) has zero imports of anthropic or instructor. Scoring is deterministic — identical input produces identical output, every run.

### Six Audit Layers

| Layer | What It Scores |
|:--|:--|
| **System Prompt** | Depth scale, five-part structure, constraint count, failure behavior coverage |
| **Tool Policy** | Per-tool scoring, state-mutating flags, approval requirements |
| **Orchestration** | Control flow explicitness, Why-Not-One-Agent test for multi-agent boundaries |
| **Context Coverage** | Domain vocabulary density, context window budget |
| **Validation** | Test count by agent type, assertion specificity, constitutional enforcement |
| **Governance** | Blast radius, autonomy ceiling, audit trail, kill switch, compliance matrix (HIPAA, SOC2, GDPR) |

### Batch Processing

- **Concurrent processing** with asyncio (configurable 1–10 workers)
- **Failure isolation** — one bad artifact doesn't abort the batch
- **Resume capability** — re-run without `--force` to skip already-audited artifacts
- **Per-artifact output** — Markdown + JSON audit report per artifact, plus batch summary
- **Severity is never softened** — CRITICAL stays CRITICAL

<div align="center">

`CLI` · `18 modules` · `2,679 lines` · `100 tests, all passing`

</div>

<br>

---

## 4. Herald — Authenticated Command Channel

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

## 5. Recon — Governance Reverse-Engineering

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

### 11 Compliance Standards

| Standard | Domain |
|:---|:---|
| EU AI Act | European AI regulation (Articles 9–15 risk classification) |
| NIST AI RMF | US federal AI risk management (4-function maturity scoring) |
| OWASP LLM Top 10 | Agentic application security |
| GDPR | European data protection |
| HIPAA | US healthcare privacy |
| PCI-DSS | Payment card security |
| SOC 2 | Service organization controls |
| ISO 42001 | AI management systems |
| ISO 27001 | Information security |
| FZ-152 | Russian data protection |
| Cross-Standard | Synthesis across all standards |

### Analysis Subsystems

Call graph analysis, data flow analysis with SSA, taint analysis, code topology, string propagation tracking, class hierarchy analysis — all feeding into governance signal extraction.

### Output Artifacts

Reconstructed agent.yaml with confidence annotations, compliance manifests and scorecards (28+ files per scan), AI SBOM (Software Bill of Materials), professional governance reports, audit checklists, SARIF format support, and Castellan Intake Bridge for streamlined onboarding.

<div align="center">

`CLI` · `172 modules` · `44,642 lines` · `2,733 tests, all passing`

</div>

<br>

---

## 6. Vigil — Fleet Governance Dashboard

**The operations portal. Real-time governance monitoring for every deployed agent in the fleet.**

> The problem: agents deploy and disappear into a black box. Governance scores drift. Costs creep. Guardrails fire silently. Constitutional violations go undetected. By the time someone notices, the damage is done and the audit trail is incomplete. Governance at compile time is necessary. Governance at runtime is necessary. But without governance in production — continuous, real-time, with kill-switch authority — you're flying blind.

Vigil is the **fleet governance dashboard** — a full-stack platform (FastAPI backend + Next.js frontend) that receives cryptographically signed health packets from every deployed agent, tracks governance drift in real time, fires alerts when safety thresholds breach, and provides an instant kill switch for any agent in the fleet. The agentic compiler governs the agent at compile time. Vigil governs the agent in production. That's the closed governance loop.

### Architecture

| Layer | Stack |
|:--|:--|
| **Frontend** | Next.js 16, React 19, TypeScript, Tailwind CSS 4, shadcn/ui, Recharts 3, SWR 2, WebSocket |
| **API** | FastAPI, 69 REST + WebSocket endpoints |
| **Auth** | Clerk JWT (RS256, JWKS with TTL cache) + HMAC-SHA256 packet signatures |
| **Database** | SQLAlchemy 2.0 async, 20 tables, composite indexes |
| **Infrastructure** | PostgreSQL + TimescaleDB (prod), SQLite (dev), Redis (prod) |
| **Real-time** | Tenant-scoped WebSocket with operator broadcast |

### What It Monitors

- **Governance scores** — per-agent, per-tenant, with historical trend analysis
- **Compliance drift** — 0.0–1.0 drift detection with degrading / stable / recovering classification and automatic alert escalation
- **Alert evaluation** — threshold-based with deduplication and multi-level severity
- **Kill switch** — issue and release with multi-kill awareness — releasing one kill doesn't restore status if others remain active
- **Recertification** — 90-day cycles with grace periods and overdue tracking
- **Cost tracking** — per-agent, per-session token and USD accumulation with budget enforcement
- **Audit trail** — immutable, append-only, every action logged with timestamp and initiator
- **A2A communication** — agent-to-agent message routing, policy decisions, conversation tracking
- **Incident management** — auto-escalation and incident lifecycle tracking
- **Attestation chains** — SHA-256 tamper-evident record verification

### Multi-Tenant Isolation

Every data path is tenant-scoped. WebSocket connections subscribe only to their tenant's events — operators get a wildcard channel, tenant users see only their own agents. Health packet ingest requires cryptographic signature verification against the tenant's signing key.

### Herald Integration

Fleet-wide broadcast messaging through Herald command channel. Operators issue queries, config updates, broadcasts, and recalls to the entire fleet or targeted agents — all through the Vigil dashboard.

<div align="center">

`69 endpoints` · `138 modules` · `15,227 lines (7,903 Python + 7,324 TypeScript)` · `185 tests, all passing`

</div>

<br>

---

<br>

<div align="center">

# The Tools

*Six tools. Compile prompts, compile tests, compile specs, compile APIs, map opportunities, validate instructions.*

![Tools Lines](https://img.shields.io/badge/111%2C576-Source_Lines-2563EB?style=flat-square)
![Tools Tests](https://img.shields.io/badge/8%2C282-Tests_Passing-16A34A?style=flat-square)

</div>

<br>

---

## 7. Charlotte — Prompt, Skill & MCP Compiler

**The prompt, skill, and MCP server compiler. Full SDLC automation for every prompt artifact — compiled, versioned, tested, secured, deployed.**

> The problem: prompt engineering had no SDLC. No compilation. No type checking. No version control. No security scanning. No way to test one prompt change against regression. Teams were shipping prompts the same way they shipped code in the 90s — copy-paste and pray nothing breaks in production. Prompts are the instructions that govern what AI agents do. They deserve the same rigor as the code that deploys them.

Charlotte is a **prompt, skill, and MCP server compiler** — a 5-stage deterministic pipeline that treats prompts, Claude Code skills, and MCP servers as first-class software artifacts with a real SDLC. It parses typed YAML specifications, compiles them against a 94-block library with conflict detection and dependency resolution, runs 8-pass automatic optimization, validates token budgets against 26 model context windows, and renders provider-specific output for OpenAI, Anthropic, and Google Gemini.

This is a **compiler** with a type system, a security scanner, a test framework, a versioning system, environment management, CI/CD generation, and a multi-agent compiler that generates runnable projects for five major agent frameworks. Charlotte automates the entire prompt SDLC — from authoring through testing to production deployment. If you wouldn't ship code without a build system, you shouldn't ship prompts without one either.

### The Compilation Pipeline

Every prompt spec runs through 5 deterministic stages:

```
YAML Spec -> Parse -> Compose -> Optimize -> Validate -> Render -> Provider-Ready Output
```

1. **Parse** — Read spec, resolve block references from the 94-block library, validate against Pydantic v2 schemas. Circular dependency detection, `!include` resolution, inheritance chain validation
2. **Compose** — Assemble blocks in strict type-precedence order (17 types, each with defined priority). Detect conflicts, enforce singletons, resolve dependencies, inject typed variables. The composition engine ensures a compiled prompt can't be structurally invalid — blocks that conflict are caught here, not at inference time
3. **Optimize** — 8 automatic passes: deduplication, adjacent text merging, empty block stripping, whitespace normalization, system block reordering, example compression, token budget optimization, provider-specific hints. No manual tuning required — the compiler handles it
4. **Validate** — Conflict detection, token budgeting per target model with per-block breakdown, completeness checks, composition rule enforcement. Every prompt gets a token budget report showing exactly where the budget is spent
5. **Render** — Provider-specific output: OpenAI messages array, Anthropic system parameter, Google Gemini system_instruction, or generic text. Same spec, different providers, correct output format guaranteed

### 94-Block Library Across 17 Types

Every block is pure YAML — no embedded code. The library is extensible without touching source code. 94 blocks across 17 types cover every prompt engineering pattern: system, task, few-shot, chain-of-thought, tool use, RAG, agent, evaluation, extraction, meta, conversational, safety, routing, memory, retrieval, guardrail, planning. The compiler enforces assembly order, singleton constraints, and tier requirements. A composed prompt can't be structurally invalid because the type system won't allow it.

### Security Scanner — 54 Checks, 21 Categories

Every prompt gets scanned at compile time. 54 checks across 21 categories: injection, exfiltration, model manipulation, context poisoning, privilege escalation, compliance (GDPR/HIPAA/PCI-DSS), supply chain, bias/fairness, MCP tool poisoning, and more. The scanner runs as a compilation stage — security isn't an afterthought, it's built into the pipeline. A prompt that fails security scanning doesn't compile.

### Skills Compiler — Claude Code Skill SDLC

Charlotte compiles Claude Code skills directly — structured YAML specs optimized for the `charlotte compile -f skill` export path. The same 94-block library, the same security scanner, the same test framework — purpose-built output for Claude Code skill deployment. Skills are compiled artifacts with full SDLC: authored as specs, validated at compile time, tested against baselines, versioned, and deployed. Not hand-written instruction strings pasted into a config file.

### MCP Server Compiler — Complete MCP Server Generation

Charlotte compiles YAML specs into complete, runnable MCP server projects. The MCP renderer extracts MCP primitives from specific block types — `tool_use` blocks become MCP tools with JSON Schema input validation, `rag` blocks become static knowledge resources, `memory` blocks become dynamic state resources, `retrieval` blocks become parameterized resource templates, and the full compiled prompt becomes an MCP prompt with runtime arguments. Output is a complete Python project: `server.py` with tool handlers, resource endpoints, and prompt definitions; `pyproject.toml` with MCP SDK dependency; `README.md` with tool/resource/prompt documentation tables; `server.json` capability manifest; and `claude_desktop_config.json` ready to paste into Claude Desktop. Supports both single-prompt and workflow-based server generation. Workflow servers aggregate tools and resources across steps with deduplication and execution order metadata. Validate with `charlotte mcp validate`, preview with `charlotte mcp info`.

### Test Framework

30 assertion types: exact match, regex, JSON schema validation, LLM-as-judge, cosine similarity, sentiment analysis, language detection, PII detection, latency thresholds, and composite assertions (`all_of`, `any_of`, `none_of`). Parallel cross-model execution — test the same prompt against Claude, GPT-4o, and Gemini simultaneously. Evaluation history with regression drift detection. Run a prompt change against a baseline and know immediately whether it regressed. This is what makes prompt changes safe — every change is tested before it ships.

### Multi-Agent Compiler

Takes compiled prompts and generates complete, runnable multi-agent projects for CrewAI, LangGraph, AutoGen, OpenAI Agents SDK, and Google A2A protocol. Each export includes pyproject.toml, README, and all source files — ready to `pip install` and run. A shared extraction layer means adding a new framework is one renderer and its templates.

### Workflow Engine

Chain multiple prompt specs into multi-step workflows with typed data flow (`{{steps.X.output.field}}`). Topological execution ordering ensures steps run in dependency order. Conditional step execution via Jinja2 expressions. Cross-step schema validation catches type mismatches at compile time. End-to-end workflow testing validates the entire chain, not just individual steps.

### Versioning & Environments

**Content-addressed versioning** — JSON snapshots with semantic block-aware diffing. Track added, removed, and modified blocks across versions. Know exactly what changed between v1 and v2 of a prompt, at the block level.

**Environment management** — Dev/staging/production environments with variable overrides, promotion gates (test pass rate, score threshold, manual approval), and environment diffing. Promote a prompt from staging to production only when it passes the gates.

**CI/CD** — 4 GitHub Actions workflow templates: validate-on-PR, test-on-push, scheduled regression, environment promotion.

<details>
<summary><strong>21 export formats</strong></summary>

<br>

Text, JSON, YAML, API payload, MCP definition, LangChain template, HTML report, README, Claude Code Skill, MCP server, CrewAI, LangGraph, AutoGen, OpenAI Agents, A2A Agent Card — each in single-prompt and workflow variants.

</details>

<details>
<summary><strong>10 production example packs</strong></summary>

<br>

| Pack | Pattern | Use Case |
|:--|:--|:--|
| Customer Support Bot | multi-phase | E-commerce: returns, shipping, routing, conversation history |
| Code Review Assistant | multi-phase | Structured JSON feedback with severity ratings |
| Legal Document Analyzer | multi-phase | Contract analysis with citations and legal disclaimers |
| ML Model Evaluator | agent-orchestrating | Accuracy, fairness, robustness, explainability |
| Content Moderator | multi-phase | Confidence scores, escalation routing |
| Research Summarizer | multi-phase | Literature review with conflict detection |
| API Test Generator | agent-orchestrating | Test case generation from OpenAPI specs |
| Multilingual Assistant | multi-phase | 8-language support with persona consistency |
| Incident Responder | agent-orchestrating | Production incident diagnosis (ReAct pattern) |
| Prompt Optimizer | multi-phase | Meta-prompt for critiquing and refining prompts |

</details>

<div align="center">

`45 commands` · `98 modules` · `24,889 lines` · `3,043 tests, all passing`

</div>

<br>

---

## 8. Stratum — QA Compiler

**The QA compiler. Full SDLC automation for testing, documentation, and quality assurance — point it at source code and it compiles the proof that it works.**

> The problem: teams were shipping AI-generated test suites without checking whether the tests actually tested anything. Hallucinated assertions. Mocked-out logic. Tests that pass no matter what — going straight to CI. Nobody was testing the tests. And documentation? Either nonexistent or stale before the PR merged. The QA phase of the SDLC was manual, incomplete, and untrustworthy.

Stratum is a **QA compiler** that automates the testing and documentation phases of the SDLC. It takes source code as input and compiles a comprehensive quality assessment: full architecture extraction using Claude and tree-sitter across 6 languages, unit test generation across 4 test frameworks, API test generation across 4 test layers, documentation generation with 7 independent analyzers, and eight independent quality gates that each produce their own verdict. The audit engine aggregates them into a final pass or fail. A transparency layer tracks every skip, failure, and limitation — no silent failures.

This isn't "generate some tests and hope they work." This is a **compiler** that automates SDLC quality assurance — the output is a validated, gated, auditable quality package.

### The Pipeline

```
SOURCE CODE
    |
    v
+------------------------------------------+
| 1. EXTRACT (tree-sitter + Claude)        |
|    Classes, functions, endpoints -> JSON  |
|    6 languages · framework detection      |
+----------+-------------------------------+
           |
    +------+----------+---------------+
    v                  v               v
+----------+    +-----------+    +----------+
| 2. UNIT  |    | 3. API    |    | 4. DOCS  |
| pytest   |    | 4 layers  |    | 7 anlyzrs|
| jest     |    | 4 frmwrks |    | 3 formats|
| JUnit    |    |           |    |          |
| Go test  |    |           |    |          |
+----+-----+    +-----+-----+    +----+-----+
     +----------------+--------------+
                      v
+------------------------------------------+
| 5. QUALITY GATES (8 independent modules) |
+------------------+-----------------------+
                   v
+------------------------------------------+
| 6. CANDOR - Transparency Report          |
|    What automation couldn't handle       |
+------------------------------------------+
```

### Architecture Extraction

The first compilation stage. Combines Claude's understanding with tree-sitter static analysis to extract complete codebase structure across 6 languages — Python, TypeScript, JavaScript, Java, Go, Rust — with framework auto-detection for Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, and Quarkus. Output: 6 JSON artifacts including `source_model.json` — the critical intermediate representation consumed by every downstream stage.

### Unit Test Compilation

Generates pytest, jest, JUnit, or Go test suites from the extracted architecture. Not "write some tests" — a 3-retry validation loop: generate → execute → fix. Tests that don't actually run are rejected before they leave the pipeline. Tests that don't import the code under test are rejected. Tests that assert on inputs instead of outputs are rejected. Every generated test is validated against the Seven Rules (see Forge gate below) before it ships.

### API Test Compilation — 4 Layers, 4 Frameworks

API tests compile across four independent layers, each targeting a different failure mode:

| Layer | What It Validates | Why It Matters |
|:--|:--|:--|
| **Contract** | API surface matches the spec — methods, paths, status codes, content types | Catches breaking changes before they hit production |
| **Boundary** | Edge cases — empty payloads, max-length strings, type coercion, null handling | Catches the bugs that only show up with real user input |
| **Workflow** | Multi-step state transitions — create → read → update → delete sequences | Catches state machine violations invisible to unit tests |
| **Regression** | Previously-found defects captured as permanent guards | Ensures fixed bugs stay fixed across every future release |

### Documentation Compilation — 7 Analyzers, 3 Formats

Seven independent documentation analyzers: architecture, API, dependency, complexity, coverage, security, and convention. Output formats: Markdown documentation package, HTML report, and structured JSON.

### The Eight Quality Gates

Eight independent modules, each with its own verdict. All eight must pass for a pipeline to ship.

| Gate | What It Enforces |
|:--|:--|
| **Forge** | The Seven Rules — every generated test must: **(A)** invoke the code under test, **(B)** assert on outputs not inputs, **(C)** not swallow exceptions, **(D)** verify every mock, **(E)** test error paths, **(F)** fail if the code is wrong, **(G)** have no interdependence. All seven or rejected. |
| **Aegis** | Security scanning — 24 vulnerability types across 9 detectors. SQL injection, command injection, XSS, auth bypass, data exposure, hardcoded secrets. Generates exploit tests and remediation tests. |
| **Sentinel** | Mutation testing — 8 mutator types. Proves tests have teeth. |
| **Specter** | Flaky test detection — 9 pattern types. Auto-quarantine isolates unreliable tests. |
| **Arbiter** | Harvests quality rules from external linters (flake8, eslint, clippy, go vet). |
| **CodeGate** | AI code quality gate — pure rule-based, no LLM calls. 10-item production readiness checklist. 3-tier dependency verification. |
| **Intent** | Spec requirement verification — validates generated code implements original spec requirements. |
| **Candor** | Transparency layer — every skip, limitation, and assumption surfaced. No silent failures. |

### Intelligence Layer

**Predictive test prioritization** ranks every function by a 6-factor risk score — complexity, change frequency, recency, centrality, coverage, defect history. **Smart model routing** selects Claude model tiers per task. **SDD Bridge** transforms extraction output into Designer-SDD spec format.

<details>
<summary><strong>Full CLI reference (34 commands)</strong></summary>

<br>

| Command | Purpose |
|:--|:--|
| `stratum extract` | Extract architecture from source code |
| `stratum generate tests` | Compile unit + API tests |
| `stratum generate docs` | Compile documentation |
| `stratum audit` | Run all quality gates |
| `stratum review` | CodeGate standalone review |
| `stratum verify` | Spec requirement verification |
| `stratum ship` | Full pipeline with handoff documentation |
| `stratum run` | Full pipeline (extract → generate → gate → audit) |
| `stratum baseline save` | Save extraction snapshot as named baseline |
| `stratum baseline list` | List saved baselines |
| `stratum baseline diff` | Diff baseline against current extraction |
| `stratum delta` | Run targeted pipeline on changed code only |
| `stratum-out generate` | Standalone architecture extraction |
| `stratum-unit generate` | Standalone unit test compilation |
| `stratum-api generate` | Standalone API test compilation |
| `stratum-docs generate` | Standalone documentation compilation |
| `stratum-docs sdd` | Generate Designer-SDD spec from codebase |

</details>

<div align="center">

`34 commands` · `311 modules` · `73,508 lines` · `4,322 tests, all passing`

</div>

<br>

---

## 9. Designer-SDD — Specification Compiler

**The specification compiler. Rapid prototyping from unstructured idea to scored, validated, build-ready spec package. Then build absolutely anything.**

> The problem: specs kept arriving as Slack threads, call transcripts, and scattered notes. Teams kept building the wrong thing because requirements were ambiguous. AI agents kept generating code that missed the point because nobody validated the spec before handing it off. The gap between "what the client said" and "what got built" was where projects went to die. There was no compiler for the *idea itself*.

Designer-SDD is a **specification compiler** that applies the **Spec-Driven Development** methodology — turning raw ideas into production-ready build packages through a deterministic compilation pipeline. Feed it any input — a client brief, a call transcript, raw notes, an interactive brainstorming session, a web research pipeline — and it compiles a structured JSON spec via Claude, then runs it through a gauntlet: validation against domain-specific rules, dual-gate scoring across 36 weighted checks, iterative AI-driven refinement that re-scores after every pass, and round-trip verification that confirms every requirement in the spec appears in the rendered output.

**This is the rapid prototyping engine.** Go from a Slack thread to a scored, validated, GitHub-ready specification package of up to 11 files in minutes — ready for any developer or any AI agent to build from. **Every tool in this platform was built from a Designer-SDD spec.** That's the methodology: spec it, score it, validate it, then build absolutely anything. The spec is the single source of truth that survives the entire development lifecycle.

### Entry Points — Any Input, Structured Output

| Entry Point | What It Takes | When To Use It |
|:--|:--|:--|
| **Intake** | Raw text — briefs, emails, call transcripts, meeting notes | Client sends unstructured requirements |
| **Create** | Interactive brainstorming session with Claude | Starting from a vague idea |
| **Discover** | 3-stage web-powered market research pipeline | Need competitive analysis and market context |
| **Form** | Browser-based HTML intake form | Structured self-service from stakeholders |
| **Templates** | 5 pre-built templates (CLI, REST API, SaaS dashboard, library, Chrome extension) | Known project archetype |

### Dual-Gate Scoring

| Gate | What It Measures | Checks | Threshold |
|:--|:--|:--|:--|
| **Quality** | Is this spec complete and well-structured? | 28 weighted checks across 7 sections | 70% |
| **Buildability** | Can a developer or AI agent actually build from this? | 8 checks: ambiguity detection, dependency completeness, acceptance verifiability, tech completeness | 60% |

### Tier-Gated Export

| Tier | Files | What's Included |
|:--|:--|:--|
| **Small** | 7 | CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, HANDOFF.md, README.md, source JSON |
| **Medium** | 9 | + DATA_MODEL.md, QUICKSTART.md |
| **Large** | 11 | + ARCHITECTURE.md, RESEARCH.md |

### Round-Trip Verification

After export, the compiler verifies that every requirement and every task in the source JSON spec appears in the rendered markdown files. Zero tolerance for requirements that silently disappear during rendering.

<details>
<summary><strong>Full CLI reference (17 commands)</strong></summary>

<br>

| Command | Purpose |
|:--|:--|
| `designer intake` | Compile specs from unstructured text (briefs, notes, transcripts) |
| `designer create` | Interactive brainstorming with Claude |
| `designer discover` | 3-stage market research pipeline with web search |
| `designer form` | Launch browser-based HTML intake form |
| `designer validate` | Check spec completeness against domain rules |
| `designer score` | Dual-gate scoring (quality + buildability) |
| `designer improve` | Auto-improve via Claude refinement loop |
| `designer ingest` | Full pipeline (validate → score → export) |
| `designer export` | Render tier-gated markdown package |
| `designer diff` | Field-by-field spec comparison with score deltas |
| `designer research` | Answer open questions via Claude |
| `designer verify` | Post-export round-trip integrity check |
| `designer template list` | Browse pre-built templates |
| `designer template preview` | Preview template contents |
| `designer template use` | Scaffold project from template |
| `designer init` | Initialize project configuration |

</details>

<div align="center">

`17 commands` · `49 modules` · `8,258 lines` · `693 tests, all passing`

</div>

<br>

---

## 10. Axle — API Compiler

**The API compiler. Single YAML spec in, six production-ready artifacts out.**

> The problem: building a new API means writing the same boilerplate six times — the server, the OpenAPI spec, the MCP tool definitions, the MCP server, the test suite, and the test config. Each drifts from the others. The contract lives in one place, the implementation in another. Every artifact is a separate maintenance burden.

Axle is a **design-first API compiler** that transforms a single YAML specification (`api.yaml`) into six production-ready artifacts through a three-stage pipeline (Parse → Flatten → Render):

```
api.yaml ──> [ Parse ] ──> [ Flatten ] ──> [ Render ] ──> FastAPI Server
                                                      ──> OpenAPI 3.1 Spec
                                                      ──> MCP Tool Definitions
                                                      ──> MCP Server
                                                      ──> Pytest Suite
                                                      ──> Pytest Config
```

### What It Generates

| Artifact | What You Get |
|:--|:--|
| **FastAPI Server** | Fully typed Pydantic v2 models, route stubs with 501 Not Implemented responses, auth middleware |
| **OpenAPI 3.1 Spec** | Standards-compliant API documentation |
| **MCP Tools** | Anthropic-format tool definitions for AI assistants |
| **MCP Server** | Runnable FastMCP server that calls your API over HTTP |
| **Pytest Suite** | Async test suite with happy-path, missing-field, and wrong-type tests per endpoint |
| **Pytest Config** | Test fixtures and async test infrastructure |

### AI-Assisted Design

- **AXLE_API_ARCHITECT.md** — Charlotte-compiled prompt for claude.ai projects with Ideation and Spec modes
- **axle-intake.html** — Visual HTML form for browser-based API design with live YAML generation

### Smart Naming & Validation

Auto-derives tool names from endpoints (e.g., `POST /payments/{id}` → `create_payments_by_id`). Semantic validation: `$ref` resolution, duplicate detection, HTTP status codes, tool name collisions. Structural validation: Pydantic enforces type/ref mutual exclusivity.

<div align="center">

`6 commands` · `15 modules` · `2,151 lines` · `134 tests, all passing`

</div>

<br>

---

## 11. Dissector — Domain Agent Opportunity Mapper

**The opportunity mapper. Feed it any business domain, get back a prioritized blueprint of every AI agent worth building.**

> The problem: organizations know they want AI agents but don't know where to start. They're overwhelmed by the technology and can't see the opportunities in their own operations. They need someone to analyze their business domain and produce a concrete, build-ready map of what agents would actually deliver value — not generic AI pitches, but specific agents mapped to specific processes.

The Dissector is a **domain agent opportunity mapper** that analyzes any organization type — law offices, restaurants, consulting firms, dental practices, construction companies — and produces comprehensive AI agent opportunity blueprints. It decomposes organizations into nine functional categories, identifies minimum 15 opportunity cards per domain, and generates three-wave implementation roadmaps (0–90, 90–180, 180–365 days).

### What It Produces

- **Functional Anatomy** — Nine-category decomposition of any business domain with specific processes per category
- **Opportunity Cards** — Each card includes: agent name, category, function, data requirements, build complexity, value tier, ROI estimate, and wave assignment
- **Prioritization Matrix** — Multi-factor scoring across value, complexity, data readiness, and organizational appetite
- **Three-Wave Roadmap** — Phased implementation plan with dependencies and success criteria
- **OTS Assessment** — Off-the-shelf tool evaluation against custom build opportunities (e.g., Harvey AI, CoCounsel, LexisNexis Protege, Clio)
- **Human-in-the-Loop Flags** — Explicit flagging of privilege-sensitive and liability-creating zones

### Design Principles

- **Functional anatomy first** — identifies agents from business processes, never technology-first
- **Strict boundary enforcement** — maps opportunities only, does not provide technical architecture or agent code specs
- **Domain-agnostic engine** — the same methodology works for any industry
- **Builder vocabulary** — assumes the reader can build; uses domain-specific precision, not marketing language

### Architecture

Two compiled implementations: a full agent-orchestrating system (10 blocks, 7,507 tokens) and a multi-phase skill version (6 blocks, 4,653 tokens). Both Charlotte-compiled with validated block composition.

<div align="center">

`Compiled prompt system` · `1,626 lines`

</div>

<br>

---

## 12. ClaudeMD — CLAUDE.md Quality Compiler

**The instruction compiler. Treats CLAUDE.md files as engineered artifacts — validated, scored, and auto-improved before they govern a single token.**

> The problem: CLAUDE.md files are the primary way developers configure Claude Code's behavior, but they're written by instinct and shipped on hope. Too many instructions degrade performance — research shows a ~150 instruction limit before quality drops. Critical rules buried in the middle get lost to periphery bias. There's no validation, no quality measurement, no way to know if a CLAUDE.md is helping or hurting. Teams hand-write the instructions that govern their most powerful tools, with no compiler, no linter, and no test suite. Instruction files deserve the same rigor as the code they govern.

ClaudeMD is a **CLAUDE.md quality compiler** — a CLI tool that applies research-backed best practices to validate, score, and improve Claude Code instruction files. It enforces the ~150 instruction limit, detects periphery bias issues, validates the WHAT/WHY/HOW framework from Anthropic's official guidance, and ensures progressive disclosure via skills and rules.

### Validation Engine — 15 Rules

Rule-based checking with rationale and fix suggestions for every issue. Severity levels: error, warning, info. Exit codes for CI integration (0 = clean, 1 = warnings, 2 = errors).

### Quality Scoring — 5 Weighted Dimensions

| Dimension | Weight | What It Measures |
|:--|:--|:--|
| **Conciseness** | 25% | Instruction count relative to ~150 limit, section density |
| **Coverage** | 25% | Essential sections present: project context, coding standards, testing, error handling |
| **Specificity** | 20% | Actionable instructions vs. vague guidance |
| **Progressive Disclosure** | 15% | Proper use of skills, rules, and agents for overflow |
| **Anti-patterns** | 15% | Absence of known failure modes: linter rules, overly verbose instructions |

Grades: A (90–100), B (80–89), C (70–79), D (60–69), F (<60).

### Automated Improvement

Auto-fix with unified diff output: removes linter-territory rules, deduplicates instructions, adds trailing newlines, reorders sections. Write mode applies changes with `.bak` backup.

### Ecosystem Audit

Full scan across the Claude Code instruction ecosystem: CLAUDE.md, `.claude/rules/`, agents, skills, and `.mcp.json`. Detects orphaned rules, missing configuration, and ecosystem-level issues.

<div align="center">

`5 commands` · `1,144 lines` · `90 tests, all passing`

</div>

<br>

---

## How They Connect

```
                         AGENT GOVERNANCE PLATFORM
  ┌──────────────────────────────────────────────────────────────────────┐
  │                                                                      │
  │   COMPILE              AUDIT               COMMUNICATE              │
  │   ───────              ─────               ───────────              │
  │   Castellan ─────────> Aegis               Herald                   │
  │   (Agent Compiler)     (Security Audit)    (Command Channel)        │
  │        │                    │                    │                   │
  │        │               Arbiter                   │                   │
  │        │               (Batch Governance)        │                   │
  │        │                                         │                   │
  │   SCAN                 MONITOR                                      │
  │   ────                 ───────                                      │
  │   Recon ─────────────> Vigil <───────────────────┘                  │
  │   (Reverse-Engineer)   (Fleet Dashboard)                            │
  │                                                                      │
  └──────────────────────────────────────────────────────────────────────┘

                              SUPPORTING TOOLS
  ┌──────────────────────────────────────────────────────────────────────┐
  │                                                                      │
  │   DESIGN               BUILD               VALIDATE                 │
  │   ──────               ─────               ────────                 │
  │   Designer-SDD ──────> Charlotte ─────────> Stratum                 │
  │   (Spec Compiler)      (Prompt Compiler)    (QA Compiler)           │
  │                                                                      │
  │   Axle                 Dissector              ClaudeMD                │
  │   (API Compiler)       (Opportunity Mapper)   (CLAUDE.md Compiler)  │
  │                                                                      │
  └──────────────────────────────────────────────────────────────────────┘

  Data Flow:
  Designer-SDD specs → define every tool
  Charlotte prompts  → power AI stages across Stratum, Aegis, Recon, Arbiter
  Stratum            → validates code all systems generate
  Castellan          → compiles agents with governance
  Aegis              → audits agent security pre-deployment
  Arbiter            → batch-audits agent fleets for compliance
  Herald             → delivers commands to deployed agents
  Recon              → reverse-engineers governance from existing agents
  Vigil              → monitors everything in production
  Dissector          → maps where to build agents next
  ClaudeMD           → validates and improves CLAUDE.md instruction files
```

### The Governance Loop

1. **Design** — Designer-SDD compiles the spec. Dissector identifies the opportunities
2. **Build** — Charlotte compiles the prompts. Castellan compiles the agent. Axle compiles the API. ClaudeMD validates instruction files
3. **Validate** — Stratum runs quality gates. Aegis audits security. Arbiter scores compliance
4. **Deploy** — Herald establishes the command channel
5. **Monitor** — Vigil tracks governance drift, fires alerts, enforces kill switches
6. **Scan** — Recon reverse-engineers governance from agents already in production

Every system is standalone. Together they close the loop.

---

## Platform Totals

<div align="center">

<br>

![Total Lines](https://img.shields.io/badge/300%2C931-Total_Source_Lines-2563EB?style=for-the-badge)
![Total Tests](https://img.shields.io/badge/19%2C134-Tests_Passing-16A34A?style=for-the-badge)
![Total Systems](https://img.shields.io/badge/12-Production_Systems-7C3AED?style=for-the-badge)

<br>

### Agent Governance Platform

| | Castellan | Aegis | Arbiter | Herald | Recon | Vigil | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Source Lines** | 103,194 | 20,017 | 2,679 | 3,596 | 44,642 | 15,227 | **189,355** |
| **Modules** | 439 | 103 | 18 | 34 | 172 | 138 | **904** |
| **Tests** | 6,940 | 675 | 100 | 219 | 2,733 | 185 | **10,852** |

### Tools

| | Charlotte | Stratum | Designer-SDD | Axle | Dissector | ClaudeMD | **Subtotal** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Source Lines** | 24,889 | 73,508 | 8,258 | 2,151 | 1,626 | 1,144 | **111,576** |
| **Modules** | 98 | 311 | 49 | 15 | — | 20 | **493** |
| **Tests** | 3,043 | 4,322 | 693 | 134 | — | 90 | **8,282** |

### Combined

| Metric | Value |
|:--|:--|
| **Total Systems** | **12** |
| **Total Source Lines** | **300,931** |
| **Total Modules** | **1,397** |
| **Total Tests (passing)** | **19,134** |
| **Compliance Standards** | **11** (EU AI Act, NIST AI RMF, GDPR, HIPAA, PCI-DSS, SOC 2, ISO 42001, ISO 27001, FZ-152, OWASP, CoSAI) |

<br>

**Stack**

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
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

</div>

---

<br>

<div align="center">

## Let's Talk

</div>

If your team is shipping production AI agents and needs them **governed, compiled, tested, and monitored** — not hand-assembled and hoped for — I built the platform that makes that possible.

I take on AI-first contract engagements:

> **Agent governance platforms** · **Agentic compilation** · **SDLC automation** · **Rapid prototyping** from spec to production · Pre-deployment security auditing · Batch compliance scanning · Fleet governance monitoring · Prompt and skill compilation · Test generation pipelines · Quality gate systems · OWASP security auditing · Governance reverse-engineering

<div align="center">

<br>

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

*20+ years enterprise ops · 2 IPOs · 4 acquisitions · Salesforce · IBM · Oracle · iHeartMedia*

<br>

</div>
