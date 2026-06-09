# Investiga+ Case Study

**Investiga+** is a production-oriented SaaS platform for CNPJ intelligence, company data lookup, secure authentication, cached searches, user history and dashboard analytics.

This case study documents the product reasoning, architecture and technical decisions behind Investiga+ as part of the DevFlow Labs ecosystem.

---

## Case Study Documents

| Document | Purpose |
|---|---|
| [Architecture](architecture.md) | Frontend/backend boundaries, CNPJ lookup flow, cache strategy and testing approach |
| [Security Decisions](security-decisions.md) | JWT, HttpOnly Cookies, protected routes, user-scoped data and external API safety |
| [Product Roadmap](product-roadmap.md) | Product phases, SaaS evolution, monetization and company intelligence roadmap |
| [Business Context](business-context.md) | Market problem, target users, value proposition and SaaS potential |
| [Recruiter Notes](recruiter-notes.md) | What recruiters and interviewers should evaluate in this case |

---

## Product Context

Brazilian businesses often need quick access to company data for validation, analysis, internal processes, prospecting and operational decisions.

Investiga+ was built to centralize CNPJ consultation flows in a SaaS interface with secure authentication, user history, cache strategy and a maintainable fullstack architecture.

---

## Problem

Common pain points addressed by the product:

- Repetitive CNPJ lookups across disconnected tools
- Lack of historical search tracking
- Repeated external API calls for the same company
- Need for secure user access
- Need for clean dashboards and structured company data
- Difficulty evolving lookup workflows without a modular backend

---

## Solution

Investiga+ provides a SaaS interface where users can authenticate, search CNPJs, view company information, store historical searches and reuse cached results when available.

The system was designed as a real product, not just a technical demo.

---

## Core Features

- JWT authentication with HttpOnly Cookies
- CNPJ lookup through external API integration
- Local cache strategy for repeated searches
- User-based search history
- Responsive dashboard
- Profile and usage management
- Modular backend structure
- Automated tests with Jest
- Prisma ORM with PostgreSQL/SQLite support
- CI/CD-ready structure

---

## Architecture Overview

```text
Next.js Frontend
  ├── Landing page
  ├── Login and authentication flows
  ├── Dashboard
  ├── CNPJ search UI
  ├── Search history
  └── Profile area

Node.js + Express Backend
  ├── Auth module
  ├── CNPJ consultation module
  ├── History module
  ├── Validation middlewares
  ├── Error handling
  └── External API integration layer

Database
  ├── Prisma ORM
  ├── Users
  ├── Search history
  └── Cached company records
```

## Technical Stack

### Frontend

- Next.js
- React
- Chakra UI
- Framer Motion

### Backend

- Node.js
- Express.js
- Prisma ORM
- REST APIs
- JWT authentication

### Database

- PostgreSQL
- SQLite for local development

### Quality

- Jest
- Mocked integrations
- Error handling tests

### DevOps

- Docker
- GitHub Actions
- Railway-ready deployment

## Security Decisions

- JWT stored in HttpOnly Cookies
- Protected backend routes
- User-scoped records
- Centralized error handling
- Environment-based secrets
- External API access isolated in service layer

## Business Value

Investiga+ demonstrates the ability to transform a repeatable business operation into a SaaS product with authentication, persistence, history, integrations and a scalable product foundation.

## Roadmap

- Add richer company intelligence views
- Improve analytics and usage metrics
- Add administrative dashboards
- Expand test coverage
- Improve observability
- Add additional enrichment APIs

## Links

- Repository: https://github.com/devflow-modules/investiga-mais
- Live: https://investigamais.com
- Portfolio: https://devflowlabs.com.br
