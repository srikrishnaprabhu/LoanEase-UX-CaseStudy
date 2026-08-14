# LoanEase UX Case Study

# 02 User Flow

Version: 1.0  
Status: Research-Informed Draft  
Last Updated: 2026-08-14  
Author: Sri Krishna Prabhu Kasinadhuni  

---

## Purpose

This document defines the primary user flow for the LoanEase digital loan application experience.

The flow translates the research findings, personas, and user journey into a sequence of actions and decisions that the product should support.

The focus is on reducing uncertainty during two critical parts of the experience:

1. Before applying — understanding eligibility and financial information.
2. After submitting — understanding application progress and next steps.

---

# 1. Primary User Flow

The proposed primary flow is:

```text
Start
  ↓
Explore Loan
  ↓
Review Loan Information
  ↓
Check Eligibility
  ↓
Eligible?
  ├── No → Explain Result → Explore Alternatives / Exit
  │
  └── Yes
        ↓
   Review Loan Details
        ↓
   Start Application
        ↓
   Complete Application
        ↓
   Document Checklist
        ↓
   Upload Documents
        ↓
   All Required Documents Received?
        ├── No → Show Missing Documents → Upload Remaining Documents
        │
        └── Yes
              ↓
        Review Application
              ↓
        Submit Application
              ↓
        Confirmation
              ↓
        Track Application
              ↓
        Application Under Review
              ↓
        Status Update
              ↓
        Decision
        ├── Approved → Review Offer / Next Steps
        │
        └── Not Approved → Review Decision / Next Steps
```

---

# 2. Flow Overview

| Stage | Primary User Goal | Key Product Responsibility |
|---|---|---|
| Explore Loan | Understand available option | Provide clear loan information |
| Review Information | Understand financial implications | Explain terms, fees and repayment |
| Check Eligibility | Determine whether application is appropriate | Provide clear eligibility guidance |
| Start Application | Begin confidently | Explain process and requirements |
| Complete Application | Provide required information | Guide the user through the form |
| Upload Documents | Submit required documents | Show requirements and upload status |
| Review | Verify information | Allow correction before submission |
| Submit | Complete application | Confirm successful submission |
| Track | Understand progress | Show meaningful application status |
| Decision | Understand outcome | Clearly explain decision and next steps |

---

# 3. Entry Point — Explore Loan

## User Goal

Understand whether the loan is relevant to their needs.

## User Actions

The user:

1. Opens the LoanEase platform.
2. Explores available loan options.
3. Selects a relevant loan type.
4. Reviews basic information.

## Product Should Provide

- Clear loan description.
- Key eligibility information.
- Basic repayment information.
- Interest information.
- Fee information.
- Access to eligibility checking.

## UX Principle

**Explain before asking the user to commit.**

---

# 4. Review Loan Information

## User Goal

Understand the financial implications before applying.

## User Actions

The user reviews:

- Loan amount.
- Interest rate.
- Estimated EMI.
- Fees and charges.
- Repayment information.
- Important conditions.

## Key Questions

The experience should help answer:

- How much will I repay?
- What will my EMI be?
- What fees apply?
- What conditions should I know about?

## Product Opportunities

- EMI calculator.
- Transparent fee breakdown.
- Plain-language explanations.
- Contextual explanations of financial terminology.

---

# 5. Check Eligibility

## User Goal

Determine whether they are likely to qualify before completing the full application.

## User Actions

The user provides the information required by the eligibility checker.

The system evaluates the provided information and presents an eligibility result.

## Decision Point

```text
Eligibility Result
       ↓
   Eligible?
   /       \
 No         Yes
 ↓           ↓
Explain     Continue
result      application
```

---

## If Not Eligible

The system should:

- Clearly explain the result where appropriate.
- Avoid confusing or ambiguous messaging.
- Explain whether another option may be available.
- Provide a clear path forward.

The design should avoid creating the impression that the user has simply reached a dead end.

---

## If Eligible

The system should:

- Confirm the result clearly.
- Explain the next step.
- Allow the user to proceed to the application.

---

# 6. Start Application

## User Goal

Begin the application with confidence.

## Product Should Show

Before the user starts, provide:

- What information will be required.
- What documents may be required.
- Approximate process stages.
- Any important conditions.
- A clear start action.

## UX Opportunity

A short preparation step can reduce uncertainty before the user enters a longer form.

---

# 7. Complete Application

## User Goal

Provide the required information accurately.

## User Actions

The user enters relevant:

- Personal information.
- Employment information.
- Financial information.
- Loan requirements.

## Product Should Provide

