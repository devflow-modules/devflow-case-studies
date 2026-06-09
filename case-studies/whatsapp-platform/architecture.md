# WhatsApp Platform Architecture

This document describes the architectural thinking behind the DevFlow WhatsApp Platform case study.

---

## Architecture Goal

The goal is to provide a SaaS-ready operational layer for businesses using WhatsApp as a primary customer communication channel.

The architecture prioritizes:

- Multi-tenant isolation
- Secure authentication and authorization
- Reliable webhook processing
- Operational inbox workflows
- AI-assisted productivity
- Usage tracking and monetization
- Clear product boundaries

---

## High-Level Flow

```text
Customer sends WhatsApp message
        ↓
Meta WhatsApp Cloud API
        ↓
Webhook endpoint
        ↓
Signature/token validation
        ↓
Tenant/channel resolution
        ↓
Message normalization
        ↓
Conversation/thread service
        ↓
Inbox + metrics + automation rules
        ↓
Operator, manager or AI-assisted response
```

---

## Main System Boundaries

### 1. Web Application

Responsible for user-facing workflows:

- Login/session experience
- Inbox operations
- Conversation history
- Manager dashboards
- Platform admin pages
- Activation and onboarding screens
- Billing and usage visibility

### 2. API Layer

Responsible for product actions and integrations:

- Session validation
- Role-based authorization
- Tenant resolution
- WhatsApp webhook ingestion
- Message creation and status updates
- AI reply orchestration
- Usage tracking
- Billing event handling

### 3. Domain Layer

Responsible for business logic:

- Tenant activation rules
- Conversation ownership
- Queue state
- SLA classification
- Assignment rules
- Automation safety checks
- Billing limits and usage aggregation

### 4. Data Layer

Responsible for persistence:

- Tenants
- Users
- Roles
- Channels
- Conversations
- Messages
- Usage events
- Billing subscriptions
- Audit records

---

## Multi-Tenant Model

The platform is designed around tenant-scoped data.

Every operational entity should be associated with a tenant context:

- Users belong to a tenant
- WhatsApp channels belong to a tenant
- Conversations belong to a tenant
- Messages belong to a conversation and tenant
- Usage records belong to a tenant
- Billing state belongs to a tenant

This enables white-label operation, separated customer accounts and future enterprise plans.

---

## Webhook Reliability

WhatsApp integration requires webhook-first architecture.

Important design concerns:

- Validate webhook source
- Normalize payloads
- Avoid duplicate message insertion
- Make processing idempotent
- Separate ingestion from business processing when needed
- Track message status changes
- Avoid AI automation race conditions

---

## AI Assistant Boundary

AI is treated as an assistant layer, not the source of truth.

The AI layer can support:

- Suggested replies
- Draft generation
- FAQ-based answers
- Conversation summarization
- Operator productivity

The AI layer should not bypass:

- Tenant permissions
- Conversation assignment state
- Closed conversation checks
- Human override rules
- Billing and usage limits

---

## Billing and Usage Architecture

The monetization model can be supported with usage events such as:

- Sent messages
- Received messages
- AI reply generations
- Active operators
- Connected WhatsApp channels
- Tenant plan limits

Usage aggregation supports:

- Plan enforcement
- Overage calculation
- Stripe billing reconciliation
- Product analytics
- Upgrade prompts

---

## Recruiter Signal

This architecture demonstrates:

- Real SaaS design
- Multi-tenant thinking
- Integration with external APIs
- Webhook reliability concerns
- Authentication and authorization maturity
- AI workflow safety
- Product and business alignment
