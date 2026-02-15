<div align="center">

# Tim Wolfe

### AI Practitioner & Toolmaker

Los Altos, CA · [rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Tests](https://img.shields.io/badge/Tests-7%2C718_passing-brightgreen?style=flat-square)
![Lines](https://img.shields.io/badge/Source-109%2C435_lines-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

</div>

---

## About

I design, build, and ship production AI automation across the entire software development lifecycle. Not prototypes -- production platforms deployed at enterprise scale across finance, healthcare, and ecommerce.

Currently serving as an external AI automation architect, designing end-to-end test automation platforms that replace manual QA workflows with AI-driven pipelines for enterprise clients. Previously founded and led an AI practice as CIO & Head of AI Solutions, building the tooling foundations now deployed in production. Before AI, 20+ years of enterprise operations leadership including two IPOs (**Quinstreet**, **Responsys**), four major acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior roles at **Salesforce**, **iHeartMedia**, and **Axway**.

The four tools below are the platform I built and continue to evolve. Each one automates a phase of the SDLC that most teams still do by hand -- specification, prompt engineering, quality assurance, and agent deployment. They're standalone, they're tested, and they're in production.

---

<div align="center">

[Designer-SDD](#1-designer-sdd) · [Charlotte](#2-charlotte) · [Stratum](#3-stratum) · [Castellan](#4-castellan) · [How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Platform

Most AI-generated code ships without anyone checking whether it actually works. Tests that pass no matter what. Prompts held together with string concatenation. Specs that started as Slack threads. Agents that look great in demos and break in production.

I built four tools to fix that. Each one solves a specific failure mode I kept hitting across client engagements:

- **Ambiguous specs** &rarr; Designer-SDD turns unstructured ideas into scored, validated specification packages
- **Fragile prompts** &rarr; Charlotte compiles prompts through a real pipeline with type checking, security scanning, and version control
- **Unvalidated output** &rarr; Stratum extracts architecture, generates tests, and enforces seven independent quality gates before anything ships
- **Unreliable agents** &rarr; Castellan compiles, runs, tests, and deploys AI agents from declarative specs with constitutional governance

Every tool is standalone. Together they cover the full arc from raw idea to deployed, tested, production agent. The platform is self-hosting -- Designer-SDD specs defined every tool here, Charlotte compiles the prompts that power Stratum's AI stages, Stratum validates the code all four generate, and Castellan operationalizes everything into running systems.

---

## 1. Designer-SDD

**Turn unstructured ideas into scored, validated, build-ready specification packages.**

> The problem: specs kept arriving as Slack threads, call transcripts, and scattered notes. Teams kept building the wrong thing because the requirements were ambiguous. AI agents kept generating code that missed the point because nobody validated the spec before handing it off.

Designer-SDD is a specification engine. Feed it a client brief, a call transcript, raw notes -- it extracts a structured JSON spec via Claude, then puts it through a gauntlet: validation against domain-specific rules, dual-gate scoring (39 weighted checks across quality and buildability), iterative AI-driven refinement that re-scores after every pass, and round-trip verification that confirms every requirement in the spec appears in the rendered output.

The output isn't a document. It's a scored, validated, GitHub-ready documentation package of up to 11 files -- ready for a developer or an AI agent to start building from. Designer-SDD specs defined every tool in this platform, and the spec-driven workflow now drives client delivery for enterprise engagements.

### How it works

**Multiple entry points** -- intake from raw text, interactive brainstorming with Claude, 3-stage web-powered market research, browser-based HTML form, or 5 pre-built templates (CLI, REST API, SaaS dashboard, library, Chrome extension).

**Dual-gate scoring** -- two independent scoring systems run on every spec:

| Gate | What it measures | Checks | Threshold |
|------|-----------------|--------|-----------|
| **Quality** | Is this spec complete and well-structured? | 31 weighted checks across 7 sections | 70% |
| **Buildability** | Can a developer (or AI agent) actually build from this? | 8 checks: ambiguity detection, dependency completeness, acceptance verifiability, tech completeness | 60% |

**Domain-aware validation** -- CLI projects must declare exit codes. APIs must declare auth schemes. Web apps must declare error handling. Mobile apps must declare offline behavior. Not generic rules -- rules that match what you're building.

**Iterative refinement** -- score the spec, send improvement instructions to Claude, re-score, repeat. The spec gets measurably better each round. Up to 3 automated passes.

**Tier-gated export** -- small projects produce 7 files, medium 9, large 11. Always includes CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, HANDOFF.md, README.md, and the source JSON. Larger projects add DATA_MODEL.md, QUICKSTART.md, and ARCHITECTURE.md.

**Round-trip verification** -- after export, verifies that every requirement and task in the source spec actually appears in the rendered markdown. Catches drift between spec and output.

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
| `designer ingest` | Full pipeline (validate &rarr; score &rarr; export) |
| `designer export` | Render tier-gated markdown package |
| `designer diff` | Field-by-field spec comparison with score deltas |
| `designer research` | Answer open questions from RESEARCH section via Claude |
| `designer verify` | Post-export round-trip integrity check |
| `designer template list` | Browse pre-built templates |
| `designer template preview` | Preview template contents |
| `designer template use` | Scaffold project from template |
| `designer init` | Initialize project configuration |

</details>

<details>
<summary><strong>Spec gate -- 10 hard deterministic rules</strong></summary>

<br>

Every functional requirement must have a description and priority. User stories must reference requirements. Assumptions must have mitigation strategies. Open questions must have resolution status. Risks must have mitigation. Success criteria must be measurable. Definition of Done items must be actionable. Tech choices must be justified. Task breakdown must cover all requirements. No unresolved placeholders (TODO/TBD/FIXME).

Pass, conditional pass, or fail. No ambiguity.

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Strict four-layer separation: CLI &rarr; Engine &rarr; Core &larr; Util. Stateless -- zero database, zero persistence. Every operation is a pure data transformation. All Claude calls go through a single API wrapper with exponential backoff retry, fully mocked in tests. Path traversal protection at the security boundary. Token budgeting tracks API spend across sessions. Configuration loads from four layers: environment &rarr; project YAML &rarr; global YAML &rarr; built-in defaults.

</details>

```
16 commands · 53 modules · 8,590 lines · 538 tests, all passing
```

<br>

---

## 2. Charlotte

**A real compiler for AI prompts -- not a template stitcher.**

> The problem: prompt engineering was ad-hoc string concatenation. No type checking, no version control, no security scanning, no way to test one prompt change against regression. Teams were shipping prompts the same way they shipped code in the 90s -- copy-paste and pray.

Charlotte is a five-stage deterministic compiler that treats prompts as first-class software artifacts. It parses typed specifications, composes them against a 94-block library with conflict detection and dependency resolution, runs 8-pass automatic optimization, validates token budgets against 26 model context windows, and renders provider-specific output for OpenAI, Anthropic, and Google Gemini.

It has a type system, a security scanner, a test framework, a versioning system, environment management, CI/CD generation, and a multi-agent compiler that generates runnable projects for four major agent frameworks. If you wouldn't ship code without a build system, you shouldn't ship prompts without one either. Charlotte evolved from a prompt engineering platform I built for client delivery -- voice-driven multi-phase development with evaluation pipelines -- into a full compiler toolchain.

### The compilation pipeline

```
YAML Spec → Parse → Compose → Optimize → Validate → Render → Provider-Ready Output
```

1. **Parse** -- Read spec, resolve block references from the 94-block library, validate against Pydantic v2 schemas
2. **Compose** -- Assemble blocks in strict type-precedence order (17 types, each with defined priority). Detect conflicts, enforce singletons, resolve dependencies, inject typed variables
3. **Optimize** -- 8 automatic passes: deduplication, adjacent text merging, empty block stripping, whitespace normalization, system block reordering, example compression, token budget optimization, provider-specific hints
4. **Validate** -- Conflict detection, token budgeting per target model with per-block breakdown, completeness checks, composition rule enforcement
5. **Render** -- Provider-specific output: OpenAI messages array, Anthropic system parameter, Google Gemini system_instruction, or generic text

### What makes it more than a template engine

**94-block library across 17 types** -- system, task, few-shot, chain-of-thought, tool use, RAG, agent, evaluation, extraction, meta, conversational, safety, routing, memory, retrieval, guardrail, planning. Blocks are pure YAML data, not embedded code. The library is extensible without touching source.

**Security scanner** -- 54 checks across 21 categories. Injection, exfiltration, model manipulation, context poisoning, privilege escalation, compliance (GDPR/HIPAA/PCI-DSS), supply chain, bias/fairness, MCP tool poisoning, and more. Every prompt gets scanned at compile time.

**Test framework** -- 30 assertion types including exact match, regex, JSON schema validation, LLM-as-judge, cosine similarity, sentiment analysis, language detection, PII detection, latency thresholds, and composite assertions. Parallel cross-model execution. Evaluation history with regression drift detection.

**Multi-agent compiler** -- takes compiled prompts and generates complete, runnable projects for CrewAI, LangGraph, AutoGen, OpenAI Agents SDK, and Google A2A protocol. Each export includes pyproject.toml, README, and all source files. A shared extraction layer means adding a new framework is one renderer and its templates.

**21 export formats** -- text, JSON, YAML, API payload, MCP definition, LangChain template, HTML report, README, Claude Code Skill, MCP server, CrewAI, LangGraph, AutoGen, OpenAI Agents, A2A Agent Card -- each in single-prompt and workflow variants.

<details>
<summary><strong>Security scanner -- 21 categories</strong></summary>

<br>

| Category | What it checks |
|----------|---------------|
| Injection (basic + advanced) | Prompt injection, jailbreak, role hijacking, instruction override |
| Data exfiltration | Training data extraction, system prompt leaking, user data theft |
| Model manipulation | Behavior alteration, temperature/safety setting tampering |
| Output control | Format forcing, encoding tricks, output redirection |
| Context poisoning | Conflicting instructions, hidden context, delimiter manipulation |
| Resource abuse | Token inflation, recursive generation, denial-of-service |
| Privilege escalation | Role elevation, permission bypass, admin impersonation |
| Cross-prompt attacks | Session persistence, state injection |
| Compliance | GDPR, HIPAA, PCI-DSS data handling violations |
| Supply chain | Dependency confusion, package hallucination |
| Bias/fairness | Stereotyping, demographic bias, unequal treatment |
| Hallucination risk | Unsupported claims, fabrication triggers |
| Token manipulation | Tokenizer exploits, special token abuse |
| Auth boundary | Authentication bypass, session manipulation |
| Sandbox escape | Code execution, file system access, network access |
| Prompt structure | Structural vulnerabilities, delimiter confusion |
| Logging safety | PII in logs, sensitive data exposure |
| Multi-modal threats | Image-based injection, cross-modal attacks |
| Chain safety | Multi-step attack chains, sequential exploitation |
| MCP tool poisoning | Malicious tool definitions, tool injection |
| Version safety | Version rollback attacks, downgrade exploits |

</details>

<details>
<summary><strong>Workflow engine, versioning, and environments</strong></summary>

<br>

**Multi-prompt workflows** -- Chain multiple specs with typed data flow (`{{steps.X.output.field}}`). Topological execution ordering. Conditional step execution via Jinja2. Cross-step schema validation. End-to-end workflow testing.

**Content-addressed versioning** -- JSON snapshots with semantic block-aware diffing. Track added, removed, and modified blocks across versions.

**Environment management** -- Dev/staging/production environments with variable overrides, promotion gates (test pass rate, score threshold, manual approval), and environment diffing.

**CI/CD** -- 4 GitHub Actions workflow templates: validate-on-PR, test-on-push, scheduled regression, environment promotion.

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

<details>
<summary><strong>Architecture</strong></summary>

<br>

28 Pydantic v2 models enforce every data boundary. Four global registries (block types, providers, exporters, assertions) make the system pluggable at every layer. Three-tier prompt classification (single-turn, multi-phase, agent-orchestrating) with automatic detection. The agent compiler uses a shared extraction layer so all five framework renderers consume the same AgentTeam abstraction. Token budgeting across 26 registered models (8K to 2M context windows).

</details>

```
30 commands · 80 modules · 20,609 lines · 94 blocks · 2,423 tests, all passing
```

<br>

---

## 3. Stratum

**Point it at source code. It extracts the architecture, generates tests and docs, then decides whether it ships.**

> The problem: teams were shipping AI-generated test suites without checking whether the tests actually tested anything. Hallucinated assertions, mocked-out logic, tests that pass no matter what -- all going straight to CI. Nobody was testing the tests.

Stratum is a six-stage automated quality pipeline. It extracts the full architecture using Claude and tree-sitter across 6 languages, generates unit tests and API tests across multiple frameworks, produces documentation with seven independent analyzers, then runs everything through seven independent quality gates. Each gate produces its own verdict. The audit engine aggregates them into a final pass or fail. A transparency layer tracks every skip, failure, and limitation -- no silent failures. The quality gate architecture and self-healing test generation pipeline are the core of what I deliver for enterprise clients, driving pass rates above 95% across production codebases.

### The pipeline

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
│ pytest / │   │ 4 layers  │   │ 7 analyz │
│ jest     │   │ 4 framewk │   │ 3 format │
└────┬─────┘   └─────┬─────┘   └────┬─────┘
     └────────────────┼──────────────┘
                      ▼
┌──────────────────────────────────────────┐
│ 5. QUALITY GATES (7 independent modules) │
└──────────────────┬───────────────────────┘
                   ▼
┌──────────────────────────────────────────┐
│ 6. CANDOR (Transparency Report)          │
│ What automation couldn't handle          │
└──────────────────────────────────────────┘
```

### Architecture extraction

Combines Claude with tree-sitter static analysis to extract complete codebase structure across **6 languages** (Python, TypeScript, JavaScript, Java, Go, Rust) with framework auto-detection for Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, and Quarkus. Output: 6 JSON artifacts including `source_model.json` -- the critical artifact consumed by every downstream stage.

### Test generation

**Unit tests** -- generates pytest or jest test suites from extracted architecture. 3-retry validation loop: generate &rarr; execute &rarr; fix. Tests that don't actually run are rejected. Prompts passed via stdin (not CLI arguments) to prevent command injection.

**API tests across 4 layers and 4 frameworks:**

| Layer | What it validates |
|-------|-------------------|
| **Contract** | API surface matches the spec -- methods, paths, status codes, content types |
| **Boundary** | Edge cases -- empty payloads, max-length strings, type coercion, null handling |
| **Workflow** | Multi-step state transitions -- create &rarr; read &rarr; update &rarr; delete sequences |
| **Regression** | Previously-found defects captured as permanent guards |

Output in pytest, jest, Postman/Newman, or REST Assured. Architecture diff system detects changes between extractions and generates targeted regression tests.

### Documentation generation

**7 independent analyzers** -- data flow tracing, decision archaeology (reconstructs *why* decisions were made from code patterns and git history), tribal knowledge capture, change impact prediction, code smell detection, health scoring, and onboarding guide generation. Each analyzer runs independently and feeds 7 quality gates on the docs themselves (accuracy, coverage, completeness, freshness, readability, link validity). Output in Markdown, HTML (with Mermaid diagrams and search index), or PDF.

### The seven quality gates

This is the core of Stratum. Seven independent modules, each with its own verdict:

| Gate | What it enforces |
|------|-----------------|
| **Forge** | The Seven Rules -- every generated test must: **(A)** invoke the code under test, **(B)** assert on outputs not inputs, **(C)** not swallow exceptions, **(D)** verify every mock, **(E)** test error paths, **(F)** fail if the code is wrong, **(G)** have no interdependence. All seven or rejected. |
| **Aegis** | Security scanning -- 24 vulnerability types across 9 detectors. SQL injection, command injection, XSS, auth bypass, data exposure, hardcoded secrets. Generates exploit tests to prove vulnerabilities and remediation tests to verify fixes. |
| **Sentinel** | Mutation testing -- 8 mutator types. Mutates source code, runs the test suite, calculates whether the suite actually catches the mutations. Proves tests have teeth. |
| **Specter** | Flaky test detection -- 9 pattern types. Timing-dependent, random state, external dependencies, concurrency, async timing. Auto-quarantine isolates unreliable tests. |
| **Arbiter** | Harvests quality rules from external linters (flake8, eslint, clippy, go vet) and maps them to test quality categories. |
| **CodeGate** | AI code quality gate -- pure rule-based, no LLM calls. 10-item production readiness checklist. 3-tier dependency verification: recognized, hallucination risk, unverifiable. Catches hallucinated dependencies, happy-path-only logic, context-blind decisions. |
| **Intent** | Spec requirement verification -- validates that generated code actually implements the requirements from the original spec. Coverage percentage and gap analysis. |

### Candor -- the transparency layer

Tracks what automation couldn't handle and reports it honestly. Two output reports: `CANDOR_TECHNICAL.md` for developers (full detail) and `CANDOR_EXECUTIVE.md` for stakeholders (summary). Every stage feeds Candor: extraction skips, generation failures, validation errors, gate bypasses. Success rates calculated from actual file counts, not estimates.

*Philosophy: "We identify bugs. We do NOT fix them."*

<details>
<summary><strong>CLI reference (22 commands)</strong></summary>

<br>

**Unified CLI:**

| Command | Purpose |
|---------|---------|
| `stratum extract` | Extract architecture from source code |
| `stratum generate tests` | Generate unit + API tests |
| `stratum generate docs` | Generate documentation |
| `stratum audit` | Run all quality gates |
| `stratum review` | CodeGate standalone review |
| `stratum verify` | Spec requirement verification |
| `stratum ship` | Full pipeline with handoff documentation |
| `stratum run` | Full pipeline (extract &rarr; generate &rarr; gate &rarr; audit) |

**Per-module CLIs** (each with subcommands for configuration, output selection, and threshold overrides):

| Command | Purpose |
|---------|---------|
| `stratum-out generate` | Standalone architecture extraction |
| `stratum-out discover` | Project structure discovery |
| `stratum-out diagram` | Architecture diagram generation |
| `stratum-unit generate` | Standalone unit test generation |
| `stratum-unit validate` | Test validation and scoring |
| `stratum-api generate` | Standalone API test generation |
| `stratum-api plan` | Test plan generation |
| `stratum-api diff` | Architecture diff and regression targeting |
| `stratum-api report` | Traceability report generation |
| `stratum-docs generate` | Standalone documentation generation |
| `stratum-docs serve` | Live documentation preview server |
| `stratum-docs analyze` | Run individual analyzers |
| `stratum-docs gate` | Run documentation quality gates |
| `stratum-docs render` | Render to specific format (MD, HTML, PDF) |

</details>

<details>
<summary><strong>Security hardening -- 17 issues resolved</strong></summary>

<br>

Full platform audit with all issues fixed:

**Critical:** Command injection in subprocess calls (&rarr; `shlex.split()` + `shell=False`), prompt injection via CLI arguments (&rarr; stdin-based prompt passing), silent tree-sitter degradation (&rarr; logging in all extractors)

**High:** Success rate accuracy (&rarr; real file counting), stage timeouts (&rarr; `ThreadPoolExecutor` wrapper), structured logging across pipeline/audit/CLI/config, audit threshold operator corrections

**Medium:** Temp file cleanup, path traversal protection, false positive reduction in security scanning, O(n&sup2;) &rarr; O(1) optimizations, cache mutation prevention, failed stage output cleanup

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Monorepo with shared extraction core. Strict layering: CLI &rarr; Engine &rarr; Core &larr; Util. Each gate is a silo -- independent logic, independent verdict, aggregated by the audit engine. Stateless pipeline -- zero database, pure data transformation. 11 configurable stages, each independently toggleable. Stage timeouts via ThreadPoolExecutor. GitHub Actions integration via action.yml.

</details>

```
22 commands · 253 modules · 59,793 lines · 3,296 tests, all passing
```

<br>

---

## 4. Castellan

**The keeper of the gates. Define agents in YAML. Compile, run, test, gate, orchestrate, and deploy them.**

> The problem: creating production AI agents required stitching together providers, tools, memory, quality gates, and orchestration patterns from scratch every time. No standard spec format, no compilation pipeline, no way to test agent behavior before deployment. Every agent framework is code-first and quality-last.

Castellan flips the model. Write a declarative YAML spec. Compile it through a 5-stage pipeline (parse, compose, optimize, validate, scan). Run it against Anthropic, OpenAI, or Google. Gate every output through automated quality checks. Orchestrate multi-agent systems. Export to Docker, Kubernetes, FastAPI, or Claude Code skills. Agents validated before they run, not after they fail.

### Compilation

Same 5-stage pipeline proven in Charlotte, adapted for agent specifications:

1. **Parse** -- YAML to Pydantic models with `!include` directives, `extends`/`mixins` inheritance, circular dependency detection
2. **Compose** -- Block precedence ordering, Jinja2 variable injection, constitution injection
3. **Optimize** -- Whitespace normalization, duplicate removal, token savings tracking
4. **Validate** -- Completeness checks, quality scoring, 10+ validation rules
5. **Scan** -- 18+ security patterns: injection, exfiltration, escalation, jailbreak, PII, destructive commands

### Execution engine

Async-first runtime implementing the **Observe &rarr; Think &rarr; Act &rarr; Validate** cycle:

- **3 LLM providers** -- Anthropic (Claude), OpenAI, Google (Gemini) with streaming, retry, and exponential backoff
- **3 tool types** -- Python functions (auto-extracted from type hints), API calls (httpx with schema validation), shell commands (subprocess with injection prevention)
- **Sliding window memory** -- Token-budgeted conversation history that never truncates the system prompt, with working memory slots and optional long-term file-based persistence
- **Quality gates at every step** -- 4 built-in evaluators plus custom evaluator registration. Pre-execution, per-step, and post-execution checkpoints with graduated 0.0-1.0 scoring
- **Constitutional enforcement** -- Boundary checks, value alignment scoring, quality heuristics
- **Budget tracking** -- Per-run cost enforcement with automatic termination on budget exceeded

### Multi-agent orchestration

| Pattern | How it works |
|---------|-------------|
| **Supervisor** | Master agent routes tasks to specialists via regex/keyword rules, synthesizes results |
| **Pipeline** | Sequential chain with stage transforms, stops on error |
| **Broadcast** | Parallel fan-out, aggregation strategies: concat, first, or vote |
| **Peer** | Turn-based collaboration with configurable max rounds |

Dynamic routing with priority ordering. Delegation depth limiting prevents infinite loops. Checkpoint/resume serializes full orchestration state for long-running tasks.

### Production deployment

**5 export formats** -- Python package (standalone), Docker (Dockerfile + compose), FastAPI server (/chat, /health, /trace, /reset, /stream), Claude Code skill, Kubernetes (Deployment, Service, ConfigMap, Secret, Kustomization, optional Helm charts)

**HTTP serve mode** -- Multi-session FastAPI app with SSE streaming, CORS, dashboard metrics, audit log

**Resilience** -- Circuit breaker (CLOSED/OPEN/HALF_OPEN), token bucket rate limiter, fallback provider chain, response caching (LRU + TTL, memory or file-based)

**Observability** -- OpenTelemetry span export, Prometheus metrics, 8 lifecycle event hooks, Rich tree trace visualization, interactive debugger with 6 breakpoint types

<details>
<summary><strong>Testing and evaluation</strong></summary>

<br>

**Behavioral test runner** -- 7 assertion types (contains, not_contains, regex_match, json_valid, max_turns, min_length, max_length), online and offline modes, tag filtering

**Evaluation framework** -- LLM-as-judge with rubric scoring (accuracy, helpfulness, safety, relevance), multi-agent comparative eval with Elo ratings and significance testing, regression detection with baseline management

**Interactive debugger** -- 6 breakpoint types (turn_start, turn_end, tool_call, tool_result, gate_eval, error), conditional breakpoints with expression evaluation, memory/message/tool/cost inspection

**Audit system** -- Append-only audit log with FIFO eviction, query by agent/tool/time range, permission policies (deny > allow > per-tool rate > global rate), JSON export for compliance

</details>

<details>
<summary><strong>Plugin ecosystem and spec composition</strong></summary>

<br>

**4 plugin types** -- ProviderPlugin, GatePlugin, ToolPlugin, ExporterPlugin with entry point discovery

**Agent versioning** -- Migration engine with built-in migrations (v1.0 &rarr; v1.1 &rarr; v1.2 &rarr; v2.0), semantic spec diffing

**Spec composition** -- Single-parent `extends:` inheritance with recursive resolution, `mixins:` additive composition, circular dependency detection, spec-aware deep merge

**Block library** -- 21 reusable YAML blocks across 6 categories (identity, tool, memory, orchestration, gate, constitution)

**Spec generator** -- 5 quick-start profiles (support, research, code, data, custom), smart defaults, auto-generated test cases, HTML intake form

</details>

<details>
<summary><strong>Full CLI reference (32 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `agent init` | Scaffold from template |
| `agent compile` | 5-stage compilation |
| `agent run` | Interactive or single-message execution |
| `agent validate` | Completeness checks |
| `agent scan` | Security scanning |
| `agent test` | Behavioral tests (online + offline) |
| `agent score` | Constitutional + gate scoring |
| `agent candor` | Transparency analysis |
| `agent trace` / `agent replay` | Execution trace and replay |
| `agent orchestrate` | Multi-agent orchestration |
| `agent serve` | FastAPI HTTP server |
| `agent export` | 5 deployment formats |
| `agent blocks` | Block library browser |
| `agent compose` | Inheritance/mixin resolution |
| `agent schema` | JSON Schema export |
| `agent diff` / `agent migrate` | Spec versioning and migration |
| `agent eval` | LLM-as-judge evaluation framework |
| `agent generate` | Spec generation from profiles |
| `agent dashboard` / `agent audit` | Runtime observability |
| `agent doctor` / `agent selftest` / `agent info` | Diagnostics |
| `agent templates` | List available agent templates |
| `agent plugin` | Plugin management |
| `agent version` | Show version information |
| `agent env list` / `env use` / `env diff` / `env promote` | Environment management |

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Strict four-layer separation: CLI &rarr; Engine &rarr; Core &larr; Util. Async-first runtime (asyncio). File-based persistence only (no database). Provider abstraction with Anthropic primary, OpenAI/Google secondary. YAML specs version-controllable. Graduated scoring (0.0-1.0) for quality gates. Adapter pattern for Designer-SDD/Charlotte/Stratum integration.

</details>

```
32 commands · 85 modules · 20,443 lines · 1,461 tests, all passing
```

<br>

---

## How They Connect

```
  Raw Idea                    YAML Spec                     Source Code                  Agent Spec
     |                           |                              |                            |
     v                           v                              v                            v
+--------------+         +---------------+             +---------------+           +------------------+
| Designer-SDD |         |   Charlotte   |             |    Stratum    |           | Castellan        |
|              |         |               |             |               |           |                  |
| Validate     |         | Compile       |             | Extract       |           | Compile          |
| Score        |         | Validate      |             | Generate      |           | Run / Orchestrate|
| Improve      |         | Test          |             | Gate          |           | Test / Gate      |
| Export       |         | Export        |             | Audit         |           | Export / Deploy   |
+------+-------+         +-------+-------+             +-------+-------+           +--------+---------+
       |                         |                             |                            |
       v                         v                             v                            v
  Scored Spec              Provider-Ready             Pass/Fail Verdict            Running Agent
  Package (7-11            Prompts, Skills,           + Tests + Docs              (CLI, HTTP, Docker,
  markdown files)          or Agent Projects          + Transparency               K8s, Skill)
```

Each tool is standalone. Together they cover the full arc:

- **Designer-SDD** defines *what* to build
- **Charlotte** handles *how to talk to AI*
- **Stratum** validates *what was built*
- **Castellan** operationalizes *running agents*

The platform is self-hosting. Designer-SDD specs defined every tool here. Charlotte compiles the prompts that drive Stratum's AI stages. Stratum validates the code all four tools generate. Castellan turns the specs and prompts into production agent systems.

---

## Platform Totals

<div align="center">

| | Designer-SDD | Charlotte | Stratum | Castellan | **Combined** |
|:---|:---:|:---:|:---:|:---:|:---:|
| **Source Lines** | 8,590 | 20,609 | 59,793 | 20,443 | **109,435** |
| **Python Modules** | 53 | 80 | 253 | 85 | **471** |
| **Tests (passing)** | 538 | 2,423 | 3,296 | 1,461 | **7,718** |
| **CLI Commands** | 16 | 30 | 22 | 32 | **100** |

</div>

<br>

<div align="center">

**Stack:** Python 3.10+ · Claude API · OpenAI API · Google Gemini API · Pydantic v2 · tree-sitter · Typer · Click · Rich · FastAPI · Jinja2 · asyncio · httpx · tiktoken · WeasyPrint · YAML/JSON

---

*Designed, built, and tested by Tim Wolfe.*

</div>

---

<div align="center">

## Let's Talk

I built a 109,000-line, 7,718-test platform that automates the parts of the SDLC most teams are still doing by hand — and I deploy it for clients. If your team is shipping AI-generated code without validated specs, compiled prompts, or quality gates that actually enforce standards, that's the gap I close.

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

</div>
