# Investiga+ Architecture

This document describes the architectural reasoning behind Investiga+, a production-oriented SaaS platform for CNPJ intelligence and company data analysis.

---

## Architecture Goal

Investiga+ was designed to turn repeated CNPJ consultation workflows into a structured SaaS product with secure authentication, external API integration, caching, user history and dashboard-based analysis.

The architecture prioritizes:

- Secure user access
- Clean separation between frontend and backend
- Modular backend services
- External API abstraction
- Cache reuse for repeated CNPJ searches
- User-scoped history
- Testable business logic
- Deployment-ready structure

---

## High-Level Flow

```text
User logs in
    ↓
JWT session via HttpOnly Cookie
    ↓
Dashboard access
    ↓
User searches CNPJ
    ↓
Backend validates input
    ↓
Cache lookup
    ↓
If cached: return stored company record
If not cached: request external API
    ↓
Normalize response
    ↓
Persist company/cache record
    ↓
Save user search history
    ↓
Return structured company data to dashboard
```

---

## Main System Boundaries

### 1. Frontend Application

Responsible for the user-facing SaaS experience:

- Landing page
- Login and registration flows
- Dashboard interface
- CNPJ search UI
- Company result visualization
- Search history view
- Profile and account screens

### 2. Backend API

Responsible for secure business operations:

- Authentication endpoints
- JWT/session validation
- CNPJ search endpoint
- History endpoint
- User-scoped data access
- External API service layer
- Error handling
- Validation middlewares

### 3. Integration Layer

Responsible for communicating with company-data providers:

- External CNPJ API requests
- Payload normalization
- Error handling for provider failures
- Timeout/retry strategy where applicable
- Protection of provider credentials

### 4. Data Layer

Responsible for persistence:

- Users
- Cached company records
- Search history
- Account/profile data
- Usage-related records when needed

---

## Cache Strategy

A key architectural decision is avoiding unnecessary repeated external API calls.

The cache strategy supports:

- Lower latency for repeated searches
- Reduced dependency on external provider availability
- Lower API cost/rate usage
- Consistent history experience
- Better scalability for repeated CNPJ workflows

Recommended cache behavior:

- Normalize CNPJ before lookup
- Check local company records first
- Persist successful external results
- Associate every search with the authenticated user
- Keep provider-specific data isolated from frontend assumptions

---

## Authentication Boundary

Investiga+ uses secure authentication with JWT and HttpOnly Cookies.

Important principles:

- Authentication state should be validated server-side
- Protected routes should require a valid session
- User data should always be scoped to authenticated context
- Tokens should not be exposed unnecessarily to frontend JavaScript
- Secrets should live in environment variables

---

## Testing Strategy

The architecture supports automated tests around:

- Authentication flows
- Route protection
- CNPJ validation
- External API service behavior
- Error handling
- History persistence
- Cached result behavior

Mocking external integrations is important to keep test execution deterministic and avoid dependency on third-party API availability.

---

## Recruiter Signal

This architecture demonstrates:

- Fullstack SaaS delivery
- Secure authentication practices
- API integration maturity
- Cache and persistence design
- Modular backend organization
- Test-oriented thinking
- Product-focused engineering
