# WhatsApp Platform Case Study

**Portuguese version:** [README.pt-BR.md](README.pt-BR.md)

WhatsApp Platform is a multi-tenant SaaS product for customer support, WhatsApp Cloud API operations, automation, AI-assisted replies, operational metrics, activation control and billing.

This case study documents the architecture and product decisions behind one of the strongest DevFlow Labs SaaS initiatives.

---

## Case Study Documents

| Document | Purpose |
|---|---|
| [Architecture](architecture.md) | System boundaries, webhook flow, tenant model, AI layer and billing architecture |
| [Product Roadmap](product-roadmap.md) | MVP scope, product phases, monetization and enterprise-readiness path |
| [Security Decisions](security-decisions.md) | Authentication, RBAC, tenant isolation, webhook security, secrets and AI safety |
| [Business Context](business-context.md) | Market problem, target customers, value proposition and monetization strategy |
| [Recruiter Notes](recruiter-notes.md) | What recruiters and interviewers should evaluate in this case |

---

## Product Context

Many businesses depend on WhatsApp as their main communication channel but lack structure, team visibility, automation, metrics and controlled access.

The WhatsApp Platform was designed to turn WhatsApp communication into an operational SaaS product with inbox, roles, automation, AI and billing.

---

## Problem

Businesses using WhatsApp often face:

- No centralized inbox for teams
- Poor visibility into unanswered conversations
- No SLA or response metrics
- Manual onboarding of numbers
- No structured automation rules
- No AI-assisted replies
- No usage-based billing layer
- Difficulty managing multiple tenants and channels

---

## Solution

The platform provides a multi-tenant operational layer over WhatsApp Cloud API, enabling businesses to manage conversations, users, roles, automations, AI responses, metrics, activation status and billing.

---

## Personas

### Platform Admin

Responsible for global platform management, tenant visibility, activation status, internal support and administrative controls.

### Manager

Responsible for team performance, conversation queues, operational metrics and support quality.

### Operator

Responsible for responding to conversations, handling assigned threads and executing daily customer support operations.

---

## Core Features

- Multi-tenant account structure
- WhatsApp Cloud API integration
- Webhook-based inbound message handling
- Operational inbox
- Conversation history
- Role-based access control
- Manager dashboard
- Activation control center
- AI-assisted replies
- Usage tracking
- Stripe billing foundation
- SLA-oriented metrics
- Message status and audit trail

---

## Architecture Overview

```text
Next.js Application
  ├── Auth
  ├── Inbox
  ├── Conversation history
  ├── Manager dashboard
  ├── Activation center
  ├── Billing UI
  └── Admin pages

Backend/API Layer
  ├── Auth and session validation
  ├── Tenant resolution
  ├── WhatsApp webhook handler
  ├── Message processing
  ├── Conversation service
  ├── AI reply service
  ├── Usage tracking
  └── Billing integration

Database
  ├── Tenants
  ├── Users
  ├── Roles
  ├── WhatsApp channels
  ├── Inbox threads
  ├── Messages
  ├── Usage aggregates
  └── Billing subscriptions

External Services
  ├── Meta WhatsApp Cloud API
  ├── OpenAI API
  ├── Stripe
  └── Vercel/Railway/Supabase infrastructure
```

---

## Technical Stack

### Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- ShadCN UI

### Backend

- Next.js API routes / server functions
- Prisma ORM
- PostgreSQL
- JWT/session validation
- Webhook handlers

### Integrations

- Meta WhatsApp Cloud API
- OpenAI API
- Stripe billing
- External webhook flows

### Infrastructure

- Vercel
- Supabase/PostgreSQL
- GitHub Actions
- Environment-based configuration

---

## Authentication and Roles

The platform uses role-based access control with three product roles:

- `operator`
- `manager`
- `platform_admin`

Each role has access to different operational views and actions.

---

## AI Strategy

AI is used as an assistant layer, not as a replacement for the human operator.

Main AI use cases:

- Suggested replies
- Automatic replies when safe
- Conversation support
- Productivity improvement
- Operational consistency

Safety controls include:

- Avoiding replies on closed conversations
- Avoiding replies when a human is assigned
- Duplicate automation protection
- Claim/lock mechanism for automatic processing

---

## Billing Strategy

The platform supports SaaS monetization concepts such as:

- Plan limits
- Usage aggregation
- Message usage tracking
- AI usage tracking
- Overage logic
- Stripe integration
- Subscription state reconciliation

---

## Operational Metrics

Examples of operational metrics:

- Awaiting agent conversations
- Unassigned conversations
- Critical SLA threads
- Response delay
- Last inbound message
- Unanswered inbound count
- Conversation phase

---

## Business Value

This product demonstrates advanced SaaS engineering:

- Multi-tenant architecture
- Complex third-party integration
- Webhook reliability
- AI workflow design
- Billing and usage tracking
- Operational dashboards
- Role-based access
- Product-oriented engineering

---

## Roadmap

- Automation rules engine
- Sales funnel module
- Advanced analytics
- White-label tenant configuration
- More AI assistant controls
- Team performance reports
- Public product demo

---

## Portfolio Value

This is one of the strongest DevFlow Labs cases because it connects software engineering, product design, integrations, AI, operations and monetization in a single SaaS platform.
