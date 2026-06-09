# DevFlow Labs Case Studies

Public technical case studies from **DevFlow Labs**, a product engineering ecosystem focused on SaaS, automation, AI-assisted workflows, operational dashboards and reusable product architecture.

This repository works as the public portfolio layer for products and systems that may have private production code, protected business logic or internal deployment details.

---

## Priority Case Studies

These are the best case studies to review first. The three priority cases are available in English and Portuguese.

| Case | English | Portuguese | Type | What this demonstrates |
|---|---|---|---|---|
| WhatsApp Platform | [EN](case-studies/whatsapp-platform) | [PT-BR](case-studies/whatsapp-platform/README.pt-BR.md) | Multi-tenant SaaS | WhatsApp operations, webhooks, AI replies, billing, metrics and SaaS architecture |
| Investiga+ | [EN](case-studies/investiga-plus) | [PT-BR](case-studies/investiga-plus/README.pt-BR.md) | Production SaaS | Secure auth, CNPJ intelligence, API integration, caching, history and SaaS foundation |
| ApplyFlow | [EN](case-studies/applyflow) | [PT-BR](case-studies/applyflow/README.pt-BR.md) | Local-first product | Privacy-first workflows, application tracking, candidate productivity and AI-assisted coaching |

---

## What is DevFlow Labs?

**DevFlow Labs** is a product lab created by **Gustavo Marques de Lima** to design, build and document real-world digital products with a strong focus on:

- SaaS architecture
- Fullstack product engineering
- AI-assisted workflows
- Automation platforms
- Multi-tenant systems
- Privacy-first and local-first design
- Billing, usage tracking and operational dashboards
- Technical documentation as product strategy

---

## All Case Studies

| Case | Status | Type | Main Stack | What this demonstrates |
|---|---|---|---|---|
| [Investiga+](case-studies/investiga-plus) | Public product / production-oriented | SaaS | Next.js, React, Node.js, Express, Prisma, PostgreSQL, Jest | Secure auth, CNPJ intelligence, API integration, caching, history and SaaS foundation |
| [ApplyFlow](case-studies/applyflow) | Public case study | Local-first productivity product | Chrome Extension concept, Next.js, TypeScript, local storage, OpenAI optional | Privacy-first workflows, application tracking, candidate productivity and AI-assisted coaching |
| [WhatsApp Platform](case-studies/whatsapp-platform) | Private product / public case | Multi-tenant SaaS | Next.js, TypeScript, Prisma, PostgreSQL, WhatsApp Cloud API, Stripe, OpenAI | Multi-tenant architecture, webhooks, AI replies, billing, inbox operations and operational metrics |
| [DevFlow Financeiro](case-studies/financeiro) | Private product / public case | Financial SaaS | Next.js, TypeScript, Prisma, PostgreSQL, Tailwind CSS | Product score engine, dashboard UX, business rules, insights and monthly financial routines |
| [Career Suite / ATS Tools](case-studies/career-suite) | Public case study | AI-assisted career tooling | Next.js, TypeScript, OpenAI API, local-first analysis | Resume matching, job analysis, ATS-style scoring, interview preparation and privacy-aware AI |
| [Vibe Intel](https://github.com/devflow-modules/vibe-intel) | Experimental lab | AI/agents research | TypeScript, Node.js, Fastify, PNPM, Turborepo | Experimental AI agents, operational intelligence, modular packages and release automation |
| [JWT Auth](https://github.com/devflow-modules/jwt-auth) | Public module | Reusable backend module | Node.js, Express, JWT, TypeScript | Reusable authentication, middleware design, access control and package-oriented engineering |

---

## Repository Map

```text
case-studies/
├── investiga-plus/
├── applyflow/
├── whatsapp-platform/
├── financeiro/
└── career-suite/

docs/
├── architecture/
└── linkedin/
```

---

## Architecture Notes

| Document | Topic |
|---|---|
| Multi-Tenant SaaS Architecture | Tenant isolation, user roles, modular product boundaries and scalable SaaS foundations |
| Authentication and RBAC | JWT, protected routes, role-based access and secure session handling |
| AI Workflows | Human-in-the-loop AI, optional AI layers, structured output and automation safety |
| Billing and Usage | Plan limits, usage aggregation, overage logic and Stripe-based SaaS monetization |
| Local-First Products | Browser/local storage, privacy-first architecture, JSON handoff and user-owned data |

---

## Product Engineering Principles

### Product-first architecture

Each product starts from a real workflow problem and is shaped around measurable user value, operational clarity and future monetization potential.

### Modular fullstack engineering

Products are structured around clear boundaries between UI, domain logic, API layer, database, external integrations and operational concerns.

### AI as an enhancer

AI is used to accelerate analysis, support decision-making and improve productivity. Core workflows remain understandable, testable and maintainable.

### SaaS-ready foundations

Authentication, permissions, usage limits, billing, dashboards, observability and deployment concerns are treated as architecture decisions from the beginning.

### Documentation as product

READMEs, case studies, ADRs, runbooks and roadmap notes are part of the product strategy, not an afterthought.

---

## Public Repositories

| Repository | Purpose |
|---|---|
| devflow-modules/investiga-mais | Public SaaS product and technical case |
| devflow-modules/jwt-auth | Reusable authentication module |
| devflow-modules/applyflow-case-study | ApplyFlow public case study |
| devflow-modules/devflow-case-studies | Central public case study hub |
| devflow-modules/vibe-intel | Experimental AI and operational intelligence lab |

---

## Private Production Monorepo

The production-oriented DevFlow Labs monorepo is private by design:

`devflow-modules/devflow`

It is used as the canonical internal source for apps, packages, architecture, product work, deployment strategy and operational documentation.

Public repositories in this organization expose selected products, reusable modules and technical case studies without exposing sensitive business logic or private implementation details.

---

## Portfolio Value

This repository demonstrates:

- Ability to design products from zero
- Fullstack architecture maturity
- SaaS and product engineering mindset
- AI integration in real workflows
- Multi-tenant and operational systems thinking
- Technical storytelling and documentation
- Ownership over product, roadmap and engineering delivery

---

## Suggested Reading Order

1. WhatsApp Platform — strongest SaaS architecture case
2. Investiga+ — public SaaS and fullstack implementation
3. ApplyFlow — local-first and privacy-first workflow product
4. Career Suite — AI-assisted career tooling
5. DevFlow Financeiro — dashboard, score engine and product insights

---

## Roadmap

- Add screenshots and GIFs for each product
- Add architecture diagrams
- Add decision records for key trade-offs
- Add demo videos
- Expand bilingual versions beyond priority cases
- Add public demo data where applicable
- Add more detailed product metrics and roadmap notes

---

## Author

Created by Gustavo Marques de Lima.

- Portfolio: https://devflowlabs.com.br
- GitHub: https://github.com/gustavomarques00
- DevFlow Labs GitHub: https://github.com/devflow-modules
- LinkedIn: https://www.linkedin.com/in/gustavo-marques-00
