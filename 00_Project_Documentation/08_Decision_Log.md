# LoanEase UX Case Study

# 08 Decision Log

Version: 1.0  
Status: Retrospectively Documented  
Last Updated: 2026-08-12  
Author: Sri Krishna Prabhu Kasinadhuni  

---

## Purpose

This document records important project decisions and the reasoning or evidence behind them.

Where decisions are reconstructed after the fact, they are identified as retrospective documentation.

---

## Decision Log

| ID | Decision | Reason / Evidence | Outcome |
|---|---|---|---|
| D-01 | Use user research to guide design decisions | Project objective was to create an evidence-based UX case study | Adopted |
| D-02 | Use both survey and interviews | Survey provides breadth; interviews provide depth | Adopted |
| D-03 | Do not conduct observation | Financial applications involve sensitive/private information | Observation excluded |
| D-04 | Keep raw research data out of public GitHub | Privacy, data minimisation, and cleaner public repository | Adopted |
| D-05 | Use research analysis rather than raw responses in public repository | Makes findings accessible without exposing raw participant data | Adopted |
| D-06 | Treat the project as a portfolio case study rather than only an assignment | Project scope expanded beyond original assignment requirements | Adopted |
| D-07 | Use research convergence to prioritise design opportunities | Survey and interviews identified overlapping themes | Adopted |
| D-08 | Prioritise transparency and status visibility for further exploration | Strong survey and interview evidence | To inform design |

---

## Decision D-01 — Evidence-Based Design

### Decision

Design decisions should be connected to research evidence wherever possible.

### Reason

The project aims to demonstrate UX reasoning rather than simply present a visual interface.

---

## Decision D-02 — Mixed Research Methods

### Decision

Use survey and semi-structured interviews.

### Reason

The survey provides quantitative patterns, while interviews help explain user experiences and reasons behind those patterns.

---

## Decision D-03 — Observation Not Conducted

### Decision

Do not conduct observation of real financial application activity.

### Reason

The subject involves financial and potentially private information. Observing such activity would introduce privacy and ethical concerns.

### Alternative

Use survey and interviews to gather participant experiences.

---

## Decision D-04 — Raw Research Data Kept Local

### Decision

Do not publish raw survey or interview responses to GitHub.

### Reason

The raw data includes participant demographic information and research responses. Even though the user indicated that the data does not contain names, emails, phone numbers, or location data, the project adopted a conservative approach and retained raw data locally.

---

## Decision D-05 — Public Repository Contains Summarised Research

### Decision

Use analysed findings and documentation rather than raw response files in the public repository.

### Reason

The public repository should contain intentional portfolio artifacts rather than every intermediate project file.

---

## Decision D-06 — Portfolio Direction

### Decision

Develop LoanEase as a portfolio UX case study rather than treating the original university assignment as the final scope.

### Reason

The project already includes research, analysis, documentation, and an opportunity to demonstrate the full UX process.

---

## Decision D-07 — Research Convergence

### Decision

Use themes supported by both survey and interview evidence as strong candidates for design prioritisation.

### Reason

Independent quantitative and qualitative evidence converged around approval uncertainty, communication, eligibility, documentation, and transparency.

---

## Decision D-08 — Design Priority Direction

### Decision

Explore transparency and application status visibility as major design opportunities.

### Evidence

Real-time application status tracking was the most requested survey feature, with 27 responses. Interviews also repeatedly identified approval delays and lack of updates.

---

## Git/GitHub Decisions

The project also involved several repository-management decisions.

Important decisions included:

- Keeping `.gitignore` committed.
- Removing raw research files from the public repository.
- Keeping raw research files locally.
- Removing assignment-only and development-evidence material from the public repository.
- Rewriting history only when necessary to remove previously committed raw research data.
- Using `git push --force-with-lease` rather than plain `--force` when updating rewritten history.

These decisions are documented in the project handover and Git history.

---

## Related Documents

- 04_Assumptions_Log.md
- 05_Research_Planning.md
- 11_Retrospective.md

---

## Document History

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-08-12 | Sri Krishna Prabhu Kasinadhuni | Retrospectively documented major research, privacy, portfolio, and repository decisions. |