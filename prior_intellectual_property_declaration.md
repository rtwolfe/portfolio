# EXHIBIT A — PRIOR INVENTIONS DISCLOSURE

Pursuant to the Proprietary Information and Inventions Agreement between _______________________________________ ("Company") and the undersigned ("Employee"), Employee hereby identifies the following inventions, original works of authorship, developments, improvements, and trade secrets that were made by Employee prior to Employee's employment with Company, that belong solely to Employee or jointly to Employee with others, that relate in any way to any of Company's proposed businesses, products, or research and development, and that are not assigned to Company hereunder.

| | |
|---|---|
| **Employee** | Robert T. Wolfe |
| **Effective date** |  |

All items below were conceived and developed by Employee outside the scope of any prior or current employment, on Employee's own time and equipment, between December 2023 and the Effective Date, and remain under active development.

---

## Part I — Compiler and design-time components

**1. CITADEL** — Compliance-aware fleet specification compiler that converts natural-language descriptions into coordinated, governed agent and Model Context Protocol (MCP) server specifications. Carries 27 framework profiles, each with framework-specific behavioral defaults (autonomy ceilings, call-stack depth, cost limits, inter-territory crossing policies, redundancy postures), a domain-decomposition engine, a behavioral-policy compiler (mechanism specifics reserved under Item 28), an MCP security pipeline (tool-description poisoning scan, integrity manifest, topology expectation compiler, trust-decay scoring), and a stage-based orchestration pipeline producing content-addressable resumable artifacts. A single invocation produces a coordinated bundle: Castellan agent specs, Charlotte MCP-server specs, bilateral agent-to-agent trust policy, runtime-enforcement registration, command-channel protected-field config, behavioral baseline, per-agent model cards (SR 11-7 risk-tier classified), and a Merkle-anchored provenance manifest.

> **Compliance coverage:** HIPAA, PCI-DSS v4.0, SOC 2, FedRAMP (Low / Moderate / High), DoD Impact Level 4 and Impact Level 5, CNSSP-12, CMMC Levels 1 / 2 / 3, NIST 800-53, NIST 800-171 Revision 2, NIST AI Risk Management Framework (NIST IR 8596), GDPR, EU AI Act (High-Risk and Limited-Risk tiers), ISO/IEC 42001, ISO/IEC 42005, GLBA Safeguards Rule, FFIEC IT Examination Handbook, SOX IT General Controls, OCC SR 11-7, FINRA 2026, MAS AI Risk Management, Singapore IMDA, FDA PCCP, IEC 62304, and ISO 14971.

**2. CASTELLAN** — Agent compiler that converts YAML agent specifications into governed agent binaries with Python and hardened Rust output targets. Compiles the ReAct reasoning loop, multi-provider model client (Anthropic / OpenAI / Ollama / on-prem), structured tool invocation, governance enforcement hooks, and Item 9 registration directly into the binary, embedding the framework-specific governance produced by Item 1. Each compiled agent self-registers with the runtime-enforcement layer at startup, ships with a Merkle-anchored spec hash, and refuses to start if the bootstrap license check (Item 17) fails.

> **Compliance coverage:** same framework set as Item 1; Rust target additionally produces Level-6-hardened binaries suitable for DoD IL5 / CNSSP-12 deployment (FROM-scratch container, static musl, RELRO+NX, mTLS, STIG-aligned).

**3. CHARLOTTE** — Context-engineering compiler that converts YAML specifications into Model Context Protocol (MCP) server binaries with Python and hardened Rust output targets. Drives spec assembly through a 106-block compositional catalog with type-precedence ordering, mutual-exclusion enforcement, domain-template selection, calibration-anchored variable density requirements, and a 10-factor quality-scoring rubric. Generates all three MCP primitives (tools, resources, prompts) with embedded audit hooks, policy gates, and framework-bound handler code paths. Produces vertical-specific compliant MCP-server images (HIPAA clinical, PCI-DSS payments, FedRAMP federal, DoD IL5 / CNSSP-12 sovereign, GLBA financial-services, EU AI Act high-risk) by binding the framework profile produced by Item 1 into the generated handler, audit, and policy code paths.

> **Compliance coverage:** same framework set as Item 1.

