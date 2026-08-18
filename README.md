<!-- Header wave -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=111111,1F6F5C&height=150&section=header&text=Hoan%20Le&fontSize=44&fontColor=ffffff&fontAlignY=52&animation=fadeIn&desc=Senior%20Full-Stack%20Engineer%20%C2%B7%20Distributed%20%26%20Data-Driven%20Systems&descAlignY=76&descSize=15" width="100%"/>
</div>

<!-- Typing SVG -->
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=3200&pause=900&color=2E8B70&center=true&vCenter=true&multiline=false&width=580&lines=Backend+architecture+%C2%B7+NestJS+%C2%B7+PostgreSQL+%C2%B7+Go;Multi-tenant+SaaS%2C+self-hosted+on+Docker+Compose;Decision+records%2C+CI+gates%2C+acceptance+sign-off;10%2B+years+shipping+production+systems" alt="Typing SVG" />
</div>

<br/>

---

## About

Senior software engineer, 10+ years, focused on **high-performance distributed and data-driven systems**. I work end to end: Postgres schema design and NestJS APIs through to React dashboards, Go services, and the Docker Compose stack it all runs on.

Most of what I build now is **multi-tenant B2B SaaS**: row-level tenancy, entitlement enforcement, cost and nutrition calculation engines, and ML-assisted data pipelines.

I also run delivery the way a team should run it, even when the team is small. Everything lives on **GitLab** with roadmap planning, an architecture decision record or spec behind every non-obvious call, CI/CD guardrails on every merge request, and a written acceptance sign-off that a feature is not Done until its paired test suite runs green.

