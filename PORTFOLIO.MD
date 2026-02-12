# Portfolio: AI Development Platform

Solo-built platform — three tools covering the arc from idea to verified software. Define what to build, compile the prompts that talk to AI, then validate what got built. 76,103 lines of Python. 5,198 tests. All passing.

---

## Designer-SDD — Spec-Driven Development CLI

Built because specs kept arriving as Slack threads and call transcripts, and teams kept building the wrong thing from ambiguous requirements.

Takes unstructured input — a client brief, a meeting transcript, raw notes — and produces a scored, validated, exportable documentation package: constitution, spec, plan, task breakdown, handoff notes, and README. One source of truth in, GitHub-ready docs out.

**What it does:**

- Extracts structured JSON specs from raw text via Claude API
- Interactive multi-turn brainstorming with auto-detection of valid spec output in Claude responses
- 3-stage market research pipeline using web search (quick scan → deep dive → handoff to spec builder)
- Validation with domain-aware rules — CLI projects must declare exit codes, APIs must declare auth schemes, mobile must declare offline behavior
- Dual-gate scoring: quality gate (28 weighted checks across 7 sections) + buildability gate (8 checks: verifiability, dependency completeness, ambiguity, phase continuity, tech completeness, test strategy, actionability, environment)
- Iterative refinement loop — two modes: generate improvement instructions, or let Claude auto-fix in up to 3 iterations with re-scoring after each pass
- Tier-gated export: small specs produce 7 files, medium specs 9, large specs 11
- Round-trip verification confirms every requirement and task in the spec appears in the rendered output
- 5 domain templates (CLI tool, REST API, SaaS dashboard, library, Chrome extension) with customizable placeholders and merge support
- Deterministic HTML dashboard (no API needed) + premium HTML export via Claude
- Field-by-field spec diffing with quality score delta between versions

**Architecture:** Strict four-layer separation (CLI → Engine → Core ← Util). Stateless — zero database, zero persistence. Every operation is a pure data transformation. All Claude calls go through a single API wrapper with exponential backoff retry, fully mocked in tests.

**17 commands. 6,961 lines of code. 537 tests, all passing.**

---

## Charlotte — Prompt & Claude Code Skill Compiler

Built because prompt engineering was ad-hoc string concatenation — no type checking, no version control, no way to test one prompt change against regression.

Write a YAML spec declaring which blocks you need, bind your variables, and Charlotte compiles it through four deterministic stages into provider-ready output for OpenAI, Anthropic, or Google Gemini — or into a Claude Code Skill package with YAML frontmatter, trigger extraction, structured sections, and progressive disclosure. Token budgets enforced. Conflicts caught at compile time. Security scanned. Testable with assertions.

**What it does:**

- 4-stage compilation pipeline: Parse → Compose → Validate → Render
- 94 built-in blocks across 17 types (system, task, few-shot, chain-of-thought, tool-use, RAG, agent, evaluation, extraction, safety, routing, memory, retrieval, guardrail, planning, conversational, meta)
- Deterministic type-precedence composition — blocks assemble in fixed order with explicit override support
- Provider-specific renderers: OpenAI messages array, Anthropic system parameter + messages, Google Gemini system_instruction, generic text
- Per-block, per-model token budgeting across 26 registered models (8K–2M context windows), with 80% threshold warnings and completion budget estimation
- Composition rules as data — blocks declare compatibility, incompatibility, singletons, and dependencies, all enforced at compile time
- Jinja2 variable injection with 6 typed slots (string, number, boolean, array, object, document)
- 8-check security scanner: prompt injection, PII exposure, API key leaks, jailbreak patterns, safety block validation, tool-use permissions, information disclosure, severity filtering
- Test runner with 6 assertion types (exact match, contains, regex, JSON schema, LLM-as-judge, custom Python evaluators) with parallel execution, response caching, and cross-model matrix testing
- Multi-prompt workflow chaining: DAG execution via topological sort, cross-step schema validation, typed data flow between steps, per-step assertions, directory package export
- Content-addressed versioning with semantic block-aware diffing
- Claude Code Skill compiler: maps block types to structured sections (system → overview, task → workflow, few-shot → quick reference, safety → critical rules, tool-use → tools), extracts triggers and anti-triggers from routing blocks into YAML frontmatter, parses I/O pairs into tables, and auto-splits to a `references/` directory when content exceeds 500 lines — output is a ready-to-install skill package
- 8 additional export formats: text, JSON, YAML, API payload (curl + Python snippets), MCP server definition, LangChain template, HTML report, README
- Post-compile linter + file watcher with debounced auto-recompile
- LLM-guided prompt optimization with iterative variable refinement
- CI command: validate → compile → scan → lint → test in one pass

**Architecture:** 25 Pydantic v2 models. Blocks are pure YAML data validated against schemas, not embedded code. Custom block directories supported. Four global registries (block types, providers, exporters, assertions). Three-tier prompt classification (single-turn, multi-phase, agent-orchestrating) with automatic tier detection and minimum-length enforcement.

