# LoanEase UX Case Study

# 03 Information Architecture

Version: 1.0  
Status: Research-Informed Draft  
Last Updated: 2026-08-14  
Author: Sri Krishna Prabhu Kasinadhuni  

---

## Purpose

This document defines the proposed Information Architecture (IA) for the LoanEase digital loan application experience.

The IA translates the research findings, personas, user journey, and user flow into a structured set of screens, sections, navigation areas, and information relationships.

The purpose is to ensure that:

- Users can find important information easily.
- The application process is understandable.
- Eligibility and financial information are available before commitment.
- Documents and application progress are easy to track.
- Users can understand what is happening after submission.
- Important actions and next steps are clearly presented.

This is a research-informed design structure and will be refined during wireframing and usability testing.

---

# 1. Information Architecture Principles

The proposed IA follows these principles.

## 1.1 Clarity Before Commitment

Important financial and eligibility information should be available before the user begins a full application.

## 1.2 Make Progress Visible

Users should be able to understand where they are in the application process.

## 1.3 Group Related Information

Information that belongs to the same task or decision should be presented together.

## 1.4 Keep Primary Actions Obvious

Each major screen should have a clear primary action.

## 1.5 Reduce Navigation During the Application

Once the user begins an application, navigation should focus on completing and tracking that application rather than creating unnecessary movement between unrelated areas.

## 1.6 Support Both Personas

The IA should support:

- The Clarity-Seeking Applicant, who needs information before committing.
- The Progress-Focused Applicant, who needs visibility after submission.

---

# 2. Proposed High-Level Structure

The proposed LoanEase structure is:

```text
LoanEase
│
├── Home
│
├── Loans
│   ├── Loan Overview
│   ├── Loan Details
│   ├── Eligibility
│   └── Financial Information
│
├── Apply
│   ├── Application Preparation
│   ├── Personal Information
│   ├── Employment & Financial Information
│   ├── Loan Requirements
│   ├── Documents
│   ├── Review
│   └── Confirmation
│
├── My Application
│   ├── Application Status
│   ├── Progress
│   ├── Documents
│   ├── Updates
│   └── Required Actions
│
├── Notifications
│
└── Support
    ├── Help
    ├── FAQs
    └── Contact Support
```

This represents the conceptual product structure rather than a final navigation design.

---

# 3. Primary Navigation

The primary navigation should provide access to the major areas of the product.

Proposed areas:

| Navigation Area | Purpose |
|---|---|
| Home | Entry point and overview |
| Loans | Explore loan options and information |
| My Application | Track an active application |
| Notifications | View important updates |
| Support | Access help and assistance |

The exact navigation pattern will be determined during wireframing.

---

# 4. Home

## Purpose

Provide an accessible starting point for users and direct them toward the most relevant action.

## Primary Content

The Home area may contain:

- Loan options.
- Key information.
- Eligibility access.
- Application status if an application already exists.
- Important notifications.
- Support access.

## Primary User Questions

The Home experience should help answer:

- What can I do here?
- Which loan is relevant to me?
- Can I check my eligibility?
- Where is my existing application?

---

# 5. Loans

The Loans section is intended to support users before they commit to an application.

```text
Loans
│
├── Loan Overview
│
├── Loan Details
│
├── Eligibility
│
└── Financial Information
```

---

## 5.1 Loan Overview

### Purpose

Allow users to understand available loan options.

### Information

Potential content includes:

- Loan type.
- General purpose.
- Typical amount or range where appropriate.
- High-level eligibility information.
- Link to detailed information.

### Primary Action

**View Loan Details**

---

## 5.2 Loan Details

### Purpose

Help users understand the financial and practical implications of a selected loan.

### Information

Potential content includes:

- Loan amount.
- Interest information.
- Estimated repayment.
- EMI information.
- Fees and charges.
- Important terms.
- Eligibility summary.

### Primary Actions

- Calculate EMI.
- Check Eligibility.
- Start Application.

---

## 5.3 Eligibility

### Purpose

Allow users to determine whether they are likely to qualify before completing the full application.

### Information

The experience may request information relevant to eligibility.

### Result States

```text
Eligibility Check
       ↓
    Result
    /    Eligible  Not Eligible
   ↓          ↓
Continue    Explanation
Application  / Alternatives
```

### Primary Actions

For eligible users:

**Continue Application**

For users who are not eligible:

**Review Result / Explore Alternatives**

The exact eligibility logic is outside the scope of this UX project.

---

## 5.4 Financial Information

Financial information should be understandable without requiring users to navigate away from the relevant decision.

Potential content includes:

