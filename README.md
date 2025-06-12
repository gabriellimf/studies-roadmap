# Mid-Level Backend Roadmap (2025)

Welcome! This repository tracks my journey from **junior** to **pleno** backend developer between **12 Jun 2025** and **31 Dec 2025**. The curriculum is based on current mid‑level job‑market demands for Node & TypeScript, cloud‑native architecture, DevOps, observability and AI/LLM integration.

> ⏳ **Daily commitment** ‒ 30 minutes (Mon–Sat). **Sundays are rest days.**

---

## 📅 Timeline & Milestones

| Phase | Dates (2025)    | Focus                                 | Saturday Mini‑Project                       |
| ----- | --------------- | ------------------------------------- | ------------------------------------------- |
| **1** | 12 Jun → 09 Jul | Advanced JS/TS · Node internals       | CLI scraper with streaming + progress bar   |
| **2** | 10 Jul → 01 Aug | SQL (Postgres) · Prisma · NoSQL       | API refactor with Postgres + Redis cache    |
| **3** | 02 Aug → 29 Aug | DDD · Hexagonal · SOLID               | Modularise monolith into npm workspaces     |
| **4** | 30 Aug → 17 Sep | Testing · Mutation · Security         | CI pipeline with Jest + Stryker + ZAP       |
| **5** | 18 Sep → 10 Oct | Performance · Caching · Observability | k6 load test to 100 k req/s + OpTel metrics |
| **6** | 11 Oct → 07 Nov | Docker → K8s · IaC · SRE              | EKS blue‑green deployment with Grafana      |
| **7** | 08 Nov → 10 Dec | LLM theory · LangChain.js · RAG       | gRPC Doc‑Chat service on Ollama Llama 3     |
| **8** | 11 Dec → 24 Dec | Polyglot (Java or Go)                 | Utility client consuming Doc‑Chat           |
| **9** | 25 Dec → 31 Dec | Soft skills · Wrap‑up                 | RFC + demo video + final portfolio          |

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

## 🗂️ Issue Templates

<details>
<summary>Click to view generated issues</summary>

### Phase 1 – Language & Runtime Mastery

```md
**Goal**
Deep JS/TS knowledge, Node internals, async patterns.

**Tasks**
- [ ] Read ES 2025 & TypeScript 5.x advanced chapters
- [ ] Diagram Node event‑loop vs libuv thread‑pool
- [ ] Build CLI scraper with streaming & progress bar

**Acceptance Criteria**
- CLI handles 10 k requests without blocking
- Progress updates every 500 ms
```

### Phase 2 – Data & Persistence

```md
**Goal**
Design schemas, master Postgres & Prisma, understand NoSQL trade‑offs.

**Tasks**
- [ ] Index & query tuning in Postgres
- [ ] Implement Prisma migrations (zero‑downtime)
- [ ] Add Redis cache with pub/sub invalidation
- [ ] Update CLI → API layer to use DB

**Acceptance Criteria**
- API returns cached responses ≤ 50 ms for hot keys
- Automated migration succeeds with pg_dump restore test
```

### Phase 3 – Design & Architecture

```md
**Goal**
Apply DDD, Hexagonal and SOLID.

**Tasks**
- [ ] Model aggregates & value objects
- [ ] Introduce ports & adapters layer
- [ ] Refactor into npm workspaces
- [ ] Document ADR‑001

**Acceptance Criteria**
- Unit tests at domain layer pass
- Hexagon compiles without circular deps
```

### Phase 4 – Quality, Testing & Security

```md
**Goal**
Robust test suite, mutation coverage, OWASP compliance.

**Tasks**
- [ ] Add Jest + Supertest coverage ≥ 85 %
- [ ] Configure Stryker → mutation ≥ 90 %
- [ ] Run ZAP baseline scan – no high severities
- [ ] Harden JWT & OAuth2.1 flow

**Acceptance Criteria**
- CI fails if coverage or mutation drops
- ZAP report committed in /reports
```

### Phase 5 – Performance & System Design

```md
**Goal**
Scale horizontally, add observability.

**Tasks**
- [ ] Implement Redis LRU & BullMQ queue
- [ ] Instrument OpenTelemetry traces
- [ ] Expose Prometheus metrics
- [ ] k6 load test to 100 k req/s

**Acceptance Criteria**
- P95 latency < 150 ms under load
- Dashboards show traces → spans → logs linkage
```

### Phase 6 – Cloud & DevOps

```md
**Goal**
Ship to cloud with Docker, K8s, IaC & GitOps.

**Tasks**
- [ ] Containerise services (multi‑stage builds)
- [ ] Deploy to kind → EKS
- [ ] Write Terraform for VPC, EKS, RDS
- [ ] Configure ArgoCD blue‑green

**Acceptance Criteria**
- Zero‑downtime during release
- Grafana dashboard shows <1 % error rate
```

### Phase 7 – AI & LLMOps

```md
**Goal**
Integrate self‑hosted LLM + RAG service.

**Tasks**
- [ ] Study Transformers basics & embeddings
- [ ] Run Llama 3 on Ollama
- [ ] Create LangGraph pipeline with tool‑calling
- [ ] Build gRPC Doc‑Chat; store vectors in pgvector

**Acceptance Criteria**
- End‑to‑end chat answers <= 2 s
- Prompt & response traced; eval scores logged
```

### Phase 8 – Polyglot Sprint

```md
**Goal**
Taste Java (Spring Boot 3) or Go 1.23.

**Tasks**
- [ ] Complete Tour of Language (~4 h)
- [ ] Generate gRPC client for Doc‑Chat
- [ ] Benchmark vs Node client

**Acceptance Criteria**
- Client latency within 10 % of Node version
```

### Phase 9 – Soft Skills & Wrap‑up

```md
**Goal**
Document, present & seek feedback.

**Tasks**
- [ ] Draft RFC for multi‑tenant Doc‑Chat
- [ ] Record 5‑min demo video
- [ ] Mock system‑design interview
- [ ] Collect code‑review feedback & apply

**Acceptance Criteria**
- RFC merged, demo published
- Feedback reflected in final commits
```

</details>

---