**26 commands. 13,272 lines of code. 94 blocks. 1,615 tests, all passing.**

---

## Stratum — Automated Quality Pipeline

Built because teams were shipping Claude-generated test suites without checking whether the tests actually tested anything — hallucinated assertions, mocked-out logic, tests that pass no matter what, all going straight to CI.

Point it at source code. It extracts the full architecture using Claude and tree-sitter, generates unit tests and API tests across multiple frameworks, produces documentation in multiple formats, then runs everything through six independent quality gates. Each gate produces its own verdict. The audit engine aggregates them into a final pass or fail.

**What it does:**

*Extraction:*
- Claude + tree-sitter static analysis across 6 languages (Python, TypeScript, JavaScript, Java, Go, Rust) with regex fallback
- Outputs architecture as structured JSON: endpoints, schemas, data models, workflows, source traces
- Call chain tracing, component clustering, cross-cutting concern detection, route pattern recognition
- Auto-detects web frameworks (Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, Quarkus)
- Iterative refinement loop (up to 10 passes), dry-run mode for token estimation

*Unit Test Generation:*
- Tests generated from extracted source via Claude subprocess with prompt-via-stdin security
- pytest and jest output, validation loop with up to 3 retry attempts
- 86.68% test coverage on the generator itself

*API Test Generation:*
- 4 test layers: Contract (endpoint signatures), Boundary (edge cases), Workflow (multi-step state transitions), Regression (known bugs)
- 4 output frameworks: pytest, jest, Postman/Newman, RestAssured
- Architecture-driven test planning with fixture generation and traceability reports

*Documentation Generation:*
- 7 analyzers: data flow, decision archaeology, tribal knowledge, change impact, code smell detection, health scoring, onboarding guide generation
- 7 quality gates on the docs themselves: accuracy, coverage, completeness, freshness, readability (Flesch-Kincaid), broken links, aggregated verdict
- 3 output formats: Markdown, HTML (Mermaid diagrams, search index, responsive layout), PDF
- 90.86% test coverage on the generator itself

*Quality Gates (6 independent modules):*
- **Forge** — Seven Rules hard gate. Every generated test must: (A) invoke the code under test, (B) assert on outputs not inputs, (C) not swallow exceptions, (D) verify every mock, (E) test error paths, (F) fail if the code is wrong, (G) have no interdependence. All seven or rejected. Validates Python and JavaScript.
- **Aegis** — Security scanning with 9 detectors (SQL injection, command injection, NoSQL injection, XSS, authentication, authorization, data exposure, hardcoded secrets, configuration flaws) plus exploit test generation, remediation test generation, and fuzz testing.
- **Sentinel** — Mutation testing with 8 mutator types. Mutates source, runs tests, calculates whether the test suite actually catches the mutations.
- **Specter** — Flaky test detection across 9 pattern types (timing, shared state, order dependency, non-determinism, resource leaks, network, concurrency, environment, async). Parses output from pytest, jest, mocha, and vitest. Auto-quarantine for confirmed flaky tests.
- **Arbiter** — Harvests quality rules from linters (pytest, jest, mocha, cargo/clippy, go vet, cppcheck, eslint) and maps them to test quality categories. Results cached with 7-day TTL.
- **CodeGate** — AI-powered production readiness review: 10-item checklist, 3-tier dependency verification (recognized / hallucination-risk / unverifiable), explicit reasoning enforcement. Verdict: pass, conditional pass, or fail. Supports 6 languages.

*Transparency:*
- **Candor** — Tracks every extraction skip, generation failure, validation error, and gate bypass across the entire pipeline. No silent failures.

**Architecture:** Monorepo with shared extraction core. Each gate is a silo — independent logic, independent verdict, aggregated by the audit engine into a final pass/fail. Pipeline orchestrator with 11 configurable stages. All gates toggleable. Audit thresholds configurable per gate. GitHub Actions integration for CI/CD.

**5 CLI entry points. 6 commands. 233 modules. 55,870 lines of code. 3,046 tests, all passing.**

---

## How They Fit Together

**Designer-SDD** defines what to build — raw idea in, scored and validated specification package out.

**Charlotte** handles how to talk to AI — compiles prompt specs into tested, provider-ready artifacts or Claude Code Skills.

**Stratum** validates what was built — extracts architecture from finished code, generates tests and docs, runs six quality gates, produces a pass/fail audit verdict.

Each tool is standalone. Together they cover the full arc from idea to verified software.

---

## Platform Totals

| | Designer-SDD | Charlotte | Stratum | **Combined** |
|---|---|---|---|---|
| Source Lines | 6,961 | 13,272 | 55,870 | **76,103** |
| Python Modules | 45 | 55 | 233 | **333** |
| Tests (passing) | 537 | 1,615 | 3,046 | **5,198** |
| Commands | 17 | 26 | 6 | **49** |

**Stack:** Python 3.10+, CLI-first (Typer/Click), Claude API, Pydantic v2 / TypedDict validation, tree-sitter, strict architectural layering, YAML/JSON configuration, Rich terminal output.
