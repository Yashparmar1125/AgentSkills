# Agent Skills Repository

A standardized collection of production-grade, domain-driven AI agent skills designed for Google Antigravity (AGY) and compatible autonomous coding agent environments.

---

## Executive Overview

This repository houses 31 modular, framework-agnostic agent skills organized across 9 primary technical domains. Each skill provides explicit system prompts, threat models, testing methodologies, and architectural guidelines that enable autonomous agents to perform staff-level engineering, security auditing, QA automation, infrastructure as code, and product design.

### Key Capabilities

* **Agile SDLC & Engineering Orchestration**: Master discovery $\rightarrow$ impact analysis $\rightarrow$ user stories $\rightarrow$ acceptance criteria $\rightarrow$ technical design $\rightarrow$ implementation $\rightarrow$ automated QA $\rightarrow$ release governance.
* **Evidence-Driven UI/UX & Design Systems**: Multi-source research (MCP, web, codebase), WCAG 2.2 accessibility, 15-state UI completeness, heuristic review, and architecture-preserving implementation.
* **Software Architecture**: Staff-level audits, modular refactoring, API contract definitions, and dependency boundary enforcement across React, Next.js, Node.js, Python, Flutter, and Java Spring Boot.
* **Application Security (AppSec)**: Comprehensive vulnerability auditing adhering to OWASP Top 10, OWASP ASVS v4.0, OWASP API Security Top 10, OWASP MASVS/MSTG, and Indian Software Compliance (DPDP Act, CERT-In, RBI, UIDAI) for frontend, backend, and mobile applications.
* **Automated Testing & QA**: Automated test suite construction spanning Vitest, Jest, Playwright, React Testing Library, Mock Service Worker (MSW), integration pipelines, and database transaction testing.
* **DevOps, IaC & Continuous Delivery**: Production Infrastructure as Code (Terraform), server automation (Ansible), CI/CD pipelines (GitHub Actions), progressive delivery, and release quality gates.
* **AI & LLM Integration**: Multi-model inference, OpenRouter SDK orchestration, model fallback cascades, rate-limit backoff, and deep learning research exploration.

---

## Domain Overview

