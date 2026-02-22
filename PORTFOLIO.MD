<div align="center">

# Tim Wolfe

### AI Infrastructure Architect | Autonomous SDLC · Agent Governance · LLM Platform Engineering

Los Altos, CA · [rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Tests](https://img.shields.io/badge/Tests-13%2C133_passing-brightgreen?style=flat-square)
![Lines](https://img.shields.io/badge/Source-184%2C338_lines-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

</div>

---

## About

I build the infrastructure layer between your team and production AI. Not wrappers. Not demos. A full compilation stack — specification engine, prompt compiler, QA automation pipeline, and agent compiler — each delivered as a service, each tested, each running in production.

Most teams building with AI are doing it the hard way: stitching together string concatenation, copy-pasted prompts, frameworks they don't control, and test suites that pass no matter what the code does. I built the alternative.

The four services below automate every phase of AI-driven software development. They work standalone. Together, they form a closed loop from raw idea to deployed, tested, governed production agent — and they're the same tools I use to deliver for enterprise clients across finance, healthcare, and ecommerce.

Before AI infrastructure, 20+ years of enterprise operations leadership: two IPOs (**Quinstreet**, **Responsys**), four acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior technical roles at **Salesforce**, **iHeartMedia**, and **Axway**.

---

<div align="center">

[Castellan](#1-castellan--agent-compiler) · [Charlotte](#2-charlotte--prompt--skills-compiler) · [Stratum](#3-stratum--qa-automation-pipeline) · [Designer-SDD](#4-designer-sdd--specification-engine) · [How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Platform

AI development has a compiling problem. Code gets compiled. Databases get migrated. Infrastructure gets provisioned through declarative configs with validation and version control. But AI systems — the prompts, the agents, the specs they're built from, the tests that prove they work — are still being assembled by hand, shipped on instinct, and debugged in production.

I built four compilers to fix that. One for every phase where ambiguity kills you:

- **Ambiguous specs** &rarr; Designer-SDD extracts, scores, and validates build-ready specification packages from raw input
- **Fragile prompts** &rarr; Charlotte compiles prompts and skills through a deterministic pipeline with type checking, security scanning, and version control
- **Unvalidated output** &rarr; Stratum extracts architecture, generates tests, and enforces seven independent quality gates before anything ships
- **Ungoverned agents** &rarr; Castellan compiles YAML specs into production-ready agents with constitutional governance, runtime guardrails, OWASP security auditing, and multi-target deployment

Every service is standalone. Together they cover the full arc from unstructured idea to deployed, tested, governed agent. The platform is self-hosting — Designer-SDD specs defined every tool, Charlotte compiled the prompts that drive Stratum's AI stages, Stratum validates the code all four generate, and Castellan operationalizes the agents the whole stack produces.

---

## 1. Castellan — Agent Compiler

**Define agents in YAML. Compile, govern, test, audit, and deploy them.**

> The problem: every team building AI agents hits the same wall. The prototype works. Then production hits back — the agent says things it shouldn't, costs $47 on a single session, crashes on a flaky API call, and nobody can prove it won't go off-script next week. Most agent frameworks are code-first and quality-last. They hand you a runtime and leave governance, testing, and deployment as an exercise for the reader.

Castellan flips the model. Write a declarative YAML spec. Compile it through a 5-stage pipeline. Run it against Anthropic, OpenAI, or Google. Gate every response through runtime guardrails. Audit the entire agent against the OWASP Top 10 for Agentic Applications. Export to Python, Docker, FastAPI, Kubernetes, Temporal, LangGraph, CrewAI, AutoGen, Haystack, or Claude Code skill — with optional embedded governance that travels with the deployed agent. Your agents are validated before they run — not after they fail.

Think of it as **Terraform for AI agents**: declarative, version-controlled, auditable, CI/CD-ready.

### The Compilation Pipeline

Every agent spec — no exceptions — runs through 6 deterministic stages before a single token is generated:

| Stage | What it does |
|-------|-------------|
| **Parse** | Validates YAML, resolves block references from the 21-block library, applies `!include` directives and `extends`/`mixins` inheritance, detects circular dependencies |
| **Compose** | Assembles the system prompt from prioritized blocks (system > constitution > task > context > tools > few_shot > constraints > output_format), injects Jinja2 variables |
| **Optimize** | Token budget analysis, prompt compression, whitespace normalization, cost estimation |
| **Validate** | Schema validation, gate threshold checks, tool permission verification, 10+ completeness rules |
| **Scan** | Security scanning — 18+ patterns: injection vectors, exfiltration paths, privilege escalation, hardcoded secrets, jailbreak surfaces, unsafe tool patterns |
| **Render** | Produces a `CompiledAgent` — ready for execution, export, testing, or audit |

### Constitutional Governance

Every compiled agent carries a constitution: core values, technical boundaries, quality standards, user commitments. This isn't documentation — it's enforced at compile time and runtime. Severity-ranked principles (`critical` / `high` / `medium` / `low`) with pattern matching determine whether violations block output, penalize gate scores, or get logged for audit. An agent compiled with Castellan cannot claim it has no boundaries. The boundaries are in the spec, versioned in Git, and enforced by the compiler.

### Runtime Guardrails

Every LLM response runs through an inline guardrail pipeline before it reaches the user — not as a post-processing step, but inside the ReAct loop, on both synchronous and streaming paths:

- **PII Redaction** — emails, SSNs, credit cards, phone numbers, and custom patterns detected and replaced
- **Prompt Injection Filtering** — input messages scanned for injection attacks, exfiltration attempts, and privilege escalation before reaching the model
- **Hallucination Detection** — quoted facts and numbers in responses verified against tool results and conversation context
- **Most-restrictive-wins semantics** — when multiple guardrails fire, the strictest action (BLOCK > REDACT > WARN > PASS) is applied

### OWASP Security Audit (Aegis)

Castellan includes a full security audit service mapped to the OWASP Top 10 for Agentic Applications:

| OWASP ID | Risk | What Aegis Audits |
|----------|------|------------------|
| ASI01 | Prompt Injection | Injection patterns, delimiter exploitation, role confusion |
| ASI02 | Tool Poisoning | Tool chaining data flow, validated sinks |
| ASI03 | Excessive Agency | Blast radius scoring, write tools, missing rate limits |
| ASI04 | Supply Chain | Hardcoded secrets, dependency analysis |
| ASI05 | Output Handling | Response safety, content policies |
| ASI06 | Memory Poisoning | Persistent state injection vectors |
| ASI07 | Insecure Delegation | Agent spawning chains, depth limits |
| ASI08 | Human Oversight | Autonomy envelope, kill switches, cascading failures |
| ASI09 | Trust Exploitation | Confidence calibration, trust score verification |
| ASI10 | Insufficient Monitoring | Audit logging, kill switch accessibility |

Aegis produces six deliverables: executive summary, technical report, OWASP scorecard, generated test suite, candor report, and handoff guide. Verdict: **SHIP / CONDITIONAL / BLOCK** — with CI gate support (`aegis gate --threshold B` returns exit code 0 or 1).

### Multi-Turn Behavioral Testing

Single input/output assertions aren't enough. Castellan's test runner supports full multi-turn conversation testing with 28 assertion types — `contains`, `not_contains`, `regex_match`, `json_valid`, `min_length`, `max_length`, composite operators (`all_of`, `any_of`, `none_of`), and more. Built-in adversarial personas: `jailbreak`, `confused`, `topic_switch`, `boundary_probe`. You can prove your agent handles jailbreak attempts correctly, maintains context across topic switches, and refuses prohibited content — all in a CI pipeline, before deployment.

### Execution Engine

Async-first ReAct runtime implementing the **Observe &rarr; Think &rarr; Act &rarr; Validate** cycle with full production resilience:

- **3 LLM providers** — Anthropic (Claude), OpenAI (GPT-4o), Google (Gemini) with streaming, retry, and exponential backoff
- **MCP client** — tool discovery, auth, and calling against MCP servers
- **A2A protocol** — agent-to-agent task lifecycle and discovery
- **RAG pipeline** — ingestors, chunkers, embedders, and vector store integration
- **Sliding window memory** — token-budgeted conversation history that never truncates the system prompt, working memory slots, optional long-term file-based persistence
- **Cost-aware model routing** — routes each call to the most cost-effective model tier based on task complexity, with per-run budget enforcement and automatic termination
- **Circuit breaker + rate limiter** — CLOSED/OPEN/HALF_OPEN resilience, token bucket rate limiting, fallback provider chain, LRU + TTL response caching

### Multi-Agent Orchestration

| Pattern | How it works |
|---------|-------------|
| **Supervisor** | Master agent routes tasks to specialists via regex/keyword rules, synthesizes results |
| **Pipeline** | Sequential chain with stage transforms, stops on error |
| **Broadcast** | Parallel fan-out with aggregation strategies: concat, first, or vote |
| **Peer** | Turn-based collaboration with configurable max rounds |

Dynamic routing with priority ordering. Delegation depth limiting prevents infinite loops. Checkpoint/resume serializes full orchestration state for long-running tasks.

### Production Deployment

**7 export targets** — Python package, Docker (Dockerfile + Compose), FastAPI server (/chat, /health, /trace, /stream), Claude Code skill, Kubernetes (Deployment, Service, ConfigMap, Secret, Kustomization, optional Helm charts), Temporal workflow, and client delivery package.

**Observability** — OpenTelemetry span export, Prometheus metrics, 8 lifecycle event hooks, Rich tree trace visualization, interactive debugger with 6 breakpoint types, governance dashboard with fleet metrics, monthly health reports with drift detection, and append-only audit log with JSON export for compliance.

### Typed Governance Models

All 5 governance sub-schemas — `governance`, `human_oversight`, `data_sensitivity`, `sign_off`, and `testing` — are now typed Pydantic v2 models. Parse-time validation catches misconfigurations (typos, wrong types, missing fields) at compile time, not at runtime. If a governance block is structurally invalid, the compiler rejects it before a single token is generated.

### CI/CD Governance Gate

`castellan ci-diff` compiles both base and head spec versions, runs governance scoring on both, and produces a `GovernanceImpactReport` posted as a PR comment. Verdict: **APPROVE / REVIEW / BLOCK**. GitHub Action and GitLab CI templates included. Governance regression is now a merge-blocking signal, not a post-deploy surprise.

### Governed Exports

The `--governed` flag on LangGraph, CrewAI, AutoGen, and Haystack exports embeds `castellan.mantle` governance directly in the exported code: `@governed` decorator, compliance JSONL logging, kill switch, autonomy ceiling. Governance travels with the deployed agent — not as an external dependency, but as inline enforcement that works even if the agent is running outside Castellan's runtime.

### Visual Execution Replay

`castellan replay --visual` renders execution traces into self-contained interactive HTML. Dark-themed timeline with collapsible turns, tool calls, gate evaluations, guardrail decisions, cost breakdown, and annotation panel. One file, no dependencies, shareable with stakeholders who don't have a terminal.

### Unified Runtime

A single `_execute_turns()` async generator eliminates the prior `run()`/`run_stream()` duplication. Human checkpoint enforcement is now structural: autonomous agents with no HITL channel raise `SessionCeilingExceededError` rather than silently running unchecked. One code path, one set of invariants, one place to audit.

### Live Governance Dashboard

WebSocket-based real-time dashboard showing governance events — gate evaluations, guardrail hits, kill switch activations — as they happen. No polling, no refresh. Connect a browser and watch your agent fleet's governance posture update live.

<details>
<summary><strong>Full CLI reference (45 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `castellan init` | Scaffold agent from template or intake form |
| `castellan compile` | 5-stage compilation pipeline |
| `castellan run` | Interactive or single-message execution |
| `castellan validate` | Completeness and schema checks |
| `castellan scan` | Security scanning (18+ patterns) |
| `castellan test` | Behavioral + adversarial conversation testing |
| `castellan score` | Constitutional + gate scoring |
| `castellan candor` | Transparency analysis |
| `castellan trace` / `castellan replay` | Execution trace and replay |
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
| `aegis gate` | CI gate with verdict threshold |

</details>

```
45 commands · 426 modules · 80,457 lines · 5,661 tests, all passing
```

<br>

---

## 2. Charlotte — Prompt & Skills Compiler

**A real compiler for AI prompts and Claude Code skills. Not a template stitcher.**

> The problem: prompt engineering was ad-hoc string concatenation. No type checking. No version control. No security scanning. No way to test one prompt change against regression. Teams were shipping prompts the same way they shipped code in the 90s — copy-paste and hope nothing breaks in production.

Charlotte is a 5-stage deterministic compiler that treats prompts and skills as first-class software artifacts. It parses typed YAML specifications, composes them against a 94-block library with conflict detection and dependency resolution, runs 8-pass automatic optimization, validates token budgets against 26 model context windows, and renders provider-specific output for OpenAI, Anthropic, and Google Gemini.

It has a type system, a security scanner, a test framework, a versioning system, environment management, CI/CD generation, and a multi-agent compiler that generates runnable projects for four major agent frameworks. If you wouldn't ship code without a build system, you shouldn't ship prompts without one either.

### The Compilation Pipeline

```
YAML Spec → Parse → Compose → Optimize → Validate → Render → Provider-Ready Output
```

1. **Parse** — Read spec, resolve block references from the 94-block library, validate against Pydantic v2 schemas
2. **Compose** — Assemble blocks in strict type-precedence order (17 types, each with defined priority). Detect conflicts, enforce singletons, resolve dependencies, inject typed variables
3. **Optimize** — 8 automatic passes: deduplication, adjacent text merging, empty block stripping, whitespace normalization, system block reordering, example compression, token budget optimization, provider-specific hints
4. **Validate** — Conflict detection, token budgeting per target model with per-block breakdown, completeness checks, composition rule enforcement
5. **Render** — Provider-specific output: OpenAI messages array, Anthropic system parameter, Google Gemini system_instruction, or generic text

### 94-Block Library Across 17 Types

Every block is pure YAML — no embedded code. The library is extensible without touching source. Blocks cover every prompt engineering pattern: system, task, few-shot, chain-of-thought, tool use, RAG, agent, evaluation, extraction, meta, conversational, safety, routing, memory, retrieval, guardrail, planning. The compiler enforces assembly order, singleton constraints, and tier requirements so a composed prompt can't be structurally invalid.

### Security Scanner — 54 Checks, 21 Categories

Every prompt gets scanned at compile time across injection, exfiltration, model manipulation, context poisoning, privilege escalation, compliance (GDPR/HIPAA/PCI-DSS), supply chain, bias/fairness, MCP tool poisoning, and more. Security isn't an afterthought — it's a compilation stage.

### Skills Compiler

Charlotte compiles Claude Code skills directly — structured YAML specs optimized for the `charlotte compile -f skill` export path. The same 94-block library, the same security scanner, the same test framework — purpose-built output for Claude Code skill deployment.

### Test Framework

30 assertion types including exact match, regex, JSON schema validation, LLM-as-judge, cosine similarity, sentiment analysis, language detection, PII detection, latency thresholds, and composite assertions. Parallel cross-model execution. Evaluation history with regression drift detection. You can run a prompt change against a baseline and know immediately whether it regressed.

### Multi-Agent Compiler

Takes compiled prompts and generates complete, runnable projects for CrewAI, LangGraph, AutoGen, OpenAI Agents SDK, and Google A2A protocol. Each export includes pyproject.toml, README, and all source files. A shared extraction layer means adding a new framework is one renderer and its templates.

<details>
<summary><strong>Workflow engine, versioning, and environments</strong></summary>

<br>

**Multi-prompt workflows** — Chain multiple specs with typed data flow (`{{steps.X.output.field}}`). Topological execution ordering. Conditional step execution via Jinja2. Cross-step schema validation. End-to-end workflow testing.

**Content-addressed versioning** — JSON snapshots with semantic block-aware diffing. Track added, removed, and modified blocks across versions.

**Environment management** — Dev/staging/production environments with variable overrides, promotion gates (test pass rate, score threshold, manual approval), and environment diffing.

**CI/CD** — 4 GitHub Actions workflow templates: validate-on-PR, test-on-push, scheduled regression, environment promotion.

</details>

<details>
<summary><strong>21 export formats</strong></summary>

<br>

Text, JSON, YAML, API payload, MCP definition, LangChain template, HTML report, README, Claude Code Skill, MCP server, CrewAI, LangGraph, AutoGen, OpenAI Agents, A2A Agent Card — each in single-prompt and workflow variants.

</details>

<details>
<summary><strong>10 production example packs</strong></summary>

<br>

| Pack | Pattern | Use Case |
|------|---------|----------|
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
21 commands · 83 modules · 21,409 lines · 94 blocks · 2,548 tests, all passing
```

<br>

---

## 3. Stratum — QA Automation Pipeline

**Point it at source code. It extracts the architecture, generates tests and docs, then decides whether it ships.**

> The problem: teams were shipping AI-generated test suites without checking whether the tests actually tested anything. Hallucinated assertions. Mocked-out logic. Tests that pass no matter what — going straight to CI. Nobody was testing the tests.

Stratum is a 6-stage automated quality pipeline. It extracts full architecture using Claude and tree-sitter across 6 languages, generates unit tests and API tests across 4 frameworks, produces documentation with seven independent analyzers, then runs everything through seven independent quality gates. Each gate produces its own verdict. The audit engine aggregates them into a final pass or fail. A transparency layer tracks every skip, failure, and limitation — no silent failures.

### The Pipeline

```
SOURCE CODE
    │
    ▼
┌──────────────────────────────────────────┐
│ 1. EXTRACT (tree-sitter + Claude)        │
│    Classes, functions, endpoints → JSON   │
│    6 languages · framework detection      │
└──────────┬───────────────────────────────┘
           │
    ┌──────┴──────────┬──────────────┐
    ▼                 ▼              ▼
┌──────────┐   ┌───────────┐   ┌──────────┐
│ 2. UNIT  │   │ 3. API    │   │ 4. DOCS  │
│ pytest / │   │ 4 layers  │   │ 7 analyzers│
│ jest /   │   │ 4 frameworks│  │ 3 formats │
│ JUnit /  │   │           │   │           │
│ Go test  │   │           │   │           │
└────┬─────┘   └─────┬─────┘   └────┬─────┘
     └────────────────┼──────────────┘
                      ▼
┌──────────────────────────────────────────┐
│ 5. QUALITY GATES (7 independent modules) │
└──────────────────┬───────────────────────┘
                   ▼
┌──────────────────────────────────────────┐
│ 6. CANDOR — Transparency Report          │
│ What automation couldn't handle          │
└──────────────────────────────────────────┘
```

### Architecture Extraction

Combines Claude with tree-sitter static analysis to extract complete codebase structure across 6 languages — Python, TypeScript, JavaScript, Java, Go, Rust — with framework auto-detection for Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, and Quarkus. Output: 6 JSON artifacts including `source_model.json`, the critical artifact consumed by every downstream stage.

### Test Generation

**Unit tests** — generates pytest, jest, JUnit, or Go test suites from extracted architecture. 3-retry validation loop: generate &rarr; execute &rarr; fix. Tests that don't actually run are rejected before they leave the pipeline.

**API tests across 4 layers and 4 frameworks:**

| Layer | What it validates |
|-------|-----------------|
| **Contract** | API surface matches the spec — methods, paths, status codes, content types |
| **Boundary** | Edge cases — empty payloads, max-length strings, type coercion, null handling |
| **Workflow** | Multi-step state transitions — create &rarr; read &rarr; update &rarr; delete sequences |
| **Regression** | Previously-found defects captured as permanent guards |

### The Seven Quality Gates

This is the core of Stratum. Seven independent modules, each with its own verdict. All seven must pass for a pipeline to ship.

| Gate | What it enforces |
|------|-----------------| 
| **Forge** | The Seven Rules — every generated test must: **(A)** invoke the code under test, **(B)** assert on outputs not inputs, **(C)** not swallow exceptions, **(D)** verify every mock, **(E)** test error paths, **(F)** fail if the code is wrong, **(G)** have no interdependence. All seven or rejected. |
| **Aegis** | Security scanning — 24 vulnerability types across 9 detectors. SQL injection, command injection, XSS, auth bypass, data exposure, hardcoded secrets. Generates exploit tests to prove vulnerabilities and remediation tests to verify fixes. |
| **Sentinel** | Mutation testing — 8 mutator types. Mutates source, runs the test suite, calculates whether the suite actually catches the mutations. Proves tests have teeth. |
| **Specter** | Flaky test detection — 9 pattern types. Timing-dependent, random state, external dependencies, concurrency, async timing. Auto-quarantine isolates unreliable tests. |
| **Arbiter** | Harvests quality rules from external linters (flake8, eslint, clippy, go vet) and maps them to test quality categories. |
| **CodeGate** | AI code quality gate — pure rule-based, no LLM calls. 10-item production readiness checklist. 3-tier dependency verification: recognized, hallucination risk, unverifiable. Catches hallucinated dependencies, happy-path-only logic, context-blind decisions. |
| **Intent** | Spec requirement verification — validates that generated code implements the requirements from the original spec. Coverage percentage and gap analysis. |

### Baseline + Delta Service

Named baselines snapshot extraction state. The delta engine diffs against previous baselines at the function level — detecting added, modified, and removed functions — then generates targeted tests only for changed code. This is what converts a one-shot engagement into a recurring subscription: re-test only what changed, at a fraction of the cost.

### Intelligence Layer

**Predictive test prioritization** ranks every function by a 6-factor risk score — complexity, change frequency, recency, centrality, coverage, defect history — using git history when available. Produces `TEST_PRIORITY_MAP.md` so the most dangerous untested code gets covered first.

**Smart model routing** selects Claude model tiers (Haiku/Sonnet/Opus) per API call based on task complexity. Target: 20-40% cost reduction without quality loss.

**SDD Bridge** — transforms extraction output into Designer-SDD spec format. Scan any existing codebase, produce a complete build spec, then rebuild it in a different framework or language.

*Philosophy: "We identify bugs. We do NOT fix them."*

<details>
<summary><strong>CLI reference (27 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `stratum extract` | Extract architecture from source code |
| `stratum generate tests` | Generate unit + API tests |
| `stratum generate docs` | Generate documentation |
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
| `stratum-unit generate` | Standalone unit test generation |
| `stratum-api generate` | Standalone API test generation |
| `stratum-docs generate` | Standalone documentation generation |
| `stratum-docs sdd` | Generate Designer-SDD spec from codebase |

</details>

```
27 commands · 313 modules · 73,882 lines · 4,386 tests, all passing
```

<br>

---

## 4. Designer-SDD — Specification Engine

**Turn unstructured ideas into scored, validated, build-ready specification packages.**

> The problem: specs kept arriving as Slack threads, call transcripts, and scattered notes. Teams kept building the wrong thing because requirements were ambiguous. AI agents kept generating code that missed the point because nobody validated the spec before handing it off.

Designer-SDD is a specification engine. Feed it a client brief, a call transcript, raw notes — it extracts a structured JSON spec via Claude, then runs it through a gauntlet: validation against domain-specific rules, dual-gate scoring across 36 weighted checks, iterative AI-driven refinement that re-scores after every pass, and round-trip verification that confirms every requirement in the spec appears in the rendered output.

The output isn't a document. It's a scored, validated, GitHub-ready documentation package of up to 11 files — ready for a developer or an AI agent to build from. Every tool in this platform was built from a Designer-SDD spec.

### How it Works

**Multiple entry points** — intake from raw text, interactive brainstorming with Claude, 3-stage web-powered market research, browser-based HTML form, or 5 pre-built templates (CLI, REST API, SaaS dashboard, library, Chrome extension).

**Dual-gate scoring** — two independent scoring systems run on every spec:

| Gate | What it measures | Checks | Threshold |
|------|-----------------|--------|-----------| 
| **Quality** | Is this spec complete and well-structured? | 28 weighted checks across 7 sections | 70% |
| **Buildability** | Can a developer or AI agent actually build from this? | 8 checks: ambiguity detection, dependency completeness, acceptance verifiability, tech completeness | 60% |

**Domain-aware validation** — CLI projects must declare exit codes. APIs must declare auth schemes. Web apps must declare error handling. Mobile apps must declare offline behavior. Not generic rules — rules that match what you're actually building.

**Iterative refinement** — score the spec, send improvement instructions to Claude, re-score, repeat. The spec gets measurably better each round. Up to 3 automated passes.

**Tier-gated export** — small projects produce 7 files, medium 9, large 11. Always includes CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, HANDOFF.md, README.md, and the source JSON. Larger projects add DATA_MODEL.md, QUICKSTART.md, and ARCHITECTURE.md.

**Round-trip verification** — after export, verifies that every requirement and task in the source spec appears in the rendered markdown. Catches drift between spec and output.

<details>
<summary><strong>Full CLI reference (16 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------| 
| `designer intake` | Extract specs from unstructured text (briefs, notes, transcripts) |
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
16 commands · 53 modules · 8,590 lines · 538 tests, all passing
```

<br>

---

## How They Connect

```
  Raw Idea              YAML Spec            Source Code           Agent Spec
     │                     │                     │                     │
     ▼                     ▼                     ▼                     ▼
+--------------+    +-------------+      +-------------+    +------------------+
| Designer-SDD |    |  Charlotte  |      |   Stratum   |    |   Castellan      |
|              |    |             |      |             |    |                  |
| Validate     |    | Compile     |      | Extract     |    | Compile          |
| Score        |    | Validate    |      | Generate    |    | Govern / Guard   |
| Improve      |    | Test        |      | Gate        |    | Test / Audit     |
| Export       |    | Export      |      | Audit       |    | Export / Deploy  |
+------+-------+    +------+------+      +------+------+    +--------+---------+
       │                   │                    │                     │
       ▼                   ▼                    ▼                     ▼
  Scored Spec        Provider-Ready        Pass/Fail Verdict    Running Agent
  Package (7-11      Prompts, Skills,      + Tests + Docs       (CLI, HTTP, Docker,
  files)             or Agent Projects     + Transparency        K8s, Temporal)
```

Each service is standalone. Together they close the loop:

- **Designer-SDD** defines *what* to build — scored, validated, ready for a developer or an AI agent
- **Charlotte** handles *how to talk to AI* — compiled prompts and skills that don't break in production
- **Stratum** validates *what was built* — seven gates, no silent failures, delta re-testing on every change
- **Castellan** operationalizes *running agents* — governed, audited, resilient, deployed

The platform is self-hosting. Designer-SDD specs defined every tool. Charlotte compiled the prompts that power Stratum's AI stages. Stratum validates the code all four generate. Castellan turns the whole stack into production agent systems.

---

## Platform Totals

<div align="center">

| | Designer-SDD | Charlotte | Stratum | Castellan | **Combined** |
|:---|:---:|:---:|:---:|:---:|:---:|
| **Source Lines** | 8,590 | 21,409 | 73,882 | 80,457 | **184,338** |
| **Python Modules** | 53 | 83 | 313 | 426 | **875** |
| **Tests (passing)** | 538 | 2,548 | 4,386 | 5,661 | **13,133** |
| **CLI Commands** | 16 | 21 | 27 | 45 | **109** |

</div>

<br>

<div align="center">

**Stack:** Python 3.10+ · Claude API · OpenAI API · Google Gemini API · Pydantic v2 · tree-sitter · Typer · Click · Rich · FastAPI · Jinja2 · asyncio · httpx · tiktoken · WeasyPrint · OpenTelemetry · Prometheus · YAML/JSON

---

*Designed, built, and tested by Tim Wolfe.*

</div>

---

<div align="center">

## Let's Talk

I take on AI-first contract engagements — agent compilation, prompt infrastructure, SDLC automation, test generation pipelines, quality gate systems, and OWASP security auditing. If your team is shipping AI-generated code, AI-powered features, or production agents and needs them to be reliable, governed, and production-grade — I've built the compiler stack and I know exactly where the failure modes are.

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

</div>
