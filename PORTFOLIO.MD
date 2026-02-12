<details>
<summary><strong>What it does</strong></summary>

<br>

**Compilation Pipeline**
- 4-stage pipeline: Parse → Compose → Validate → Render
- 94 built-in blocks across 17 types (system, task, few-shot, chain-of-thought, tool-use, RAG, agent, evaluation, extraction, safety, routing, memory, retrieval, guardrail, planning, conversational, meta)
- Deterministic type-precedence composition — blocks assemble in fixed order with explicit override support
- Provider-specific renderers: OpenAI messages array, Anthropic system parameter + messages, Google Gemini system_instruction, generic text

**Token Budgeting & Validation**
- Per-block, per-model token budgeting across 26 registered models (8K–2M context windows), with 80% threshold warnings and completion budget estimation
- Composition rules as data — blocks declare compatibility, incompatibility, singletons, and dependencies, all enforced at compile time
- Jinja2 variable injection with 6 typed slots (string, number, boolean, array, object, document)

**Security & Testing**
- 8-check security scanner: prompt injection, PII exposure, API key leaks, jailbreak patterns, safety block validation, tool-use permissions, information disclosure, severity filtering
- Test runner with 6 assertion types (exact match, contains, regex, JSON schema, LLM-as-judge, custom Python evaluators) with parallel execution, response caching, and cross-model matrix testing

**Workflows & Versioning**
- Multi-prompt workflow chaining: DAG execution via topological sort, cross-step schema validation, typed data flow between steps, per-step assertions, directory package export
- Content-addressed versioning with semantic block-aware diffing

**Claude Code Skill Compiler**
- Maps block types to structured sections (system → overview, task → workflow, few-shot → quick reference, safety → critical rules, tool-use → tools)
- Extracts triggers and anti-triggers from routing blocks into YAML frontmatter
- Parses I/O pairs into tables, extracts imperative rules from safety blocks
- Auto-splits to a `references/` directory when content exceeds 500 lines
- Output is a ready-to-install skill package

**Export & CI**
- 9 export formats: text, JSON, YAML, API payload (curl + Python snippets), MCP server definition, LangChain template, HTML report, README, Claude Code Skill
- Post-compile linter + file watcher with debounced auto-recompile
- LLM-guided prompt optimization with iterative variable refinement
- CI command: validate → compile → scan → lint → test in one pass

</details>

**Architecture:** 25 Pydantic v2 models. Blocks are pure YAML data validated against schemas, not embedded code. Custom block directories supported. Four global registries (block types, providers, exporters, assertions). Three-tier prompt classification (single-turn, multi-phase, agent-orchestrating) with automatic tier detection and minimum-length enforcement.

```
26 commands · 13,272 lines of code · 94 blocks · 1,615 tests, all passing
```

---

## Stratum — Automated Quality Pipeline

> Built because teams were shipping Claude-generated test suites without checking whether the tests actually tested anything — hallucinated assertions, mocked-out logic, tests that pass no matter what, all going straight to CI.

Point it at source code. It extracts the full architecture using Claude and tree-sitter, generates unit tests and API tests across multiple frameworks, produces documentation in multiple formats, then runs everything through six independent quality gates. Each gate produces its own verdict. The audit engine aggregates them into a final pass or fail.

<details>
<summary><strong>Extraction</strong></summary>

<br>

- Claude + tree-sitter static analysis across 6 languages (Python, TypeScript, JavaScript, Java, Go, Rust) with regex fallback
- Outputs architecture as structured JSON: endpoints, schemas, data models, workflows, source traces
- Call chain tracing, component clustering, cross-cutting concern detection, route pattern recognition
- Auto-detects web frameworks (Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, Quarkus)
- Iterative refinement loop (up to 10 passes), dry-run mode for token estimation

</details>

<details>
<summary><strong>Test Generation</strong></summary>

<br>

