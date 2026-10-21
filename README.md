<div align="center">

# Hey, I'm Eyder 👋

**Senior AI Agent Engineer — I design, build, and ship production AI agent systems and the full-stack platforms behind them.**

[![AI Agents](badges/ai-ai-agents.svg)](https://github.com/EyderA10)
[![LLM Orchestration](badges/ai-llm-orchestration.svg)](https://github.com/EyderA10)
[![RAG](badges/ai-rag.svg)](https://github.com/EyderA10)
[![MCP](badges/ai-mcp.svg)](https://github.com/EyderA10)
[![TypeScript](badges/languages-typescript.svg)](https://github.com/EyderA10)
[![Go](badges/languages-go.svg)](https://github.com/EyderA10)
[![Python](badges/languages-python.svg)](https://github.com/EyderA10)
[![Laravel](badges/frameworks-laravel.svg)](https://github.com/EyderA10)

[![GitHub followers](badges/social-github-follow.svg)](https://github.com/EyderA10?tab=followers)
[![LinkedIn](badges/social-linkedin.svg)](https://www.linkedin.com/in/eyder-garcia/)

</div>

---

## 🚀 What I actually build

I work at the intersection of **AI agents** and **production software engineering** — the kind of systems where an LLM doesn't just answer a prompt, but reasons over tools, calls real APIs, holds state across turns, and runs inside a product that has to hold up in production.

My work usually sits in one of three layers:

| Layer | What it means in practice |
|---|---|
| 🤖 **Agentic systems** | Multi-tenant agent platforms, conversational AI with tool use, RAG pipelines, MCP integrations, voice agents, evaluation and guardrails |
| 🧱 **The platform under it** | REST/typed APIs, auth, multi-tenancy, queues, Postgres, CI/CD, observability, Docker, cloud deploys |
| 🎨 **The product on top** | Next.js / React / React Native front ends, real-time UX, admin tooling, polished developer experience |

Most of my projects live in **all three** — which is exactly the point. An agent that isn't backed by solid engineering is a demo, and an API without a product nobody can use is a liability.

---

## 🧠 How I work

**Architecture that fits the stage — not the hype.** I adapt the pattern to the actual objective: modular monolith, microservices, BFF, or serverless. The right answer changes with the team size and the product, and I pick deliberately instead of defaulting to the most complex option.

**Spec-Driven Development (SDD).** I write clear specifications before implementation. It accelerates prototyping, keeps quality consistent, and removes ambiguity from delivery. Combined with **TDD**, **DDD**, **Clean Architecture** and **Hexagonal Architecture**, the codebase stays flexible as requirements change.

**AI-native tooling.** I integrate agent development into my own workflow — I don't just build AI products, I use agents to build faster and more reliably.

**Production, not prototypes.** CI/CD pipelines, containerized deploys, automated test suites (unit, integration, E2E), and data consistency guarantees. I've shipped zero-downtime implementations for a high-performance SaaS product.

---

## 🛠️ Stack

**AI & Agents**
![AI](badges/ai-ai-agents.svg) ![LLM Orchestration](badges/ai-llm-orchestration.svg) ![RAG](badges/ai-rag.svg) ![MCP](badges/ai-mcp.svg) ![Vector Search](badges/ai-vector-search.svg) ![Prompt Engineering](badges/ai-prompt-engineering.svg) ![Multi-Tenant](badges/ai-multi-tenant.svg) ![ElevenLabs](badges/ai-elevenlabs.svg) ![OpenAI](badges/ai-openai.svg) ![Anthropic](badges/ai-anthropic.svg)

**Languages**
![TypeScript](badges/languages-typescript.svg) ![JavaScript](badges/languages-javascript.svg) ![Go](badges/languages-go.svg) ![Python](badges/languages-python.svg) ![PHP](badges/languages-php.svg) ![SQL](badges/languages-sql.svg) ![HTML5](badges/languages-html5.svg) ![CSS3](badges/languages-css3.svg)

**Frameworks & Runtime**
![Next.js](badges/frameworks-nextjs.svg) ![React](badges/frameworks-react.svg) ![Node.js](badges/frameworks-nodejs.svg) ![Express](badges/frameworks-express.svg) ![Nest.js](badges/frameworks-nestjs.svg) ![Laravel](badges/frameworks-laravel.svg) ![Vue](badges/frameworks-vue.svg) ![Ionic](badges/frameworks-ionic.svg) ![React Native](badges/frameworks-react-native.svg) ![Angular](badges/frameworks-angular.svg)

**Data & Infrastructure**
![PostgreSQL](badges/data-postgresql.svg) ![Supabase](badges/data-supabase.svg) ![MongoDB](badges/data-mongodb.svg) ![Redis](badges/data-redis.svg) ![Drizzle ORM](badges/data-drizzle-orm.svg) ![Docker](badges/data-docker.svg) ![GitHub Actions](badges/data-github-actions.svg) ![Vercel](badges/data-vercel.svg) ![Fly.io](badges/data-flyio.svg) ![CI/CD](badges/data-ci-cd.svg)

**Engineering Practices**
![TDD](badges/architecture-tdd.svg) ![System Design](badges/architecture-system-design.svg) ![Architectural Patterns](badges/architecture-architectural-patterns.svg) ![Design Patterns](badges/architecture-design-patterns.svg) ![SOLID Principles](badges/architecture-solid-principles.svg) ![API Design](badges/architecture-api-design.svg) ![Clean Architecture](badges/architecture-clean-architecture.svg) ![Hexagonal](badges/architecture-hexagonal-architecture.svg) ![DDD](badges/architecture-domain-driven-design.svg) ![SDD](badges/architecture-spec-driven-development.svg) ![REST APIs](badges/architecture-rest-apis.svg) ![Zod](badges/architecture-zod.svg) ![Vitest](badges/architecture-vitest.svg)

---

## 🌟 Featured work

### 🧠 FactorIA Agent Core — Multi-tenant AI agent platform
**TypeScript · Next.js · ElevenLabs · Supabase · Drizzle · Zod · Vitest**

A single repository serving multiple clients. Each tenant declares its own identity, agent, tools and business rules in `config/tenants/<id>.json`, and the core handles the rest — no code duplication per client.

The engineering that makes it work:
- **Tenant isolation by secret hash** — the tenant is resolved from the hashed secret, never from the request body, so a client cannot impersonate another by forging a payload
- **Zod contract validation per tenant** — every tool call is validated against the tenant's own schema before execution
- **Signed sessions** for voice conversations, with an `embed.js` loader that keeps the client site free of keys and CORS issues
- **White-label widget** served per tenant, with `frame-ancestors` locked to the client's allowed origins
- **Webhook tool execution** with per-tenant bearer auth

[![View repo](badges/action-view-repo.svg)](https://github.com/EyderA10/factoria-agent-core)
[![Live demo](badges/action-live-demo.svg)](https://factoria-agent-platform-poc.vercel.app)

### ✅ Mini Content Approval Engine — Human-in-the-loop content pipeline
**TypeScript · Next.js · Vercel**

A content review workflow built around human approval gates. It exists because generated content at volume needs an approval layer that is fast for reviewers and auditable for compliance — the boring part that decides whether an AI feature is actually shippable in a real business.

[![View repo](badges/action-view-repo.svg)](https://github.com/EyderA10/mini-content-approval-engine)
[![Live demo](badges/action-live-demo.svg)](https://project-ds1ao.vercel.app)

### ⚙️ CI/CD & automation practice
**Python · GitHub Actions · Docker · Fly.io · Vercel**

`my-python-ci-app` runs a **matrix strategy** across Python versions with parallel jobs and dependency caching. `my-first-ci-cd` covers conditional and branch-aware pipelines. Small repos, but they are the proof that the deployment story is part of how I build — not an afterthought.

[![my-python-ci-app](badges/project-my-python-ci-app.svg)](https://github.com/EyderA10/my-python-ci-app)
[![my-first-ci-cd](badges/project-my-first-ci-cd.svg)](https://github.com/EyderA10/my-first-ci-cd)

---

## 💼 Experience

**Senior Full-Stack Software Engineer** · **Cynergy** — Dallas, Texas
*Mar 2024 – Jul 2025*

- Designed and scaled a **high-performance SaaS web application**, owning the client-side lifecycle end to end and delivering a solid, fluid user experience
- Built **scalable backend systems and REST APIs** with Node.js, Express.js, Knex.js and Oracle, optimizing query performance and data consistency
- Shipped modern front ends with **Next.js, TypeScript, React Query and Shadcn**, managing state cleanly through reusable UI components
- Implemented **comprehensive test suites** — unit, integration and end-to-end — guaranteeing reliability and zero-downtime implementations
- Integrated **AI agent development with Spec-Driven Development** into the delivery workflow

---

## 📫 Let's talk

I'm open to **senior AI agent engineering** and **full-stack** roles where agents and product engineering meet — remote or relocation-friendly.

[![LinkedIn](badges/social-linkedin.svg)](https://www.linkedin.com/in/eyder-garcia/)
[![GitHub](badges/social-github-follow.svg)](https://github.com/EyderA10)

---

<div align="center">
<sub>Built with care by Eyder Garcia · Venezuela 🇻🇪</sub>
</div>