- Interest information.
- EMI calculation.
- Repayment information.
- Fees.
- Important charges.
- Loan terms.
- Explanations of unfamiliar terminology.

### Design Principle

**Financial information should be presented in plain language wherever possible.**

---

# 6. Apply

The Apply section contains the main application workflow.

```text
Apply
│
├── Application Preparation
│
├── Personal Information
│
├── Employment & Financial Information
│
├── Loan Requirements
│
├── Documents
│
├── Review
│
└── Confirmation
```

---

# 7. Application Preparation

## Purpose

Prepare the user before entering the application.

## Information

The preparation screen should explain:

- What information is required.
- What documents may be required.
- Main application stages.
- Important conditions.
- What happens after submission.

### Primary Action

**Start Application**

---

# 8. Personal Information

## Purpose

Collect required personal information.

## Information Structure

Potential categories include:

- Personal details.
- Contact information.
- Address information.

The exact fields will be determined during detailed wireframing.

### UX Requirements

- Clear labels.
- Simple instructions.
- Validation.
- Error prevention.
- Progress indication.

---

# 9. Employment & Financial Information

## Purpose

Collect information relevant to the user's financial situation and application.

Potential information categories include:

- Employment.
- Income.
- Financial commitments.
- Other relevant application information.

The exact fields should not be assumed until the product requirements are defined.

### UX Requirements

- Explain unfamiliar terms.
- Avoid unnecessary complexity.
- Provide clear validation.
- Preserve progress.

---

# 10. Loan Requirements

## Purpose

Capture the user's requested loan information.

Potential information includes:

- Requested loan amount.
- Loan purpose.
- Desired repayment information.
- Other relevant requirements.

### Primary UX Goal

Keep the user aware of the financial context while completing the application.

---

# 11. Documents

The Documents area supports the collection and tracking of required documents.

```text
Documents
│
├── Required Documents
├── Uploaded Documents
├── Missing Documents
└── Upload Status
```

## Information

Each document should communicate:

- Document name.
- Whether it is required.
- Submission status.
- Upload action.
- Whether further action is required.

## Example Information Structure

```text
Documents

✓ Identity Proof
   Submitted

✓ Address Proof
   Submitted

○ Income Proof
   Required

○ Bank Statement
   Required

2 of 4 completed
```

The exact visual treatment will be decided during wireframing.

---

# 12. Review Application

## Purpose

Allow the user to verify their application before submission.

## Information Groups

```text
Review Application
│
├── Personal Information
├── Employment Information
├── Financial Information
├── Loan Details
├── Documents
└── Terms / Important Information
```

## User Actions

The user should be able to:

- Review information.
- Edit information.
- Confirm documents.
- Review important terms.
- Submit the application.

### Primary Action

**Submit Application**

---

# 13. Confirmation

## Purpose

Confirm that the application has been successfully submitted and explain what happens next.

## Information

The confirmation should include:

- Submission confirmation.
- Application/reference number.
- Current status.
- What happens next.
- Expected update information where available.
- Access to application tracking.

### Primary Action

**Track Application**

---

# 14. My Application

The My Application area is the central location for post-submission visibility.

```text
My Application
│
├── Overview
├── Status
├── Progress
├── Documents
├── Updates
└── Required Actions
```

This area directly addresses the strongest research finding around application uncertainty.

---

# 15. Application Overview

## Purpose

Give users a concise summary of their current application.

## Information

Potential content:

- Application number.
- Loan type.
- Requested amount.
- Current status.
- Last update.
- Required action.
- Next expected step.

### Primary Action

**View Application Status**

---

# 16. Application Status

## Purpose

Show the current stage of the application.

## Proposed Status Structure

```text
Application Submitted
        ↓
Documents Under Review
        ↓
Application Under Review
        ↓
Decision Pending
        ↓
Decision Available
```

The actual status names and process will be refined during later design.

---

## Status Information

Each status should answer:

- Where am I?
- What has happened?
- What is happening now?
- Do I need to do anything?
- What happens next?

---

# 17. Application Progress

## Purpose

Make the overall process understandable at a glance.

## Example Structure

```text
Application Progress

✓ Application Submitted
✓ Documents Received
● Application Under Review
○ Decision Pending
○ Decision Available
```

The exact progress model is a design hypothesis and should be tested.

---

# 18. Documents Within My Application

The post-submission Documents area allows the user to understand the status of submitted documentation.

Potential states:

- Received.
- Under review.
- Additional information required.
- Action required.

## Key UX Goal

The user should not have to guess whether their documents were successfully received.

---

# 19. Updates

## Purpose

