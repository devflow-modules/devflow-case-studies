# ApplyFlow Architecture

This document describes the architectural reasoning behind ApplyFlow, a local-first job application workflow assistant.

---

## Architecture Goal

ApplyFlow is designed to help candidates organize job applications without giving up control over their career data.

The architecture prioritizes:

- Local-first data handling
- Privacy-first workflow design
- Human-in-the-loop assistance
- Portable JSON import/export
- Optional AI features
- Browser-extension assisted workflows
- Dashboard-based visibility

---

## High-Level Flow

```text
Candidate views job opportunity
        ↓
ApplyFlow captures or imports job context
        ↓
User reviews and saves application data locally
        ↓
Dashboard organizes application funnel
        ↓
Reusable answer bank supports forms/interviews
        ↓
Optional AI layer helps analyze fit and prepare responses
        ↓
User remains in control of every action
```

---

## Main System Boundaries

### 1. Browser Extension Layer

Responsible for assisted workflows near the job application context.

Potential responsibilities:

- Detect application pages
- Suggest reusable answers
- Capture job metadata with user approval
- Avoid blind submissions
- Store local workflow state

### 2. Dashboard Layer

Responsible for productivity and visibility.

Potential responsibilities:

- Application funnel
- Job tracking board
- Reusable answer bank
- Metrics and status views
- JSON import/export
- Optional AI coaching interface

### 3. Shared Domain Layer

Responsible for contracts and reusable logic.

Potential responsibilities:

- Candidate profile schema
- Job opportunity schema
- Application status model
- Answer bank model
- Import/export validation
- Job scoring heuristics

### 4. Optional AI Layer

Responsible for assisting analysis without owning the workflow.

Potential responsibilities:

- Job fit analysis
- Resume-to-job comparison
- Interview preparation prompts
- Response improvement suggestions
- Application prioritization support

---

## Local-First Model

The local-first model means that the user's career workflow can operate without requiring centralized storage.

Benefits:

- Better privacy
- Lower infrastructure cost
- Easier portability
- User-owned data
- Reduced backend dependency

---

## Human-in-the-Loop Design

ApplyFlow is not designed for blind mass application.

The user should always review:

- Captured job data
- Suggested answers
- AI-generated analysis
- Exported data
- Any action related to an application

---

## Recruiter Signal

This architecture demonstrates:

- Product architecture thinking
- Privacy-first design
- Browser extension workflow reasoning
- TypeScript domain modeling
- AI as an assistive layer
- Candidate productivity use case understanding