*Unit Tests:*
- Tests generated from extracted source via Claude subprocess with prompt-via-stdin security
- pytest and jest output, validation loop with up to 3 retry attempts
- 86.68% test coverage on the generator itself

*API Tests:*
- 4 test layers: Contract (endpoint signatures), Boundary (edge cases), Workflow (multi-step state transitions), Regression (known bugs)
- 4 output frameworks: pytest, jest, Postman/Newman, RestAssured
- Architecture-driven test planning with fixture generation and traceability reports

</details>

<details>
<summary><strong>Documentation Generation</strong></summary>

<br>

- 7 analyzers: data flow, decision archaeology, tribal knowledge, change impact, code smell detection, health scoring, onboarding guide generation
- 7 quality gates on the docs themselves: accuracy, coverage, completeness, freshness, readability (Flesch-Kincaid), broken links, aggregated verdict
- 3 output formats: Markdown, HTML (Mermaid diagrams, search index, responsive layout), PDF
- 90.86% test coverage on the generator itself

</details>

<details open>
<summary><strong>Quality Gates — 6 independent modules</strong></summary>

<br>

| Gate | What it does |
|------|-------------|
| **Forge** | Seven Rules hard gate. Every test must: (A) invoke the code under test, (B) assert on outputs not inputs, (C) not swallow exceptions, (D) verify every mock, (E) test error paths, (F) fail if the code is wrong, (G) have no interdependence. All seven or rejected. |
| **Aegis** | Security scanning — 9 detectors (SQL injection, command injection, NoSQL injection, XSS, auth, authorization, data exposure, hardcoded secrets, config flaws) + exploit generation, remediation generation, fuzz testing. |
| **Sentinel** | Mutation testing — 8 mutator types. Mutates source, runs tests, calculates whether the suite actually catches the mutations. |
| **Specter** | Flaky test detection — 9 pattern types (timing, shared state, order dependency, non-determinism, resource leaks, network, concurrency, environment, async). Parses pytest, jest, mocha, vitest. Auto-quarantine. |
| **Arbiter** | Rule harvesting from linters (pytest, jest, mocha, cargo/clippy, go vet, cppcheck, eslint) mapped to test quality categories. 7-day cache. |
| **CodeGate** | AI production readiness review — 10-item checklist, 3-tier dependency verification, explicit reasoning enforcement. Pass / conditional pass / fail. 6 languages. |

</details>

<details>
<summary><strong>Transparency</strong></summary>

<br>

**Candor** — Tracks every extraction skip, generation failure, validation error, and gate bypass across the entire pipeline. No silent failures.

</details>

**Architecture:** Monorepo with shared extraction core. Each gate is a silo — independent logic, independent verdict, aggregated by the audit engine into a final pass/fail. Pipeline orchestrator with 11 configurable stages. All gates toggleable. Audit thresholds configurable per gate. GitHub Actions integration for CI/CD.

```
5 CLI entry points · 6 commands · 233 modules · 55,870 lines of code · 3,046 tests, all passing
```

---

## How They Fit Together

```
  Raw Idea                    YAML Spec                     Source Code
     │                           │                              │
     ▼                           ▼                              ▼
┌─────────────┐          ┌──────────────┐              ┌──────────────┐
│ Designer-SDD│          │  Charlotte   │              │   Stratum    │
│             │          │              │              │              │
│ Validate    │          │ Compile      │              │ Extract      │
│ Score       │          │ Validate     │              │ Generate     │
│ Improve     │          │ Test         │              │ Gate         │
│ Export      │          │ Export       │              │ Audit        │
└──────┬──────┘          └──────┬───────┘              └──────┬───────┘
       │                        │                             │
       ▼                        ▼                             ▼
  Scored Spec             Provider-Ready              Pass/Fail Verdict
  Package (7-11           Prompts or Claude           + Tests + Docs
  markdown files)         Code Skills                 + Transparency
```

Each tool is standalone. Together they cover the full arc from idea to verified software.

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
