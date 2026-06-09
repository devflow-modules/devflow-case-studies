# WhatsApp Platform Security Decisions

This document summarizes the security-oriented decisions behind the DevFlow WhatsApp Platform case study.

---

## Security Goals

The platform handles customer communication workflows, tenant data, billing state and external integrations. Security decisions focus on:

- Tenant isolation
- Secure authentication
- Role-based access control
- Safe webhook handling
- Protection of API keys and secrets
- Controlled AI automation
- Auditability

---

## Authentication

The platform is designed around authenticated sessions and protected routes.

Recommended principles:

- Server-side session validation
- Secure cookie handling where applicable
- Token expiration
- Refresh flow when needed
- No sensitive tokens exposed unnecessarily to the browser

---

## Authorization

Access should be role-based and tenant-scoped.

Core roles:

- `operator`
- `manager`
- `platform_admin`

Role boundaries:

- Operators should only handle assigned or visible conversations.
- Managers should access team and tenant-level operational metrics.
- Platform admins should manage activation, support and platform-level settings.

---

## Tenant Isolation

Every query and mutation should resolve tenant context before accessing operational data.

Important rules:

- Never trust tenant identifiers sent from the client without validation.
- Always derive user permissions from authenticated context.
- Ensure conversations, messages, channels and usage records are tenant-scoped.
- Avoid cross-tenant dashboard aggregation unless explicitly authorized.

---

## Webhook Security

Webhook endpoints require strict handling because they receive external traffic.

Key decisions:

- Validate verification tokens during setup.
- Validate request origin/signature when supported.
- Normalize inbound payloads before persistence.
- Make message ingestion idempotent.
- Avoid leaking webhook secrets in logs.
- Treat webhook payloads as untrusted input.

---

## Secrets and Environment Variables

Sensitive values should remain outside the repository.

Examples:

- WhatsApp access token
- WhatsApp verify token
- App secret
- Stripe secret key
- Stripe webhook secret
- OpenAI API key
- Database URL
- JWT/session secret

---

## AI Safety Controls

AI should not act without product-level safeguards.

Controls:

- Do not auto-reply to closed conversations.
- Do not auto-reply when a human operator is actively assigned.
- Avoid duplicate automation runs.
- Track AI usage per tenant.
- Allow human review where possible.
- Log automation decisions for debugging and accountability.

---

## Billing and Usage Integrity

Billing-related data should be treated as critical business state.

Decisions:

- Track usage events server-side.
- Reconcile subscription state with Stripe webhooks.
- Avoid trusting client-side plan state.
- Store billing identifiers securely.
- Enforce plan limits from server-side checks.

---

## Auditability

Operational systems benefit from audit records.

Recommended audit points:

- Login events
- Role changes
- Tenant activation changes
- Webhook failures
- AI-generated replies
- Billing state updates
- Message assignment changes

---

## Recruiter Signal

This case demonstrates practical understanding of:

- Secure SaaS boundaries
- RBAC
- Tenant isolation
- Webhook security
- Secret management
- AI automation safety
- Billing integrity
