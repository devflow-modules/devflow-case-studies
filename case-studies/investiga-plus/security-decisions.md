# Investiga+ Security Decisions

This document summarizes the security-oriented decisions behind the Investiga+ case study.

---

## Security Goals

Investiga+ handles authenticated users, company lookup history, external API access and user-scoped data. Security decisions focus on:

- Secure authentication
- Protected routes
- User-scoped records
- Safe external API usage
- Environment-based secrets
- Input validation
- Centralized error handling

---

## Authentication

Investiga+ uses JWT-based authentication with HttpOnly Cookies.

Key principles:

- Keep session tokens away from direct frontend JavaScript access where possible.
- Validate tokens on protected backend routes.
- Use token expiration.
- Keep authentication secrets in environment variables.
- Protect dashboard and search routes behind authenticated access.

---

## Authorization and Data Scope

Every user-facing record should be scoped to the authenticated user.

Examples:

- Search history belongs to the authenticated user.
- Profile data belongs to the authenticated user.
- Dashboard data should not expose other users' records.
- Administrative access should be separated from regular user access if introduced later.

---

## Input Validation

CNPJ search flows require validation before external API calls.

Validation goals:

- Normalize CNPJ input.
- Reject invalid formats.
- Avoid unnecessary external API calls.
- Reduce malformed requests.
- Keep error feedback predictable.

---

## External API Safety

External API credentials and provider details should be isolated in the backend service layer.

Decisions:

- Never expose provider tokens to the frontend.
- Centralize provider communication in a service module.
- Normalize provider responses before returning data to the UI.
- Handle provider failures with controlled errors.
- Avoid logging sensitive request data.

---

## Environment Variables

Sensitive values should remain outside the repository.

Examples:

- JWT secret
- Database URL
- External API credentials
- Deployment secrets
- Production configuration

---

## Error Handling

Centralized error handling improves security and maintainability.

Principles:

- Avoid leaking internal stack traces to users.
- Return predictable API errors.
- Log server errors internally.
- Separate validation errors from provider errors.
- Keep authentication errors clear but not overly detailed.

---

## Recruiter Signal

This case demonstrates practical understanding of:

- JWT authentication
- HttpOnly Cookies
- Route protection
- User-scoped access
- External API protection
- Validation before integration calls
- Secure backend boundaries
