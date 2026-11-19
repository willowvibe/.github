<p align="center">
  <img src="https://img.shields.io/badge/WillowVibe-Data%20Engineering%20Studio-6366f1?style=for-the-badge&logoColor=white" />
  &nbsp;
  <img src="https://img.shields.io/badge/Built%20in-Bengaluru%2C%20India-FF6B35?style=for-the-badge" />
  &nbsp;
  <img src="https://img.shields.io/badge/Focus-Data%20%7C%20AI%20%7C%20OSS-22c55e?style=for-the-badge" />
  &nbsp;
  <a href="https://willowvibe.github.io/"><img src="https://img.shields.io/badge/Portfolio-Live%20demos-6366f1?style=for-the-badge" alt="Portfolio" /></a>
</p>

<br/>

<h1 align="center">🌿 WillowVibe</h1>

<p align="center">
  <strong>Open-source data infrastructure tools. Built in India. Used everywhere.</strong><br/>
  We build lightweight, self-hosted tooling that gives small data teams enterprise-grade
  pipeline observability, auditing, and automation — without vendor lock-in or SaaS bills.
</p>

<p align="center">
  <a href="https://github.com/willowvibe/pipelineprobe">
    <img src="https://img.shields.io/github/stars/willowvibe/pipelineprobe?style=flat-square&label=PipelineProbe%20⭐&color=6366f1" />
  </a>
  &nbsp;
  <a href="https://github.com/willowvibe/ObservaKit">
    <img src="https://img.shields.io/github/stars/willowvibe/ObservaKit?style=flat-square&label=ObservaKit%20⭐&color=7c3aed" />
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/Python-Expert-3776AB?style=flat-square&logo=python&logoColor=white" />
  &nbsp;
  <img src="https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white" />
  &nbsp;
  <img src="https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white" />
  &nbsp;
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" />
</p>

---

## 🔍 What We Build

WillowVibe is a **data engineering & AI tooling studio** — solo-founded, contributor-driven, OSS-first.

- **Pipeline Auditing** — point-in-time health checks on Airflow + dbt + warehouses; one command, one report
- **Data Observability** — continuous monitoring for pipeline health, data freshness, volume anomalies, and schema drift
- **FinOps for Data** — tracking Snowflake credits and BigQuery bytes billed, turning cloud cost chaos into actionable visibility
- **AI-Augmented Pipelines** — embedding AI at the right layer of the data stack without replacing what already works
- **PLM Analytics** — BOM, revision and change-control modelling that turns vendor PLM exports into tested marts
- **Document AI (RAG)** — retrieval-augmented assistants that answer from your documents with citations, evaluated before they ship
- **Open-Source First** — every internal tool we build, we ship as OSS so the community benefits

We operate a **solo + contributor model** — lean by design, moving fast, building things that solve real problems for data teams.

---

## 🚀 Projects

### 🔬 [PipelineProbe](https://github.com/willowvibe/pipelineprobe)

> Instant Data Pipeline Audit Report for Airflow + dbt + modern warehouses

Run a single command, get a full HTML audit report. PipelineProbe is a **read-only CLI audit tool** for data engineers who want a fast, objective health check of their pipeline stack — before a migration, after an incident, or as a recurring CI gate.

```bash
pip install pipelineprobe==0.3.1
pipelineprobe init      # generates pipelineprobe.yml
pipelineprobe audit     # produces pipelineprobe-report.html
```

- ✅ **Airflow checks** — high failure-rate DAGs, missing retries, stale pipelines
- ✅ **dbt checks** — models with zero tests and failing test runs
- ✅ **Warehouse checks** — oversized tables and missing audit timestamps (Postgres; BigQuery and Snowflake cost insights)
- ✅ **HTML + JSON report** — traffic-light severity, health score 0–100, per-issue recommendations
- ✅ **CI-ready** — `fail_on_critical` exit code gates for GitHub Actions / GitLab CI
- ✅ **Zero mutations** — 100% read-only; safe to run against production

**Stack:** Python · Typer · Pydantic · httpx · Jinja2 · psycopg2 · dbt artifacts

