<p align="center">
  <img src="https://img.shields.io/badge/WillowVibe-Data%20Engineering%20Studio-6366f1?style=for-the-badge&logoColor=white" />
  &nbsp;
  <img src="https://img.shields.io/badge/Built%20in-Bengaluru%2C%20India-FF6B35?style=for-the-badge" />
  &nbsp;
  <img src="https://img.shields.io/badge/Focus-Data%20%7C%20AI%20%7C%20OSS-22c55e?style=for-the-badge" />
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
- **Open-Source First** — every internal tool we build, we ship as OSS so the community benefits

We operate a **solo + contributor model** — lean by design, moving fast, building things that solve real problems for data teams.

---

## 🚀 Projects

### 🔬 [PipelineProbe](https://github.com/willowvibe/pipelineprobe) — *New*

> Instant Data Pipeline Audit Report for Airflow + dbt + modern warehouses

Run a single command, get a full HTML audit report. PipelineProbe is a **read-only CLI audit tool** for data engineers who want a fast, objective health check of their pipeline stack — before a migration, after an incident, or as a recurring CI gate.

```bash
pip install pipelineprobe
pipelineprobe init      # generates pipelineprobe.yml
pipelineprobe audit     # produces pipelineprobe-report.html
```

- ✅ **Airflow checks** — high failure-rate DAGs, missing retries, missing SLAs, stale pipelines
- ✅ **dbt checks** — models with zero tests, failing test runs, orphaned models
- ✅ **Warehouse checks** — oversized tables, missing audit timestamps (Postgres, BigQuery, Snowflake)
- ✅ **HTML + JSON report** — traffic-light severity, health score 0–100, per-issue recommendations
- ✅ **CI-ready** — `fail_on_critical` exit code gates for GitHub Actions / GitLab CI
- ✅ **Zero mutations** — 100% read-only; safe to run against production

**Stack:** Python · Typer · Pydantic · httpx · Jinja2 · psycopg2 · dbt artifacts

[![PipelineProbe Repo](https://img.shields.io/badge/→%20View%20PipelineProbe-6366f1?style=for-the-badge)](https://github.com/willowvibe/pipelineprobe)
[![MIT License](https://img.shields.io/github/license/willowvibe/pipelineprobe?style=flat-square)](https://github.com/willowvibe/pipelineprobe/blob/main/LICENSE)

---

### 🔭 [ObservaKit](https://github.com/willowvibe/ObservaKit)

> Self-hosted Data Observability & FinOps Starter Kit for small data teams

ObservaKit gives 1–5 person data teams the **5 core observability pillars** — Freshness, Volume, Quality, Schema Drift, and Pipeline Health — in a single `docker-compose up`. No Monte Carlo. No Metaplane. No SaaS bill.

- ✅ Freshness Monitor — detects stale tables by tracking `max(updated_at)`
- ✅ Volume Anomaly — Z-score detection against 7-day rolling averages
- ✅ Quality Checks — Soda Core & Great Expectations templates, ready to use
- ✅ Schema Drift Detector — snapshots `information_schema`, diffs on every run
- ✅ Pipeline Health — Airflow/Prefect REST API + OpenTelemetry + Grafana
- ✅ FinOps Tracker — Snowflake credits & BigQuery bytes billed, natively
- ✅ Native dbt Integration — parses `run_results.json` directly, no extra packages

**Stack:** Python · FastAPI · SQLAlchemy · Alembic · Prometheus · Grafana · Docker Compose · dbt · Airflow / Prefect

[![ObservaKit Repo](https://img.shields.io/badge/→%20View%20ObservaKit-7c3aed?style=for-the-badge)](https://github.com/willowvibe/ObservaKit)
[![MIT License](https://img.shields.io/github/license/willowvibe/ObservaKit?style=flat-square)](https://github.com/willowvibe/ObservaKit/blob/main/LICENSE)

---

## 🗂️ All Repositories

| Repo | Description | Language | Status |
|------|-------------|----------|--------|
| [🔬 pipelineprobe](https://github.com/willowvibe/pipelineprobe) | Instant pipeline audit CLI — Airflow + dbt + warehouse | Python | `active` |
| [🔭 ObservaKit](https://github.com/willowvibe/ObservaKit) | Self-hosted data observability & FinOps starter kit | Python | `active` |
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
| **AI / ML** | LangChain · OpenAI APIs · Vector DBs (Qdrant / ChromaDB) |

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
    <a href="https://github.com/willowvibe/pipelineprobe">Try PipelineProbe 🔬</a>
    &nbsp;·&nbsp;
    <a href="https://github.com/willowvibe/ObservaKit">Star ObservaKit ⭐</a>
  </sub>
</p>
