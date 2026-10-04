<!-- Header wave -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=111111,1F6F5C&height=200&section=header&text=Hoan%20Le&fontSize=44&fontColor=ffffff&fontAlignY=30&animation=fadeIn&desc=Senior%20Full-Stack%20Engineer%20%C2%B7%20Distributed%20and%20Data-Driven%20Systems&descAlignY=47&descSize=15" width="100%"/>
</div>

<!-- Typing SVG -->
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=3200&pause=900&color=2E8B70&center=true&vCenter=true&multiline=false&width=580&lines=Backend+architecture+%C2%B7+NestJS+%C2%B7+PostgreSQL+%C2%B7+Go;Multi-tenant+SaaS%2C+self-hosted+on+Docker+Compose;Swift+and+Flutter+apps%2C+on+device%2C+no+tracking;Decision+records%2C+CI+gates%2C+acceptance+sign-off;10%2B+years+shipping+production+systems" alt="Typing SVG" />
</div>

<br/>

---

## About

Senior software engineer in Hanoi, 10+ years on production platforms, focused on **high-performance distributed and data-driven systems**. I work end to end: Postgres schema design and NestJS APIs through to React dashboards, Go services, and the Docker Compose stack it all runs on. Lately also native apps in Swift and Flutter.

Most of what I build is **multi-tenant B2B software**: row-level tenancy, entitlement enforcement, cost and nutrition calculation engines, ML-assisted data pipelines, and realtime systems.

I also run delivery the way a team should run it, even when the team is small. Everything is planned on **GitLab** with a roadmap, an architecture decision record or spec behind every non-obvious call, CI/CD guardrails on every merge request, and a written acceptance sign-off: a feature is not Done until its paired test suite runs green.

