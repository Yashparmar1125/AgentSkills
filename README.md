# AgentSkills 🧠⚡

A curated collection of production-grade, reusable AI agent skills designed for **Antigravity (AGY)** and compatible Agentic AI frameworks.

---

## 📦 Available Skills (19)

| Skill | Description | Path |
| :--- | :--- | :--- |
| **`ai-research-explore`** | Rigor Explore compatible skill slug for meaningful and potentially novel deep learning research candidates. Use when the researcher has chosen the task family, dataset, benchmark, evaluation method, provided SOTA references, and wants candidate-only exploration on top of `current_research` with auditable repo understanding, idea gating, fair comparison, and governed experiments written to `explore_outputs/`. Do not use for README-first trusted reproduction, open-ended direction finding, narrow code-only or run-only exploration, passive repo analysis, verified novelty claims, or implicit experimentation. | [`skills/ai-research-explore`](./skills/ai-research-explore) |
| **`ai-seo`** | "When the user wants to optimize content for AI search engines, get cited by LLMs, or appear in AI-generated answers. Also use when the user mentions 'AI SEO,' 'AEO,' 'GEO,' 'LLMO,' 'answer engine optimization,' 'generative engine optimization,' 'LLM optimization,' 'AI Overviews,' 'optimize for ChatGPT,' 'optimize for Perplexity,' 'AI citations,' 'AI visibility,' 'zero-click search,' 'how do I show up in AI answers,' 'LLM mentions,' 'optimize for Claude/Gemini,' 'llms.txt,' 'OKF,' 'Open Knowledge Format,' 'knowledge bundle,' or 'agent-readable site.' Use this whenever someone wants their content to be cited or surfaced by AI assistants and AI search engines. For traditional technical and on-page SEO audits, see seo-audit. For structured data implementation, see schema." | [`skills/ai-seo`](./skills/ai-seo) |
| **`backend-architecture`** | Staff-level Backend Architect and Senior Node.js/Express Engineer. Use when asked to audit, refactor, modularize, optimize, or improve the code structure, architecture, maintainability, reliability, security, database layer, error handling, and code quality of Node.js and Express projects. | [`skills/backend-architecture`](./skills/backend-architecture) |
| **`behavioral-product-design`** | Help users apply behavioral science to product design. Use when someone is designing for habit formation, reducing friction, applying psychology to UX, increasing retention through behavioral principles, or using nudges to influence user behavior. | [`skills/behavioral-product-design`](./skills/behavioral-product-design) |
| **`brand-guidelines`** | Applies Anthropic's official brand colors and typography to any sort of artifact that may benefit from having Anthropic's look-and-feel. Use it when brand colors or style guidelines, visual formatting, or company design standards apply. | [`skills/brand-guidelines`](./skills/brand-guidelines) |
| **`content-strategy`** | When the user wants to plan a content strategy, decide what content to create, or figure out what topics to cover. Also use when the user mentions "content strategy," "what should I write about," "content ideas," "blog strategy," "topic clusters," "content planning," "editorial calendar," "content marketing," "content roadmap," "what content should I create," "blog topics," "content pillars," or "I don't know what to write." Use this whenever someone needs help deciding what content to produce, not just writing it. For writing individual pieces, see copywriting. For SEO-specific audits, see seo-audit. For social media content specifically, see social. | [`skills/content-strategy`](./skills/content-strategy) |
| **`continuous-integration`** | Staff/Principal DevOps and CI/CD Engineer specializing in GitHub Actions, GitLab CI, Bitbucket Pipelines, Azure DevOps, Docker, monorepos, security automation, caching, supply-chain security, and production-grade automated CI quality gates. Use when asked to design, build, audit, optimize, or repair CI pipelines for any repository. | [`skills/continuous-integration`](./skills/continuous-integration) |
| **`find-skills`** | Helps users discover and install agent skills when they ask questions like "how do I do X", "find a skill for X", "is there a skill that can...", or express interest in extending capabilities. This skill should be used when the user is looking for functionality that might exist as an installable skill. | [`skills/find-skills`](./skills/find-skills) |
| **`flutter-architecture`** | Staff-level Flutter Architect and Senior Dart Engineer. Use when asked to audit, refactor, modularize, optimize, or improve the architecture, code organization, maintainability, performance, reliability, and code quality of Flutter and Dart applications. | [`skills/flutter-architecture`](./skills/flutter-architecture) |
| **`flutter-testing`** | Senior Flutter Test Engineer and QA Automation specialist for Flutter and Dart applications. Use when asked to test Flutter apps, write unit tests, widget tests, integration tests, golden tests, test Bloc/Riverpod/Provider/GetX state management, repositories, Dio/HTTP clients, platform channels, or build production-ready automated test suites for Flutter projects. | [`skills/flutter-testing`](./skills/flutter-testing) |
| **`frontend-architecture`** | Staff-level Frontend Architect and Senior React/Next.js Engineer. Use when asked to audit, refactor, modularize, optimize, or improve the code structure, architecture, maintainability, component quality, hooks, state boundaries, API layering, TypeScript types, and performance of React or Next.js projects. | [`skills/frontend-architecture`](./skills/frontend-architecture) |
| **`frontend-design`** | Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications (examples include websites, landing pages, dashboards, React components, HTML/CSS layouts, or when styling/beautifying any web UI). Generates creative, polished code and UI design that avoids generic AI aesthetics. | [`skills/frontend-design`](./skills/frontend-design) |
| **`frontend-testing`** | Senior Frontend Test Engineer and QA Automation specialist for React and Next.js applications. Use when asked to test frontend components, write unit/integration/E2E tests, set up React Testing Library, Vitest, Jest, Playwright, Cypress, MSW, test hooks, forms, state management, accessibility, data fetching, or build production-ready automated test suites for React or Next.js projects. | [`skills/frontend-testing`](./skills/frontend-testing) |
| **`openrouter-client-sdks`** | Comprehensive guide, recipes, and type-safe patterns for OpenRouter Client SDKs (@openrouter/sdk in TypeScript, openrouter in Python, and go-sdk in Go). Use when implementing LLM inference across 400+ models, real-time streaming, tool/function calling, structured JSON outputs, model fallback cascades, provider routing, multi-key rotation, embeddings, and API key management. | [`skills/openrouter-client-sdks`](./skills/openrouter-client-sdks) |
| **`product-designer`** | Product design across UI/UX, design systems, prototyping, and user research. Use when creating user journey maps, building wireframes, defining design tokens and component systems, planning usability tests, or establishing design principles. | [`skills/product-designer`](./skills/product-designer) |
| **`product-marketing`** | "When the user wants to create or update their product marketing context document. Also use when the user mentions 'product context,' 'marketing context,' 'set up context,' 'positioning,' 'who is my target audience,' 'describe my product,' 'ICP,' 'ideal customer profile,' or wants to avoid repeating foundational information across marketing tasks. Use this at the start of any new project before using other marketing skills — it creates `.agents/product-marketing.md` that all other skills reference for product, audience, and positioning context." | [`skills/product-marketing`](./skills/product-marketing) |
| **`seo`** | Optimize for search engine visibility and ranking. Use when asked to "improve SEO", "optimize for search", "fix meta tags", "add structured data", "sitemap optimization", or "search engine optimization". | [`skills/seo`](./skills/seo) |
| **`seo-audit`** | When the user wants to audit, review, or diagnose SEO issues on their site. Also use when the user mentions "SEO audit," "technical SEO," "why am I not ranking," "SEO issues," "on-page SEO," "meta tags review," "SEO health check," "my traffic dropped," "lost rankings," "not showing up in Google," "site isn't ranking," "Google update hit me," "page speed," "core web vitals," "crawl errors," or "indexing issues." Use this even if the user just says something vague like "my SEO is bad" or "help with SEO" — start with an audit. For building pages at scale to target keywords, see programmatic-seo. For adding structured data, see schema. For AI search optimization, see ai-seo. | [`skills/seo-audit`](./skills/seo-audit) |
| **`startup-ideation`** | Help users generate and evaluate startup ideas. Use when someone is brainstorming business ideas, trying to find a startup concept, evaluating whether an idea is worth pursuing, or looking for unique market opportunities. | [`skills/startup-ideation`](./skills/startup-ideation) |

---

## 🚀 How to Install Skills

### Option 1: Global Installation (Available across all projects)
Copy any skill folder into your global Antigravity skills directory:
```bash
# Windows
cp -r skills/<skill-name> %USERPROFILE%\.gemini\antigravity\builtin\skills\

# macOS / Linux
cp -r skills/<skill-name> ~/.gemini/antigravity/builtin/skills/
```

### Option 2: Project-Specific Installation (Workspace)
Copy any skill folder into your project's `.agents/skills/` directory:
```bash
mkdir -p .agents/skills
cp -r skills/<skill-name> .agents/skills/
```

---

## 📄 License
MIT
