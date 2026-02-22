<div align="center">

# Tim Wolfe

### AI Infrastructure Architect

Autonomous SDLC  ·  Agent Governance  ·  LLM Platform Engineering

Los Altos, CA · [rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-React%20%2B%20Next.js-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Source](https://img.shields.io/badge/Source-189%2C222_lines-blue?style=flat-square)
![Tests](https://img.shields.io/badge/Tests-13%2C498_passing-brightgreen?style=flat-square)
![Systems](https://img.shields.io/badge/Production_Systems-5-purple?style=flat-square)
![License](https://img.shields.io/badge/License-Proprietary-orange?style=flat-square)

</div>

---

## About

I build **compilers** for AI — agentic compilers, prompt compilers, QA compilers, specification compilers — and an operations portal that watches governed agents run in production. Not wrappers. Not demos. Not prompt templates. **Four production compilers and a fleet operations portal** that close the loop from raw idea to deployed, governed, monitored agent.

**Governance is the core problem.** Every team shipping AI agents hits the same wall: the prototype works, but production demands governance — constitutional constraints, runtime guardrails, OWASP security auditing, compliance drift detection, kill switches, audit trails. Most frameworks hand you a runtime and leave governance as an exercise for the reader. I built compilers that make governance structural. It's enforced at compile time. It travels with the deployed agent. It's monitored in real time. It's not optional.

**Four compilers, one closed loop:**

- **Specification Compiler** (Designer-SDD) — compiles unstructured ideas into scored, validated build packages. Rapid prototyping starts here: spec it, score it, build anything from it
- **Prompt, Skill & MCP Compiler** (Charlotte) — compiles prompts, Claude Code skills, and MCP servers through a deterministic pipeline with a 94-block type system, security scanning, versioning, and CI/CD generation. MCP server generation produces complete Python projects with tool handlers, resource endpoints, prompt definitions, and Claude Desktop config from compiled specs. SDLC automation for every prompt artifact
- **QA Compiler** (Stratum) — extracts full architecture, compiles unit tests + API tests + documentation, then enforces eight quality gates. SDLC automation for test generation, documentation, and quality assurance
- **Agentic Compiler** (Castellan) — the heart of the stack. YAML in, governed production agent out. Constitutional governance, runtime guardrails, OWASP audit, multi-target deployment. This is the agent compiler
- **Agentic Portal** (Monitoring Portal) — receives cryptographically signed health packets from every deployed agent, tracks governance drift in real time, fires alerts, instant kill switch. The closed loop on every compiled agent

Every system is standalone. Together they automate the full SDLC for AI agents — from rapid prototyping through governed deployment to real-time fleet monitoring. The platform is self-hosting: these are the same compilers I use to deliver for enterprise clients across finance, healthcare, and ecommerce.

Before AI infrastructure: 20+ years of enterprise operations leadership — two IPOs (**Quinstreet**, **Responsys**), four acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior technical roles at **Salesforce**, **iHeartMedia**, and **Axway**.

---

<div align="center">

### The Compiler Stack — Agent Governance + SDLC Automation

[Castellan — Agentic Compiler](#1-castellan--agentic-compiler) · [Charlotte — Prompt, Skill & MCP Compiler](#2-charlotte--prompt-skill--mcp-compiler) · [Stratum — QA Compiler](#3-stratum--qa-compiler) · [Designer-SDD — Specification Compiler](#4-designer-sdd--specification-compiler)

### The Agentic Portal — Fleet Governance + Operations

[Monitoring Portal — Fleet Operations](#5-castellan-monitoring-portal--fleet-operations)

---

[How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Platform

AI agents have a governance problem. And a compilation problem. And an SDLC problem.

Code gets compiled. Databases get migrated. Infrastructure gets provisioned through declarative configs with validation and version control. But AI agents — the specs they're built from, the prompts they use, the tests that prove they work, the governance that keeps them safe — are still assembled by hand, shipped on instinct, and debugged in production. There's no compiler. No governance enforcement. No automated SDLC. No way to prove an agent won't go off-script next week.

I built four compilers and an agentic operations portal to fix that. Each compiler automates a phase of the AI SDLC where hand-assembly fails. The portal closes the loop with real-time governance monitoring:

- **Rapid prototyping** → Designer-SDD compiles unstructured ideas — briefs, transcripts, notes — into scored, validated, build-ready specification packages. The output isn't a document. It's a complete SDD package that any developer or AI agent can build from. Spec it, score it, build absolutely anything.
- **Prompt SDLC** → Charlotte compiles prompts, Claude Code skills, and MCP servers through a 5-stage deterministic pipeline with a 94-block type system, security scanning across 54 checks, version control, and CI/CD generation. MCP server generation produces complete Python projects from compiled specs — tool handlers, resource endpoints, prompt definitions, and client config. Full SDLC automation for every prompt artifact — compiled, versioned, tested, deployed.
- **QA automation** → Stratum compiles source code into comprehensive quality assessments — extracting full architecture across 6 languages, generating unit tests, API tests, and documentation, then enforcing eight independent quality gates. SDLC automation for test generation and quality assurance.
- **Agentic compilation + governance** → Castellan compiles YAML specs into production-ready governed agents with constitutional governance, runtime guardrails, OWASP security auditing, and multi-target deployment. This is the agentic compiler. Governance is structural — enforced at compile time, embedded in the deployed agent, monitored in production.
- **Fleet governance** → The Monitoring Portal receives cryptographically signed health packets from every deployed agent, tracks governance drift in real time, fires alerts when safety thresholds breach, and provides an instant kill switch for any agent in the fleet. The agentic portal that closes the governance loop.

Every system is standalone. Together they automate the full SDLC from unstructured idea to deployed, tested, governed, monitored agent. The platform is self-hosting — Designer-SDD specs defined every tool, Charlotte compiled the prompts that drive Stratum's AI stages, Stratum validates the code all five generate, Castellan compiles the agents, and the Monitoring Portal watches them run.

---

<br>

<div align="center">

# The Compiler Stack

*Four compilers. Agent governance. Full SDLC automation.*

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

<details>
<summary><strong>Full CLI reference (51 commands)</strong></summary>

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

```
51 commands · 665 modules · 81,394 lines · 5,880 tests, all passing
```

<br>

---

## 2. Charlotte — Prompt, Skill & MCP Compiler

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

```
45 commands · 178 modules · 19,706 lines · 2,600 tests, all passing
```

<br>

---

## 3. Stratum — QA Compiler

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

The first compilation stage. Combines Claude's understanding with tree-sitter static analysis to extract complete codebase structure across 6 languages — Python, TypeScript, JavaScript, Java, Go, Rust — with framework auto-detection for Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, and Quarkus. Output: 6 JSON artifacts including `source_model.json` — the critical intermediate representation consumed by every downstream stage. This is the AST equivalent for codebases — a structured representation that all downstream compilers consume.

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

Four layers, four frameworks (FastAPI, Flask, Express, Spring), combinatorial coverage. The API test compiler generates the entire test matrix from the extracted architecture.

### Documentation Compilation — 7 Analyzers, 3 Formats

Seven independent documentation analyzers, each producing structured output:

1. **Architecture analyzer** — system components, dependencies, data flow
2. **API analyzer** — endpoint catalog, request/response schemas, auth requirements
3. **Dependency analyzer** — dependency tree, version constraints, security advisories
4. **Complexity analyzer** — cyclomatic complexity, coupling metrics, hotspot identification
5. **Coverage analyzer** — test coverage mapping, untested code paths
6. **Security analyzer** — vulnerability surface area, exposure points
7. **Convention analyzer** — coding patterns, naming conventions, style consistency

Output formats: Markdown documentation package, HTML report, and structured JSON for downstream consumption by other tools.

### The Eight Quality Gates

The core of Stratum. Eight independent modules, each with its own verdict. All eight must pass for a pipeline to ship.

| Gate | What It Enforces |
|:--|:--|
| **Forge** | The Seven Rules — every generated test must: **(A)** invoke the code under test, **(B)** assert on outputs not inputs, **(C)** not swallow exceptions, **(D)** verify every mock, **(E)** test error paths, **(F)** fail if the code is wrong, **(G)** have no interdependence. All seven or rejected. |
| **Aegis** | Security scanning — 24 vulnerability types across 9 detectors. SQL injection, command injection, XSS, auth bypass, data exposure, hardcoded secrets. Generates exploit tests to prove vulnerabilities and remediation tests to verify fixes. |
| **Sentinel** | Mutation testing — 8 mutator types. Mutates source, runs the test suite, calculates whether the suite actually catches the mutations. Proves tests have teeth. |
| **Specter** | Flaky test detection — 9 pattern types. Timing-dependent, random state, external dependencies, concurrency, async timing. Auto-quarantine isolates unreliable tests. |
| **Arbiter** | Harvests quality rules from external linters (flake8, eslint, clippy, go vet) and maps them to test quality categories. |
| **CodeGate** | AI code quality gate — pure rule-based, no LLM calls. 10-item production readiness checklist. 3-tier dependency verification: recognized, hallucination risk, unverifiable. Catches hallucinated dependencies, happy-path-only logic, context-blind decisions. |
| **Intent** | Spec requirement verification — validates that generated code implements the requirements from the original spec. Coverage percentage and gap analysis. |
| **Candor** | Transparency layer — every skip, limitation, and assumption surfaced. No silent failures. |

### Baseline + Delta Service

Named baselines snapshot extraction state. The delta engine diffs against previous baselines at the function level — detecting added, modified, and removed functions — then generates targeted tests only for changed code. This is what converts a one-shot engagement into a recurring subscription: re-test only what changed, at a fraction of the cost.

### Intelligence Layer

**Predictive test prioritization** ranks every function by a 6-factor risk score — complexity, change frequency, recency, centrality, coverage, defect history — using git history when available. Produces `TEST_PRIORITY_MAP.md` so the most dangerous untested code gets covered first.

**Smart model routing** selects Claude model tiers (Haiku/Sonnet/Opus) per API call based on task complexity. Target: 20–40% cost reduction without quality loss.

**SDD Bridge** — transforms extraction output into Designer-SDD spec format. Scan any existing codebase, produce a complete build spec, then rebuild it in a different framework or language. This is the bridge between "what exists" and "what to build next."

*Philosophy: "We identify bugs. We do NOT fix them."*

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

```
34 commands · 499 modules · 73,792 lines · 4,436 tests, all passing
```

<br>

---

## 4. Designer-SDD — Specification Compiler

**The specification compiler. Rapid prototyping from unstructured idea to scored, validated, build-ready spec package. Then build absolutely anything.**

> The problem: specs kept arriving as Slack threads, call transcripts, and scattered notes. Teams kept building the wrong thing because requirements were ambiguous. AI agents kept generating code that missed the point because nobody validated the spec before handing it off. The gap between "what the client said" and "what got built" was where projects went to die. There was no compiler for the *idea itself*.

Designer-SDD is a **specification compiler** that applies the **Spec-Driven Development** methodology — turning raw ideas into production-ready build packages through a deterministic compilation pipeline. Feed it any input — a client brief, a call transcript, raw notes, an interactive brainstorming session, a web research pipeline — and it compiles a structured JSON spec via Claude, then runs it through a gauntlet: validation against domain-specific rules, dual-gate scoring across 36 weighted checks, iterative AI-driven refinement that re-scores after every pass, and round-trip verification that confirms every requirement in the spec appears in the rendered output.

**This is the rapid prototyping engine.** Go from a Slack thread to a scored, validated, GitHub-ready specification package of up to 11 files in minutes — ready for any developer or any AI agent to build from. **Every tool in this platform was built from a Designer-SDD spec.** That's the methodology: spec it, score it, validate it, then build absolutely anything. The spec is the single source of truth that survives the entire development lifecycle.

### The SDD Methodology — Rapid Prototyping Through Compilation

Spec-Driven Development inverts the traditional workflow. Instead of building first and documenting later (or never), SDD **compiles the specification** *before* a single line of code is written. The spec goes through the same kind of rigorous validation that code goes through in CI — scoring, domain-specific rule checking, iterative improvement, and round-trip verification. By the time a developer or AI agent starts building, the spec has already been validated, scored, and proven complete.

This is what makes rapid prototyping safe at scale. You're not prototyping blind — you're prototyping from a compiled, validated spec. The spec catches ambiguity. The dual-gate scoring catches incompleteness. The refinement loop fixes both. By the time you hand the spec to Claude Code or a developer, it's been through more validation than most production code reviews.

### Entry Points — Any Input, Structured Output

| Entry Point | What It Takes | When To Use It |
|:--|:--|:--|
| **Intake** | Raw text — briefs, emails, call transcripts, meeting notes | Client sends unstructured requirements |
| **Create** | Interactive brainstorming session with Claude | Starting from a vague idea |
| **Discover** | 3-stage web-powered market research pipeline | Need competitive analysis and market context |
| **Form** | Browser-based HTML intake form | Structured self-service from stakeholders |
| **Templates** | 5 pre-built templates (CLI, REST API, SaaS dashboard, library, Chrome extension) | Known project archetype |

Every entry point produces the same intermediate representation — a structured JSON spec — that feeds into the same compilation pipeline. The input format doesn't matter. The output quality is deterministic.

### Dual-Gate Scoring

Two independent scoring systems run on every spec. Both must pass their thresholds:

| Gate | What It Measures | Checks | Threshold |
|:--|:--|:--|:--|
| **Quality** | Is this spec complete and well-structured? | 28 weighted checks across 7 sections | 70% |
| **Buildability** | Can a developer or AI agent actually build from this? | 8 checks: ambiguity detection, dependency completeness, acceptance verifiability, tech completeness | 60% |

A spec that scores high on quality but low on buildability is a well-written document that nobody can build from. A spec that scores high on buildability but low on quality is buildable but incomplete. Both gates must pass.

### Domain-Aware Validation

Not generic rules — rules that match what you're actually building:

- **CLI projects** must declare exit codes, argument parsing, help text conventions
- **REST APIs** must declare auth schemes, error response formats, rate limiting
- **Web applications** must declare error handling, loading states, responsive breakpoints
- **Mobile applications** must declare offline behavior, push notification handling
- **Libraries** must declare public API surface, versioning strategy, backward compatibility

The validator knows what kind of thing you're building and enforces the rules that kind of thing requires.

### Iterative Refinement

Score the spec. Send targeted improvement instructions to Claude based on which checks failed. Re-score. Repeat. The spec gets measurably better each round — up to 3 automated passes. Each pass produces a score delta so you can see exactly what improved.

### Tier-Gated Export

The output scales with project complexity:

| Tier | Files | What's Included |
|:--|:--|:--|
| **Small** | 7 | CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, HANDOFF.md, README.md, source JSON |
| **Medium** | 9 | + DATA_MODEL.md, QUICKSTART.md |
| **Large** | 11 | + ARCHITECTURE.md, RESEARCH.md |

Every export includes CONSTITUTION.md — the project's values and constraints, defined before a single line of code is written. This feeds directly into Castellan's constitutional governance when the spec produces an agent.

### Round-Trip Verification

After export, the compiler verifies that every requirement and every task in the source JSON spec appears in the rendered markdown files. Catches drift between the spec and the output. If the spec says "the system shall support SSO" but no rendered file mentions SSO, the verification fails. Zero tolerance for requirements that silently disappear during rendering.

### The Build Anything Pipeline — From Compiled Spec to Production

The SDD spec is the universal input format. Once the specification compiler produces a validated package:

- Hand it to a **developer** — TASKS.md is a ready-made sprint backlog, PLAN.md is the technical architecture, CONSTITUTION.md defines the guardrails
- Hand it to **Claude Code** — the spec + CONSTITUTION.md is everything an AI agent needs to build the entire project. This is rapid prototyping: idea → compiled spec → built system, with governance baked in from the first line
- Feed it to **Castellan** — if the spec describes an agent, the agentic compiler turns it into a governed production system with constitutional governance, runtime guardrails, and multi-target deployment
- Feed it to **Stratum** — after building, the QA compiler validates the output against the original spec via the Intent gate. The SDLC loop closes: spec → build → verify

The spec is the anchor. Everything else is derived. This is why every tool in this platform was built from a Designer-SDD spec — because the methodology works.

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

```
17 commands · 74 modules · 7,909 lines · 582 tests, all passing
```

<br>

---

<br>

<div align="center">

# The Agentic Portal

*Compile the agent. Deploy the agent. Govern the agent in production.*

</div>

<br>

---

## 5. Castellan Monitoring Portal — Fleet Governance & Operations

**The agentic portal. Real-time governance monitoring for every compiled agent in the fleet.**

> The problem: agents deploy and disappear into a black box. Governance scores drift. Costs creep. Guardrails fire silently. Constitutional violations go undetected. By the time someone notices, the damage is done and the audit trail is incomplete. Governance at compile time is necessary. Governance at runtime is necessary. But without governance in production — continuous, real-time, with kill-switch authority — you're flying blind.

The Monitoring Portal is the **agentic portal** — Castellan's governance and operations layer for deployed agent fleets. A full-stack platform (FastAPI backend + Next.js frontend) that receives cryptographically signed health packets from every deployed Castellan agent, tracks governance drift in real time, fires alerts when safety thresholds breach, and provides an instant kill switch for any agent in the fleet. The agentic compiler governs the agent at compile time. The agentic portal governs the agent in production. That's the closed governance loop.

### Architecture

| Layer | Stack |
|:--|:--|
| **Frontend** | Next.js, React, TypeScript, SWR, WebSocket |
| **API** | FastAPI, 15 REST + WebSocket endpoints |
| **Auth** | Clerk JWT (RS256, JWKS with TTL cache) + HMAC-SHA256 packet signatures |
| **Database** | SQLAlchemy async, 10 tables, composite indexes |
| **Real-time** | Tenant-scoped WebSocket with operator broadcast |

### What It Monitors

- **Governance scores** — per-agent, per-tenant, with historical trend analysis over a configurable window
- **Compliance drift** — degrading / stable / recovering classification with automatic alert escalation
- **Alert evaluation** — threshold-based with deduplication (upsert on active alerts, composite index for fast lookup)
- **Kill switch** — issue and release with multi-kill awareness — releasing one kill doesn't restore status if others remain active
- **Recertification** — 90-day cycles with grace periods and overdue tracking
- **Cost tracking** — per-agent, per-session token and USD accumulation
- **Audit trail** — immutable, append-only, every action logged with timestamp and initiator

### Multi-Tenant Isolation

Every data path is tenant-scoped. WebSocket connections subscribe only to their tenant's events — operators get a wildcard channel, tenant users see only their own agents. Health packet ingest requires cryptographic signature verification against the tenant's signing key. New agent registration requires an explicit `tenant_id` — no scanning across tenants.

### Security Hardened

10 security findings (3 HIGH, 4 MEDIUM, 3 LOW) identified and resolved pre-production:

| Severity | Fix |
|:--|:--|
| **HIGH** | JWKS cache with TTL (3600s) and force-refresh on key rotation |
| **HIGH** | Tenant-scoped WebSocket isolation — no cross-tenant data leakage |
| **HIGH** | Required `tenant_id` for new agent registration — eliminates O(n) tenant scanning |
| **MEDIUM** | Kill release checks for other active kills before restoring agent status |
| **MEDIUM** | Alert deduplication — upsert on `(agent_id, alert_type)` with composite index |
| **MEDIUM** | Dev mode defaults to `viewer` role, not `operator`, with startup warning |
| **MEDIUM** | CORS origins configurable per environment via settings |
| **LOW** | Column rename for clarity (`signing_key_hash` → `signing_key`) |
| **LOW** | Configurable drift trend window (default: 20 packets) |
| **LOW** | Automated data retention with daily background purge (default: 90 days) |

```
15 endpoints · 92 modules · 6,421 lines (2,729 Python + 3,692 TypeScript)
```

<br>

---

## How They Connect

```
  Raw Idea              YAML Spec            Source Code           Agent Spec
     |                     |                     |                     |
     v                     v                     v                     v
+--------------+    +-------------+      +-------------+    +------------------+
| Designer-SDD |    |  Charlotte  |      |   Stratum   |    |    Castellan     |
| Specification|    | Prompt/Skill|      |     QA      |    |    Agentic       |
| Compiler     |    | /MCP Compiler|     |   Compiler  |    |    Compiler      |
|              |    |             |      |             |    |                  |
| Validate     |    | Compile     |      | Extract     |    | Compile          |
| Score        |    | Validate    |      | Generate    |    | Govern / Guard   |
| Improve      |    | Test        |      | Gate        |    | Test / Audit     |
| Export       |    | Export      |      | Audit       |    | Export / Deploy  |
+------+-------+    +------+------+      +------+------+    +--------+---------+
       |                   |                    |                     |
       v                   v                    v                     v
  Scored Spec        Provider-Ready        Pass/Fail Verdict    Running Agent ------+
  Package (7-11      Prompts, Skills,      + Tests + Docs       (CLI, HTTP, Docker, |
  files)             MCP Servers, or       + Transparency        K8s, Temporal)      |
                     Agent Projects                                                  |
                                                                                     |
                                                                                     v
                                                                   +------------------------+
                                                                   |   Monitoring Portal    |
                                                                   |   The Agentic Portal   |
                                                                   |                        |
                                                                   |   Health packets       |
                                                                   |   Governance drift     |
                                                                   |   Alert evaluation     |
                                                                   |   Kill switch          |
                                                                   |   Audit trail          |
                                                                   +------------------------+
```

Each system is standalone. Each is a compiler. Together they automate the full SDLC for AI agents:

- **Designer-SDD** (Specification Compiler) — compiles *what to build*. Rapid prototyping from raw idea to scored, validated spec package
- **Charlotte** (Prompt, Skill & MCP Compiler) — compiles *how agents communicate*. Full SDLC automation for prompts, skills, and MCP servers
- **Stratum** (QA Compiler) — compiles *proof that it works*. SDLC automation for testing, documentation, and quality gates
- **Castellan** (Agentic Compiler) — compiles *the agent itself*. Governance is structural — constitutional, runtime, and deployment
- **Monitoring Portal** (Agentic Portal) — governs *the agent in production*. Governance drift, alerts, kill switch, audit trail

**Four compilers. One agentic portal. Full SDLC automation with governance at every phase.**

The platform is self-hosting. Designer-SDD specs defined every tool. Charlotte compiled the prompts, skills, and MCP servers that power Stratum's AI stages. Stratum validates the code all five generate. Castellan compiles the agents with embedded governance. The Monitoring Portal watches them run.

---

## Platform Totals

<div align="center">

| | Designer-SDD | Charlotte | Stratum | Castellan | Monitoring Portal | **Combined** |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|
| **Source Lines** | 7,909 | 19,706 | 73,792 | 81,394 | 6,421 | **189,222** |
| **Modules** | 74 | 178 | 499 | 665 | 92 | **1,508** |
| **Tests (passing)** | 582 | 2,600 | 4,436 | 5,880 | — | **13,498** |
| **Commands / Endpoints** | 17 | 45 | 34 | 51 | 15 | **162** |

</div>

<br>

<div align="center">

**Stack:** Python 3.10+ · TypeScript · React · Next.js · Claude API · OpenAI API · Google Gemini API · Pydantic v2 · SQLAlchemy 2.0 · FastAPI · tree-sitter · Typer · Click · Rich · Jinja2 · asyncio · httpx · tiktoken · OpenTelemetry · Prometheus · Clerk · WebSockets · YAML/JSON

</div>

---

<div align="center">

## Let's Talk

I take on AI-first contract engagements: **agentic compilation**, **agent governance**, **SDLC automation**, **rapid prototyping** from spec to production, prompt and skill compilation, test generation pipelines, quality gate systems, OWASP security auditing, and fleet governance monitoring. If your team is shipping production agents and needs them governed, compiled, tested, and monitored — not hand-assembled and hoped for — I built the compiler stack that makes that possible.

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

</div>