- 🏗️ Building **[MiseOS](https://miseos.io)**, kitchen operations SaaS, pre-launch with early access
- 🧩 Side projects you can open right now at **[craftthecode.dev](https://craftthecode.dev)**
- 📱 Three apps under **[apps.craftthecode.dev](https://apps.craftthecode.dev)**, the first one in store review
- ✍️ Writing up production bugs at **[craftthecode.dev/blog](https://craftthecode.dev/blog)**
- 🌏 **Hanoi, Vietnam** (GMT+7), working with teams across US, EU and APAC
- 💼 **Open to senior / staff engineering roles and select contract work**

---

## Selected Work

| Project | What it is | Stack | Status |
|---|---|---|---|
| **[MiseOS](https://miseos.io)** | Multi-tenant kitchen-ops SaaS: recipe costing against moving supplier prices, nutrition and allergen labels, inventory | NestJS · Next.js · PostgreSQL · Python/FastAPI · Go · Docker Compose | Pre-launch, in active development |
| **[Guglu Homes](https://guglu.ca)** | Canada-wide MLS® real-estate marketplace, 175,000+ listings, web and native mobile | Next.js · NestJS · Flutter · PostgreSQL · Socket.IO | Live, client project |
| **[Games Portal](https://games-portal.craftthecode.dev)** | One server hosting many turn-based games as plugins: Xiangqi and Gomoku, matchmaking, server clock, Glicko-2 ratings, replays, spectating, a browser-side engine | NestJS 11 · Next.js 16 · Prisma · PostgreSQL · WebSockets · Web Workers | Live, 9 decision records |
| **[Classio](https://classio.craftthecode.dev)** | White-label operations software for small tutoring centres: roster, attendance with make-up sessions, tuition, reminders. One instance per customer, not SaaS | Next.js 16 · NestJS 11 · MikroORM 7 · PostgreSQL 17 · Playwright | Demo live, 7 decision records |
| **[Latch](https://latch.craftthecode.dev)** | Two-sided property marketplace built in public: 571 listings, map search, agency back office | Next.js 16 · NestJS 11 · Prisma 7 · Postgres FTS · Leaflet | Live, [12 decision records published](https://latch.craftthecode.dev/about-project) |
| **[Termilo](https://github.com/craft-the-code/termilo)** | Local-first SSH terminal manager, no cloud sync, native performance | Tauri v2 (Rust) · React · TypeScript · xterm.js | Shipped, open source |

---

## MiseOS, architecture notes

The system I spend most of my time on: a **13-repo** platform for professional kitchens.

<table>
<tr><td width="58%">

**Engineering surface**

- **Multi-tenant spine.** PostgreSQL row-level security, organization-owned resources, entitlement limits enforced server side rather than decorating a pricing page
- **Costing and nutrition engines.** Recipe yield tracking, real-time plate cost against moving supplier prices, region-aware compliance labels (FDA, CFIA, EU), with the source of every nutrition value recorded
- **ML services.** Hierarchical ingredient categorizer (scikit-learn) and recipe-line parser in Python/FastAPI. Accuracy is measured on a held-out slice (about 88% at level 2) and a CI ratchet stops it from sliding back
- **Ingestion pipeline.** Go orchestration layer handling proxy rotation, caching and queueing over stateless Python fetch workers
- **Recipe library.** A system cookbook with a rights-cleared publish gate, which tenants clone with provenance kept
- **Self-hosted deployment.** Docker Compose across dev, staging and prod, fronted by nginx and Cloudflare, with GitLab CI/CD change detection so only touched services redeploy

</td><td width="42%" valign="top">

**By the numbers**

| | |
|---|---|
| Repos | 13 |
| Architecture decision records | 29 |
| Schema migrations | 23 |
| Backend test specs | 91 |
| Frontend test files | 45 |
| Regression suites vs. deployed env | 14 |

</td></tr>
</table>

---

## Apps

Native apps under one rule set: processing on device, no account, no tracking. Each repo carries its own ADRs and changelog.

| App | What it does | Stack | Status |
|---|---|---|---|
| **[Logic Nook](https://apps.craftthecode.dev/logic-nook)** | Two calm logic puzzles a day, offline. A pure-Dart engine generates, grades and uniqueness-checks every puzzle | Flutter · Dart · 152 tests | Submitted to the App Store and Google Play, October 2026 |
| **[Batch Light](https://apps.craftthecode.dev/batch-light)** | Batch product photos for marketplace sellers: background removal, sizing for 11 marketplaces, a compliance check per photo, SKU file names | Swift 6 · SwiftUI · Vision · SwiftData · 198 tests | TestFlight beta, iPhone and Mac |
| **[Spokewise](https://apps.craftthecode.dev/spokewise)** | A local-first planner for iPhone, iPad and Mac: tasks, habits, journal and health around one weekly review | Swift · SwiftUI · GRDB · 278 tests | In development |

Spokewise's core is plain Swift, tested on Linux under a 90% coverage gate. It carries a hybrid logical clock and per-field last-writer-wins merging, ready for sync.

---

## How I engineer

The part that does not show up in a language chart. Every MiseOS and craftthecode project runs this way.

**Planned on GitLab, delivered issue first.** Roadmap to milestone to issue, with the board as the source of truth. Work arrives as small stacked merge requests rather than one big branch, so review stays possible.

**Written down before it is built.** Every non-obvious architectural call gets an ADR or a spec, recorded with the alternatives that were rejected and why. A trade-off with no downside listed is usually one nobody thought about. 29 ADRs on MiseOS, 12 on Latch, 9 on Games Portal, 7 on Classio; [Latch publishes its set openly](https://latch.craftthecode.dev/about-project).

**Four tiers of automated quality, wired into CI/CD:**

| Tier | Runs | Covers |
|---|---|---|
| 0 | Every merge request | Lint, types, unit tests, build |
| 1 | Nightly and pre-release | Regression suites against the deployed environment |
| 2 | Before every `develop → main` | Release smoke |
| 3 | After deploy | Production verification |

**Acceptance sign-off, not just a merge.** Each delivery names the suite that accepts it, planned up front alongside the spec as unit, integration, e2e or regression coverage. A feature is not Done when it merges. It is Done when that named suite is green in CI on a run you can link, and the board move carries the pipeline URL. I wrote that ledger after finding 50 issues marked Done whose accepting suites had never run.

**Measured, not assumed.** For Latch I benchmarked a dedicated search service against plain Postgres and shipped Postgres when it won: 3.9 ms indexed full-text search, and a listing page cut from 915 KB to 38 KB. For the Games Portal engine, difficulty levels are accuracy targets checked by a self-play ladder, not a guess at search depth.

---

## Writing

Bugs that passed every check, written up with a reproduction you can run:

- [The advisory lock that never held: raw SQL in MikroORM 7](https://craftthecode.dev/blog/mikroorm-raw-sql-outside-transaction)
- [The Next.js rewrite that read the wrong machine's environment](https://craftthecode.dev/blog/nextjs-rewrites-are-build-time)

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
![MikroORM](https://img.shields.io/badge/MikroORM-111111?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

**Frontend** &nbsp;
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Mobile and desktop** &nbsp;
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-0D96F6?style=flat-square&logo=swift&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri-24C8D8?style=flat-square&logo=tauri&logoColor=white)

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
| **1,938** | 176 | 19 days | 86 on 2026-07-21 |

<sub>Last updated 2026-09-28. Includes private contributions.</sub>
<!-- STATS:END -->

> **Note:** my primary day-to-day repositories are **self-hosted on GitLab** (MiseOS, craft-the-code),
> so the graph above reflects only the GitHub-hosted share of my work.

**Languages by lines of code**, measured across 30 active repositories, October 2026:

```
TypeScript    ██████████████████████░░░░░░░░░░░  67.4%
Swift         ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   7.4%
JavaScript    ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   7.2%
Infra / CI    █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   3.8%
Go            █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   3.7%
Python        █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   3.7%
CSS           █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   2.9%
Dart          █░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   2.8%
Shell         ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   1.0%
```

---

## Connect

<div align="center">

[![Website](https://img.shields.io/badge/craftthecode.dev-111111?style=for-the-badge&logoColor=white)](https://craftthecode.dev)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-in%2Fledaihoan-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ledaihoan)
&nbsp;
[![MiseOS](https://img.shields.io/badge/MiseOS-miseos.io-1F6F5C?style=for-the-badge)](https://miseos.io)
&nbsp;
[![Apps](https://img.shields.io/badge/Apps-apps.craftthecode.dev-111111?style=for-the-badge)](https://apps.craftthecode.dev)
&nbsp;
[![Open Source](https://img.shields.io/badge/Open%20Source-craft--the--code-111111?style=for-the-badge&logo=github)](https://github.com/craft-the-code)

</div>

<!-- Footer wave -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=1F6F5C,111111&height=100&section=footer" width="100%"/>
</div>