[![PipelineProbe Demo](https://img.shields.io/badge/→%20Open%20the%20live%20demo-6366f1?style=for-the-badge)](https://willowvibe.github.io/pipelineprobe/)
[![PipelineProbe Repo](https://img.shields.io/badge/→%20View%20the%20source-312e81?style=for-the-badge)](https://github.com/willowvibe/pipelineprobe)
[![PyPI](https://img.shields.io/pypi/v/pipelineprobe?style=flat-square)](https://pypi.org/project/pipelineprobe/)
[![MIT License](https://img.shields.io/github/license/willowvibe/pipelineprobe?style=flat-square)](https://github.com/willowvibe/pipelineprobe/blob/main/LICENSE)

---

### 🔭 [ObservaKit](https://github.com/willowvibe/ObservaKit)

> Self-hosted Data Observability & FinOps Starter Kit for small data teams

ObservaKit gives 1–5 person data teams the **5 core observability pillars** — Freshness, Volume, Quality, Schema Drift, and Pipeline Health — in a single `docker-compose up`. No Monte Carlo. No Metaplane. No SaaS bill.

- ✅ Freshness Monitor — detects stale tables by tracking `max(updated_at)`
- ✅ Volume Anomaly — Z-score detection against 7-day rolling averages
- ✅ Quality Checks — Soda Core checks, with Great Expectations templates (GX execution not yet implemented)
- ✅ Schema Drift Detector — snapshots `information_schema`, diffs on every run
- ✅ Pipeline Health — Airflow/Prefect REST API + OpenTelemetry + Grafana
- ✅ FinOps Tracker — Snowflake credits & BigQuery bytes billed, natively
- ✅ Native dbt Integration — parses `run_results.json` directly, no extra packages

**Stack:** Python · FastAPI · SQLAlchemy · Alembic · Prometheus · Grafana · Docker Compose · dbt · Airflow / Prefect

[![ObservaKit Demo](https://img.shields.io/badge/→%20Open%20the%20live%20demo-7c3aed?style=for-the-badge)](https://willowvibe.github.io/ObservaKit/)
[![ObservaKit Repo](https://img.shields.io/badge/→%20View%20the%20source-4c1d95?style=for-the-badge)](https://github.com/willowvibe/ObservaKit)
[![MIT License](https://img.shields.io/github/license/willowvibe/ObservaKit?style=flat-square)](https://github.com/willowvibe/ObservaKit/blob/main/LICENSE)

---

### 🧬 [plm-bom-pipeline](https://github.com/willowvibe/plm-bom-pipeline)

> A synthetic bicycle manufacturer's PLM data, modelled into tested analytics in one command

Parts, revisions, five-level BOMs and ECR → ECO → ECN change control, generated deterministically from seed 42. dbt turns ten exports into seven tested marts on DuckDB; a self-contained HTML report reads them back. Seven seeded PLM defects each fail exactly one named test.

```bash
git clone https://github.com/willowvibe/plm-bom-pipeline
cd plm-bom-pipeline && make demo   # generate, dbt build + tests, write the report (~15s)
```

- ✅ **BOM intelligence** — recursive explosion with a cycle guard, where-used, cost and weight rollups
- ✅ **Change control** — ECO cycle times and cross-product change impact
- ✅ **Data quality** — 195 checks; `make verify-defects` proves one-failure attribution across nine datasets
- ✅ **PLM ↔ ERP reconciliation** — full outer join of the eBOM and a synthetic ERP mBOM
- ✅ **Static by default** — report and dbt docs are files; no dashboard server to run

**Stack:** Python · dbt · DuckDB · pytest · GitHub Pages

[![plm-bom-pipeline Demo](https://img.shields.io/badge/→%20Open%20the%20live%20demo-0f766e?style=for-the-badge)](https://willowvibe.github.io/plm-bom-pipeline/)
[![plm-bom-pipeline Repo](https://img.shields.io/badge/→%20View%20the%20source-134e4a?style=for-the-badge)](https://github.com/willowvibe/plm-bom-pipeline)
[![MIT License](https://img.shields.io/github/license/willowvibe/plm-bom-pipeline?style=flat-square)](https://github.com/willowvibe/plm-bom-pipeline/blob/main/LICENSE)

---

### 📚 [rag-docs-chatbot](https://github.com/willowvibe/rag-docs-chatbot) — *New*

> Ask questions of a document set and get answers that cite the exact page — or an explicit "I don't know"

A retrieval-augmented chatbot over the public NIST SP 800-63B / 800-63-4 guidelines. FastAPI serves answers backed by Postgres + pgvector and local BGE embeddings; the live public demo runs a free model with a per-IP hourly limit.

```bash
git clone https://github.com/willowvibe/rag-docs-chatbot
cd rag-docs-chatbot && python3 -m venv .venv && .venv/bin/pip install -r requirements-dev.txt
make up && make ingest && make serve   # bring your own OLLAMA_API_KEY / OpenRouter / Anthropic key
```

- ✅ **Page-level citations** — every claim carries a `[n]` marker back to the exact page
- ✅ **Refuses when the documents don't answer** — an explicit "I don't know" instead of a guess
- ✅ **Hybrid retrieval** — vector + full-text search with a MiniLM cross-encoder reranker, all behind flags
- ✅ **Evaluated** — 40-question suite: 87.5% evidence hit@5, faithfulness 0.97 (published in `eval/report.md`)
- ✅ **Production-minded** — per-IP rate limiting in Postgres and a fallback chain across model providers

**Stack:** Python · FastAPI · PostgreSQL + pgvector · fastembed (BGE) · Vercel · Neon

[![rag-docs-chatbot Demo](https://img.shields.io/badge/→%20Open%20the%20live%20demo-1d4ed8?style=for-the-badge)](https://rag-docs-chatbot-three.vercel.app)
[![rag-docs-chatbot Repo](https://img.shields.io/badge/→%20View%20the%20source-1e3a8a?style=for-the-badge)](https://github.com/willowvibe/rag-docs-chatbot)
[![rag-docs-chatbot Walkthrough](https://img.shields.io/badge/→%20Watch%20the%20demo-2563eb?style=for-the-badge)](https://willowvibe.github.io/rag-docs-chatbot/)
[![MIT License](https://img.shields.io/github/license/willowvibe/rag-docs-chatbot?style=flat-square)](https://github.com/willowvibe/rag-docs-chatbot/blob/main/LICENSE)

---

### 🏗️ [data-pipeline-template](https://github.com/willowvibe/data-pipeline-template) — *New*

> Start a client data project in a day: one Copier command generates ingestion, dbt, CI, Docker and optional Airflow

A Copier template that renders a working weather pipeline — Open-Meteo → DuckDB or Postgres → dbt marts — with optional Airflow 3.4, where astronomer-cosmos turns every dbt model and test into its own task. Swap the source; keep the tests, CI and orchestration.

```bash
pipx install copier
copier copy gh:willowvibe/data-pipeline-template my-pipeline
cd my-pipeline && make install && make up
```

- ✅ **Four stacks, all tested** — DuckDB or Postgres, with or without Airflow; CI renders and runs every combination
- ✅ **Real orchestration test** — CI brings up the generated Airflow stack with `make up` and requires every DAG run to succeed
- ✅ **dbt done properly** — typed staging, documented marts, grain and relationship tests, source freshness
- ✅ **Offline by default** — a recorded API fixture keeps tests and demos off the network
- ✅ **Upgradable** — `copier update` pulls template fixes into existing projects

**Stack:** Copier · dbt Core · DuckDB · PostgreSQL · Apache Airflow 3 · astronomer-cosmos · GitHub Actions

[![data-pipeline-template Demo](https://img.shields.io/badge/→%20Watch%20the%20demo-0e7490?style=for-the-badge)](https://willowvibe.github.io/data-pipeline-template/#demo)
[![data-pipeline-template Repo](https://img.shields.io/badge/→%20View%20the%20source-155e75?style=for-the-badge)](https://github.com/willowvibe/data-pipeline-template)
[![MIT License](https://img.shields.io/github/license/willowvibe/data-pipeline-template?style=flat-square)](https://github.com/willowvibe/data-pipeline-template/blob/main/LICENSE)

---

## 🗂️ All Repositories

| Repo | Description | Language | Status |
|------|-------------|----------|--------|
| [🔬 pipelineprobe](https://github.com/willowvibe/pipelineprobe) | Instant pipeline audit CLI — Airflow + dbt + warehouse | Python | `active` |
| [🔭 ObservaKit](https://github.com/willowvibe/ObservaKit) | Self-hosted data observability & FinOps starter kit | Python | `active` |
| [🧬 plm-bom-pipeline](https://github.com/willowvibe/plm-bom-pipeline) | Synthetic PLM data → tested BOM and change-control analytics | Python · dbt | `active` |
| [📚 rag-docs-chatbot](https://github.com/willowvibe/rag-docs-chatbot) | Cited-answer RAG chatbot over NIST guidelines — FastAPI + pgvector | Python | `active` |
| [🏗️ data-pipeline-template](https://github.com/willowvibe/data-pipeline-template) | Copier template: tested dbt + optional Airflow project in one command | Python · dbt | `active` |
| [🧰 toolscontainer](https://github.com/willowvibe/toolscontainer) | Multi-purpose Python utility scripts & automations | Python | `maintained` |
| [🕷️ scrapy-bot](https://github.com/willowvibe/scrapy-bot) | Scrapy + Flask web scraping bot experiment | Python | `archived` |
| [💻 online-ide](https://github.com/willowvibe/online-ide) | Lightweight online Python execution environment | Python | `experimental` |

---

## 🛠️ Tech We Work With

| Layer | Tools |
|-------|-------|
| **Data Engineering** | Python · dbt · Apache Airflow · Prefect · Apache Spark |
| **Warehouses** | PostgreSQL · Snowflake · BigQuery · DuckDB |
| **Observability** | Prometheus · Grafana · OpenTelemetry · Soda Core |
| **Backend** | FastAPI · SQLAlchemy · Alembic · Pydantic |
| **Infra & DevOps** | Docker · Docker Compose · Terraform · GitHub Actions |
| **AI / ML** | LLM APIs (Anthropic · OpenRouter · Ollama) · pgvector · fastembed · RAG evaluation |

---

## 🌱 Our Open-Source Philosophy

> *"Build what the ecosystem needs. Share what you build. Let the community make it better."*

Every project we open-source follows three rules:
1. **Zero vendor lock-in** — runs on infra you own and control
2. **Quickstart in under 10 minutes** — if onboarding is painful, it won't get adopted
3. **Progressive complexity** — adopt one layer at a time; no all-or-nothing commitment

We actively maintain what we ship. Issues get responses. PRs get reviewed. Roadmaps get published.

---

## 🤝 Contributing

All public repos welcome contributions. Best places to start:

- 🔬 **PipelineProbe** → [`good first issues`](https://github.com/willowvibe/pipelineprobe/issues?q=is%3Aopen+label%3A%22good+first+issue%22)
  - Add a new warehouse connector (Redshift, DuckDB)
  - Add a new rule (task duration outliers, dbt source freshness)
  - Improve the HTML report template

- 🔭 **ObservaKit** → [`good first issues`](https://github.com/willowvibe/ObservaKit/issues?q=is%3Aopen+label%3A%22good+first+issue%22)
  - Add a new warehouse connector (Redshift, Delta Lake)
  - Write a Grafana dashboard for a new observability use case
  - Improve documentation or add a real-world example

Read [`CONTRIBUTING.md`](https://github.com/willowvibe/pipelineprobe/blob/main/CONTRIBUTING.md) before opening a PR.

---

## 📬 Get In Touch

We are open to:

- **Collaborations** on data tooling, AI pipelines, or observability infra
- **Consulting engagements** — data platform audits, pipeline migrations, cost optimization
- **Freelance / contract data engineering** for startups and scaleups

| Channel | Link |
|---------|------|
| 🐙 GitHub | [@willowvibe](https://github.com/willowvibe) |
| 🔬 PipelineProbe Issues | [Open an issue](https://github.com/willowvibe/pipelineprobe/issues) |
| 🔭 ObservaKit Issues | [Open an issue](https://github.com/willowvibe/ObservaKit/issues) |
| 🔐 Security Reports | See [`SECURITY.md`](https://github.com/willowvibe/ObservaKit/blob/main/SECURITY.md) |

---

<p align="center">
  <sub>
    🌿 <strong>WillowVibe</strong> — Bengaluru, India &nbsp;·&nbsp;
    Building in the open since 2024 &nbsp;·&nbsp;
    <a href="https://willowvibe.github.io/">Portfolio hub 🌿</a>
    &nbsp;·&nbsp;
    <a href="https://willowvibe.github.io/pipelineprobe/">PipelineProbe demo 🔬</a>
    &nbsp;·&nbsp;
    <a href="https://willowvibe.github.io/ObservaKit/">ObservaKit demo ⭐</a>
    &nbsp;·&nbsp;
    <a href="https://rag-docs-chatbot-three.vercel.app">rag-docs-chatbot demo 📚</a>
    &nbsp;·&nbsp;
    <a href="https://willowvibe.github.io/data-pipeline-template/">data-pipeline-template demo 🏗️</a>
  </sub>
</p>
