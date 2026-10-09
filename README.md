<h1 align="center">Hi, I'm Abdullahi 👋</h1>

<p align="center">
  I build backend systems and developer tools for <b>AI infrastructure</b>:<br/>
  LLM inference routing, agent observability, and data pipelines.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/the-abdullahi-mohamed/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=go,python,ts,react,nextjs,fastapi,postgres,redis,docker,githubactions&perline=10" alt="Tech stack" />
</p>

---

## 🛩️ [Agent Black Box](https://github.com/abdullahimohamed101/agent-black-box)

**A flight recorder for AI agents.** It records every model call, tool call, file edit, shell command, retry and failure, with cost and latency attached, and streams the run live to a dashboard.

<p align="center">
  <img src="https://raw.githubusercontent.com/abdullahimohamed101/agent-black-box/HEAD/docs/screenshots/phase-7/dashboard.png" width="85%" alt="Agent Black Box dashboard" />
</p>

- **Stack:** Python SDK → FastAPI → PostgreSQL (events + outbox) → workers → SSE → Next.js
- **Integrations:** adapters for OpenAI, Anthropic, LangGraph and MCP, with a shared conformance suite
- **Performance (one-laptop baseline):** batch ingest acknowledged in 27.5 ms p50 and 43.7 ms p95 at about 3.2k events/s, against a p95 target of 150 ms
- **Demo:** a coding agent fixes a broken OAuth service, hits a failing test, retries and passes, all visible live with diffs, shell output and cost

## ⚡ [ServerFlow](https://github.com/abdullahimohamed101/ServerFlow)

**A distributed LLM inference control plane in Go.** It serves an OpenAI-compatible API, including streaming, and schedules requests across a pool of vLLM workers.

- **Components:** gateway, control plane with worker registry (register, heartbeat, death detection), pluggable schedulers (round-robin, random, least-active, least-queue), API-key auth on PostgreSQL
- **Gateway overhead:** about **0.5 ms p95**, against a 25 ms budget
- **Fault tolerance:** a request that fails before any output is retried on another worker. In a 1,000-request test with one always-failing worker, **0 requests failed for clients**
- **Benchmarking:** a harness runs reproducible load tests with seeded workloads, repeated runs and side-by-side comparisons

## 🎯 [Internship Aggregator](https://github.com/abdullahimohamed101/recruiting-help)

**A pipeline that collects US internship, co-op and new-grad postings** from GitHub, Discord, Instagram and Slack sources. It normalizes and deduplicates them, tags sponsorship status, and posts alerts to Discord.

- **Stack:** a TypeScript monorepo with a collector, intake API, processor, GitHub poller and Discord bot, on PostgreSQL with signed ingestion

## 📈 [Real-Time Risk Dashboard](https://github.com/abdullahimohamed101/realtimedashboard)

**A portfolio risk dashboard.** It ingests holdings, computes rolling Sharpe, Beta, VaR and CVaR plus Fama-French 3-factor exposures, and pushes updates over WebSockets.

- **Stack:** FastAPI, SQLAlchemy and Alembic, APScheduler, Redis pub/sub, React, Vite and Recharts, Docker Compose, GitHub Actions CI

---

<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=abdullahimohamed101&show_icons=true&hide_border=true&theme=transparent&count_private=true" alt="GitHub stats" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=abdullahimohamed101&layout=compact&hide_border=true&theme=transparent&langs_count=6" alt="Top languages" />
</p>