- 🏗️ Building **[MiseOS](https://miseos.io)**, kitchen operations SaaS, in active development
- 🏢 Studio and client work at **[craftthecode.dev](https://craftthecode.dev)**
- 🌏 **Hanoi, Vietnam** (GMT+7), working with teams across US, EU and APAC
- 💼 **Open to senior / staff engineering roles and select contract work**

---

## Selected Work

| Project | What it is | Stack | Status |
|---|---|---|---|
| **[MiseOS](https://miseos.io)** | Multi-tenant kitchen-ops SaaS: recipe costing, nutrition compliance, inventory forecasting | NestJS · Next.js · PostgreSQL · Python/FastAPI · Go · Docker Compose | In active development |
| **[Latch](https://latch.craftthecode.dev)** | Two-sided property marketplace, buyer browse plus agency dashboards, built in public | Next.js 16 · NestJS 11 · Prisma 7 · Postgres FTS · Leaflet | Live, [decision records published](https://latch.craftthecode.dev/about-project) |
| **Guglu Homes** | Canada-wide MLS® real-estate marketplace, 175,000+ listings, web and native mobile | Next.js · NestJS · Flutter · PostgreSQL · Socket.IO | Live, client project |
| **[EcoMall](https://ecomall.craftthecode.dev)** | Multi-vendor marketplace: per-vendor storefronts, cart, checkout, order tracking | Next.js · NestJS · PostgreSQL · Redis · Traefik | Live |
| **[Termilo](https://github.com/craft-the-code/termilo)** | Local-first SSH terminal manager, no cloud sync, native performance | Tauri v2 (Rust) · React · TypeScript · xterm.js | Shipped, open source |

---

## MiseOS, architecture notes

The system I spend most of my time on. A **15-repo** platform for professional kitchens.

<table>
<tr><td width="58%">

**Engineering surface**

- **Multi-tenant spine.** PostgreSQL row-level security, organization-owned resources, entitlement limits enforced server side rather than decorating a pricing page
- **Costing and nutrition engines.** Recipe yield tracking, real-time plate cost against moving supplier prices, region-aware compliance labels (FDA, CFIA, EU)
- **ML services.** Ingredient categorizer and recipe-line parser in Python/FastAPI with spaCy and FAISS, accuracy gated as a CI suite
- **Ingestion pipeline.** Go orchestration layer handling proxy rotation, caching and queueing over stateless Python fetch workers
- **Self-hosted deployment.** Docker Compose across dev, staging and prod, fronted by nginx and Cloudflare, with GitLab CI/CD change detection so only touched services redeploy

</td><td width="42%" valign="top">

**By the numbers**

| | |
|---|---|
| Repos | 15 |
| Architecture decision records | 28 |
| Schema migrations | 30 |
| Backend test specs | 85 |
| Frontend test files | 42 |
| Regression suites vs. deployed env | 13 |

</td></tr>
</table>

---

## How I engineer

The part that does not show up in a language chart. Every MiseOS and craftthecode project runs this way.

**Planned on GitLab, delivered issue first.** Roadmap to milestone to issue, with the board as the source of truth. Work arrives as small stacked merge requests rather than one big branch, so review stays possible.

**Written down before it is built.** Every non-obvious architectural call gets an ADR or a spec, recorded with the alternatives that were rejected and why. A trade-off with no downside listed is usually one nobody thought about. 28 ADRs on MiseOS alone; [Latch publishes its set openly](https://latch.craftthecode.dev/about-project).

**Four tiers of automated quality, wired into CI/CD:**

| Tier | Runs | Covers |
|---|---|---|
| 0 | Every merge request | Lint, types, unit tests, build |
| 1 | Nightly and pre-release | Regression suites against the deployed environment |
| 2 | Before every `develop → main` | Release smoke |
| 3 | After deploy | Production verification |

**Acceptance sign-off, not just a merge.** Each delivery names the suite that accepts it, planned up front alongside the spec as unit, integration, e2e or regression coverage. A feature is not Done when it merges. It is Done when that named suite is green in CI on a run you can link, and the board move carries the pipeline URL. I wrote that ledger after finding 50 issues marked Done whose accepting suites had never run.

**Measured, not assumed.** For Latch I benchmarked a dedicated search service against plain Postgres and shipped Postgres when it won: 3.9 ms indexed full-text search, and a listing page cut from 915 KB to 38 KB.

---

## Tech Stack

<div align="center">

**Backend** &nbsp;
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**Data** &nbsp;
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

**Frontend** &nbsp;
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Infrastructure and delivery** &nbsp;
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI%2FCD-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

</div>

---

## Activity

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=ledaihoan&bg_color=00000000&color=1F6F5C&line=2E8B70&point=111111&area=true&area_color=2E8B70&hide_border=true" width="100%" alt="Contribution Graph"/>
</div>

<!-- STATS:START -->
<!-- Auto-generated by .github/workflows/stats.yml, do not edit by hand. -->
| Contributions (last year) | Active days | Longest streak | Busiest day |
|---|---|---|---|
| **1,834** | 174 | 19 days | 86 on 2026-07-21 |

<sub>Last updated 2026-08-18. Includes private contributions.</sub>
<!-- STATS:END -->

> **Note:** my primary day-to-day repositories are **self-hosted on GitLab** (MiseOS, craft-the-code),
> so the graph above reflects only the GitHub-hosted share of my work.

**Languages by lines of code**, measured across 25 active repositories, August 2026:

```
TypeScript    ██████████████████████████░░░░░░░  79.2%
Go            ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   4.7%
Python        ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   4.6%
JavaScript    █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   3.8%
Infra / CI    █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   3.2%
CSS           █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   2.6%
Shell         ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   1.0%
```

---

## Connect

<div align="center">

[![Website](https://img.shields.io/badge/craftthecode.dev-111111?style=for-the-badge&logoColor=white)](https://craftthecode.dev)
&nbsp;
[![MiseOS](https://img.shields.io/badge/MiseOS-miseos.io-1F6F5C?style=for-the-badge)](https://miseos.io)
&nbsp;
[![Open Source](https://img.shields.io/badge/Open%20Source-craft--the--code-111111?style=for-the-badge&logo=github)](https://github.com/craft-the-code)

</div>

<!-- Footer wave -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=1F6F5C,111111&height=100&section=footer" width="100%"/>
</div>
