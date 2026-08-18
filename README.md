<!-- Header wave -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=111111,1F6F5C&height=150&section=header&text=Hoan%20Le&fontSize=44&fontColor=ffffff&fontAlignY=52&animation=fadeIn&desc=Senior%20Full-Stack%20Engineer%20%C2%B7%20Distributed%20%26%20Data-Driven%20Systems&descAlignY=76&descSize=15" width="100%"/>
</div>

<!-- Typing SVG -->
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=3200&pause=900&color=2E8B70&center=true&vCenter=true&multiline=false&width=560&lines=Backend+architecture+%C2%B7+NestJS+%C2%B7+PostgreSQL+%C2%B7+Go;Multi-tenant+SaaS+on+self-hosted+k3s;Decision+records%2C+CI+gates%2C+regression+suites;10%2B+years+shipping+production+systems" alt="Typing SVG" />
</div>

<br/>

---

## About

Senior software engineer, 10+ years, focused on **high-performance distributed and data-driven systems**. I work end-to-end — Postgres schema design and NestJS APIs through to React dashboards, Go services, and the k3s cluster it all runs on.

Most of what I build now is **multi-tenant B2B SaaS**: row-level tenancy, entitlement enforcement, cost/nutrition calculation engines, and ML-assisted data pipelines. I run it the way a team should be run even when the team is small — architecture decision records, CI-enforced quality gates, and a functional regression suite that runs against the deployed environment.

- 🏗️ Building **[MiseOS](https://miseos.io)** — kitchen operations SaaS, in active development
- 🏢 Studio work at **[craftthecode.dev](https://craftthecode.dev)** — client and reference builds
- 🌏 **Hanoi, Vietnam** (GMT+7) · working with teams across US · EU · APAC
- 💼 **Open to senior / staff engineering roles and select contract work**

---

## Selected Work

| Project | What it is | Stack | Status |
|---|---|---|---|
| **[MiseOS](https://miseos.io)** | Multi-tenant kitchen-ops SaaS: recipe costing, nutrition compliance, inventory forecasting | NestJS · Next.js · PostgreSQL · Python/FastAPI · Go · k3s | In active development |
| **[Latch](https://latch.craftthecode.dev)** | Two-sided property marketplace — buyer browse + agency dashboards, built in public | Next.js 16 · NestJS 11 · Prisma 7 · Postgres FTS · Leaflet | Live · [10 public ADRs](https://latch.craftthecode.dev/about-project) |
| **Guglu Homes** | Canada-wide MLS® real-estate marketplace, 175,000+ listings, web + native mobile | Next.js · NestJS · Flutter · PostgreSQL · Socket.IO | Live · client project |
| **[EcoMall](https://ecomall.craftthecode.dev)** | Multi-vendor marketplace — per-vendor storefronts, cart, checkout, order tracking | Next.js · NestJS · PostgreSQL · Redis · Traefik | Live |
| **[Termilo](https://github.com/craft-the-code/termilo)** | Local-first SSH terminal manager — no cloud sync, native performance | Tauri v2 (Rust) · React · TypeScript · xterm.js | Shipped · open source |

---

## MiseOS — architecture notes

The system I spend most of my time on. A **15-repo** platform for professional kitchens.

<table>
<tr><td width="58%">

**Engineering surface**

- **Multi-tenant spine** — PostgreSQL row-level security, organization-owned resources, server-side entitlement enforcement
- **Costing & nutrition engines** — recipe yield tracking, real-time plate cost against moving supplier prices, region-aware compliance labels (FDA · CFIA · EU)
- **ML services** — ingredient categorizer and recipe-line parser (Python/FastAPI, spaCy, FAISS), accuracy gated in CI
- **Ingestion pipeline** — Go orchestration layer (proxy rotation, caching, queueing) over stateless Python fetch workers
- **Self-hosted infra** — k3s, CloudNativePG, HashiCorp Vault, GitLab CI/CD with per-deploy version pinning

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

The part that doesn't show up in a language chart:

- **Decision records over tribal knowledge** — 38 ADRs across MiseOS and Latch. Every non-obvious architectural call is written down with its trade-offs, including the ones argued and rejected. [Latch publishes its 10 openly.](https://latch.craftthecode.dev/about-project)
- **Gates, not vibes** — ML accuracy, tenancy isolation, menu economics, allergen derivation and release smoke all run as CI suites against the deployed environment. A red gate blocks the release.
- **Measured, not assumed** — benchmarked a dedicated search service against plain Postgres for Latch and shipped Postgres when it won: 3.9 ms indexed full-text search, and a listing page cut from 915 KB to 38 KB.
- **Issue-first delivery** — small stacked merge requests over big-bang branches, so review stays possible.

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

**Infrastructure** &nbsp;
![k3s](https://img.shields.io/badge/k3s-FFC61C?style=flat-square&logo=kubernetes&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Vault](https://img.shields.io/badge/Vault-FFEC6E?style=flat-square&logo=vault&logoColor=black)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

</div>

---

## Activity

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=ledaihoan&bg_color=00000000&color=1F6F5C&line=2E8B70&point=111111&area=true&area_color=2E8B70&hide_border=true" width="100%" alt="Contribution Graph"/>
</div>

<!-- STATS:START -->
<!-- Auto-generated by .github/workflows/stats.yml — do not edit by hand. -->
| Contributions (last year) | Active days | Longest streak | Busiest day |
|---|---|---|---|
| **1,834** | 174 | 19 days | 86 on 2026-07-21 |

<sub>Last updated 2026-08-18. Includes private contributions.</sub>
<!-- STATS:END -->

> **Note:** my primary day-to-day repositories are **self-hosted on GitLab** (MiseOS, craft-the-code),
> so the graph above reflects only the GitHub-hosted share of my work.

**Languages by lines of code** — measured across 25 active repositories, August 2026:

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