- Clear labels.
- Simple instructions.
- Appropriate input validation.
- Progress indication.
- Explanations where needed.
- Ability to correct information.

---

# 8. Document Checklist

## User Goal

Understand exactly what documents are required.

## Product Should Show

A document checklist containing:

- Required document.
- Submission status.
- Upload action.
- Missing document indication.
- Completion state.

Example:

```text
Documents

✓ Identity Proof
✓ Address Proof
○ Income Proof
○ Bank Statement

2 of 4 completed
```

The exact interface will be determined during wireframing.

---

# 9. Upload Documents

## User Goal

Submit the required documents successfully.

## User Actions

The user:

1. Selects a required document.
2. Uploads the document.
3. Waits for confirmation.
4. Reviews the document status.
5. Continues until all required documents are submitted.

## Decision Point

```text
Document uploaded
       ↓
Successfully received?
   /           \
 No             Yes
 ↓               ↓
Retry /          Mark as
replace          complete
                 ↓
        Remaining documents?
            /        \
          Yes         No
           ↓           ↓
        Continue     Review
```

## Product Should Provide

- Upload progress.
- Success confirmation.
- Failure messaging.
- Clear retry option.
- Missing-document indication.

---

# 10. Review Application

## User Goal

Confirm that the application is correct before submission.

## User Actions

The user reviews:

- Personal information.
- Financial information.
- Loan details.
- Documents.
- Important terms and conditions.

## Product Should Provide

- Clear summary.
- Edit actions.
- Document status.
- Important financial information.
- Clear submission action.

---

# 11. Submit Application

## User Goal

Submit the completed application.

## User Action

The user confirms and submits the application.

## Product Response

The system should provide:

- Immediate submission confirmation.
- Application/reference number.
- Current application status.
- Explanation of what happens next.
- Expected next update or timeline where available.

---

# 12. Application Confirmation

This is an important transition point.

The user has completed their part of the process and now enters the waiting stage.

## The Confirmation Should Answer

- Was my application submitted?
- What is my application number?
- What happens next?
- Is any action required from me?
- How can I track the application?

## Key UX Principle

**Do not leave the user wondering what happens after submission.**

---

# 13. Track Application

## User Goal

Understand the current state of the application.

## Proposed Status Model

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

The exact statuses will be validated and refined during later design.

---

## Each Status Should Communicate

- Current stage.
- What has already happened.
- What is happening now.
- Whether the user needs to act.
- What happens next.

---

# 14. Status Update

## User Goal

Receive meaningful information without repeatedly checking or contacting support.

## Product Should Provide

- Status change notification.
- Clear explanation.
- Date/time of update where appropriate.
- Required action, if any.
- Link back to application details.

## Example

```text
Application Update

Your documents have been reviewed.

Current status:
Application Under Review

No action is required from you at this time.

We'll notify you when the status changes.
```

This is an example of the type of communication to explore, not final UI copy.

---

# 15. Additional Information Required

The application may require additional information or documents during review.

## Decision Point

```text
Application Under Review
          ↓
Additional information required?
       /             \
     No               Yes
      ↓                ↓
Continue review    Request information
                       ↓
                 User submits information
                       ↓
                  Continue review
```

## Product Should Provide

- Clear explanation of what is required.
- Reason for the request where appropriate.
- Exact document/information needed.
- Submission method.
- Confirmation after submission.

---

# 16. Decision

The application reaches a final decision.

```text
Decision
   ↓
Approved?
 /      \
Yes      No
 ↓        ↓
Review   Review
offer    outcome
 ↓        ↓
Next     Next
steps    steps
```

---

# 17. Approved Outcome

## User Goal

Understand the approval and what happens next.

## Product Should Provide

- Approval confirmation.
- Approved amount.
- Interest information.
- EMI / repayment information.
- Applicable fees.
- Important terms.
- Clear next action.

The user should not have to search across multiple areas to understand the approved offer.

---

# 18. Not Approved Outcome

## User Goal

Understand the outcome and available next steps.

## Product Should Provide

Where appropriate:

- Clear decision information.
- Understandable explanation.
- Next-step guidance.
- Support access.

The exact level of explanation must respect financial and regulatory constraints and will be treated as a design consideration rather than assumed functionality.

---

# 19. Primary Critical Flow

Based on the research, the most important flow to explore further is:

```text
Check Eligibility
      ↓
Understand Loan
      ↓
Start Application
      ↓
Complete Application
      ↓
Submit Documents
      ↓
Review
      ↓
Submit Application
      ↓
Confirmation
      ↓
Track Application
      ↓
Status Updates
      ↓
Decision
```