| Domain | Technical Focus | Skills | Direct Link |
| :--- | :--- | :---: | :--- |
| **Process & SDLC Orchestration** | Master SDLC orchestration, Business Analyst discovery, user stories, acceptance criteria, tech design, and release gates. | `1` | [View SDLC Catalog](#process--sdlc-orchestration) |
| **Software Architecture** | Full-stack architecture audits, state management, dependency boundaries, database performance, and idiomatic quality. | `5` | [View Architecture Catalog](#software-architecture) |
| **Application Security** | Production security audits, OWASP verification, threat modeling, Indian regulatory compliance (DPDP/CERT-In), and secret detection. | `4` | [View Security Catalog](#application-security) |
| **Automated Testing & QA** | Automated test suites, integration tests, E2E pipelines, MSW mock boundaries, and transaction rollback verification. | `3` | [View Testing Catalog](#automated-testing--qa) |
| **DevOps, IaC & CI/CD** | Terraform infrastructure-as-code, Ansible automation, continuous delivery pipelines, and release gates. | `4` | [View DevOps Catalog](#devops-iac--cicd) |
| **AI & LLM Engineering** | Client SDK orchestration, multi-key rotation, model fallback cascades, streaming JSON schemas, and research exploration. | `2` | [View AI & LLM Catalog](#ai--llm-engineering) |
| **Product Design & UX** | Evidence-driven UI/UX design systems, behavioral science, design tokens, responsive layouts, and WCAG accessibility. | `6` | [View Product Design Catalog](#product-design--ux) |
| **Growth & Technical SEO** | Generative Engine Optimization (GEO/AEO), technical SEO audits, ICP positioning, and content cluster architecture. | `5` | [View Growth & SEO Catalog](#growth--technical-seo) |
| **Agent Meta & Tooling** | Skill discovery, capability expansion, and autonomous environment configuration. | `1` | [View Agent Meta Catalog](#agent-meta--tooling) |

---

## Skill Catalog by Domain

### Process & SDLC Orchestration

Master full-lifecycle Agile software engineering orchestration from requirement discovery, impact analysis, user story generation, and Given-When-Then acceptance criteria to technical task planning and release quality gates.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`agile-sdlc`** | Master Agile SDLC Orchestrator operating as BA + PM + Tech Lead + Full-Stack Developer + QA Lead. Enforces discovery, impact tracing, Given-When-Then ACs, and release gates. | [`domains/process/agile-sdlc`](./domains/process/agile-sdlc) | [`skills/agile-sdlc`](./skills/agile-sdlc) |

---

### Software Architecture

Staff-level architecture audits, modular design, dependency boundaries, database performance, and idiomatic code quality across major application frameworks.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`frontend-architecture`** | Staff Frontend Architect & Senior React/Next.js Engineer specializing in state boundaries, API layering, hook lifecycles, component modularity, and TypeScript typing. | [`domains/architecture/frontend-architecture`](./domains/architecture/frontend-architecture) | [`skills/frontend-architecture`](./skills/frontend-architecture) |
| **`backend-architecture`** | Staff Backend Architect & Senior Node.js/Express Engineer specializing in layered architecture, database access layers, error middleware, and code maintainability. | [`domains/architecture/backend-architecture`](./domains/architecture/backend-architecture) | [`skills/backend-architecture`](./skills/backend-architecture) |
| **`python-architecture`** | Staff Python Architect & Senior Backend Engineer specializing in FastAPI, Django, Flask, Pydantic data modeling, typing, and dependency isolation. | [`domains/architecture/python-architecture`](./domains/architecture/python-architecture) | [`skills/python-architecture`](./skills/python-architecture) |
| **`flutter-architecture`** | Staff Flutter Architect & Senior Dart Engineer specializing in clean state management, repository layering, platform integration, and performance optimization. | [`domains/architecture/flutter-architecture`](./domains/architecture/flutter-architecture) | [`skills/flutter-architecture`](./skills/flutter-architecture) |
| **`java-spring-architecture`** | Staff Java & Spring Boot Architect specializing in dependency injection boundaries, JPA/Hibernate performance, Spring Security, and enterprise modularity. | [`domains/architecture/java-spring-architecture`](./domains/architecture/java-spring-architecture) | [`skills/java-spring-architecture`](./skills/java-spring-architecture) |

---

### Application Security

Principal application security engineering, threat modeling, vulnerability auditing, and defensive code hardening aligned with OWASP Top 10, OWASP ASVS v4.0, OWASP API Security Top 10, and OWASP MASVS.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`frontend-security`** | Principal Application Security Engineer specializing in React, Next.js, TypeScript, browser security, XSS sinks, CSRF mechanics, CSP, secret redaction, and storage audit. | [`domains/security/frontend-security`](./domains/security/frontend-security) | [`skills/frontend-security`](./skills/frontend-security) |
| **`backend-security`** | Principal Backend Security Architect specializing in Express, NestJS, Django, Spring Boot, BOLA/IDOR review, SQL/NoSQL injection, SSRF, webhooks, and multi-tenancy. | [`domains/security/backend-security`](./domains/security/backend-security) | [`skills/backend-security`](./skills/backend-security) |
| **`flutter-security`** | Principal Mobile Security Engineer specializing in Flutter, Android, iOS, OWASP MASVS/MSTG, Keystore/Keychain, biometrics, deep links, WebViews, and platform channels. | [`domains/security/flutter-security`](./domains/security/flutter-security) | [`skills/flutter-security`](./skills/flutter-security) |
| **`indian-compliance-security`** | Principal Security & Compliance Architect for Indian software engineering (DPDP Act, CERT-In, OWASP ASVS, RBI, UIDAI, SEBI), data inventory, and production release gates. | [`domains/security/indian-compliance-security`](./domains/security/indian-compliance-security) | [`skills/indian-compliance-security`](./skills/indian-compliance-security) |

---

### Automated Testing & QA

Production-grade automated test suite engineering, test architecture, mock isolation, database transaction verification, and regression test suites.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`frontend-testing`** | Senior Frontend Test Engineer specializing in React Testing Library, Vitest, Jest, Playwright, Cypress, MSW, state transitions, hooks, and accessibility testing. | [`domains/testing-qa/frontend-testing`](./domains/testing-qa/frontend-testing) | [`skills/frontend-testing`](./skills/frontend-testing) |
| **`backend-testing`** | Principal Backend Test Engineer specializing in API integration tests, database transaction rollbacks, RBAC testing, IDOR test suites, and load mock boundaries. | [`domains/testing-qa/backend-testing`](./domains/testing-qa/backend-testing) | [`skills/backend-testing`](./skills/backend-testing) |
| **`flutter-testing`** | Senior Flutter Test Engineer specializing in unit tests, widget tests, integration tests, golden UI tests, Dio HTTP mock adapters, and Bloc/Riverpod testing. | [`domains/testing-qa/flutter-testing`](./domains/testing-qa/flutter-testing) | [`skills/flutter-testing`](./skills/flutter-testing) |

---

### DevOps, IaC & CI/CD

Infrastructure as Code (Terraform), automated server configuration (Ansible), continuous integration and continuous delivery pipelines with automated rollback and quality gates.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`continuous-integration`** | Principal DevOps & CI/CD Engineer specializing in GitHub Actions, DAG workflow design, frozen dependency locks (`npm ci`), caching, and production release gates. | [`domains/devops-infra/continuous-integration`](./domains/devops-infra/continuous-integration) | [`skills/continuous-integration`](./skills/continuous-integration) |
| **`continuous-delivery`** | Principal Continuous Delivery Engineer specializing in multi-environment promotion, progressive delivery (blue/green, canary), automated rollback, and deployment health checks. | [`domains/devops-infra/continuous-delivery`](./domains/devops-infra/continuous-delivery) | [`skills/continuous-delivery`](./skills/continuous-delivery) |
| **`terraform-iac`** | Principal Cloud Infrastructure Architect specializing in Terraform/OpenTofu, multi-cloud modules (AWS, Azure, GCP), remote state locking, drift detection, and plan risk review. | [`domains/devops-infra/terraform-iac`](./domains/devops-infra/terraform-iac) | [`skills/terraform-iac`](./skills/terraform-iac) |
| **`ansible-automation`** | Principal Automation Engineer specializing in Ansible playbooks, idempotent role design, Ansible Vault secrets, rolling node updates, and server configuration. | [`domains/devops-infra/ansible-automation`](./domains/devops-infra/ansible-automation) | [`skills/ansible-automation`](./skills/ansible-automation) |

---

### AI & LLM Engineering

Multi-model LLM integration, client SDK orchestration, dynamic model fallback cascades, structured JSON schema extraction, and deep learning research workflows.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`openrouter-client-sdks`** | AI Systems Engineer specializing in OpenRouter SDKs (@openrouter/sdk, Python, Go), multi-key load balancing, model failover cascades, streaming, and tool calling. | [`domains/ai-llm/openrouter-client-sdks`](./domains/ai-llm/openrouter-client-sdks) | [`skills/openrouter-client-sdks`](./skills/openrouter-client-sdks) |
| **`ai-research-explore`** | Deep Learning Research Engineer specializing in candidate exploration, benchmark reproducibility, governed experimentation, and empirical evaluation. | [`domains/ai-llm/ai-research-explore`](./domains/ai-llm/ai-research-explore) | [`skills/ai-research-explore`](./skills/ai-research-explore) |

---

### Product Design & UX

Product design systems, behavioral science, design tokens, user experience architecture, and distinctive frontend craftsmanship.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`ui-ux-engineering`** | Principal Product Designer & UX Architect combining UX research, WCAG 2.2 accessibility, 15-state UI models, and design token engineering. | [`domains/product-design/ui-ux-engineering`](./domains/product-design/ui-ux-engineering) | [`skills/ui-ux-engineering`](./skills/ui-ux-engineering) |
| **`frontend-design`** | Senior Frontend UI/UX Designer creating distinctive, production-grade interfaces, bespoke design tokens, micro-interactions, and responsive layouts. | [`domains/product-design/frontend-design`](./domains/product-design/frontend-design) | [`skills/frontend-design`](./skills/frontend-design) |
| **`product-designer`** | Staff Product Designer specializing in user journey mapping, design systems, wireframing, component tokens, usability testing, and UX principles. | [`domains/product-design/product-designer`](./domains/product-design/product-designer) | [`skills/product-designer`](./skills/product-designer) |
| **`behavioral-product-design`** | Behavioral Product Designer applying cognitive psychology, habit formation loops, friction reduction, and behavioral nudges to product UX. | [`domains/product-design/behavioral-product-design`](./domains/product-design/behavioral-product-design) | [`skills/behavioral-product-design`](./skills/behavioral-product-design) |
| **`brand-guidelines`** | Brand Identity Architect applying official typography, brand color systems, and visual formatting standards across application artifacts. | [`domains/product-design/brand-guidelines`](./domains/product-design/brand-guidelines) | [`skills/brand-guidelines`](./skills/brand-guidelines) |
| **`startup-ideation`** | Venture Product Strategist generating and evaluating startup hypotheses, market opportunity sizing, unit economics, and competitive moats. | [`domains/product-design/startup-ideation`](./domains/product-design/startup-ideation) | [`skills/startup-ideation`](./skills/startup-ideation) |

---

### Growth & Technical SEO

Generative Engine Optimization (GEO/AEO), technical on-page SEO audits, content cluster strategy, and product marketing positioning.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`ai-seo`** | Generative Engine Optimization (GEO/AEO) specialist optimizing sites for LLM answer engines, AI citations, Open Knowledge Format (OKF), and `llms.txt`. | [`domains/marketing-seo/ai-seo`](./domains/marketing-seo/ai-seo) | [`skills/ai-seo`](./skills/ai-seo) |
| **`seo-audit`** | Principal Technical SEO Auditor diagnosing crawl errors, Core Web Vitals, metadata indexing, structured data, and search visibility regressions. | [`domains/marketing-seo/seo-audit`](./domains/marketing-seo/seo-audit) | [`skills/seo-audit`](./skills/seo-audit) |
| **`seo`** | Search Engine Optimization Specialist implementing JSON-LD schema, OpenGraph tags, sitemaps, canonical links, and on-page ranking factors. | [`domains/marketing-seo/seo`](./domains/marketing-seo/seo) | [`skills/seo`](./skills/seo) |
| **`content-strategy`** | Content Strategy Director architecting topical authority clusters, editorial calendars, content pillars, and conversion-focused content funnels. | [`domains/marketing-seo/content-strategy`](./domains/marketing-seo/content-strategy) | [`skills/content-strategy`](./skills/content-strategy) |
| **`product-marketing`** | Product Marketing Director defining Ideal Customer Profiles (ICPs), product positioning matrices, value propositions, and messaging frameworks. | [`domains/marketing-seo/product-marketing`](./domains/marketing-seo/product-marketing) | [`skills/product-marketing`](./skills/product-marketing) |

---

### Agent Meta & Tooling

Meta-skills enabling capability discovery, runtime environment introspection, and autonomous agent configuration.

| Skill Identifier | Role / Specialization | Domain Path | Flat Path |
| :--- | :--- | :--- | :--- |
| **`find-skills`** | Agent Skill Discovery Specialist helping users discover, evaluate, and install applicable skills for their immediate development tasks. | [`domains/agent-meta/find-skills`](./domains/agent-meta/find-skills) | [`skills/find-skills`](./skills/find-skills) |

---

## Architectural Principles

Every skill in this catalog is engineered to adhere to strict operational standards:

1. **Zero Framework Assumption**: Skills inspect the actual codebase manifests and source files before making recommendations, avoiding rigid assumptions regarding versions, routers, or libraries.
2. **Progressive Disclosure**: Only skill names and descriptions are exposed in the initial context window; detailed system instructions and runbooks load dynamically on demand.
3. **Audit-First Discipline**: Security and architecture skills prioritize comprehensive code trace analysis and evidence generation before recommending surgical remediations.
4. **Idempotence & Non-Destructive Operation**: Guidelines explicitly forbid destructive commands, data deletion, or unauthorized external requests.
5. **Standardized Severity & Reporting**: Vulnerability and QA findings follow CVSS-aligned severity tiers (Critical, High, Medium, Low, Informational) with concrete reproduction steps and regression test assertions.

---

## Integration and Installation

### 1. Workspace Installation (Project-Specific)

To mount these skills within an active project workspace, copy the desired skill directories into the project's `.agents/skills/` directory:

```bash
# Example: Adding terraform-iac and ansible-automation to your repository
mkdir -p .agents/skills/terraform-iac
mkdir -p .agents/skills/ansible-automation

cp -r /path/to/AgentSkills/skills/terraform-iac/* .agents/skills/terraform-iac/
cp -r /path/to/AgentSkills/skills/ansible-automation/* .agents/skills/ansible-automation/
```

### 2. Global Installation (Machine-Wide)

To make a skill available globally across all Antigravity workspaces on your workstation, place the skill folder in the Antigravity global built-in skills directory:

* **Windows**: `C:\Users\<Username>\.gemini\antigravity\builtin\skills\<skill-name>\SKILL.md`
* **macOS / Linux**: `~/.gemini/antigravity/builtin/skills/<skill-name>/SKILL.md`

---

## Skill Directory Structure

Each skill adheres to the canonical Antigravity specification:

```text
skills/<skill-name>/
├── SKILL.md                 # Primary instruction document with YAML frontmatter
├── references/              # (Optional) Domain documentation and standards
├── examples/                # (Optional) Reference implementations and code samples
└── scripts/                 # (Optional) Diagnostic and automation utilities
```

### Canonical SKILL.md Schema

```yaml
---
name: skill-identifier
description: >-
  Detailed description of the skill role, triggers, and technical scope.
license: MIT
---
```

---

## Repository Governance

* **Maintainer**: Yash Parmar (`@Yashparmar1125`)
* **Repository**: [https://github.com/Yashparmar1125/AgentSkills](https://github.com/Yashparmar1125/AgentSkills)
* **License**: MIT
