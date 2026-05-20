# Adrian Gachewa
**Full-Stack Engineer · Python · AWS · Backend systems**

Nairobi, Kenya · gachewaadrian@gmail.com · +254 717 990 230
github.com/GachewaRa · gachewara.github.io

---

Backend-leaning full-stack engineer, 3 years building production Python systems on AWS infrastructure. Currently leading development at M-taka, owning backend architecture and contributing to all major technical decisions across the stack. Strong on Python (FastAPI, Django), REST API design, Postgres, and containerized AWS deployments. Architecture-school background plus dedicated study of distributed-system design — microservices decomposition, orchestration patterns, data-flow trade-offs — inform how I approach architectural decisions.

---

## Experience

### Lead Developer — M-taka *(Jul 2025 – Present)*
*Early-stage Kenyan startup. Software for the waste-management sector.*

- Led the architectural redesign and 3-month rebuild of the company's core platform. Made the call to rebuild rather than patch, owned the architecture end to end, and shipped without service interruption. Contributed to all major technical decisions in close collaboration with the CTO.
- Built backend services in Python (Django) backed by Postgres, deployed in Docker containers through a CI/CD pipeline.
- Drove a substantial performance gain on the data-heaviest parts of the system — slowest views moved from **minutes to sub-second**, standard views from seconds to a few hundred milliseconds — through query optimization and right-sized deployment topology.
- Designed the platform's configurability model so most new customer needs resolve through configuration rather than code changes.
- Shipped offline-first functionality across the user-facing application, with a sync model that minimizes conflicts.
- Owned the data migration between legacy and successor systems across incompatible schemas.
- Coordinated a team of two developers through the rebuild while leading from the backend.

### Freelance Full-Stack Developer *(2023 – 2025)*

- **Edmond Serenity** ([edmondserenity.com](https://edmondserenity.com)) — Resident management system for a US nursing home: patient records, medication schedules, daily care logs. Co-built with one collaborator. Live since Oct 2025.
- **Murunga Mangich Advocates** ([murungamangichadvs.co.ke](https://murungamangichadvs.co.ke)) — Document management system for a Kenyan law firm. Built solo. Live since Feb 2026.
- Earlier work (2023–2024): REST APIs, bots, internal tools, and business sites for Kenyan SMBs.

---

## Selected Project

### Aktaba — Personal knowledge-management platform
*[aktaba.com](https://aktaba.com) · Solo build · Live since early 2026 · 8 months idea to launch*

A polymath's notebook: ingest highlights from books, slice them into notes, tag them across domains, attach them to projects, reason through ideas on linked canvases. Designed, built, and operated end-to-end.

- **Backend:** FastAPI (Python) serving a REST API to a SvelteKit frontend. Stateless services, JWT auth, S3-backed document storage.
- **Data:** Postgres for relational records; Neo4j for the typed, weighted link graph between notes inside matters. Write-time fan-out keeps the two stores consistent.
- **Deployment:** AWS-hosted with regular backups and streaming replication. ~600ms typical page latency from East Africa.
- In daily active use: 2,500+ notes across 120 tags, 50 projects, 90+ highlights, 20 documents.

---

## Stack

**Languages:** Python · TypeScript · SQL · Bash
**Backend:** FastAPI · Django · REST · async patterns · service decomposition · query optimization
**Data:** Postgres · Neo4j · Redis · relational + graph modeling · migrations · streaming replication
**Frontend:** SvelteKit · React · PWA / offline-first
**Cloud & Infra:** AWS · S3 · Docker · CI/CD (GitHub Actions) · Linux
**Strengths:** distributed-system design · microservices decomposition & orchestration trade-offs · database modeling · architectural decision-making · technical writing · cross-team collaboration

---

## Education

**Bachelor of Architectural Studies** — Technical University of Kenya, 2023
Masterplanning, structural reasoning, and design under constraint — disciplines I now apply to software systems.

**Self-directed:** worked through standard texts on networking, algorithms, and databases. *Software Architecture: The Hard Parts* anchors my understanding of microservices decomposition, distributed-system trade-offs, and orchestration patterns. Bootcamp 2023.

---

## Languages

English · Kiswahili

*References available on request.*