This flow directly addresses the strongest research themes:

- Eligibility uncertainty.
- Financial clarity.
- Documentation friction.
- Approval uncertainty.
- Status visibility.
- Communication.

---

# 20. Persona-Specific Flow Priorities

## Clarity-Seeking Applicant

Primary flow emphasis:

```text
Loan Information
      ↓
Eligibility
      ↓
Financial Understanding
      ↓
Application Guidance
      ↓
Document Requirements
```

### Primary UX Goal

Help the user confidently decide whether and how to apply.

---

## Progress-Focused Applicant

Primary flow emphasis:

```text
Application Submission
      ↓
Confirmation
      ↓
Application Tracking
      ↓
Status Updates
      ↓
Decision
```

### Primary UX Goal

Help the user understand what is happening after submission without unnecessary uncertainty.

---

# 21. Key Screens Implied by the Flow

The flow suggests that the product may require screens or states for:

1. Loan selection / overview.
2. Loan details.
3. Eligibility checker.
4. Eligibility result.
5. Application preparation.
6. Application form.
7. Document checklist.
8. Document upload.
9. Application review.
10. Submission confirmation.
11. Application tracker.
12. Status details.
13. Additional information request.
14. Decision.
15. Approved offer / next steps.
16. Not-approved outcome / next steps.

These are **requirements derived from the flow**, not a final screen list.

The actual information architecture will be refined before wireframing.

---

# 22. Error and Edge States

The design should eventually account for situations such as:

- Invalid information.
- Missing required information.
- Failed document upload.
- Unsupported document.
- Missing document.
- Session interruption.
- Additional information required.
- Application status delayed.
- Application not approved.

These states should be considered during wireframing rather than added only after the primary screens are complete.

---

# 23. User Flow Principles

The flow should follow these principles:

### 1. Explain before commitment

Users should understand important information before entering major commitments.

### 2. Make progress visible

Users should know where they are in a multi-step process.

### 3. Confirm important actions

Sensitive or significant actions should provide clear confirmation.

### 4. Reduce repeated effort

Users should not unnecessarily repeat information or document submission.

### 5. Communicate during waiting

Waiting should not become a communication dead end.

### 6. Make the next action obvious

At every important stage, users should understand what they can or should do next.

### 7. Support informed decisions

Financial information should be understandable before the user commits.

---

# 24. Research-to-Flow Traceability

| Research Finding | Flow Response |
|---|---|
| Eligibility difficulty | Eligibility checker before full application |
| EMI calculator requested by 26 participants | Financial information stage |
| Document collection difficulty | Dedicated document checklist |
| Upload progress requested by 22 participants | Document status |
| Long approval process | Application tracking |
| Lack of status updates | Status notifications |
| Estimated timeline requested by 21 participants | Timeline information |
| Poor customer support | Support access |
| Unclear fees | Transparent loan information |
| Difficulty understanding loan terms | Plain-language explanations |

---

# 25. Scope Boundary

This flow represents the **UX experience**, not the actual internal banking workflow.

The project does not attempt to model:

- Internal credit scoring.
- Bank employee workflows.
- Backend processing.
- Regulatory decision systems.
- Internal risk assessment.
- Actual loan approval algorithms.

Where the real-world process is unknown, the design will use clearly defined conceptual states rather than pretending to represent actual banking infrastructure.

---

# 26. Research Limitations

The flow is based on:

- 41 valid survey responses.
- 12 semi-structured interviews.
- Research synthesis.
- Research-informed personas.
- User journey analysis.

It has not yet been validated through usability testing.

Therefore, this flow should be treated as a **research-informed design hypothesis**.

---

# 27. Next Step

The next stage is to translate the user flow into an **Information Architecture and Screen/Content Structure**.

That will determine:

- What information belongs on each screen.
- How screens are grouped.
- What users need to access at each stage.
- Which content is primary or secondary.
- How the application tracker should be structured.

Only after this structure is established should detailed wireframing begin.

---

## Related Documents

- [06 Research Synthesis](../02_Research/06_Research_Synthesis.md)
- [07 Personas](../02_Research/07_Personas.md)
- [01 User Journey](01_User_Journey.md)
- [02 Problem Statement](../00_Project_Documentation/02_Problem_Statement.md)
- [08 Decision Log](../00_Project_Documentation/08_Decision_Log.md)
- [11 Retrospective](../00_Project_Documentation/11_Retrospective.md)

---

## Document History

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-08-14 | Sri Krishna Prabhu Kasinadhuni | Created research-informed primary user flow connecting research findings, personas, journey stages, and proposed product interactions. |