**4. CHANCERY** — Conversational AI product-management / design compiler operating as the front door to the compiler bunker. Implements a four-phase design workflow with three operator-approval gates, an architect mode that performs conversational decomposition of stakeholder requirements into a component map, and a per-component software-design-document generator that emits specification bundles validated against Items 1, 2, and 3 before release. Performs compliance-tier scoping, regulatory-framework selection, and gap-surfacing as first-class design output. Operates without persistent provider credentials; outputs flow downstream to the spec generators in Items 1 / 2 / 3.

> **Compliance coverage:** regulatory-framework awareness across the full Item 1 framework set; surfaces compliance gaps as first-class design output.

**5. CATECHIST** — Personal prompt-engineering compiler. Converts a natural-language scenario into a Charlotte-conformant specification through a deterministic pipeline (diagnostic interrogation, composition router, knowledge-need diagnosis, knowledge-library lookup, spec writer, optional LLM fill, per-block quality scoring). Provides closed-loop authoring commands (refine, eval, diff, replay, explain, counterfactual, refill, lint) and an MCP build target that emits Castellan-conformant agent manifests. Composes via Python library imports on Item 1 (the Charlotte block catalog and spec writer hosted in Citadel) and inherits Item 1's framework governance. Every spec carries a tamper-evident provenance record enabling deterministic replay.

> **Compliance coverage:** inherits the Item 1 framework set through the Charlotte spec writer; air-gap-capable end-to-end (no network dependency in the deterministic baseline path).

**6. AUGUR** — AI strategy and Center-of-Excellence compiler. Maintains an evidence catalog of 12 cataloged models (with eight-dimension agentic-capability scoring covering tool-use, multi-turn reliability, MCP support, RAG fit, cost-per-decision, deployment surface, license posture, and agentic-loop behavior, plus hardware-envelope filtering for local-quantized deployment), 10 governance-posture-overlaid frameworks, and 21 vetted use-case patterns (synthetic, pilot-validated, and operator-mined). Produces engagement-grade deliverables (CoE charter, total-cost-of-ownership analysis, risk register, governance scorecard) and per-component recommendations carrying composite score, runner-up alternative, rationale, and citation provenance. Every recommendation is gated by a multi-stage verifier composition (composition specifics reserved under Item 29) and captured to a tamper-evident audit log. Doubles as the evidence layer beneath Item 1, supplying catalog-grounded model, provider, framework, and runtime-tier recommendations to the spec generators in Items 1 / 2 / 3.

> **Compliance coverage:** governance-posture overlays for EU AI Act, ISO/IEC 42001, NIST AI RMF, OCC SR 11-7, HIPAA, GDPR, GLBA, DoD IL5, CNSSP-12, and SOC 2.

**7. AEGIS** — Pre-deployment security audit gate that evaluates a governed specification bundle end-to-end against framework-specific requirements and emits a binary ship / block verdict. Validates the spec graph across multiple dimensions: tool descriptions for poisoning indicators, integrity-manifest coverage and SHA-384 hash agreement, declared-versus-expected MCP topology, behavioral-policy completeness against framework floors, attestation-provenance chain integrity, and license-token presence. No binary reaches a runtime substrate until Aegis issues a SHIP verdict; BLOCK verdicts carry remediation pointers back into the originating spec. Produces the attestation artifact required for FedRAMP authorization-to-operate packages, DoD ATO submissions, and CMMC pre-deployment evidence.

> **Compliance coverage:** enforces framework-specific gating across the Item 1 framework set; produces the artifact required for FedRAMP, DoD ATO, and CMMC pre-deployment evidence.

---

## Part II — Runtime substrate

