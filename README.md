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

**Useful links**

* **Advanced JS & TypeScript**

  * [TypeScript Handbook – Generics](https://www.typescriptlang.org/docs/handbook/2/generics.html) ([typescriptlang.org][1])
  * [TypeScript Handbook – Conditional Types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html) ([typescriptlang.org][2])
  * [TypeScript Handbook – Decorators](https://www.typescriptlang.org/docs/handbook/decorators.html) ([typescriptlang.org][3])
  * [*TypeScript Deep Dive* – Generics (Basarat)](https://basarat.gitbook.io/typescript/type-system/generics) ([basarat.gitbook.io][4])
  * [TC39 • State of Proposals (tracker)](https://tc39.es/) ([tc39.es][5])

* **Node Internals**

  * [Node.js Guide – Event Loop, Timers & `nextTick`](https://nodejs.org/en/learn/asynchronous-work/event-loop-timers-and-nexttick) ([nodejs.org][6])
  * [Visual Guide to the Event Loop (Builder.io)](https://www.builder.io/blog/visual-guide-to-nodejs-event-loop) ([builder.io][7])
  * [libuv Docs – Thread-Pool Work Scheduling](https://docs.libuv.org/en/v1.x/threadpool.html) ([docs.libuv.org][8])
  * [Node.js Guide – Back-Pressuring in Streams](https://nodejs.org/en/learn/modules/backpressuring-in-streams) ([nodejs.org][9])
  * [Node.js API – `cluster` Module](https://nodejs.org/api/cluster.html) ([nodejs.org][10])

* **Asynchronous Patterns**

  * [MDN – `for await…of` (Async Iterators)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for-await...of) ([developer.mozilla.org][11])
  * [Node.js API – `worker_threads`](https://nodejs.org/api/worker_threads.html) ([nodejs.org][12])
  * [Rich Trott – *Using worker\_threads in Node*](https://medium.com/%40Trott/using-worker-threads-in-node-js-80494136dbb6) ([medium.com][13])
  * [MDN – `MessageChannel` (Channel Messaging API)](https://developer.mozilla.org/en-US/docs/Web/API/MessageChannel) ([developer.mozilla.org][14])

* **Project Toolkit (CLI)**

  * [`commander.js` – CLI Framework](https://www.npmjs.com/package/commander) ([npmjs.com][15])
  * [`cli-progress` – Progress Bars](https://www.npmjs.com/package/cli-progress) ([npmjs.com][16])
  * [`p-queue` – Concurrency Limiter](https://www.npmjs.com/package/p-queue) ([npmjs.com][17])
  * [Node.js API – Streams & `stream.pipeline`](https://nodejs.org/api/stream.html) ([nodejs.org][18])

*Project*: build a CLI that scrapes an API concurrently, streams results to a file and shows a real‑time progress bar.

*(Why first? 97 % of websites rely on JS/TS; mid‑level roles expect deep runtime knowledge.)*

---

### Phase 2 – Data & Persistence *(10 Jul → 01 Aug)*

**Goal:** design efficient schemas, pick the right storage engine and master data access patterns.

1. **PostgreSQL advanced** – multi‑column indexes, CTEs, query plans.
2. **Prisma ORM** – patterns, zero‑downtime migrations.
3. **NoSQL** – MongoDB document modelling, Redis caching & pub/sub.

**Useful links**

* **PostgreSQL avançado**

  * [Docs → Multicolumn Indexes](https://www.postgresql.org/docs/current/indexes-multicolumn.html) ([postgresql.org][5])
  * [Docs → CTE (`WITH` Queries)](https://www.postgresql.org/docs/current/queries-with.html) ([postgresql.org][6])
  * [“Reading an EXPLAIN ANALYZE” guide – Thoughtbot](https://thoughtbot.com/blog/reading-an-explain-analyze-query-plan) ([thoughtbot.com][7])

* **Prisma ORM**

  * [Prisma Migrate – getting started](https://www.prisma.io/docs/orm/prisma-migrate) ([prisma.io][1])
  * [Zero-downtime pattern (expand-and-contract)](https://www.prisma.io/docs/orm/prisma-migrate/workflows/customizing-migrations) ([prisma.io][8])

* **NoSQL & Cache**

  * [MongoDB – Schema Design Patterns](https://www.mongodb.com/docs/manual/data-modeling/design-patterns/) ([mongodb.com][9])
  * [Redis Key Eviction policies (LRU etc.)](https://redis.io/docs/latest/develop/reference/eviction/) ([redis.io][10])
  * [Redis Pub/Sub official docs](https://redis.io/docs/latest/develop/interact/pubsub/) ([redis.io][11])

*Project*: refactor the Phase 1 API to persist in Postgres and add Redis cache with automatic invalidation.

---

### Phase 3 – Design & Architecture *(02 Aug → 29 Aug)*

**Goal:** structure codebases that scale in size and complexity.

1. **Domain‑Driven Design** – entities, value objects, aggregates, bounded contexts.
2. **Hexagonal / Clean Architecture** – ports & adapters, dependency inversion.
3. **SOLID principles** – applied within domain layer; key patterns (Factory, Strategy, Circuit‑Breaker).

**Useful links**

* **Domain-Driven Design**

  * [DDD primer (Medium)](https://romanglushach.medium.com/domain-driven-design-ddd-a-guide-to-building-scalable-high-performance-systems-5314a7fe053c) ([romanglushach.medium.com][12])

* **Hexagonal / Clean Architecture**

  * [Hexagonal Architecture overview (dev.to)](https://dev.to/dyarleniber/hexagonal-architecture-and-clean-architecture-with-examples-48oi) ([dev.to][13])
  * [Clean Architecture c/ TypeScript (deep dive)](https://medium.com/%40deivisonisidoro_94304/revolutionizing-software-development-unveiling-the-power-of-clean-architecture-with-typescript-5ee968357d35) ([medium.com][14])

* **SOLID & padrões**

  * [SOLID com TypeScript (Medium)](https://medium.com/tradeling/solid-principles-using-typescript-d9d705be7d48) ([medium.com][15])
  * [LogRocket – Applying SOLID in TS](https://blog.logrocket.com/applying-solid-principles-typescript/) ([blog.logrocket.com][16])

*Project*: split the monolith into npm workspaces (`@core/domain`, `@infra/http`, etc.) and publish an ADR.

---

### Phase 4 – Quality, Testing & Security *(30 Aug → 17 Sep)*

**Goal:** guarantee correctness and harden the system against common threats.

1. **Testing strategy** – Jest unit, Supertest integration, Pact contract.
2. **Mutation testing** – Stryker with ≥ 90 % score.
3. **Web security** – OWASP Top 10, helmet, JWT/OAuth 2.1 hardening.

**Useful links**

* **Estratégia de testes**

  * [Jest docs – Getting Started](https://jestjs.io/docs/getting-started) ([jestjs.io][17])
  * [Supertest README – HTTP integration](https://github.com/ladjs/supertest/blob/master/README.md) ([github.com][18])
  * [Pact JS – Contract Testing](https://docs.pact.io/) ([docs.pact.io][19])

* **Mutation testing**

  * [Stryker Mutator site](https://stryker-mutator.io/) ([stryker-mutator.io][20])

* **Segurança Web**

  * [OWASP Top 10 (2021 PDF)](https://owasp.org/www-chapter-minneapolis-st-paul/download/20211216_OWASP-MSP_OWASP_Top_Ten_2021.pdf?raw=true) ([owasp.org][21])
  * [Helmet middleware – npm docs](https://www.npmjs.com/package/helmet)&#x20;
  * [OAuth 2.1 & JWT best practices (Auth0)](https://identityunlocked.auth0.com/public/49/Identity%2C-Unlocked.--bed7fada/c71b9fbd) ([identityunlocked.auth0.com][22])

*Project*: create a GitHub Actions pipeline that fails on coverage/mutation regression and runs a ZAP baseline scan.

---

### Phase 5 – Performance & System Design *(18 Sep → 10 Oct)*

**Goal:** make the service observable, cache‑friendly and horizontally scalable.

1. **Caching patterns** – Redis LRU, CDN cache‑tag, TTL tuning.
2. **Queues & async workflows** – BullMQ basics, Kafka overview.
3. **Observability** – pino logs, OpenTelemetry traces, Prometheus/Grafana metrics.

**Useful links**

* **Caching & filas**

  * [Redis eviction policy guide](https://redis.io/docs/latest/develop/reference/eviction/) ([redis.io][10])
  * [BullMQ – Intro & Queue API](https://docs.bullmq.io/guide/introduction) ([docs.bullmq.io][3])
  * [Kafka Quickstart – official](https://kafka.apache.org/quickstart) ([kafka.apache.org][23])

* **Observabilidade**

  * [Pino logger homepage](https://getpino.io/) ([getpino.io][24])
  * [OpenTelemetry JS – Getting Started](https://opentelemetry.io/docs/languages/js/getting-started/) ([opentelemetry.io][25])
  * [Prometheus + Grafana node\_exporter setup](https://grafana.com/docs/grafana-cloud/send-data/metrics/metrics-prometheus/prometheus-config-examples/noagent_linuxnode/) ([grafana.com][26])
  * [k6 examples – load testing](https://k6.io/docs/examples/) ([k6.io][27])
    
*Project*: load‑test with k6 to 100 k req/s and tune until P95 latency < 150 ms.

---

### Phase 6 – Cloud & DevOps *(11 Oct → 07 Nov)*

**Goal:** ship reliably to the cloud using containers, IaC and GitOps.

1. **Containerisation** – Docker multi‑stage builds; Compose.
2. **Kubernetes fundamentals** – pods, deployments, services, ingress.
3. **Infrastructure as Code** – Terraform/Pulumi for AWS; start AWS SAA prep.
4. **GitOps & SRE** – ArgoCD blue‑green deploy, SLI/SLO and incident run‑books.

**Useful links**

* **Docker & Compose**

  * [Docker Docs – Multi-stage Builds](https://docs.docker.com/build/building/multi-stage/) ([docs.docker.com][28])
  * [Compose file reference](https://docs.docker.com/reference/compose-file/) ([docs.docker.com][29])

* **Kubernetes fundamentals**

  * [Kubernetes Overview](https://kubernetes.io/docs/concepts/overview/) ([kubernetes.io][30])
  * [Deployments & rolling updates](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) ([kubernetes.io][31])

* **IaC & GitOps**

  * [Terraform – Official Docs](https://developer.hashicorp.com/terraform/docs) ([developer.hashicorp.com][2])
  * [Pulumi AWS (TypeScript) guide](https://www.pulumi.com/registry/packages/aws/how-to-guides/aws-ts-resources/) ([pulumi.com][32])
  * [Argo CD blue-green deploy (practical guide)](https://dev.to/mark_mwendia_0298dd9c0aad/implementing-blue-green-deployments-with-argo-cd-and-helm-a-practical-guide-6b6) ([dev.to][4])
  * [SRE workbook – Incident Runbooks](https://sre.google/workbook/incident-response/) ([sre.google][33])
    
*Project*: deploy the system to EKS with blue‑green rollout and live Grafana dashboards.

---

### Phase 7 – AI & LLMOps *(08 Nov → 10 Dec)*

**Goal:** integrate and operate large language models from Node services.

1. **LLM foundations** – transformers, embeddings, fine‑tune vs RAG.
2. **LangChain.js & LangGraph** – agent orchestration, tool‑calling, memory.
3. **Self‑hosting models** – run Llama 3 or Mistral locally via Ollama + `llama‑cpp` bindings.
4. **Vector stores & guardrails** – pgvector / Qdrant, prompt evaluation.

**Useful links**

* **Fundamentos LLM & vetores**

  * [Transformer models explained (TechRadar)](https://www.techradar.com/pro/what-are-transformer-models) ([techradar.com][34])
  * [pgvector – vector search for Postgres](https://github.com/pgvector/pgvector) ([github.com][35])
  * [Qdrant quickstart](https://qdrant.tech/documentation/quickstart/) ([qdrant.tech][36])

* **LangChain & LangGraph**

  * [LangChain.js – Intro](https://js.langchain.com/docs/introduction/) ([js.langchain.com][37])
  * [LangGraph repo & docs](https://github.com/langchain-ai/langgraph) ([github.com][38])

* **Self-hosting & guardrails**

  * [llama.cpp (ggml) – self-host](https://github.com/ggml-org/llama.cpp) ([github.com][39])
  * [Ollama + llama.cpp thread (Reddit)](https://www.reddit.com/r/LocalLLaMA/comments/1cjaybn/how_ollama_uses_llamacpp/) ([reddit.com][40])
  * [Guardrails AI – Docs intro](https://www.guardrailsai.com/docs) ([guardrailsai.com][41])
    
*Project*: deliver a gRPC Doc‑Chat micro‑service (RAG) with tracing and metrics.

---

### Phase 8 – Polyglot Sprint *(11 Dec → 24 Dec)*

**Goal:** gain basic fluency in a second backend language.

1. **Language tour** – Java (Spring Boot 3) *or* Go 1.23.
2. **gRPC client** – generate and call Doc‑Chat service.
3. **Benchmarking** – compare latency & throughput against the Node client.

**Useful links**

* **Java / Spring Boot**

  * [Spring Boot 3 – Project page](https://spring.io/projects/spring-boot) ([spring.io][42])

* **Go 1.23**

  * [Go 1.23 Release Notes](https://go.dev/doc/go1.23) ([go.dev][43])

* **gRPC client**

  * [gRPC Go quickstart](https://grpc.io/docs/languages/go/quickstart/) ([grpc.io][44])

* **Benchmarks**

  * [Performance benchmark Node vs Go (ITNext)](https://itnext.io/performance-benchmark-node-js-vs-go-9dbad158c3b0) ([itnext.io][45])
    
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

