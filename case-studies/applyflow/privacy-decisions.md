# ApplyFlow Privacy Decisions

This document summarizes the privacy-oriented decisions behind ApplyFlow.

---

## Privacy Goals

ApplyFlow handles sensitive career data such as job opportunities, application status, reusable answers, interview notes and candidate context.

The product design focuses on:

- User ownership of data
- Local-first storage
- Optional AI usage
- No blind automation
- Portable export/import
- Minimal centralized dependency

---

## Local-First Data

The default model keeps career workflow data under user control.

Benefits:

- Lower exposure of personal data
- Easier portability
- Reduced platform trust burden
- Better user autonomy
- Simpler MVP infrastructure

---

## Optional AI Layer

AI should be optional and controlled by the user.

Design principles:

- AI is an assistant, not an autopilot.
- User decides when to analyze a job.
- User reviews generated content.
- API key usage can be user-controlled.
- AI outputs are suggestions, not submissions.

---

## No Blind Submission

ApplyFlow should not mass-submit applications without explicit user review.

This protects:

- Candidate reputation
- Application quality
- Platform ethics
- Compliance with job platform rules
- User trust

---

## Data Portability

JSON import/export allows the user to move their data without lock-in.

Portable data may include:

- Applications
- Job descriptions
- Answer bank
- Status history
- Notes
- Matching metadata

---

## Recruiter Signal

This case demonstrates practical understanding of privacy-aware product design, AI workflow safety and responsible automation.