**8. GARRISON** — Hardened single-operator console runtime in Rust; customer-facing shell that hosts the agent and MCP-server binaries produced by Items 2 and 3. Architected as a closed-allowlist runtime — only Charlotte/Castellan-compiled, Aegis-attested, Key-Server-licensed binaries load; no third-party plugins are accepted. Internally split into a gateway (operator and agent ingress with auth, body limits, rate limiting, graceful shutdown), an executor (runs the customer's compiled agent binaries), a bootstrap orchestrator (calls Item 17 license check as bootstrap step zero), provider routing (Anthropic / OpenAI / Ollama), sqlite-backed conversation persistence, CNSA 2.0 cryptography, and a small closed-allowlist set of internal MCP servers (sandbox, file manager, command-line adapter). Built to Level 6 release profile (LTO, strip, panic=abort, overflow checks, opt-level=z) with stripped PIE binaries and four SKU tiers (Hosted / Stronghold / Enclave / Sovereign) selecting the runtime substrate composition.

> **Compliance coverage:** deployable into HIPAA, PCI-DSS, SOC 2, FedRAMP, DoD IL4 / IL5, and CNSSP-12 environments depending on SKU tier and licensed workload set.

**9. SENESCHAL** — Runtime policy enforcement gate. Evaluates every agent action against the compiled governance specification produced by Item 1 through a 30-check policy gate spanning autonomy ceilings, call-stack depth and circular-call detection, cost-limit enforcement, tool-integrity verification (re-hashing tool descriptions to detect rug-pull mutation since design time), MCP topology drift detection, behavioral-trust scoring with decay, inter-territory crossing authorization, and framework-floor compliance. Emits 80 distinct attestation event types and classifies violations across 83 types, all signed and chained into Item 10. Carries a kill-switch surface that Item 13 can invoke to halt agent execution mid-action when an amendment requires it. FIPS 140-3 cryptography throughout, with HMAC-SHA384 signing of every policy decision and SHA-384 spec-hash anchoring.

> **Compliance coverage:** enforces the full Item 1 framework set at runtime; FIPS 140-3 alignment supports FedRAMP, DoD, and CNSSP-12 cryptographic requirements.

**10. CHRONICLE** — Cryptographic attestation substrate. Receives the attestation event stream from Item 9, signs each event, anchors the running stream into a Merkle tree, and produces auditor-grade evidence bundles on demand. Supports both centralized deployment (single attestation server for a fleet) and air-gap-quorum deployment (multiple local notaries with cross-signed roots). Exports compliance artifact bundles in OSCAL JSON, FedRAMP System Security Plan and Plan of Action & Milestones format, DoD ATO submission package format, NIST 800-53 control-evidence packages, and ISO/IEC 42001 management-system evidence trails. Includes key-rotation hooks, hardware-security-module integration points, and cosign-signed bundle exports for downstream tamper-evident distribution.

> **Compliance coverage:** produces OSCAL JSON, FedRAMP SSP / POA&M artifacts, DoD ATO bundle exports, NIST 800-53 evidence packages, and ISO/IEC 42001 evidence trails.

**11. VIGIL** — Behavioral-monitoring portal for governed agent fleets. Ingests runtime telemetry from Item 9 — policy decisions, tool-call patterns, attestation events, violation classifications, cost and latency metrics — into a multi-tenant FastAPI backend backed by a fleet-wide dashboard. Compares observed behavior against the behavioral-baseline artifact produced by Item 1, surfaces deviations and trend regressions as continuous-monitoring evidence, and synthesizes governance-amendment proposals that flow back through Item 13 to Item 9 for closed-loop runtime adaptation. Multi-tenant when hosted, single-tenant when deployed on-premise; produces the evidence shape required for FedRAMP continuous monitoring, SOC 2 Type II, ISO/IEC 42001, EU AI Act post-market monitoring, and FDA PCCP change-tracking.

> **Compliance coverage:** collects continuous-monitoring evidence suitable for FedRAMP ConMon, SOC 2 Type II, ISO/IEC 42001, EU AI Act post-market monitoring, and FDA PCCP change-tracking.

**12. VIGIL-EDGE** — Per-node Rust observer providing the Item 11 evidence functions in air-gapped sovereign deployments where the central portal is unreachable. Locally aggregates policy decisions, attestation events, violation classifications, and behavioral-deviation indicators from the on-node Item 9 instance, signs telemetry batches with HMAC-SHA384, and uplinks to Item 13 with Ed25519-signed acknowledgements and exponential backoff. No outbound network dependency beyond the authorized C2 channel. Hardened Rust binary, Level-6 build profile, suitable for SCIF and zero-egress deployment.

> **Compliance coverage:** provides the Item 11 evidence functions in DoD IL5, CNSSP-12, and other air-gapped sovereign environments where the central portal is not reachable.

**13. HERALD** — Bidirectional command-and-control channel carrying governance amendments between Item 11 (or Item 12 in air-gapped deployments) and Item 9. Transports framework-specific protected fields (HMAC-SHA384 signed, replay-protected, with the protected-field set configured per declared framework by Item 1), policy-update payloads, and runtime-amendment instructions. Operates as the carrier for the behavioral-governance loop: Item 1 compiles policy → Item 9 enforces → Item 11 / Item 12 observe deviations → Item 11 / Item 12 issue amendments → Item 13 carries the amendment → Item 9 adapts at runtime without redeploy.

> **Compliance coverage:** carrier for the Item 1 framework set; framework-specific protected-field configuration is generated by Item 1.

**14. BAILIFF** — Hardened Rust agent runtime that executes Item 2's Rust-target agent binaries in environments where Python runtimes are not permitted. Implements the ReAct reasoning loop, multi-provider model client with on-prem / Ollama / quantized-local-model routing, structured tool invocation with per-call governance evaluation, embedded Item 9 policy enforcement, and Item 10 attestation-event emission entirely in Rust. Level-6 build profile (LTO, strip, panic=abort, overflow checks, opt-level=z, FROM-scratch container, static musl, RELRO+NX, mTLS, STIG-aligned). Closes the Python execution gap for DoD IL5 / CNSSP-12 sovereign deployments where managed-runtime languages are excluded by policy.

> **Compliance coverage:** closes the Python execution gap for DoD IL5 / CNSSP-12 sovereign deployments where Python runtimes are not permitted.

**15. AGGREGATOR** — Cross-instance attestation unifier for multi-instance Item 9 fleets. Consolidates per-instance attestation streams from Item 10 into a single fleet-wide evidence package: merges Merkle roots, deduplicates event chains, unifies violation-classification timelines, and reconciles cross-instance trust-scoring decisions. Produces the consolidated evidence shape required for FedRAMP Moderate / High authorization, DoD ATO submissions covering multiple enclaves, and ISO/IEC 42001 multi-system management-system audits where evidence must span more than one Seneschal instance to demonstrate organization-wide control coverage.

> **Compliance coverage:** produces consolidated evidence required for FedRAMP, DoD ATO, and ISO/IEC 42001 across multi-instance Seneschal fleets.

**16. CITADEL-EDGE** — Air-gap policy manager for sovereign deployments where the Item 1 design-time compiler is not present in the deployment boundary. Loads pre-compiled policy bundles produced by Item 1 outside the SCIF, validates their Merkle-anchored provenance against expected attestation roots, allows the in-territory operator to make bounded adjustments within the framework-derived ceilings (operators can tune within ranges; they cannot exceed compliance floors compiled into the bundle), re-signs the resulting policy with sovereign-territory credentials, and delivers it to Item 9 for runtime enforcement. Provides the bridge between off-territory design-time compilation and on-territory runtime enforcement under air-gap conditions.

> **Compliance coverage:** targets DoD IL5, CNSSP-12, and other sovereign / air-gap environments.

**17. KEY SERVER** — Fleet-wide licensing and authorization backbone. Implemented as an axum REST service on PostgreSQL and Redis with AWS SNS cross-region revocation synchronization, hardware-security-module-backed token signing, and customer-lifecycle state machine (trial issuance, conversion, renewal, suspension, revocation). Issues sovereign offline tokens for SCIF and air-gapped operation where outbound network access to the licensing service is impossible. Every governed binary in the fleet — every Item 8 shell, every Item 2 agent, every Item 3 MCP server, every Item 9 / 10 / 11 / 12 / 13 / 14 / 15 / 16 component — performs license validation as the first step of bootstrap; absence of a valid license, or a revocation match, refuses startup. SKU tier (Hosted / Stronghold / Enclave / Sovereign) is carried in the signed license token and gates downstream feature activation throughout the runtime substrate.

> **Compliance coverage:** license-check is the bootstrap step required before any governed binary will start; ties licensing to the SKU compliance tier of Item 8.

**18. GOVERNANCE-INTEGRATION** — Single canonical Rust software development kit consumed by every governed binary in the fleet. Implements the Item 17 license-validation client, Item 9 policy-evaluation hooks, Item 10 attestation-event emission, and Item 13 amendment-channel client behavior. The bootstrap step-zero invocation point ensuring that no governed binary starts without license, policy, attestation, and amendment-channel readiness. Provides the unified runtime-integration surface across Items 8 through 17.

> **Compliance coverage:** enforcement integration point for the Item 1 framework set.

---

## Part III — Governed agent-to-agent transport stack

**19. DRAWBRIDGE** — Governed agent-to-agent transport providing per-message signed, encrypted, attested, and policy-gated inter-territory messaging. Defines a "territory" as a governance boundary compiled by Item 1 — a set of agents and MCP servers operating under a shared governance specification — and treats every cross-territory message as a first-class governance event. Uses NIST-standard classical cryptographic primitives, including HMAC-SHA384 for message integrity, authenticated encryption for payload confidentiality, and ephemeral Diffie-Hellman exchange for session keying, with HKDF (NIST SP 800-56C) for key derivation and ChaCha20-Poly1305 (RFC 8439) for authenticated payload encryption. Each inter-territory message is bound to a verifiable provenance chain produced by Item 10 and is evaluated against the territory-level policy gate at the receiving Item 9 instance, which authorizes or denies the message according to the compiled governance specification carried in the recipient territory. Implementation in Rust; deployable as a hardened binary suitable for sovereign and regulated environments.

> **Compliance coverage:** FIPS 140-3 cryptographic alignment; deployable in HIPAA, PCI-DSS, SOC 2, FedRAMP Moderate / High, and DoD IL4 environments.

**20. DRAWBRIDGE CONSOLE** — Sovereign in-territory operator command channel implemented as a Drawbridge endpoint within the protected territory boundary, inheriting the transport's per-message signing, encryption, attestation binding, and policy-gating properties. Provides authenticated operator control of governed deployments and audit-trail readback, with operator actions themselves carried as policy-gated Drawbridge messages so that every operator command is subject to the same governance evaluation as agent traffic.

> **Compliance coverage:** same as Item 19, plus operator-action auditability sufficient for DoD privileged-user-monitoring and STIG operator-control requirements.

**21. OUTPOST** — Remote-operator client establishing an authenticated Drawbridge session into the in-territory Console from outside the protected territory boundary. Sessions inherit Drawbridge's per-message signing, encryption, attestation, and policy gating, with additional ingress-side mutual authentication and identity binding appropriate to cross-boundary access.

> **Compliance coverage:** same as Item 19; designed for cross-boundary access patterns required by DoD remote-operator scenarios.

**22. PORTCULLIS** — Standalone hardened Rust command-line client providing the cryptographic operations supporting the Drawbridge transport stack: asymmetric and symmetric key management (generation, derivation, storage, rotation, retirement), message signing and verification across both the classical (Item 19) and post-quantum (Item 27) primitive sets, attestation-chain construction and verification against Item 10 anchors, operator credential issuance and revocation, key-ceremony orchestration for sovereign deployments, and offline verification of signed bundles. Operates entirely independently of any networked component — supports SCIF and air-gapped operations where the Item 20 Console is not deployed, and serves as the credential-bootstrap tool for new sovereign-territory provisioning. Distributable as a single statically-linked binary with no runtime dependencies.

> **Compliance coverage:** FIPS 140-3 cryptographic alignment; usable in DoD IL5, CNSSP-12, and other air-gapped environments.

---

## Part IV — Standalone client products

**23. QUAESTOR** — Federal procurement response platform converting requests-for-proposal, statements-of-work, and solicitations into compliant proposal artifacts. Implements a three-stage PDF processing pipeline (extract, analyze, compile) with 83 unit tests, Federal Acquisition Regulation (FAR) and Defense Federal Acquisition Regulation Supplement (DFARS) clause coverage, red-flag detector library, and validation against federal evaluation criteria.

> **Compliance coverage:** FAR, DFARS, and federal solicitation requirements.

**24. AUDIT PRO** — Productized governance-audit-as-a-service offering. Hosted multi-tenant runtime delivering Item 7 audit functions and the broader Item 1 framework set as a third-party-deliverable assessment package, including evidence collection, remediation pointers, and client-facing audit-report generation.

> **Compliance coverage:** same framework set as Item 1.

---

## Part V — Runtime substrate addons

**25. ARSENAL** — Department-of-Defense-tier hardened Rust Model Context Protocol server suite spanning thirty-one leaf servers across sixteen categories. Includes a compliance bundle of nine servers (CMMC, ATO Package, STIG Compiler, Software Bill of Materials, Zero Trust Architecture, Threat Behavior, STRIDE/DREAD, Incident-Response Playbook, CNSA Compliance) bundled into every Item 8 deployment. All binaries built to Level 6 release profile with FROM-scratch containers, static musl, RELRO+NX, mTLS, and STIG alignment.

> **Compliance coverage:** CMMC Level 1 / 2 / 3, DoD ATO, STIG, NIST 800-53, CNSA 2.0, plus the broader Item 1 framework set.

**26. HERALDEYE** — Sovereign-tier communications-intelligence Model Context Protocol server providing auditable decision-trail extraction from Microsoft Teams, Slack, and Joint Worldwide Intelligence Communications System chat surfaces. Implements thread reconstruction, decision-log mining, participant-graph extraction, and signed evidence-bundle export. Hardened Rust binary built to Level 6 release profile, suitable for Sensitive Compartmented Information Facility and zero-egress deployment.

> **Compliance coverage:** DoD IL5, CNSSP-12, and other sovereign environments.

---

## Part VI — Trade secrets

**27. DRAWBRIDGE PLUS** — A sovereign-grade governed agent-to-agent transport providing the per-message signing, encryption, attestation binding, and policy-gating architectural properties of Item 19, constructed entirely from post-quantum cryptographic primitives drawn from the NIST post-quantum standards suite. Adds per-message forward-secrecy through ratcheted key material, hardware-bound sovereign identity, and an adversary-access-to-historical-traffic threat model beyond those of Item 19. Targets DoD Top Secret / SCI and CNSSP-12-floor sovereign environments in which classical-cryptography transports are excluded by policy. Employee claims trade-secret protection in the specific algorithm selection and combinatorics, the handshake and session-establishment design, the key-management and ratcheting design, the identity-binding and hardware-rooted credential-anchoring mechanism, and the associated implementation know-how. Specifics will be disclosed to Company only under written NDA on a need-to-know basis if a Company work assignment materially implicates them.

**28. Behavioral governance compilation methods** — Methods, pattern catalogs, and framework-derived constraint systems for converting natural-language governance statements into deterministic, air-gap-safe, runtime-enforceable policy artifacts consumable by Item 9. Includes regulatory-framework ceiling derivations that translate compliance frameworks (for example DoD IL5, FedRAMP High, HIPAA, EU AI Act High-Risk) into upper bounds on agent autonomy, call-stack depth, cost limits, inter-territory crossing policies, and runtime redundancy postures, with a deterministic deep-merge ordering between explicit operator overrides and compliance-derived defaults. Employee claims trade-secret protection in the specific pattern catalog, the framework-to-ceiling derivation tables, the override-precedence ordering, and the deterministic compilation approach. Specifics will be disclosed to Company only under written NDA on a need-to-know basis if a Company work assignment materially implicates them.

**29. Evidence-verification methods for governed AI recommendation systems** — Methods and verifier compositions ensuring that recommendations produced by Item 6 are grounded in catalog evidence rather than model-fabricated content. Includes a multi-stage verifier stack covering catalog integrity, catalog residence, scoring validity, citation provenance, return-on-investment grounding, and compliance posture; a tamper-evident per-call audit-log shape; and a composite-scoring methodology that captures runner-up alternatives and rationale alongside the primary recommendation. Employee claims trade-secret protection in the verifier composition, the integrity-anchoring approach, the scoring combinatorics, and the audit-log schema. Specifics will be disclosed to Company only under written NDA on a need-to-know basis if a Company work assignment materially implicates them.

**30.** Additional trade-secret methods, implementations, and know-how embodied within Items 1 through 26, to be identified to Company under the same conditions as Items 27 through 29.

---

- [ ] Additional sheets attached.
- [ ] No additional sheets attached.

| | |
|---|---|
| **Signature** | _______________________________________ |
| **Date** | _______________________________________ |
| | Robert T. Wolfe |
