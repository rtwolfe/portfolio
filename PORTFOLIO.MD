<div align="center">

# AI Development Platform

### Automated specification, prompt compilation, and quality assurance for AI-assisted software development

**Solo-built over one year**

<br>

87,912 lines of Python · 377 modules · 6,248 tests · All passing · 59 CLI commands

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Tests](https://img.shields.io/badge/Tests-6%2C248_passing-brightgreen?style=flat-square)
![Lines](https://img.shields.io/badge/Source-87%2C912_lines-blue?style=flat-square)
![Modules](https://img.shields.io/badge/Modules-377-purple?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

</div>

---

<div align="center">

[Designer-SDD](#-designer-sdd--spec-driven-development-cli) · [Charlotte](#-charlotte--prompt--application-compiler) · [Stratum](#-stratum--automated-quality-pipeline) · [How They Connect](#how-they-connect) · [Platform Totals](#platform-totals)

</div>

---

One person, three tools, one platform. Designer-SDD produces the specs that define what to build. Charlotte compiles the prompts that power the AI stages. Stratum validates what got built and decides whether it ships. Each tool is standalone, but each one feeds the others -- Designer-SDD specs defined every tool here, Charlotte compiles the prompts powering Stratum's AI stages, and Stratum validates the code all three generate. The platform is self-hosting.

The strict layering, the stateless architecture, the investment in 6,248 tests -- all deliberate choices for an 88K-line codebase that has to stay maintainable with a single developer. No shortcuts. No "it works on my machine." Every module tested, every gate enforced, every failure tracked.

<br>

---

## <img width="20" height="20" src="https://img.shields.io/badge/-1-blue?style=flat-square" alt="1"> Designer-SDD -- Spec-Driven Development CLI

> Built because specs kept arriving as Slack threads and call transcripts, and teams kept building the wrong thing from ambiguous requirements.

Designer-SDD is a specification engine. Feed it a client brief, a call transcript, a Slack dump, raw notes -- it extracts a structured JSON spec via Claude, then puts it through a gauntlet: validation against domain-specific rules, dual-gate scoring (36 weighted checks across quality and buildability), iterative AI-driven refinement that re-scores after every pass, and round-trip verification that confirms every requirement in the spec appears in the rendered output. The output isn't a document -- it's a scored, validated, GitHub-ready documentation package of up to 11 files. Designer-SDD specs defined every tool in this platform, including Charlotte and Stratum themselves.

<details open>
<summary><strong>Spec entry and discovery</strong></summary>

<br>

Multiple paths from raw input to structured spec:

- **Intake** -- Extracts structured JSON specs from unstructured text (briefs, notes, transcripts) via Claude with 17 context-aware system prompts. Auto-detects domain and tier.
- **Create** -- Interactive multi-turn brainstorming with Claude. Auto-detects when valid spec output appears in conversation and extracts it.
- **Discover** -- 3-stage market research pipeline using web search tools: quick scan (5 searches) → deep dive (10 searches with competitive analysis) → handoff to spec builder with findings.
- **Form** -- Browser-based HTML intake form for structured spec capture without command-line interaction.
- **Templates** -- 5 pre-built spec templates (CLI tool, REST API, SaaS dashboard, library/package, Chrome extension) with customizable placeholders and merge support. All templates pass quality gate out-of-the-box.

</details>

<details open>
<summary><strong>Scoring and validation</strong></summary>

<br>

This is the core of what makes Designer-SDD more than a document generator:

- **Quality gate** -- 28 weighted checks across 7 sections (constitution, spec, plan, tasks, handoff, README, research). Section weights graduated: Constitution 1.0x, Spec 1.5x, Plan 2.0x, Tasks 2.0x, Handoff 1.0x, README 0.5x, Research 0.5x. Not binary pass/fail -- graduated scoring with per-section breakdowns. Threshold: 70%.
- **Buildability gate** -- 8 checks that ask "can a developer actually build this?": acceptance verifiability, dependency completeness, ambiguity detection, phase continuity, tech completeness, test strategy, DoD actionability, environment specification. Threshold: 60%.
- **Spec gate** -- 10 hard deterministic rules (A-J): every functional req has description + priority, user stories reference requirements, assumptions have mitigation, open questions have resolution status, risks have mitigation, success criteria are measurable, DoD items are actionable, tech choices justified, task breakdown covers requirements, no unresolved placeholders (TODO/TBD/FIXME). Pass/conditional pass/fail.
- **Domain-aware validation** -- CLI projects must declare exit codes. APIs must declare auth schemes. Web apps must declare auth and error handling. Mobile must declare offline behavior. Not generic rules -- rules that match the domain.
- **Round-trip verification** -- after export, verifies that every requirement and task in the source spec actually appears in the rendered markdown. Catches drift between spec and output.
- **Iterative refinement** -- two modes: generate structured improvement instructions, or let Claude auto-fix the spec in up to 3 iterations with re-scoring after each pass. The spec gets measurably better each round.

</details>

<details>
<summary><strong>Output and export</strong></summary>

<br>

- **Tier-gated export** -- small specs produce 7 files, medium specs 9, large specs 11:
  - Always: `CONSTITUTION.md`, `SPEC.md`, `PLAN.md`, `TASKS.md`, `HANDOFF.md`, `README.md`, `spec.json`
  - Medium/Large: `DATA_MODEL.md`, `QUICKSTART.md`
  - Large: `ARCHITECTURE.md`
  - If research section present: `RESEARCH.md`
- **Deterministic HTML dashboard** (305KB interactive dashboard, no API needed) with metrics, timeline visualization, tech stack breakdown, scoring details
- **Premium HTML export** via Claude for styled documentation
- **Field-by-field spec diffing** with quality score delta between versions
- **Research command** -- answer open questions from RESEARCH section using Claude with optional `--apply` flag to write findings back into the spec

</details>

<details>
<summary><strong>Full CLI reference</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `designer intake` | Extract specs from raw text |
| `designer create` | Interactive brainstorming |
| `designer discover` | Market research pipeline |
| `designer form` | HTML form launcher |
| `designer validate` | Check completeness |
| `designer score` | Dual-gate scoring (quality + buildability) |
| `designer improve` | Auto-improve via Claude loop |
| `designer ingest` | Full pipeline (validate → score → export) |
| `designer export` | Render markdown package |
| `designer diff` | Compare spec versions |
| `designer research` | Answer open questions |
| `designer verify` | Post-export integrity check |
| `designer template list` | Browse available templates |
| `designer template preview` | Preview template contents |
| `designer template use` | Scaffold from template |
| `designer init` | Initialize new project |

</details>

**Architecture:** Strict four-layer separation (CLI → Engine → Core ← Util). Stateless -- zero database, zero persistence. Every operation is a pure data transformation. All Claude calls go through a single API wrapper with exponential backoff retry, fully mocked in tests. Path traversal protection at the security boundary prevents writing outside the output directory. Token budgeting tracks API spend across sessions. Configuration loads from four layers: environment → project YAML → global YAML → built-in defaults. 537 tests covering every validator, every scorer, every renderer, and every CLI command -- runs in under 4 seconds.

```
16 commands · 52 modules · 8,246 lines of code · 537 tests, all passing
```

<br>

---

## <img width="20" height="20" src="https://img.shields.io/badge/-2-blue?style=flat-square" alt="2"> Charlotte -- Prompt & Application Compiler

> Built because prompt engineering was ad-hoc string concatenation -- no type checking, no version control, no way to test one prompt change against regression.

Charlotte is a real compiler. Not a template stitcher, not a string formatter -- a five-stage deterministic pipeline that parses typed specifications, composes them against a 94-block library with conflict detection and dependency resolution, runs 8-pass automatic optimization (deduplication, merging, compression, provider-specific hints), validates token budgets against 26 model context windows, and renders provider-specific output for OpenAI, Anthropic, and Google Gemini. It has a type system (6 typed variable slots), a security scanner (54 checks across 21 categories including injection, exfiltration, compliance, and bias), a test framework (30 assertion types with parallel cross-model execution), a versioning system (content-addressed snapshots with semantic diffing), environment management (dev/staging/production with promotion gates), GitHub Actions CI generation, red team simulation, cost estimation, a multi-prompt workflow engine (DAG execution with typed data flow between steps), and a multi-agent compiler that generates runnable projects for four major agent frameworks plus Google A2A protocol Agent Cards. Charlotte compiles the prompt specifications that drive Stratum's extraction and generation stages.

<details open>
<summary><strong>Five-stage compilation pipeline</strong></summary>

<br>

Every compilation passes through five deterministic stages:

1. **Parse** -- Read YAML/JSON spec, resolve block references from the 94-block library, validate schema against Pydantic v2 models.
2. **Compose** -- Assemble blocks in strict type-precedence order (system → guardrail → safety → routing → task → few_shot → chain_of_thought → planning → tool_use → retrieval → rag → extraction → memory → meta → conversational → agent → evaluation). Detect conflicts, enforce singletons, resolve dependencies, inject typed variables.
3. **Optimize** -- 8-pass automatic optimization: block deduplication, adjacent text merging, empty block stripping, whitespace normalization, system block reordering, example compression, token budget optimization, provider-specific hints.
4. **Validate** -- Conflict detection, token budgeting per target model with per-block breakdown, completeness checks, composition rule enforcement. Blocks declare compatibility, incompatibility, singletons, and dependencies -- all enforced at compile time.
5. **Render** -- Provider-specific format transformation: OpenAI messages array, Anthropic system parameter + messages, Google Gemini system_instruction, generic text.

</details>

<details open>
<summary><strong>94-block library across 17 types</strong></summary>

<br>

| Type | Count | Examples |
|------|-------|---------|
| **system** | 6 | role_definition, persona, behavioral, expertise_boundaries, multi_audience, output_personality |
| **task** | 6 | analyze, classify, compare, generate, summarize, transform |
| **few_shot** | 6 | io_pairs, edge_cases, conversation, chain, labeled, negative |
| **chain_of_thought** | 5 | step_by_step, reasoning_first, scratchpad, decomposition, self_correction |
| **tool_use** | 5 | function_calling, multi_tool, api_integration, error_handling, output_parser |
| **rag** | 6 | document_context, contextual_qa, multi_document, citation_enforcer, conflicting_sources, summarize_then_answer |
| **agent** | 5 | goal_decomposition, plan_execute, react, memory, reflection |
| **evaluation** | 6 | rubric, checklist, pairwise, completeness, factual_accuracy, tone_style |
| **extraction** | 6 | json_schema, field_extraction, table, comparison, entity_classification, timeline |
| **meta** | 5 | prompt_generator, refiner, critique, ab_test, simplifier |
| **conversational** | 5 | history_window, state_management, dynamic_injection, clarification, persona_consistency |
| **safety** | 6 | content_filter, injection_defense, pii_protection, hallucination_guardrail, output_sanitizer, scope_limiter |
| **routing** | 5 | input_classifier, tool_selector, agent_handoff, complexity_estimator, language_detector |
| **memory** | 5 | conversation_window, entity_tracker, session_state, long_term_retrieval, working_context |
| **retrieval** | 6 | semantic_search, hybrid_search, contextual_chunking, query_expansion, source_filter, result_formatter |
| **guardrail** | 6 | input_validator, output_validator, topic_boundary, format_enforcer, pii_shield, factuality_check |
| **planning** | 5 | task_decomposition, sequential_steps, tree_of_thought, iterative_refinement, resource_allocation |

Blocks are pure YAML data validated against schemas, not embedded code -- the library is extensible without touching source. Custom blocks auto-register from any block directory.

</details>

<details open>
<summary><strong>Security scanner -- 54 checks across 21 categories</strong></summary>

<br>

| Category | What it checks |
|----------|---------------|
| **Injection (basic + advanced)** | Prompt injection patterns, jailbreak attempts, role hijacking, instruction override |
| **Data exfiltration** | Attempts to extract training data, system prompts, or user information |
| **Model manipulation** | Attempts to alter model behavior, temperature, or safety settings |
| **Output control** | Format forcing, encoding tricks, output redirection |
| **Context poisoning** | Conflicting instructions, hidden context, delimiter manipulation |
| **Resource abuse** | Token inflation, recursive generation, denial-of-service patterns |
| **Privilege escalation** | Role elevation, permission bypass, admin impersonation |
| **Cross-prompt attacks** | Session persistence, state injection across prompts |
| **Compliance** | GDPR, HIPAA, PCI-DSS data handling violations |
| **Supply chain** | Dependency confusion, package hallucination |
| **Bias/fairness** | Stereotyping, demographic bias, unequal treatment |
| **Hallucination risk** | Unsupported claims, fabrication triggers |
| **Token manipulation** | Tokenizer exploits, special token abuse |
| **Auth boundary** | Authentication bypass, session manipulation |
| **Sandbox escape** | Code execution, file system access, network access |
| **Prompt structure** | Structural vulnerabilities, delimiter confusion |
| **Logging safety** | PII in logs, sensitive data exposure |
| **Multi-modal threats** | Image-based injection, cross-modal attacks |
| **Chain safety** | Multi-step attack chains, sequential exploitation |
| **MCP tool poisoning** | Malicious tool definitions, tool injection |
| **Version safety** | Version rollback attacks, downgrade exploits |

</details>

<details>
<summary><strong>Testing framework -- 30 assertion types</strong></summary>

<br>

Test runner executes compiled prompts against live LLM providers with parallel cross-model matrix testing:

| Assertion | What it validates |
|-----------|------------------|
| `exact` | Exact string match |
| `contains` / `not_contains` | Substring presence/absence |
| `starts_with` / `ends_with` | String prefix/suffix |
| `regex` | Regular expression match |
| `json_schema` | JSON schema validation |
| `json_valid` / `xml_valid` / `yaml_valid` | Format validation |
| `llm_as_judge` | LLM evaluates response quality |
| `custom_evaluator` | User-defined evaluation function |
| `length_between` / `word_count` / `token_count` | Size constraints |
| `sentiment` | Sentiment analysis |
| `language` | Language detection |
| `no_pii` / `no_profanity` | Content safety |
| `similarity` | Cosine similarity scoring |
| `latency` | Response time thresholds |
| `format_match` | Format pattern matching |
| `all_of` / `any_of` / `none_of` | Composite assertions |
| `rubric` | Rubric-based grading |
| `grounded` | Factual grounding check |
| `guardrail` | Safety guardrail validation |
| `structural` | Structural pattern matching |
| `consistency` | Cross-response consistency |

Evaluation system with history tracking, baseline management, and regression drift detection.

</details>

<details>
<summary><strong>Agent compiler -- multi-framework export</strong></summary>

<br>

Charlotte's agent compiler takes compiled prompts and workflows containing agent blocks and generates complete, runnable projects for four major agent frameworks:

- **CrewAI** -- YAML agent/task definitions, crew orchestration, `@tool` stubs, hierarchical/sequential process selection
- **LangGraph** -- StateGraph with typed state, node functions, conditional edges, ToolNode integration, MemorySaver checkpointing
- **AutoGen** -- AssistantAgent definitions, GroupChat with speaker selection (auto for supervised, round-robin for flat), UserProxyAgent, tool registration
- **OpenAI Agents SDK** -- Agent definitions with handoffs, `@function_tool` stubs, triage agent pattern, async Runner entry point
- **Google A2A Protocol** -- Agent Cards with capability detection, skill extraction from tools, input/output mode declaration

Each export includes `pyproject.toml`, README, and all source files needed to run. A shared extraction layer maps Charlotte's agent blocks (react, plan_execute, goal_decomposition, memory, reflection) to framework-specific constructs without duplicating logic across renderers. Hierarchy detection (supervisor vs hierarchical vs flat) drives framework-appropriate orchestration patterns. All generated Python passes `ast.parse()` validation; all JSON/YAML/TOML is structurally valid.

Multi-agent workflow compilation enriches the base workflow pipeline with agent roles per step, handoff protocols (from routing blocks + dependency edges), shared memory configuration, and automatic hierarchy detection.

</details>

<details>
<summary><strong>Claude Code skill compiler</strong></summary>

<br>

Charlotte compiles to Claude Code Skills -- structured skill packages that Claude Code can invoke directly:

- Maps block types to structured sections (system → overview, task → workflow, few-shot → quick reference, safety → critical rules, tool-use → tools)
- Extracts triggers and anti-triggers from routing blocks into YAML frontmatter
- Parses I/O pairs into tables, extracts imperative rules from safety blocks
- Auto-splits to a `references/` directory when content exceeds 500 lines
- Output is a ready-to-install skill package

</details>

<details>
<summary><strong>Workflows, versioning, and environment management</strong></summary>

<br>

- **Multi-prompt workflows** -- Chain multiple specs with typed data flow (`{{steps.X.output.field}}`). Topological execution ordering via Kahn's algorithm. Conditional step execution via Jinja2. Cross-step schema validation (10 checks). End-to-end workflow testing. Directory package export (manifest.json + per-step files).
- **Content-addressed versioning** -- JSON snapshots with semantic block-aware diffing. Track added/removed/modified blocks, variable changes, and structural differences between versions.
- **Environment management** -- Dev/staging/production environments with variable overrides, promotion gates (test pass rate, score threshold, manual approval), and environment diffing.
- **GitHub Actions CI generation** -- 4 workflow templates: validate-on-PR, test-on-push, scheduled regression, environment promotion.
- **21 export formats** -- text, JSON, YAML, API payload, MCP definition, LangChain template, HTML report, README, Claude Code Skill, MCP server (single + workflow), CrewAI (single + workflow), LangGraph (single + workflow), AutoGen (single + workflow), OpenAI Agents (single + workflow), A2A Agent Card (single + workflow).
- **LLM-guided optimization** -- Iterative variable refinement with automatic improvement suggestions.
- **Cost estimation** -- Budget projection based on token counts and expected volume.

</details>

<details>
<summary><strong>10 example application packs</strong></summary>

<br>

| Pack | Tier | Blocks | Use Case |
|------|------|--------|----------|
| **customer_support_bot** | multi_phase | 8 | E-commerce chatbot: returns, shipping, routing, conversation history |
| **code_review_assistant** | multi_phase | 6 | Code reviewer with structured JSON feedback, severity ratings |
| **legal_document_analyzer** | multi_phase | 6 | Contract analyzer with citations, legal disclaimers |
| **ml_model_evaluator** | agent_orchestrating | 8 | ML evaluation: accuracy, fairness, robustness, explainability |
| **content_moderator** | multi_phase | 7 | Moderation with confidence scores, escalation routing |
| **research_summarizer** | multi_phase | 7 | Literature review with conflict detection, comparison tables |
| **api_test_generator** | agent_orchestrating | 8 | Test case generation from OpenAPI specs |
| **multilingual_assistant** | multi_phase | 6 | 8-language support with language detection, persona consistency |
| **incident_responder** | agent_orchestrating | 7 | Production incident diagnosis (ReAct pattern) |
| **prompt_optimizer** | multi_phase | 7 | Meta-prompt for critiquing and refining prompts |

Each pack includes spec.yaml, README, and pre-compiled outputs (text, HTML, README).

</details>

**Architecture:** 28 Pydantic v2 models enforce every data boundary. Blocks are pure YAML data validated against schemas, not embedded code -- the library is extensible without touching source. Four global registries (block types, providers, exporters, assertions) make the system pluggable at every layer. Three-tier prompt classification (single-turn, multi-phase, agent-orchestrating) with automatic tier detection and minimum-length enforcement. The agent compiler uses a shared extraction layer so all five framework renderers consume the same AgentTeam abstraction -- adding a new framework means one renderer and its templates, nothing else. Token budgeting across 26 registered models (8K to 2M context windows) with 80% threshold warnings and completion budget estimation. The compiler itself is tested with 2,573 tests -- more than most production applications have total.

```
21 commands · 79 modules · 20,263 lines of code · 94 blocks · 30 templates · 2,573 tests, all passing
```

<br>

---

## <img width="20" height="20" src="https://img.shields.io/badge/-3-blue?style=flat-square" alt="3"> Stratum -- Automated Quality Pipeline

> Built because teams were shipping Claude-generated test suites without checking whether the tests actually tested anything -- hallucinated assertions, mocked-out logic, tests that pass no matter what, all going straight to CI.

Point it at source code. It extracts the full architecture using Claude and tree-sitter across 6 languages, generates unit tests and API tests across multiple frameworks, produces documentation in three formats with seven independent analyzers, then runs everything through seven independent quality gates. Each gate produces its own verdict. The audit engine aggregates them into a final pass or fail. A transparency layer tracks every skip, failure, and limitation across the entire pipeline -- no silent failures. Stratum validates every tool in this platform, including itself.

<details open>
<summary><strong>6-stage pipeline</strong></summary>

<br>

```
SOURCE CODE
    │
    ▼
┌──────────────────────────────────────────┐
│ 1. EXTRACT (tree-sitter + Claude)        │
│    Classes, functions, endpoints → JSON   │
│    6 languages · framework detection      │
└──────────┬───────────────────────────────┘
           │ architecture JSON
    ┌──────┴──────────┬──────────────┐
    ▼                 ▼              ▼
┌──────────┐   ┌───────────┐   ┌──────────┐
│ 2. UNIT  │   │ 3. API    │   │ 4. DOCS  │
│ pytest/  │   │ 4 layers  │   │ 7 analyz │
│ jest     │   │ 4 framewk │   │ 3 format │
└────┬─────┘   └─────┬─────┘   └────┬─────┘
     └────────────────┼──────────────┘
                      ▼
┌──────────────────────────────────────────┐
│ 5. QUALITY GATES (7 independent modules) │
│ Forge · Aegis · Sentinel · Specter       │
│ Arbiter · CodeGate · Intent              │
└──────────────────┬───────────────────────┘
                   ▼
┌──────────────────────────────────────────┐
│ 6. CANDOR (Transparency Report)          │
│ What automation couldn't handle          │
└──────────────────────────────────────────┘
```

The pipeline is fully configurable. Each stage is independently toggleable. Stage timeouts are enforced via `ThreadPoolExecutor`. Failed stage outputs are automatically cleaned up.

</details>

<details open>
<summary><strong>Architecture extraction</strong></summary>

<br>

Stratum-Out combines Claude with tree-sitter static analysis to extract complete codebase structure:

- **6 language parsers** -- Python, TypeScript, JavaScript, Java, Go, Rust, plus a generic regex fallback for unsupported languages
- **10+ extraction services** -- Extractor, Discovery, CallChain tracer, Clusterer, CrossCutting concern detection, RoutePattern recognition, EndpointExtractor, ProjectDetector, QualityGate, ClaudeClient
- **3-layer context model** -- L1 Skeleton (AST-level structure), L2 Feature Slices (source-level function groupings), L3 Cross-Cutting (error handling, config, logging patterns)
- **Framework auto-detection** -- Flask, FastAPI, Django, Express, Koa, Nest.js, Spring, Quarkus
- **Output artifacts** -- 6 JSON files including `source_model.json` (the critical artifact consumed by downstream stages), plus architecture diagrams
- **Iterative refinement** -- up to 10 extraction passes for complex codebases
- **Dry-run mode** -- token estimation before committing to API calls
- **GitHub Actions integration** -- `action.yml` for CI/CD deployment

</details>

<details open>
<summary><strong>Unit test generation</strong></summary>

<br>

Generates validated unit tests from extracted architecture metadata:

- **Framework support** -- pytest (Python), jest (JavaScript/TypeScript)
- **Security** -- Prompts passed to Claude via stdin, not CLI arguments, preventing command injection
- **Validation loop** -- 3-retry cycle: generate → execute → fix. Tests that don't actually run are rejected.
- **Claude subprocess** -- Uses `claude --print` for generation, with `shlex.split()` + `shell=False` for secure subprocess execution
- **Prompt templates** -- Jinja2 `.j2` templates for structured, reproducible prompt generation
- **Coverage** -- 86.68% test coverage on the generator itself (204 tests)

</details>

<details open>
<summary><strong>API test generation</strong></summary>

<br>

Architecture-driven API test generation across four layers and four frameworks:

**4 test layers:**

| Layer | Purpose |
|-------|---------|
| **Contract** | Endpoint signatures -- verifies the API surface matches the spec (methods, paths, status codes, content types) |
| **Boundary** | Edge cases -- empty payloads, max-length strings, type coercion, null handling, negative IDs, boundary values |
| **Workflow** | Multi-step state transitions -- create → read → update → delete sequences, authentication flows, data dependency chains |
| **Regression** | Known bugs -- captures previously-found defects as permanent regression guards |

**4 output frameworks:**

| Framework | Output |
|-----------|--------|
| **pytest** | Python test classes with `requests`/`httpx` |
| **jest** | JavaScript test suites with `supertest`/`axios` |
| **Postman/Newman** | Collection JSON for Postman import and Newman CLI execution |
| **RestAssured** | Java test classes for REST Assured framework |

- Parses architecture from JSON, YAML, and Markdown input formats
- Generates intelligent test plans with fixture factories and data generators
- Produces traceability reports linking tests back to spec requirements
- Architecture diff system detects changes between extractions and generates targeted regression tests
- Bridge layer consumes Stratum-Out JSON/YAML output directly
- 382 tests on the generator itself

</details>

<details open>
<summary><strong>Documentation generation</strong></summary>

<br>

**7 independent analyzers:**

| Analyzer | What it produces |
|----------|-----------------|
| **Data Flow** | Traces data through the system -- inputs, transformations, outputs, storage points, external boundaries |
| **Decision Archaeology** | Reconstructs why architectural decisions were made from code patterns, comments, git history, and structural cues |
| **Tribal Knowledge** | Captures implicit knowledge -- undocumented conventions, naming patterns, configuration assumptions, setup rituals |
| **Change Impact** | Predicts blast radius of changes -- which modules, tests, and consumers are affected by modifying a given file |
| **Code Smells** | Detects quality issues -- long methods, deep nesting, god classes, feature envy, inappropriate intimacy, dead code |
| **Health Scoring** | Scores codebase health across multiple dimensions -- complexity, test coverage, documentation ratio, dependency freshness |
| **Onboarding** | Generates onboarding guides -- "start here" paths, key concepts, common tasks, gotchas, contribution workflow |

**7 quality gates on the docs themselves:**

| Gate | What it enforces |
|------|-----------------|
| **Accuracy** | Do code references in the docs match the actual source? |
| **Coverage** | Is every public module/class/function documented? |
| **Completeness** | Are all sections filled in, or are there TODO/TBD placeholders? |
| **Freshness** | Is the documentation older than the code it describes? |
| **Readability** | Flesch-Kincaid scoring -- is the documentation accessible? |
| **Links** | Are all cross-references and external links valid? |
| **Aggregator** | Combines all gate scores into a weighted final verdict |

**3 output formats:**

- **Markdown** -- Standard GitHub-flavored markdown with proper heading hierarchy
- **HTML** -- Responsive layout with Mermaid diagrams, client-side search index, syntax highlighting via Pygments
- **PDF** -- Print-ready output via WeasyPrint

Supports Python, JavaScript, and Java extraction with git history analysis. Live documentation server for real-time preview. 90.86% test coverage on the generator itself (832 tests).

</details>

<details open>
<summary><strong>Quality gates -- 7 independent modules</strong></summary>

<br>

| Gate | What it does |
|------|-------------|
| **Forge** | Seven Rules hard gate. Every generated test must: **(A)** invoke the code under test, **(B)** assert on outputs not inputs, **(C)** not swallow exceptions, **(D)** verify every mock, **(E)** test error paths, **(F)** fail if the code is wrong (no tautologies), **(G)** have no interdependence. All seven or rejected. Validators for both Python and JavaScript. 8-phase generation pipeline: dependency analysis → boundary classification → mock strategy → test case design → generation → rule validation (hard gate) → quality assessment → output formatting. |
| **Aegis** | Security scanning -- 24 vulnerability types across 9 detectors: SQL injection, command injection, NoSQL injection, XSS, auth bypass, authorization flaws, data exposure, hardcoded secrets, config flaws. Generates exploit tests to prove vulnerabilities and remediation tests to verify fixes. Includes fuzzer with payload database. Path-component EXCLUDE matching (set intersection on `path.parts`) prevents false positives on paths like `contest/`, `attestation/`. |
| **Sentinel** | Mutation testing -- 8 mutator types: arithmetic (`+` → `-`), comparison (`==` → `!=`), logical (`and` → `or`), return values (`return x` → `return None`), constants (`0` → `1`), boundary conditions (`<` → `<=`), negate conditions (`if x` → `if not x`), remove exceptions (`raise` deleted). Mutates source, runs the test suite, calculates whether the suite actually catches the mutations. Uses `shlex.split()` + `shell=False` for secure subprocess execution. |
| **Specter** | Flaky test detection -- 9 pattern types: timing-dependent, random state, external service dependencies, concurrency issues, async timing, non-deterministic output, file system timing, network timing, clock mocking issues. Parses pytest, jest, mocha, vitest output. Auto-quarantine logic isolates unreliable tests. Runtime flaky detection catches intermittent failures. |
| **Arbiter** | Rule harvesting from external linters: pytest, jest, mocha, cargo/clippy, go vet, cppcheck, eslint. Maps linter rules to test quality categories. 7-day cache with safe retrieval -- `harvest()` returns new `HarvestResult` instead of mutating cached objects, preventing rule accumulation. |
| **CodeGate** | AI code quality gate -- pure Python, no LLM calls (rule-based heuristics only). 10-item production readiness checklist: error paths handled, input validation present, no hardcoded secrets, logging present, no blocking in async contexts, resource cleanup, types explicit, testable, concurrency safe, failure isolation. 3-tier dependency verification: Tier 1 recognized (real package), Tier 2 hallucination risk (plausible but unknown), Tier 3 unverifiable. AI-specific defect detection: hallucinated dependencies, happy-path-only logic, context blindness, over-engineering, training data matching. Deterministic verdicts: PASS (no critical/high), CONDITIONAL PASS (1-2 high), FAIL (any critical or 3+ high). Supports 6 languages. Markdown + HTML (dark theme) output. |
| **Intent** | Spec requirement verification -- validates that generated code and tests actually implement the requirements from the original spec. Checks coverage of functional requirements, non-functional requirements, and acceptance criteria. Produces coverage percentage and gap analysis. |

</details>

<details open>
<summary><strong>Candor -- transparency layer</strong></summary>

<br>

Tracks what automation couldn't handle and reports it honestly -- no silent failures:

- **Event types** -- boundary issues, complexity issues, unsupported patterns, external dependencies, file issues, quality gate findings
- **Semantic events** -- `QUALITY_RULE_VIOLATION`, `SECURITY_VULNERABILITY`, `CODE_QUALITY_FINDING`, `FLAKY_TEST_DETECTED`
- **Two output reports** -- `CANDOR_TECHNICAL.md` (full detail for developers) and `CANDOR_EXECUTIVE.md` (summary for stakeholders)
- **Real metrics** -- success rate calculated from actual file counts via `rglob()`, not estimates
- **Pipeline-wide** -- every stage feeds Candor: extraction skips, generation failures, validation errors, gate bypasses

</details>

<details>
<summary><strong>Audit engine and configuration</strong></summary>

<br>

The audit engine aggregates all gate verdicts into a final pipeline decision:

- **9 audit checks** with configurable thresholds per gate
- **Per-gate thresholds** -- Aegis max severity, Sentinel minimum mutation score, Specter max flaky count, Forge require-all-pass, CodeGate max verdict, Intent min coverage
- **Config validation** -- `__post_init__()` validates all enums and thresholds with warnings (not errors) to prevent breaking existing configs
- **11 configurable stages** -- each independently toggleable. Default: Forge and Candor enabled, others opt-in.
- **Stage timeouts** -- `ThreadPoolExecutor` wrapper, disabled by default (set to 0)
- **Path traversal protection** -- CLI blocks access to `/etc`, `/proc`, `/sys`, `/dev`

</details>

<details>
<summary><strong>Full CLI reference</strong></summary>

<br>

| Command | Purpose |
|---------|---------|
| `stratum extract` | Extract architecture from source code |
| `stratum generate tests` | Generate unit + API tests |
| `stratum generate docs` | Generate documentation |
| `stratum audit` | Run all quality gates |
| `stratum review` | CodeGate standalone review |
| `stratum run` | Full pipeline (extract → generate → gate → audit) |
| `stratum-out generate` | Legacy extraction CLI |
| `stratum-unit generate` | Legacy unit test CLI |
| `stratum-api generate` | Legacy API test CLI |
| `stratum-docs generate` | Legacy documentation CLI |

Plus subcommands for per-module configuration, output selection, and threshold overrides.

</details>

<details>
<summary><strong>Security hardening (17 issues fixed)</strong></summary>

<br>

Full platform audit completed with all 17 security and correctness issues resolved:

**Critical:** Sentinel command injection (→ `shlex.split()` + `shell=False`), Unit generator subprocess injection (→ stdin-based prompt passing), Silent tree-sitter degradation (→ logging in all extractors)

**High:** Candor success_rate accuracy (→ real file counting), EventType mismatches (→ semantic event types), No stage timeouts (→ `ThreadPoolExecutor` wrapper), No logging (→ structured logging in pipeline/audit/CLI/config), Audit threshold bugs (→ operator corrections)

**Medium:** Temp file cleanup (→ try/finally), Path traversal (→ `_resolve_path()` validator), Aegis false positives (→ path-component matching), Docs O(n²) (→ O(1) dicts), Arbiter cache mutation (→ immutable returns), No cleanup on failure (→ failed stage output removal)

**Structural:** 39 integration tests, 12 performance benchmarks, config validation, CLI error handling

</details>

**Architecture:** Monorepo with shared extraction core. Strict layering: CLI → Engine → Core ← Util (no circular imports). Each gate is a silo -- independent logic, independent verdict, aggregated by the audit engine into a final pass/fail. Stateless pipeline -- zero database, zero persistence, pure data transformation. Consumer models unchanged: each module (out, unit, api, docs) maintains its own data models. Template paths resolved via `Path(__file__).parent` for relocatability. Pipeline orchestrator with 11 configurable stages. All gates toggleable. GitHub Actions integration via `action.yml`. 3,138 tests covering every extractor, every generator, every gate, and every CLI command.

```
22 commands · 246 modules · 59,403 lines of code · 3,138 tests, all passing
```

<br>

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
  Package (7-11            Prompts, Skills,           + Tests + Docs
  markdown files)          or Agent Projects          + Transparency
```

Each tool is standalone. Together they cover the full arc from idea to verified software:

- **Designer-SDD** defines *what* to build -- structured specs from unstructured input
- **Charlotte** handles *how to talk to AI* -- compiled, tested, versioned prompts
- **Stratum** validates *what was built* -- extraction, generation, and multi-gate quality enforcement

Designer-SDD specs defined every tool in this platform. Charlotte compiles the prompts that drive Stratum's AI stages. Stratum validates the code all three tools generate. The platform is self-hosting.

---

## Platform Totals

<div align="center">

| | Designer-SDD | Charlotte | Stratum | **Combined** |
|:---|:---:|:---:|:---:|:---:|
| **Source Lines** | 8,246 | 20,263 | 59,403 | **87,912** |
| **Python Modules** | 52 | 79 | 246 | **377** |
| **Tests (passing)** | 537 | 2,573 | 3,138 | **6,248** |
| **Commands** | 16 | 21 | 22 | **59** |

</div>

<br>

<div align="center">

**Stack:** Python 3.10+ · Typer/Click · Claude API · Pydantic v2 · tree-sitter · Jinja2 · Rich · YAML/JSON · WeasyPrint · tiktoken

---

*Solo-designed, solo-built, solo-tested. Every module. Every gate. Every test.*

</div>
