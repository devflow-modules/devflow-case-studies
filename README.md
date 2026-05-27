# DevFlow Labs Case Studies

Public technical case studies for **DevFlow Labs**, a product lab focused on SaaS, automation, AI-assisted workflows and business tools.

This repository documents product reasoning, architecture, technical decisions and roadmap behind DevFlow Labs initiatives without exposing private implementation details.

---

## Purpose

The goal of this repository is to present DevFlow Labs as a real product engineering ecosystem, not only a collection of code repositories.

It serves as a public portfolio layer for:

- SaaS product architecture
- Fullstack engineering decisions
- AI-assisted workflows
- Automation platforms
- Multi-tenant product design
- Operational dashboards
- Privacy-first and local-first product concepts
- Technical documentation as portfolio

---

## Product Ecosystem

### Investiga+
SaaS platform for CNPJ intelligence, company data lookup, secure authentication, cached searches, history and dashboard analytics.

**Repository:** https://github.com/devflow-modules/investiga-mais  
**Live:** https://investigamais.com

**Highlights:**
- Secure authentication with JWT and HttpOnly Cookies
- External API integration
- Prisma ORM and PostgreSQL
- User history and cache strategy
- Jest tests
- CI/CD-ready structure

---

### ApplyFlow
Local-first workflow assistant for job applications, focused on candidate productivity, job tracking, reusable answers and privacy-first workflow design.

**Case Study:** https://github.com/devflow-modules/applyflow-case-study

**Highlights:**
- Browser extension architecture concept
- Next.js dashboard
- Local-first data flow
- JSON export/import
- Optional AI coaching
- Human-in-the-loop workflow

---

### WhatsApp Platform
Multi-tenant WhatsApp Cloud API platform for customer support, operational inbox, automation, AI replies, metrics, activation control and billing.

**Highlights:**
- Multi-tenant architecture
- Role-based access control
- Meta WhatsApp Cloud API integration
- Event processing
- AI-assisted replies
- Operational dashboards

---

### DevFlow Financeiro
Financial management product focused on health score, insights, monthly routine checklist, categorization and dashboard-based decision support.

**Highlights:**
- Product score engine
- Actionable insights
- Monthly operational routine
- Dashboard-first UX
- Business rules layer
- SaaS-ready architecture

---

### Career Suite / ATS Tools
Career workflow tools for resume analysis, job matching, interview preparation and application support.

**Highlights:**
- Resume and job description analysis
- ATS-style scoring
- Optional AI coaching
- Local-first analysis concepts
- Technical case study documentation

---

## Architecture Themes

### Product-first engineering
Every product starts from a real workflow problem and is shaped around user value, operational clarity and future monetization potential.

### Modular fullstack architecture
Projects are structured around clear boundaries between frontend, backend, database, services, integrations and business logic.

### SaaS-ready foundations
Authentication, permissions, dashboards, usage limits and deployment are treated as core architecture concerns.

### AI as an enhancer
AI is used to improve productivity, analysis and decision support, while core workflows remain understandable and maintainable.

### Documentation as product
Case studies, READMEs, architecture notes and roadmaps are part of the product strategy and portfolio positioning.

---

## Core Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- Chakra UI
- ShadCN UI
- Framer Motion

### Backend
- Node.js
- Express
- Prisma ORM
- PostgreSQL
- REST APIs
- JWT authentication

### Infrastructure
- Vercel
- Railway
- Render
- Supabase
- Docker
- GitHub Actions

### AI and Integrations
- OpenAI API
- Meta WhatsApp Cloud API
- Stripe
- ReceitaWS
- External SaaS APIs

### Testing and Quality
- Jest
- Playwright
- Testing Library
- Pytest
- CI/CD validation

---

## Portfolio Value

This repository helps demonstrate:

- Ability to design products from zero
- Strong fullstack architecture skills
- Business-oriented engineering mindset
- SaaS and automation experience
- AI integration in real workflows
- Product documentation and technical storytelling
- Ownership over roadmap, implementation and delivery

---

## Suggested Reading Order

1. **Investiga+** for a production-oriented SaaS case
2. **ApplyFlow** for local-first and privacy-first product design
3. **WhatsApp Platform** for multi-tenant architecture and integrations
4. **DevFlow Financeiro** for product scoring and dashboard UX
5. **Career Suite** for AI-assisted career workflows

---

## Roadmap

- Add individual case study folders for each product
- Add architecture diagrams
- Add screenshots and product flows
- Add decision records for key engineering choices
- Add deployment and observability notes
- Add public demo references where available
- Add bilingual versions of the most important case studies

---

## Planned Repository Structure

```text
case-studies/
├── investiga-plus/
├── applyflow/
├── whatsapp-platform/
├── financeiro/
└── career-suite/

docs/
├── architecture/
├── product-decisions/
├── roadmap/
└── demos/
```

---

## Status

This repository is an evolving public portfolio layer for DevFlow Labs.

Some products are private or partially private by design. This repository exists to communicate the engineering decisions, product thinking and business context behind them while protecting implementation details.

---

## Author

Created by Gustavo Marques de Lima.

- Portfolio: https://devflowlabs.com.br
- GitHub: https://github.com/gustavomarques00
- DevFlow Labs GitHub: https://github.com/devflow-modules
- LinkedIn: https://www.linkedin.com/in/gustavo-marques-00