Provide a central record of important application communications.

Potential update types include:

- Application submitted.
- Document received.
- Status changed.
- Additional information required.
- Decision available.

## Information Hierarchy

Each update should make the following clear:

1. What changed?
2. When did it change?
3. Does the user need to act?
4. What should they do next?

---

# 20. Required Actions

## Purpose

Clearly identify actions the user must take.

Examples include:

- Upload missing document.
- Provide additional information.
- Review updated information.
- Respond to a request.

## Design Principle

**Required actions should be visually distinguishable from informational updates.**

---

# 21. Notifications

## Purpose

Provide timely updates without requiring users to repeatedly check the application.

Potential notifications include:

- Application submission confirmation.
- Document submission confirmation.
- Status changes.
- Additional information requests.
- Decision availability.

Notifications should link back to the relevant application context.

---

# 22. Support

The Support area provides assistance when users cannot resolve a question through the application.

```text
Support
│
├── Help
├── FAQs
└── Contact Support
```

## Support Goals

Users should be able to:

- Find answers to common questions.
- Understand unfamiliar terms.
- Get help with application problems.
- Contact support when required.

This responds to the research finding that customer support and communication are important parts of the loan experience.

---

# 23. Information Hierarchy

The product should distinguish between:

### Primary Information

Information required to make the current decision or complete the current task.

Examples:

- Eligibility result.
- Current application status.
- Required document.
- Primary financial information.
- Required next action.

### Secondary Information

Supporting information that helps users understand the primary information.

Examples:

- Definitions.
- Explanations.
- FAQs.
- Additional terms.

### Tertiary Information

Information that should remain accessible but should not distract from the primary task.

Examples:

- Detailed policy information.
- Extended help content.
- Additional background information.

---

# 24. Core Application Information Model

The main application can be understood as five connected information groups:

```text
Application
│
├── Applicant Information
│
├── Loan Information
│
├── Financial Information
│
├── Documents
│
└── Status & Updates
```

These groups should remain logically connected throughout the experience.

---

# 25. Relationship Between Information Areas

The conceptual relationship is:

```text
Loan Information
       ↓
Eligibility
       ↓
Application
       ├── Applicant Information
       ├── Financial Information
       ├── Loan Requirements
       └── Documents
                ↓
           Submission
                ↓
          Application Status
                ↓
             Updates
                ↓
             Decision
```

This relationship provides the foundation for the later screen architecture.

---

# 26. Global Access

Some functions should remain accessible across relevant areas.

Potential global functions include:

- Notifications.
- Support.
- Application status.
- Account/profile access where required.

The exact placement will be decided during wireframing.

---

# 27. Persona Alignment

## Clarity-Seeking Applicant

The IA should make these areas easy to reach:

```text
Loans
  ↓
Loan Details
  ↓
Financial Information
  ↓
Eligibility
  ↓
Application Preparation
```

### Primary Need

**Understand before committing.**

---

## Progress-Focused Applicant

The IA should make these areas easy to reach:

```text
My Application
  ↓
Status
  ↓
Progress
  ↓
Documents
  ↓
Updates
  ↓
Required Actions
```

### Primary Need

**Understand what is happening after submission.**

---

# 28. Key Navigation Decision

The strongest navigation decision from the research is to treat **My Application** as a central post-submission destination rather than making users repeatedly navigate through the original application process to find their status.

This supports the research finding that lack of application status visibility is a major source of uncertainty.

---

# 29. Proposed Screen Inventory

The current IA implies the following primary screens or states:

| # | Screen / State | Primary Purpose |
|---|---|---|
| 1 | Home | Entry and overview |
| 2 | Loan Overview | Explore loan options |
| 3 | Loan Details | Understand a selected loan |
| 4 | Eligibility Checker | Assess likely eligibility |
| 5 | Eligibility Result | Communicate eligibility outcome |
| 6 | Application Preparation | Explain requirements before starting |
| 7 | Personal Information | Collect applicant details |
| 8 | Employment & Financial Information | Collect financial context |
| 9 | Loan Requirements | Capture requested loan details |
| 10 | Document Checklist | Show required documents |
| 11 | Document Upload | Submit documents |
| 12 | Application Review | Verify information |
| 13 | Submission Confirmation | Confirm successful submission |
| 14 | Application Overview | Summarise active application |
| 15 | Application Status | Show current status |
| 16 | Application Progress | Show progress through stages |
| 17 | Application Documents | Show document status |
| 18 | Application Updates | Show communication history |
| 19 | Required Actions | Show tasks requiring attention |
| 20 | Decision | Communicate outcome |
| 21 | Approved Offer / Next Steps | Explain approved outcome |
| 22 | Not Approved / Next Steps | Explain outcome and available next steps |
| 23 | Notifications | Show important updates |
| 24 | Support | Help and assistance |

