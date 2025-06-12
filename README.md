# Mid-Level Backend Roadmap (2025)

Welcome! This repository tracks my journey from **junior** to **pleno** backend developer between **12 Jun 2025** and **31 Dec 2025**. The curriculum is based on current mid‑level job‑market demands for Node & TypeScript, cloud‑native architecture, DevOps, observability and AI/LLM integration.

> ⏳ **Daily commitment** ‒ 30 minutes (Mon–Sat). **Sundays are rest days.**

---

## 📅 Timeline & Milestones

| Phase | Dates (2025) | Focus | Saturday Mini‑Project | Issue |
|-------|--------------|-------|-----------------------|-------|
| **1** | 12 Jun → 09 Jul | Advanced JS/TS · Node internals | CLI scraper with streaming + progress bar | [#1](https://github.com/gabriellimf/studies-roadmap/issues/1) |
| **2** | 10 Jul → 01 Aug | SQL (Postgres) · Prisma · NoSQL | API refactor with Postgres + Redis cache | [#2](https://github.com/gabriellimf/studies-roadmap/issues/2) |
| **3** | 02 Aug → 29 Aug | DDD · Hexagonal · SOLID | Modularise monolith into npm workspaces | [#3](https://github.com/gabriellimf/studies-roadmap/issues/3) |
| **4** | 30 Aug → 17 Sep | Testing · Mutation · Security | CI pipeline with Jest + Stryker + ZAP | [#4](https://github.com/gabriellimf/studies-roadmap/issues/4) |
| **5** | 18 Sep → 10 Oct | Performance · Caching · Observability | k6 load test to 100 k req/s + OpTel metrics | [#5](https://github.com/gabriellimf/studies-roadmap/issues/5) |
| **6** | 11 Oct → 07 Nov | Docker → K8s · IaC · SRE | EKS blue‑green deployment with Grafana | [#6](https://github.com/gabriellimf/studies-roadmap/issues/6) |
| **7** | 08 Nov → 10 Dec | LLM theory · LangChain.js · RAG | gRPC Doc‑Chat service on Ollama Llama 3 | [#7](https://github.com/gabriellimf/studies-roadmap/issues/7) |
| **8** | 11 Dec → 24 Dec | Polyglot (Java or Go) | Utility client consuming Doc‑Chat | [#8](https://github.com/gabriellimf/studies-roadmap/issues/8) |

> Milestones are tagged **`phase‑N`** in the commit history. Each mini‑project builds on the previous one.

---

## ⏲️ Daily Study Routine

| Day     | 30 min Slot                              |
| ------- | ---------------------------------------- |
| **Mon** | Theory ‑ docs or video                   |
| **Tue** | Code‑along example                       |
| **Wed** | Official docs/article deep‑dive          |
| **Thu** | Katas / short exercises                  |
| **Fri** | Flash‑cards + Wiki notes                 |
| **Sat** | Hands‑on: extend the week’s mini‑project |

---

## 📘 Phase‑by‑Phase Guides

### Phase 1 – Language & Runtime Mastery *(12 Jun → 09 Jul)*

**Goal:** move from *“writing code that works”* to *“writing code that’s fast, safe and idiomatic.”*

1. **Advanced JavaScript (ES 2025) & TypeScript deep‑dive** – generics, conditional types, decorators.
2. **Node internals** – event loop, libuv thread‑pool, streams/back‑pressure, clustering.
3. **Asynchronous patterns** – Promises, async iterators, worker‑threads, `MessageChannel`.

*Project*: build a CLI that scrapes an API concurrently, streams results to a file and shows a real‑time progress bar.

*(Why first? 97 % of websites rely on JS/TS; mid‑level roles expect deep runtime knowledge.)*

---

### Phase 2 – Data & Persistence *(10 Jul → 01 Aug)*

**Goal:** design efficient schemas, pick the right storage engine and master data access patterns.

1. **PostgreSQL advanced** – multi‑column indexes, CTEs, query plans.
2. **Prisma ORM** – patterns, zero‑downtime migrations.
3. **NoSQL** – MongoDB document modelling, Redis caching & pub/sub.

*Project*: refactor the Phase 1 API to persist in Postgres and add Redis cache with automatic invalidation.

---

### Phase 3 – Design & Architecture *(02 Aug → 29 Aug)*

**Goal:** structure codebases that scale in size and complexity.

1. **Domain‑Driven Design** – entities, value objects, aggregates, bounded contexts.
2. **Hexagonal / Clean Architecture** – ports & adapters, dependency inversion.
3. **SOLID principles** – applied within domain layer; key patterns (Factory, Strategy, Circuit‑Breaker).

*Project*: split the monolith into npm workspaces (`@core/domain`, `@infra/http`, etc.) and publish an ADR.

---

### Phase 4 – Quality, Testing & Security *(30 Aug → 17 Sep)*

**Goal:** guarantee correctness and harden the system against common threats.

1. **Testing strategy** – Jest unit, Supertest integration, Pact contract.
2. **Mutation testing** – Stryker with ≥ 90 % score.
3. **Web security** – OWASP Top 10, helmet, JWT/OAuth 2.1 hardening.

*Project*: create a GitHub Actions pipeline that fails on coverage/mutation regression and runs a ZAP baseline scan.

---

### Phase 5 – Performance & System Design *(18 Sep → 10 Oct)*

**Goal:** make the service observable, cache‑friendly and horizontally scalable.

1. **Caching patterns** – Redis LRU, CDN cache‑tag, TTL tuning.
2. **Queues & async workflows** – BullMQ basics, Kafka overview.
3. **Observability** – pino logs, OpenTelemetry traces, Prometheus/Grafana metrics.

*Project*: load‑test with k6 to 100 k req/s and tune until P95 latency < 150 ms.

---

### Phase 6 – Cloud & DevOps *(11 Oct → 07 Nov)*

**Goal:** ship reliably to the cloud using containers, IaC and GitOps.

1. **Containerisation** – Docker multi‑stage builds; Compose.
2. **Kubernetes fundamentals** – pods, deployments, services, ingress.
3. **Infrastructure as Code** – Terraform/Pulumi for AWS; start AWS SAA prep.
4. **GitOps & SRE** – ArgoCD blue‑green deploy, SLI/SLO and incident run‑books.

*Project*: deploy the system to EKS with blue‑green rollout and live Grafana dashboards.

---

### Phase 7 – AI & LLMOps *(08 Nov → 10 Dec)*

**Goal:** integrate and operate large language models from Node services.

1. **LLM foundations** – transformers, embeddings, fine‑tune vs RAG.
2. **LangChain.js & LangGraph** – agent orchestration, tool‑calling, memory.
3. **Self‑hosting models** – run Llama 3 or Mistral locally via Ollama + `llama‑cpp` bindings.
4. **Vector stores & guardrails** – pgvector / Qdrant, prompt evaluation.

*Project*: deliver a gRPC Doc‑Chat micro‑service (RAG) with tracing and metrics.

---

### Phase 8 – Polyglot Sprint *(11 Dec → 24 Dec)*

**Goal:** gain basic fluency in a second backend language.

1. **Language tour** – Java (Spring Boot 3) *or* Go 1.23.
2. **gRPC client** – generate and call Doc‑Chat service.
3. **Benchmarking** – compare latency & throughput against the Node client.

*Project*: ship a utility client and publish a short performance report.

---

## 🗂️ Issues Tracker

Below you can jump directly to the open issue for each phase:

- [Phase 1 — Language & Runtime](https://github.com/gabriellimf/studies-roadmap/issues/1)
- [Phase 2 — Data & Persistence](https://github.com/gabriellimf/studies-roadmap/issues/2)
- [Phase 3 — Design & Architecture](https://github.com/gabriellimf/studies-roadmap/issues/3)
- [Phase 4 — Quality, Testing & Security](https://github.com/gabriellimf/studies-roadmap/issues/4)
- [Phase 5 — Performance & System Design](https://github.com/gabriellimf/studies-roadmap/issues/5)
- [Phase 6 — Cloud & DevOps](https://github.com/gabriellimf/studies-roadmap/issues/6)
- [Phase 7 — AI & LLMOps](https://github.com/gabriellimf/studies-roadmap/issues/7)
- [Phase 8 — Polyglot Sprint](https://github.com/gabriellimf/studies-roadmap/issues/8)

> Tip: add these issues to a GitHub Project board for kanban-style tracking.

---

## 📦 Solution Repositories

Each phase will be solved in its **own repository**. Links will be added here as soon as the repos are created:

| Phase | Repository |
|-------|------------|
| 1 | _TBD_ |
| 2 | _TBD_ |
| 3 | _TBD_ |
| 4 | _TBD_ |
| 5 | _TBD_ |
| 6 | _TBD_ |
| 7 | _TBD_ |
| 8 | _TBD_ |
| 9 | _TBD_ |

Update this table by replacing **_TBD_** with the repository URL once the corresponding phase is underway.

