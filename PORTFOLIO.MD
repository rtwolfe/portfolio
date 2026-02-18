<div align="center">

# Tim Wolfe

### AI Infrastructure Architect | Autonomous SDLC · Agent Governance · LLM Platform Engineering

Los Altos, CA · [rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Tests](https://img.shields.io/badge/Tests-9%2C157_passing-brightgreen?style=flat-square)
![Lines](https://img.shields.io/badge/Source-134%2C326_lines-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

</div>

---

## About

I build compilers for the AI SDLC.

Not wrappers. Not prompt templates. Not demos. Compilers — tools with parse stages, composition engines, typed validation, quality gates, and deterministic output — that take unstructured inputs and produce production artifacts an LLM can execute or a team can ship.

I've been building this platform for four years. It covers the full arc of AI software development: from a raw idea to a validated spec, from a spec to compiled prompts and skills, from source code to test suites and architecture docs, from a YAML file to a deployed agent, and from a deployed agent to a security audit that decides whether it ships. Five tools. One pipeline. Nothing like it exists.

I deliver this as a service. Enterprise clients in finance, healthcare, and ecommerce hire me to run it against their codebases, their agents, and their teams' AI workflows — and they get back something that took months of manual work, in 48 hours, with quality gates that prove it's real.

Before AI, I spent 20+ years in enterprise operations leadership: two IPOs (**Quinstreet**, **Responsys**), four major acquisitions (**IBM**/DemandTec, **EMC**/Syncplicity, **Oracle**/Responsys, **Netmarble**/Kabam), and senior technical roles at **Salesforce**, **iHeartMedia**, and **Axway**. I know what production looks like. That's why this platform is built the way it is.

---

<div align="center">

[Stratum](#1-stratum) · [Designer-SDD](#2-designer-sdd) · [Charlotte](#3-charlotte) · [Castellan](#4-castellan) · [Aegis](#5-aegis) · [How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

## The Compiler Stack

Every tool solves a failure mode that I kept hitting — and that everyone else is still hitting:

| Tool | Input | Output | What it replaces |
|------|-------|--------|-----------------|
| **Stratum** | Any repo | Unit tests · API tests · C4 docs · SDD spec | Manual QA · manual documentation · manual reverse engineering |
| **Designer-SDD** | Anything unstructured | Scored, validated, LLM-executable spec package | Slack threads · ambiguous briefs · hallucinated requirements |
| **Charlotte** | YAML prompt spec | Compiled prompts · skills · agent projects | String concatenation · ad-hoc prompt files · untested prompts |
| **Castellan** | YAML agent spec | Running, tested, deployed AI agent | Framework stitching · code-first agent development |
| **Aegis** | Agent source directory | OWASP scorecard · SHIP/CONDITIONAL/BLOCK verdict | Shipping agents nobody audited |

The platform is self-hosting. Designer-SDD specs defined every tool here. Charlotte compiled the prompts that power Stratum's AI stages. Stratum validated the code all five generate. Aegis audits the security posture. Castellan turns specs into production agent systems. The stack eats its own output.

---

## 1. Stratum

**Point it at any repo. 48 hours later: unit tests, API tests, C4 architecture documentation, and a reverse-engineered spec that lets you rebuild the whole thing.**

> Teams are shipping AI-generated test suites without verifying the tests actually test anything. Hallucinated assertions. Mocked-out logic. Tests that pass whether or not the code works. And nobody is producing documentation that tells you how a system actually operates — let alone documentation structured so an AI can rebuild it.

Stratum is what I deliver to enterprise clients. A customer hands me a repo — any language, any framework — and Stratum runs advanced AST scanning with tree-sitter across 6 languages, extracts the complete architecture, and runs a six-stage automated pipeline. The outputs: unit tests with a self-healing validation loop, API tests across four layers, stunning C4 architecture documentation with Mermaid diagrams and a searchable HTML index, and a reverse-engineered SDD spec in Designer-SDD format — so the entire codebase can be handed to an LLM and rebuilt or modernized from scratch.

Seven independent quality gates decide whether any of it ships. Every gate produces its own verdict. The audit engine aggregates them. Nothing gets through that shouldn't. The gate architecture drives pass rates above 95% across production codebases.

This is not a documentation generator. It is not a test scaffold. It is a complete quality and intelligence pipeline for any existing codebase, delivered as a service.

### The four deliverables

**Unit tests — generated, validated, and self-healing.**
Generated from AST extraction using a 3-retry loop: generate → execute → fix. Tests that don't actually run are rejected outright. Every hallucinated import, nonexistent method, and mocked-out assertion gets caught and corrected before delivery. The fix log is included in the handoff — clients see exactly what the generator hallucinated and what it corrected.

**API tests — four layers deep, four frameworks.**

| Layer | What it validates |
|-------|-------------------|
| **Contract** | API surface matches the spec — methods, paths, status codes, content types |
| **Boundary** | Edge cases — empty payloads, max-length strings, type coercion, null handling |
| **Workflow** | Multi-step state transitions — create → read → update → delete sequences |
| **Regression** | Previously-found defects captured as permanent guards |

Output in pytest, jest, Postman/Newman, or REST Assured. The architecture diff system detects changes between extractions and generates targeted regression tests automatically.

**C4 architecture documentation — seven analyzers, three formats.**
Seven independent analyzers run against the extracted architecture: data flow tracing, decision archaeology (reconstructs *why* architectural decisions were made from code patterns and commit history), tribal knowledge capture, change impact prediction, code smell detection, health scoring, and onboarding guide generation. Output in Markdown, HTML with Mermaid diagrams and full search index, or PDF. The C4 diagrams are enterprise-grade — the kind that belong in a technical due diligence package.

**Reverse-engineered SDD spec — the capability nobody else has.**
Every Stratum run produces a complete specification of the scanned codebase in Designer-SDD format. This is not a README. It is a structured, scored, validated spec document that can be fed directly back into the compile pipeline — so that any legacy codebase becomes a first-class AI build target. Hand Stratum a system that's been running for ten years with no documentation. Get back everything needed to rebuild it, modernize it, or extend it with AI. This closes the loop between existing systems and the compiler stack.

### The seven quality gates

Seven independent modules. Seven independent verdicts. The audit engine aggregates them into a final pass or fail. Every gate is a silo — no shared state, no shared assumptions.

| Gate | What it enforces |
|------|-----------------|
| **Forge** | The Seven Rules — every generated test must: invoke the code under test, assert on outputs not inputs, not swallow exceptions, verify every mock, test error paths, fail when the code is wrong, and have no interdependence. All seven or it's rejected. |
| **Aegis** | Security scanning — 24 vulnerability types across 9 detectors. SQL injection, command injection, XSS, auth bypass, hardcoded secrets. Generates exploit tests that prove each vulnerability and remediation tests that verify each fix. |
| **Sentinel** | Mutation testing — 8 mutator types. Mutates the source code, runs the test suite against it, calculates whether the suite actually catches the mutations. Tests that don't catch mutations don't pass. |
| **Specter** | Flaky test detection — 9 pattern types: timing-dependent logic, random state, external service dependencies, concurrency issues, async timing. Auto-quarantine isolates unreliable tests before they poison CI. |
| **Arbiter** | Harvests quality rules from external linters — flake8, eslint, clippy, go vet — and maps them to test quality categories. No replication, just integration. |
| **CodeGate** | AI code quality gate — pure rule-based, zero LLM calls. 10-item production readiness checklist. 3-tier dependency verification: recognized, hallucination risk, unverifiable. Catches hallucinated imports before they reach the client. |
| **Intent** | Spec requirement verification — validates that the generated code actually implements the requirements from the original spec. Coverage percentage and gap analysis. Answers the question nobody else asks: did we build what was asked for? |

### Candor — the transparency layer

A transparency layer tracks every skip, failure, and limitation and reports it honestly. `CANDOR_TECHNICAL.md` for engineers. `CANDOR_EXECUTIVE.md` for stakeholders. Success rates are calculated from actual file counts, not estimates. If automation couldn't handle something, it says so — and says exactly why.

*"We identify bugs. We do NOT fix them."*

<details>
<summary><strong>CLI reference (22 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `stratum run` | Full pipeline — extract → generate → gate → audit |
| `stratum ship` | Full pipeline with client handoff documentation |
| `stratum extract` | Architecture extraction only |
| `stratum generate tests` | Unit + API test generation |
| `stratum generate docs` | Documentation generation |
| `stratum audit` | All seven quality gates |
| `stratum review` | CodeGate standalone review |
| `stratum verify` | Spec requirement verification |
| `stratum-out generate` | Standalone architecture extraction |
| `stratum-out discover` | Project structure discovery |
| `stratum-out diagram` | C4 diagram generation |
| `stratum-unit generate` | Unit test generation |
| `stratum-unit validate` | Test validation and scoring |
| `stratum-api generate` | API test generation |
| `stratum-api plan` | Test plan generation |
| `stratum-api diff` | Architecture diff and regression targeting |
| `stratum-api report` | Traceability report |
| `stratum-docs generate` | Documentation generation |
| `stratum-docs serve` | Live preview server |
| `stratum-docs analyze` | Individual analyzer runs |
| `stratum-docs gate` | Documentation quality gates |
| `stratum-docs render` | Render to MD, HTML, or PDF |

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Monorepo with shared extraction core. Strict layering: CLI → Engine → Core ← Util. Each quality gate is a silo — independent logic, independent verdict, aggregated by the audit engine. Stateless pipeline — zero database, pure data transformation. 11 configurable stages, each independently toggleable. Stage timeouts via ThreadPoolExecutor prevent runaway generation. GitHub Actions integration via action.yml. AST extraction via tree-sitter across Python, TypeScript, JavaScript, Java, Go, and Rust with framework auto-detection for Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, and Quarkus. Multi-provider LLM client with smart model routing — cheap models for extraction and summarization, best models for generation, mid-tier for validation retries.

</details>

```
31 commands · 312 modules · 73,357 lines · 4,226 tests, all passing
```

<br>

---

## 2. Designer-SDD

**A spec-driven development compiler. Throw anything at it — a brief, a transcript, a napkin sketch — and it outputs a scored, validated specification package that an LLM can build from.**

> AI agents hallucinate requirements. They build what they assume, not what was asked. The reason is almost always the same: nobody validated the spec before handing it off. Ambiguous requirements produce ambiguous software. The problem isn't the model. It's what you fed it.

Designer-SDD is a compiler for requirements. It takes any unstructured input — client brief, call transcript, raw notes, competitive analysis, a Slack thread — extracts a structured specification via Claude, then runs it through a gauntlet: domain-specific validation, dual-gate scoring across 39 weighted checks, iterative AI-driven refinement that re-scores after every pass, and round-trip verification that confirms every requirement in the spec appears in the rendered output.

The output is not a document you read. It is a scored, validated, GitHub-ready package of up to 11 files — structured specifically so that LLMs can build from it without asking clarifying questions. The spec is the source of truth. If it's not in the spec, it doesn't get built.

Designer-SDD specs defined every tool in this platform. It will spec anything: CLI tools, REST APIs, SaaS dashboards, data pipelines, mobile apps, Chrome extensions, AI agents. Whatever the domain, whatever the complexity, one intake produces a build-ready package.

And because Stratum outputs SDD format, any existing codebase can be fed back through Designer-SDD — turning a reverse-engineering scan into a forward-facing build plan. Legacy systems become first-class AI build targets.

### The compilation process

**Multiple entry points.** Raw text intake, interactive brainstorming with Claude, 3-stage web-powered market research, browser-based HTML form, or five pre-built templates. However the idea arrives, Designer-SDD can receive it.

**Dual-gate scoring.** Two independent scoring systems on every spec:

| Gate | What it measures | Checks | Threshold |
|------|-----------------|--------|-----------|
| **Quality** | Is this spec complete and well-structured? | 31 weighted checks across 7 sections | 70% |
| **Buildability** | Can a developer or AI agent actually build from this without asking questions? | 8 checks: ambiguity detection, dependency completeness, acceptance verifiability, tech completeness | 60% |

Both gates must pass. A beautifully structured spec that can't be built is not a spec — it's a roadmap to the wrong place.

**Domain-aware validation.** CLI projects must declare exit codes. APIs must declare auth schemes. Web apps must declare error handling. Mobile apps must declare offline behavior. The validator knows what you're building and enforces rules that match — not generic rules that apply to everything and mean nothing.

**Iterative refinement.** Score the spec. Send targeted improvement instructions to Claude. Re-score. Repeat. Up to three automated passes. The spec gets measurably better each round — not just longer.

**Tier-gated export.** Small projects: 7 files. Medium: 9. Large: 11. Every tier includes CONSTITUTION.md, SPEC.md, PLAN.md, TASKS.md, HANDOFF.md, README.md, and source JSON. Larger tiers add DATA_MODEL.md, QUICKSTART.md, and ARCHITECTURE.md. HANDOFF.md is the single most important file — it contains everything an implementing agent needs to start building without cross-referencing anything else.

**Round-trip verification.** After export, the system verifies that every requirement and task in the source spec appears in the rendered markdown. Drift between spec and output is caught before delivery.

**10 hard gate rules.** Every functional requirement must have a description and priority. User stories must reference requirements. Assumptions must have mitigation strategies. Open questions must have resolution status. Risks must have mitigation. Success criteria must be measurable. Definition of Done items must be actionable. Tech choices must be justified. Task breakdown must cover all requirements. No unresolved placeholders — no TODO, no TBD, no FIXME. Pass, conditional pass, or fail. No ambiguity.

<details>
<summary><strong>Full CLI reference (16 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `designer intake` | Extract spec from unstructured text |
| `designer create` | Interactive brainstorming with Claude |
| `designer discover` | 3-stage market research pipeline |
| `designer form` | Launch browser-based HTML intake form |
| `designer validate` | Domain-specific completeness check |
| `designer score` | Dual-gate scoring (quality + buildability) |
| `designer improve` | Auto-improve via Claude refinement loop |
| `designer ingest` | Full pipeline (validate → score → export) |
| `designer export` | Render tier-gated markdown package |
| `designer diff` | Field-by-field spec comparison with score deltas |
| `designer research` | Answer open questions via Claude |
| `designer verify` | Post-export round-trip integrity check |
| `designer template list` | Browse pre-built templates |
| `designer template preview` | Preview template contents |
| `designer template use` | Scaffold from template |
| `designer init` | Initialize project configuration |

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Strict four-layer separation: CLI → Engine → Core ← Util. Stateless — zero database, zero persistence. Every operation is a pure data transformation. All Claude calls route through a single API wrapper with exponential backoff retry, fully mocked in tests. Path traversal protection at the security boundary. Token budgeting tracks API spend across sessions. Configuration loads from four layers: environment → project YAML → global YAML → built-in defaults.

</details>

```
16 commands · 53 modules · 8,590 lines · 554 tests, all passing
```

<br>

---

## 3. Charlotte

**A prompt and skills compiler with a typed block system. Not a template engine. A compiler — with a parse stage, a composition engine, type checking, conflict detection, security scanning, and a test framework.**

> Prompt engineering is still string concatenation. Copy-paste a system prompt. Inject some variables. Ship it. No version control, no type checking, no security scanning, no regression testing. Teams are shipping prompts the same way they shipped code in 1995. And then they're surprised when their AI behaves differently in production.

Charlotte is a five-stage deterministic compiler that treats prompts as first-class software artifacts. It parses typed YAML specifications, composes them through a 94-block library with conflict detection and dependency resolution, runs eight automatic optimization passes, validates token budgets against 26 model context windows, and renders provider-specific output for OpenAI, Anthropic, and Google Gemini.

The block compiler is what makes Charlotte different from everything else in this space. Ninety-four blocks across 17 typed categories. Each type has defined precedence in the composition order, singleton enforcement where appropriate, conflict detection against incompatible block types, and dependency resolution for blocks that require others. Compile prompts. Compile skills. Compile multi-agent projects for five major frameworks. Charlotte is years ahead of where the rest of the industry is on this problem.

### The compilation pipeline

```
YAML Spec → Parse → Compose → Optimize → Validate → Render → Provider-Ready Output
```

1. **Parse** — Resolve block references from the 94-block library. Validate against Pydantic v2 schemas. Catch malformed specs before they cost tokens.
2. **Compose** — Assemble blocks in strict type-precedence order across 17 types. Detect conflicts. Enforce singletons. Resolve dependencies. Inject typed variables.
3. **Optimize** — Eight automatic passes: deduplication, adjacent text merging, empty block stripping, whitespace normalization, system block reordering, example compression, token budget optimization, provider-specific hints.
4. **Validate** — Conflict detection, token budgeting with per-block breakdown against each target model, completeness checks, composition rule enforcement.
5. **Render** — Provider-specific output: OpenAI messages array, Anthropic system parameter, Google Gemini system_instruction, or generic text.

### The block compiler

**94 blocks across 17 typed categories:** system, task, few-shot, chain-of-thought, tool use, RAG, agent, evaluation, extraction, meta, conversational, safety, routing, memory, retrieval, guardrail, planning. Blocks are pure YAML data — not embedded code, not string templates. The library is extensible without touching source.

**The type system enforces:** composition precedence (each type has a defined position in the assembled output), singleton rules (system blocks can only appear once), conflict detection (incompatible block type combinations are rejected at compile time), and dependency resolution (blocks that require other blocks get them automatically).

This is what a prompt compiler actually looks like. Everything else is a template stitcher.

### Skills compilation

Charlotte compiles Claude Code Skills directly from prompt specs — formatted, validated, ready to deploy. Skills are a first-class export target alongside the standard provider formats.

### Security scanning at compile time

54 checks across 21 categories run against every prompt before it ships: injection, exfiltration, model manipulation, context poisoning, privilege escalation, compliance (GDPR/HIPAA/PCI-DSS), supply chain, bias and fairness, MCP tool poisoning, and more. Security is part of compilation, not an afterthought.

### The test framework

30 assertion types: exact match, regex, JSON schema validation, LLM-as-judge, cosine similarity, sentiment analysis, language detection, PII detection, latency thresholds, and composite assertions. Parallel cross-model execution. Evaluation history with regression drift detection. You can test a prompt change against every model you care about, in parallel, before it deploys.

### Multi-agent compiler

Takes compiled prompts and generates complete, runnable projects for five major frameworks: CrewAI, LangGraph, AutoGen, OpenAI Agents SDK, and Google A2A protocol. Every export includes pyproject.toml, README, and all source files. A shared extraction layer means adding a new framework is one renderer and its templates — the abstraction holds.

### 21 export formats

Text, JSON, YAML, API payload, MCP definition, LangChain template, HTML report, README, Claude Code Skill, MCP server, CrewAI, LangGraph, AutoGen, OpenAI Agents, A2A Agent Card — each in single-prompt and workflow variants.

<details>
<summary><strong>Security scanner — 21 categories in full</strong></summary>

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
<summary><strong>Workflow engine, versioning, environments, and CI/CD</strong></summary>

<br>

**Multi-prompt workflows** — Chain multiple specs with typed data flow (`{{steps.X.output.field}}`). Topological execution ordering via Kahn's algorithm. Conditional step execution via Jinja2. Cross-step schema validation. End-to-end workflow testing.

**Content-addressed versioning** — JSON snapshots with semantic block-aware diffing. Track added, removed, and modified blocks across versions. Not file diffs — block diffs.

**Environment management** — Dev/staging/production environments with variable overrides, promotion gates (test pass rate, score threshold, manual approval), and environment diffing.

**CI/CD** — Four GitHub Actions workflow templates: validate-on-PR, test-on-push, scheduled regression, environment promotion.

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

28 Pydantic v2 models enforce every data boundary. Four global registries (block types, providers, exporters, assertions) make the system pluggable at every layer. Three-tier prompt classification — single-turn, multi-phase, agent-orchestrating — with automatic detection. The multi-agent compiler uses a shared extraction layer so all five framework renderers consume the same AgentTeam abstraction. Token budgeting across 26 registered models from 8K to 2M context windows.

</details>

```
30 commands · 80 modules · 20,609 lines · 94 blocks · 2,592 tests, all passing
```

<br>

---

## 4. Castellan

**An agent compiler. Write a YAML spec. Castellan compiles, runs, tests, gates, and deploys a production AI agent.**

> Every AI agent framework is code-first and quality-last. You stitch together providers, tools, memory, and orchestration patterns from scratch. You write the agent, then figure out how to test it. You deploy it, then figure out how to govern it. Castellan inverts this. The spec is the artifact. The agent is the output.

Castellan is a compiler for AI agents. Write a declarative YAML spec. Compile it through a five-stage pipeline. Run it against Anthropic, OpenAI, or Google. Gate every output through automated quality checks. Orchestrate multi-agent systems. Export to Docker, Kubernetes, FastAPI, or Claude Code Skills. Constitutional governance is baked in — not bolted on — and enforcement is deterministic, not probabilistic.

For enterprise clients, Castellan is how agent specs turn into deployed, observable, governed production systems.

### Compilation

Five-stage pipeline — the same architecture proven in Charlotte, adapted for agents:

1. **Parse** — YAML to Pydantic models with `!include` directives, `extends`/`mixins` inheritance, and circular dependency detection
2. **Compose** — Block precedence ordering, Jinja2 variable injection, constitution injection
3. **Optimize** — Whitespace normalization, duplicate removal, token savings tracking
4. **Validate** — Completeness checks, quality scoring, 10+ validation rules
5. **Scan** — 18+ security patterns: injection, exfiltration, privilege escalation, jailbreak, PII, destructive commands

### Constitutional enforcement

Every compiled agent carries a constitution — core values, technical boundaries, quality standards. The ConstitutionEnforcer runs deterministic pattern-based checks against every output: boundary violations (destructive shell commands, forbidden APIs, credential exposure), value alignment failures, and quality standard violations. This is not an LLM guardrail. It is compiled governance — reproducible, fast, and provably correct.

### Execution engine

Async-first runtime implementing **Observe → Think → Act → Validate:**

- **3 LLM providers** — Anthropic (Claude), OpenAI, Google (Gemini) with streaming, retry, and exponential backoff
- **3 tool types** — Python functions (auto-extracted from type hints), API calls (httpx with schema validation), shell commands (subprocess with injection prevention)
- **Sliding window memory** — Token-budgeted history that never truncates the system prompt, with working memory slots and optional long-term persistence
- **Quality gates at every step** — Pre-execution, per-step, and post-execution checkpoints with graduated 0.0–1.0 scoring
- **Budget tracking** — Per-run cost enforcement with automatic termination on budget exceeded

### Multi-agent orchestration

| Pattern | How it works |
|---------|-------------|
| **Supervisor** | Master agent routes tasks to specialists via configurable rules, synthesizes results |
| **Pipeline** | Sequential chain with stage transforms, stops on error |
| **Broadcast** | Parallel fan-out, aggregation strategies: concat, first, or vote |
| **Peer** | Turn-based collaboration with configurable max rounds |

Delegation depth limiting prevents infinite loops. Checkpoint/resume serializes full orchestration state for long-running tasks.

### Production deployment

Five export formats: Python package, Docker (Dockerfile + compose), FastAPI server (/chat, /health, /trace, /reset, /stream), Claude Code Skill, Kubernetes (Deployment, Service, ConfigMap, Secret, Kustomization, optional Helm). Circuit breaker (CLOSED/OPEN/HALF_OPEN), token bucket rate limiter, fallback provider chain, LRU+TTL response cache. OpenTelemetry span export, Prometheus metrics, 8 lifecycle event hooks, Rich tree trace visualization, interactive debugger with 6 breakpoint types.

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
| `agent templates` | Available templates |
| `agent plugin` | Plugin management |
| `agent env list` / `env use` / `env diff` / `env promote` | Environment management |

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Strict four-layer separation: CLI → Engine → Core ← Util. Async-first runtime via asyncio. File-based persistence — no database. Provider abstraction with Anthropic primary, OpenAI/Google secondary. YAML specs are version-controllable artifacts. Graduated scoring (0.0–1.0) for quality gates. Adapter pattern enables Designer-SDD/Charlotte/Stratum integration. 4 plugin types (ProviderPlugin, GatePlugin, ToolPlugin, ExporterPlugin) with entry point discovery. 21 reusable YAML blocks across 6 categories (identity, tool, memory, orchestration, gate, constitution).

</details>

```
32 commands · 85 modules · 20,443 lines · 1,486 tests, all passing
```

<br>

---

## 5. Aegis

**Pre-deployment security audit for AI agents. OWASP Top 10 for Agentic Applications. One intake. One pipeline. SHIP, CONDITIONAL, or BLOCK.**

> AI agents are shipping to production without anyone checking whether they're vulnerable to prompt injection, credential leakage, excessive agency, memory poisoning, or multi-agent trust exploitation. Quality gates check that code works. Nobody checks whether it's secure. Aegis is the gate that nothing ships without.

Aegis audits AI agents against the OWASP Top 10 for Agentic Applications before they deploy. Point it at an agent's source directory. It runs a five-stage DAG: intake extraction builds an Agent Architecture Profile from prompts, tools, credentials, memory systems, delegations, and constraints. Three audit layers run in parallel — prompt, behavior, and code. Cross-layer graph analysis finds structural vulnerabilities that are invisible to any single layer. A scoring engine maps every finding to ASI01–ASI10 with 122 check-ID mappings. Final verdict: **SHIP**, **CONDITIONAL**, or **BLOCK**.

The three audit layers integrate the entire platform: Charlotte's 54-check prompt scanner, Castellan's 22-pattern behavioral scanner and constitutional gate, Stratum's 11-detector code analysis with exploit and remediation test generation. Built-in fallback checks cover the critical surface area when external tools aren't available. Six cross-layer graph analyzers examine what no single layer can see: tool chaining risk, privilege scope density, memory poisoning paths, delegation chains, cascade failure risk, kill switch presence.

For clients delivering AI agents, Aegis is the pre-deployment gate. Every finding includes file, line, evidence, OWASP category, severity, and remediation guidance. The verdict is not a score — it is a decision.

### OWASP ASI coverage

| Category | What it covers |
|----------|---------------|
| **ASI01** Prompt Injection | Direct/indirect injection, jailbreak, context overflow |
| **ASI02** Insecure Tool Implementation | SQL injection, command injection, path traversal, SSRF, insecure deserialization |
| **ASI03** Sensitive Information Disclosure | Hardcoded secrets, credential leakage, system prompt exposure |
| **ASI04** Insecure Output Handling | Unsanitized output, XSS, format manipulation |
| **ASI05** Excessive Agency | Privilege escalation, over-permissioned tools, eval/exec, tool chaining |
| **ASI06** Memory Poisoning | Unsanitized memory writes, poisoning paths, RAG contamination |
| **ASI07** Multi-Agent Trust Exploitation | Unscoped delegation, credential inheritance, trust boundary violations |
| **ASI08** Uncontrolled Autonomy | Missing kill switch, no behavioral bounds, cascade failure risk |
| **ASI09** Misinformation and Hallucination | Missing confidence scoring, hallucination risk |
| **ASI10** Unbounded Consumption | No timeout, unbounded loops, missing resource limits |

### Verdicts

| Verdict | Condition |
|---------|-----------|
| **BLOCK** | ≥2 categories FAIL, or any critical finding in ASI01 / ASI03 / ASI05 |
| **CONDITIONAL** | 1 category FAIL, or any critical finding outside blocked categories |
| **SHIP** | 0 FAIL, ≤2 WARN, 0 critical findings |

ASI01 (Prompt Injection), ASI03 (Sensitive Information Disclosure), and ASI05 (Excessive Agency) are gate-blocking. One critical finding in any of them triggers BLOCK regardless of everything else. Some vulnerabilities are non-negotiable.

<details>
<summary><strong>CLI reference (9 commands)</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `aegis audit` | Full 5-stage pipeline with all deliverables |
| `aegis scan` | Prompt + behavior only |
| `aegis audit-prompts` | Prompt audit layer only |
| `aegis audit-behavior` | Behavior audit layer only |
| `aegis audit-code` | Code audit layer only |
| `aegis scorecard` | Display scorecard from previous audit |
| `aegis gate` | CI gate — exit 0 if verdict meets threshold |
| `aegis diff` | Compare two audits, show scorecard delta |
| `aegis estimate` | Cost and timeline estimate before running |

</details>

<details>
<summary><strong>Deliverables (6 renderers)</strong></summary>

<br>

Every audit produces six deliverables: executive summary (one-page non-technical ship/no-ship brief), technical report (findings by OWASP category with file, line, evidence, and remediation), OWASP scorecard (machine-readable JSON), test suite (exploit tests that prove each vulnerability, remediation tests that verify each fix), Candor report (what wasn't tested and exactly why — for compliance officers and regulators), and handoff package (prioritized remediation plan).

```
aegis-output/
  scorecard.json         verdict.json          findings.json
  executive_summary.md   technical_report.md   candor_report.md
  test_suite/            handoff/              .aegis/
```

</details>

<details>
<summary><strong>Architecture</strong></summary>

<br>

Five-stage DAG with parallel audit barrier via ThreadPoolExecutor. Six extractors build the Agent Architecture Profile from source across all file formats — .yaml, .py, .ts, .java, .go, .json, .md, .txt. Framework heuristics detect LangChain, CrewAI, and OpenAI Agents SDK. Three audit layers each try the external platform tool, then fall back to 26 built-in checks. Six cross-layer graph analyzers run post-barrier: tool chaining, privilege scope density, kill switch presence, memory poisoning paths, delegation chain analysis, cascade failure simulation. Cascade analysis builds a failure dependency graph, simulates per-component failure, and scores blast radius — catching failure propagation patterns that no single-layer audit can see. Pydantic v2 models throughout. The Scorecard is the single data structure: every stage writes to it, deliverables only read from it. 122 check-ID to OWASP-category mappings in a maintained lookup table.

</details>

```
9 commands · 56 modules · 11,327 lines · 299 tests, all passing
```

<br>

---

## How They Connect

```
Raw Idea          YAML Spec          Any Repo           Agent Spec        Agent Directory
    |                  |                  |                  |                  |
    v                  v                  v                  v                  v
+----------+    +----------+    +----------+    +----------+    +----------+
|Designer- |    | Charlotte|    |  Stratum |    | Castellan|    |   Aegis  |
|SDD       |    |          |    |          |    |          |    |          |
|          |    | Compile  |    | AST Scan |    | Compile  |    | Intake   |
| Compile  |    | Validate |    | Unit     |    | Run      |    | 3 Audits |
| Score    |    | Test     |    | API      |    | Test     |    | Cross-   |
| Export   |    | Export   |    | C4 Docs  |    | Gate     |    | Layer    |
|          |    |          |    | SDD Spec |    | Export   |    | Score    |
+----------+    +----------+    +----+-----+    +----------+    +----------+
    |                |               |               |               |
    v                v               v               v               v
Scored Spec    Provider-Ready   Pass/Fail +     Running Agent   SHIP /
Package        Prompts, Skills  Tests + Docs +  (CLI, HTTP,     CONDITIONAL /
(7-11 files)   Agent Projects   SDD Spec ──►    Docker, K8s,    BLOCK +
                                Designer-SDD    Skill)          OWASP Scorecard
```

**The loop that makes this a platform:** Stratum's SDD output feeds directly into Designer-SDD. Scan any existing codebase, extract the full architecture, produce a structured spec, compile from the spec. Legacy systems become AI build targets. The compiler stack eats existing software.

- **Stratum** scans what exists and produces the spec to rebuild it
- **Designer-SDD** compiles what to build from anything
- **Charlotte** compiles how to talk to AI — prompts, skills, and blocks
- **Castellan** compiles and deploys the agents that do the work
- **Aegis** audits everything before it ships

---

## Platform Totals

<div align="center">

| | Designer-SDD | Charlotte | Stratum | Castellan | Aegis | **Combined** |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|
| **Source Lines** | 8,590 | 20,609 | 73,357 | 20,443 | 11,327 | **134,326** |
| **Python Modules** | 53 | 80 | 312 | 85 | 56 | **586** |
| **Tests (passing)** | 554 | 2,592 | 4,226 | 1,486 | 299 | **9,157** |
| **CLI Commands** | 16 | 30 | 31 | 32 | 9 | **118** |

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

I built a 134,000-line, 9,157-test compiler stack for the AI SDLC — and I deliver it as a service. If your organization is shipping AI-generated code without validated specs, compiled prompts, quality gates, or security audits that actually enforce standards, that's the gap I close.

Nobody else is doing this.

**Tim Wolfe** · Los Altos, CA

[rtwolfe@gmail.com](mailto:rtwolfe@gmail.com) · 650-390-5003 · [LinkedIn](https://linkedin.com/in/timwolfe) · [Telegram](https://t.me/timwolfe)

</div>