This is a working inventory. Some items may eventually become states within a screen rather than separate screens.

---

# 30. Screen vs State Consideration

Not every item in the inventory necessarily requires a separate screen.

For example:

- Eligibility Result may be a state within the Eligibility screen.
- Upload success may be a state within Document Upload.
- Additional information required may be a state within Application Status.
- Decision may be a state within Application Overview.
- Required Actions may be displayed within the Application Overview.

The final decision should be based on task complexity and usability during wireframing.

---

# 31. Navigation Model

The proposed conceptual model is:

```text
                    ┌──────────────┐
                    │     Home     │
                    └──────┬───────┘
                           │
             ┌─────────────┴─────────────┐
             ↓                           ↓
      ┌──────────────┐           ┌────────────────┐
      │    Loans     │           │ My Application │
      └──────┬───────┘           └───────┬────────┘
             │                           │
             ↓                           ↓
       Loan Details                 Status / Progress
             │                           │
             ↓                           ├── Documents
        Eligibility                     ├── Updates
             │                           └── Actions
             ↓
        Application
             │
             ↓
        Documents
             │
             ↓
          Review
             │
             ↓
        Confirmation
             │
             └──────────────→ My Application
```

This is a conceptual structure and not a final visual navigation design.

---

# 32. Information Architecture Priorities

Based on the research, the following areas should receive the strongest attention during wireframing:

### Priority 1 — Application Status

Users need clear visibility after submission.

### Priority 2 — Eligibility and Financial Information

Users need clarity before committing.

### Priority 3 — Documents

Users need to understand requirements and submission status.

### Priority 4 — Application Progress

Users need to understand what has happened and what remains.

### Priority 5 — Updates and Required Actions

Users need timely communication and clear next steps.

---

# 33. IA-to-Research Traceability

| Research Finding | Information Architecture Response |
|---|---|
| Eligibility difficulty | Dedicated Eligibility area |
| Financial terminology confusion | Financial Information within Loan Details |
| EMI calculator requested by 26 participants | Financial Information area |
| Eligibility checker requested by 25 participants | Eligibility area |
| Document collection difficulty | Dedicated Documents area |
| Upload progress requested by 22 participants | Document status and progress |
| Long approval process | My Application area |
| Lack of status updates | Application Status and Updates |
| Estimated approval timeline requested by 21 participants | Status / Progress information |
| Poor customer support | Dedicated Support area |
| Unclear fees | Loan Details / Financial Information |

---

# 34. Scope Boundary

This Information Architecture represents the proposed user-facing structure of the LoanEase experience.

It does not attempt to model:

- Internal bank systems.
- Backend architecture.
- Credit scoring infrastructure.
- Internal employee dashboards.
- Regulatory processing.
- Actual banking system integrations.

Where the real-world system is unknown, this IA intentionally remains at the user-experience level.

---

# 35. Validation Plan

The IA is a design hypothesis and should be validated through:

1. Wireframing.
2. Navigation review.
3. Task-based usability testing.
4. Observation of navigation errors.
5. Feedback on information clarity.
6. Iteration based on findings.

Particular attention should be given to whether users can:

- Find eligibility information.
- Understand loan costs.
- Locate required documents.
- Find their application status.
- Identify required actions.
- Understand what happens next.

---

# 36. Next Step

The next stage is **Screen Requirements / Content Structure**.

Before creating detailed wireframes, each priority screen should be defined by:

- Screen purpose.
- Primary user goal.
- Required information.
- Primary action.
- Secondary actions.
- Navigation.
- Important states.
- Error conditions.
- Persona relevance.

This will provide the bridge between the Information Architecture and the first wireframes.

---

## Related Documents

- [06 Research Synthesis](../02_Research/06_Research_Synthesis.md)
- [07 Personas](../02_Research/07_Personas.md)
- [01 User Journey](01_User_Journey.md)
- [02 User Flow](02_User_Flow.md)
- [02 Problem Statement](../00_Project_Documentation/02_Problem_Statement.md)
- [08 Decision Log](../00_Project_Documentation/08_Decision_Log.md)
- [11 Retrospective](../00_Project_Documentation/11_Retrospective.md)

---

## Document History

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-08-14 | Sri Krishna Prabhu Kasinadhuni | Created research-informed Information Architecture connecting research findings, personas, user journey, and user flow to the proposed LoanEase screen structure. |
