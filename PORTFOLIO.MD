<div align="center">

# AI Development Platform

**Solo-built. Three tools. Idea to verified software.**

<br>

76,103 lines of Python · 333 modules · 5,198 tests · All passing

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Tests](https://img.shields.io/badge/Tests-5%2C198_passing-brightgreen?style=flat-square)
![Lines](https://img.shields.io/badge/Source-76%2C103_lines-blue?style=flat-square)
![Modules](https://img.shields.io/badge/Modules-333-purple?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

</div>

---

<div align="center">

[Designer-SDD](#designer-sdd--spec-driven-development-cli) · [Charlotte](#charlotte--prompt--claude-code-skill-compiler) · [Stratum](#stratum--automated-quality-pipeline) · [How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

One person, three tools, one platform. Designer-SDD produces the specs that define what to build. Charlotte compiles the prompts that power the AI stages. Stratum validates what got built and decides whether it ships. Each tool is standalone. Each one also feeds the others. The strict layering, the stateless architecture, the investment in test coverage -- all deliberate choices for a codebase that has to stay maintainable with a single developer.

<br>

## Designer-SDD -- Spec-Driven Development CLI

> Built because specs kept arriving as Slack threads and call transcripts, and teams kept building the wrong thing from ambiguous requirements.

Takes unstructured input -- a client brief, a meeting transcript, raw notes -- and produces a scored, validated, exportable documentation package: constitution, spec, plan, task breakdown, handoff notes, and README. One source of truth in, GitHub-ready docs out. Designer-SDD specs are used internally to define every tool in this platform, including Stratum and Charlotte themselves.

<details>
<summary><strong>What it does</strong></summary>

<br>

- Extracts structured JSON specs from raw text via Claude API
- Interactive multi-turn brainstorming with auto-detection of valid spec output in Claude responses
- 3-stage market research pipeline using web search (quick scan --> deep dive --> handoff to spec builder)
- Validation with domain-aware rules -- CLI projects must declare exit codes, APIs must declare auth schemes, mobile must declare offline behavior
- Dual-gate scoring: quality gate (28 weighted checks across 7 sections) + buildability gate (8 checks: verifiability, dependency completeness, ambiguity, phase continuity, tech completeness, test strategy, actionability, environment)
- Iterative refinement loop -- two modes: generate improvement instructions, or let Claude auto-fix in up to 3 iterations with re-scoring after each pass
- Tier-gated export: small specs produce 7 files, medium specs 9, large specs 11
- Round-trip verification confirms every requirement and task in the spec appears in the rendered output
- 5 domain templates (CLI tool, REST API, SaaS dashboard, library, Chrome extension) with customizable placeholders and merge support
- Deterministic HTML dashboard (no API needed) + premium HTML export via Claude
- Field-by-field spec diffing with quality score delta between versions

</details>

**Architecture:** Strict four-layer separation (CLI --> Engine --> Core <-- Util). Stateless -- zero database, zero persistence. Every operation is a pure data transformation. All Claude calls go through a single API wrapper with exponential backoff retry, fully mocked in tests.

```
17 commands · 6,961 lines of code · 537 tests, all passing
```

---

## Charlotte -- Prompt & Claude Code Skill Compiler

> Built because prompt engineering was ad-hoc string concatenation -- no type checking, no version control, no way to test one prompt change against regression.

Write a YAML spec declaring which blocks you need, bind your variables, and Charlotte compiles it through four deterministic stages into provider-ready output for OpenAI, Anthropic, or Google Gemini. Token budgets enforced. Conflicts caught at compile time. Security scanned. Testable with assertions. Charlotte compiles the prompt specifications that drive Stratum's extraction and generation stages.

<details>
<summary><strong>Claude Code Skill Compiler</strong></summary>

<br>

Charlotte also compiles to Claude Code Skills -- structured skill packages that Claude Code can invoke directly. This is the most unusual export target:

- Maps block types to structured sections (system --> overview, task --> workflow, few-shot --> quick reference, safety --> critical rules, tool-use --> tools)
- Extracts triggers and anti-triggers from routing blocks into YAML frontmatter
- Parses I/O pairs into tables, extracts imperative rules from safety blocks
- Auto-splits to a `references/` directory when content exceeds 500 lines
- Output is a ready-to-install skill package

</details>

<details>
<summary><strong>Full feature set</strong></summary>

<br>

**Compilation Pipeline**
- 4-stage pipeline: Parse --> Compose --> Validate --> Render
- 94 built-in blocks across 17 types (system, task, few-shot, chain-of-thought, tool-use, RAG, agent, evaluation, extraction, safety, routing, memory, retrieval, guardrail, planning, conversational, meta)
- Deterministic type-precedence composition -- blocks assemble in fixed order with explicit override support
- Provider-specific renderers: OpenAI messages array, Anthropic system parameter + messages, Google Gemini system_instruction, generic text

**Token Budgeting & Validation**
- Per-block, per-model token budgeting across 26 registered models (8K-2M context windows), with 80% threshold warnings and completion budget estimation
- Composition rules as data -- blocks declare compatibility, incompatibility, singletons, and dependencies, all enforced at compile time
- Jinja2 variable injection with 6 typed slots (string, number, boolean, array, object, document)

**Security & Testing**
- 8-check security scanner: prompt injection, PII exposure, API key leaks, jailbreak patterns, safety block validation, tool-use permissions, information disclosure, severity filtering
- Test runner with 6 assertion types (exact match, contains, regex, JSON schema, LLM-as-judge, custom Python evaluators) with parallel execution, response caching, and cross-model matrix testing

**Workflows & Versioning**
- Multi-prompt workflow chaining: DAG execution via topological sort, cross-step schema validation, typed data flow between steps, per-step assertions, directory package export
- Content-addressed versioning with semantic block-aware diffing

**Export & CI**
- 9 export formats: text, JSON, YAML, API payload (curl + Python snippets), MCP server definition, LangChain template, HTML report, README, Claude Code Skill
- Post-compile linter + file watcher with auto-recompile
- LLM-guided prompt optimization with iterative variable refinement
- CI command: validate --> compile --> scan --> lint --> test in one pass

</details>

**Architecture:** 25 Pydantic v2 models. Blocks are pure YAML data validated against schemas, not embedded code. Custom block directories supported. Four global registries (block types, providers, exporters, assertions). Three-tier prompt classification (single-turn, multi-phase, agent-orchestrating) with automatic tier detection and minimum-length enforcement.

```
26 commands · 13,272 lines of code · 94 blocks · 1,615 tests, all passing
```

---

## Stratum -- Automated Quality Pipeline

> Built because teams were shipping Claude-generated test suites without checking whether the tests actually tested anything -- hallucinated assertions, mocked-out logic, tests that pass no matter what, all going straight to CI.

Point it at source code. It extracts the full architecture using Claude and tree-sitter, generates unit tests and API tests across multiple frameworks, produces documentation in multiple formats, then runs everything through six independent quality gates. Each gate produces its own verdict. The audit engine aggregates them into a final pass or fail. Stratum validates every tool in this platform, including itself.

<details>
<summary><strong>Extraction, generation, and documentation</strong></summary>

<br>

**Extraction**
- Claude + tree-sitter static analysis across 6 languages (Python, TypeScript, JavaScript, Java, Go, Rust) with regex fallback
- Outputs architecture as structured JSON: endpoints, schemas, data models, workflows, source traces
- Call chain tracing, component clustering, cross-cutting concern detection, route pattern recognition
- Auto-detects web frameworks (Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, Quarkus)
- Iterative refinement loop (up to 10 passes), dry-run mode for token estimation

**Unit Test Generation**
- Tests generated from extracted source via Claude subprocess with prompt-via-stdin security
- pytest and jest output, validation loop with up to 3 retry attempts
- 86.68% test coverage on the generator itself

**API Test Generation**
- 4 test layers: Contract (endpoint signatures), Boundary (edge cases), Workflow (multi-step state transitions), Regression (known bugs)
- 4 output frameworks: pytest, jest, Postman/Newman, RestAssured
- Architecture-driven test planning with fixture generation and traceability reports

**Documentation Generation**
- 7 analyzers: data flow, decision archaeology, tribal knowledge, change impact, code smell detection, health scoring, onboarding guide generation
- 7 quality gates on the docs themselves: accuracy, coverage, completeness, freshness, readability (Flesch-Kincaid), broken links, aggregated verdict
- 3 output formats: Markdown, HTML (Mermaid diagrams, search index, responsive layout), PDF
- 90.86% test coverage on the generator itself

</details>

<details open>
<summary><strong>Quality Gates -- 6 independent modules</strong></summary>

<br>

| Gate | What it does |
|------|-------------|
| **Forge** | Seven Rules hard gate. Every test must: (A) invoke the code under test, (B) assert on outputs not inputs, (C) not swallow exceptions, (D) verify every mock, (E) test error paths, (F) fail if the code is wrong, (G) have no interdependence. All seven or rejected. |
| **Aegis** | Security scanning -- 9 detectors (SQL injection, command injection, NoSQL injection, XSS, auth, authorization, data exposure, hardcoded secrets, config flaws) + exploit generation, remediation generation, fuzz testing. |
| **Sentinel** | Mutation testing -- 8 mutator types. Mutates source, runs tests, calculates whether the suite actually catches the mutations. |
| **Specter** | Flaky test detection -- 9 pattern types (timing, shared state, order dependency, non-determinism, resource leaks, network, concurrency, environment, async). Parses pytest, jest, mocha, vitest. Auto-quarantine. |
| **Arbiter** | Rule harvesting from linters (pytest, jest, mocha, cargo/clippy, go vet, cppcheck, eslint) mapped to test quality categories. 7-day cache. |
| **CodeGate** | AI production readiness review -- 10-item checklist, 3-tier dependency verification, explicit reasoning enforcement. Pass / conditional pass / fail. 6 languages. |

**Candor** (transparency) -- Tracks every extraction skip, generation failure, validation error, and gate bypass across the entire pipeline. No silent failures.

</details>

**Architecture:** Monorepo with shared extraction core. Each gate is a silo -- independent logic, independent verdict, aggregated by the audit engine into a final pass/fail. Pipeline orchestrator with 11 configurable stages. All gates toggleable. Audit thresholds configurable per gate. GitHub Actions integration for CI/CD.

```
6 commands · 233 modules · 55,870 lines of code · 3,046 tests, all passing
```

---

## How They Connect

```
  Raw Idea                    YAML Spec                     Source Code
     |                           |                              |
     v                           v                              v
+--------------+         +---------------+             +---------------+
| Designer-SDD |         |   Charlotte   |             |    Stratum    |
|              |         |               |             |               |
| Validate     |         | Compile       |             | Extract       |
| Score        |         | Validate      |             | Generate      |
| Improve      |         | Test          |             | Gate          |
| Export       |         | Export        |             | Audit         |
+------+-------+         +-------+-------+             +-------+-------+
       |                         |                             |
       v                         v                             v
  Scored Spec              Provider-Ready             Pass/Fail Verdict
  Package (7-11            Prompts or Claude          + Tests + Docs
  markdown files)          Code Skills                + Transparency
```

Designer-SDD produces the specs that defined every tool here. Charlotte compiles the prompts that power Stratum's AI stages. Stratum validates the code that all three tools generate. They're standalone, but they eat their own cooking.

---

## Platform Totals

<div align="center">

| | Designer-SDD | Charlotte | Stratum | **Combined** |
|:---|:---:|:---:|:---:|:---:|
| **Source Lines** | 6,961 | 13,272 | 55,870 | **76,103** |
| **Python Modules** | 45 | 55 | 233 | **333** |
| **Tests (passing)** | 537 | 1,615 | 3,046 | **5,198** |
| **Commands** | 17 | 26 | 6 | **49** |

</div>

<br>

<div align="center">

**Stack:** Python 3.10+ · Typer/Click · Claude API · Pydantic v2 · tree-sitter · Rich · YAML/JSON

</div>
