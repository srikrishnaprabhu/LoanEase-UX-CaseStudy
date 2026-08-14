# LoanEase UX Case Study

# 04 Screen Requirements & Content Structure

Version: 1.0  
Status: Research-Informed Draft  
Last Updated: 2026-08-14  
Author: Sri Krishna Prabhu Kasinadhuni  

---

## Purpose

This document translates the LoanEase Information Architecture into practical screen requirements.

It defines what each priority screen should accomplish before wireframing begins.

For each screen, this document identifies:

- Screen purpose.
- Primary user goal.
- Required information.
- Primary action.
- Secondary actions.
- Navigation considerations.
- Important states.
- Error or edge conditions.
- Persona relevance.

This document intentionally focuses on **structure and content**, not visual styling.

The final layout, typography, colours, components, and interaction details will be explored during wireframing and UI design.

---

# 1. Screen Prioritisation

Not every item in the Information Architecture needs to become a separate detailed screen.

For the first wireframing pass, the following screens are prioritised:

### Tier 1 — Core Experience

1. Home / Loan Overview
2. Loan Details
3. Eligibility Checker
4. Eligibility Result
5. Application Preparation
6. Application Form
7. Document Checklist / Upload
8. Application Review
9. Submission Confirmation
10. Application Status / Tracker
11. Application Updates / Required Actions
12. Decision / Outcome

### Tier 2 — Supporting Experience

13. Notifications
14. Support / Help

The Tier 1 screens form the main portfolio story because they directly address the research-supported problems.

---

# 2. Screen Requirement Format

Each screen is described using the following structure:

| Requirement | Meaning |
|---|---|
| Purpose | Why the screen exists |
| Primary User Goal | What the user is trying to accomplish |
| Required Information | Information needed to complete the task |
| Primary Action | Most important action |
| Secondary Actions | Other useful actions |
| Important States | Different conditions the screen must support |
| Error / Edge Cases | Problems the user may encounter |
| Persona Relevance | Which research-informed need it addresses |

---

# 3. Screen 01 — Home / Loan Overview

## Purpose

Provide a clear starting point for users who are exploring LoanEase.

## Primary User Goal

Understand what LoanEase offers and identify the appropriate next action.

## Required Information

- Loan options.
- High-level loan descriptions.
- Key eligibility information.
- Access to loan details.
- Eligibility access.
- Existing application status, when applicable.

## Primary Action

**Explore Loan**

## Secondary Actions

- Check Eligibility.
- View Existing Application.
- View Notifications.
- Get Help.

## Important States

### New User

Show loan exploration and eligibility options.

### Existing Applicant

Show relevant application status or shortcut to the active application.

## Error / Edge Cases

- No loan products available.
- User is not signed in when application information is requested.
- Temporary loading or service failure.

## Persona Relevance

### Clarity-Seeking Applicant

Needs a clear starting point and understandable information.

### Progress-Focused Applicant

Needs quick access to an existing application.

---

# 4. Screen 02 — Loan Details

## Purpose

Help users understand a selected loan before deciding whether to apply.

## Primary User Goal

Understand the financial and practical implications of the loan.

## Required Information

- Loan type.
- Loan amount or range.
- Interest information.
- Estimated EMI.
- Repayment information.
- Fees and charges.
- Key eligibility requirements.
- Important terms.
- Relevant explanations.

## Primary Action

**Check Eligibility**

## Secondary Actions

- Calculate EMI.
- Start Application.
- Review Eligibility Information.

## Important States

### Default

Show loan information.

### Different Loan Amount

Update relevant repayment/EMI information.

### Information Expanded

Show explanations for unfamiliar terms.

## Error / Edge Cases

- Calculator input is invalid.
- Loan amount is outside supported range.
- Financial information cannot be loaded.

## Persona Relevance

Strongly supports the Clarity-Seeking Applicant.

---

# 5. Screen 03 — Eligibility Checker

## Purpose

Allow users to determine whether they are likely to qualify before completing the full application.

## Primary User Goal

Find out whether continuing with the application is appropriate.

## Required Information

Only information required for the eligibility assessment should be requested at this stage.

Potential categories may include:

- Basic personal information.
- Employment information.
- Income information.
- Relevant eligibility inputs.

The exact eligibility fields are intentionally not fixed here because the project does not define an actual banking eligibility algorithm.

## Primary Action

**Check Eligibility**

## Secondary Actions

- Learn About Eligibility.
- Go Back.

## Important States

### Empty / Initial State

User has not entered required information.

### In Progress

User is completing the eligibility inputs.

### Processing

System is evaluating the submitted information.

### Eligible

User can continue.

### Not Eligible

User receives an appropriate result and next-step guidance.

## Error / Edge Cases

- Missing required input.
- Invalid input.
- Temporary processing failure.
- Unable to determine result.

## Persona Relevance

Strongly supports the Clarity-Seeking Applicant.

---

# 6. Screen 04 — Eligibility Result

## Purpose

Clearly communicate the result of the eligibility check.

## Primary User Goal

Understand the result and decide what to do next.

## Required Information

- Eligibility result.
- Relevant explanation.
- Important limitations or conditions.
- Next-step guidance.

## Primary Action

### If Eligible

**Continue Application**

### If Not Eligible

**Review Result / Explore Alternatives**

## Secondary Actions

- Review Loan Details.
- Contact Support.

## Important States

### Eligible

The user can continue toward the application.

### Not Eligible

The user receives clear information without being left at a dead end.

## Error / Edge Cases

The design should avoid presenting the eligibility result as a guaranteed final loan approval if it is only a preliminary assessment.

## Persona Relevance

Supports the need for clarity before commitment.

---

# 7. Screen 05 — Application Preparation

## Purpose

Prepare the user for the application before they begin.

## Primary User Goal

Understand what will be required and what the process involves.

## Required Information

- Application stages.
- Information required.
- Document requirements.
- Approximate process expectations.
- Important conditions.
- What happens after submission.

## Primary Action

**Start Application**

## Secondary Actions

- Review Loan Details.
- Review Eligibility.
- Exit / Return.

## Important States

### Ready to Start

All relevant preparation information is visible.

### Incomplete Preparation

If information is missing, explain what is required.

## Persona Relevance

Supports both personas by reducing uncertainty before commitment.

---

# 8. Screen 06 — Application Form

## Purpose

Collect the information required to complete the loan application.

## Primary User Goal

Provide accurate information with minimal confusion.

## Required Information

The form may be divided into logical groups:

```text
Application
│
├── Personal Information
├── Employment Information
├── Financial Information
└── Loan Requirements
```

The exact fields should be defined only when product requirements are established.

## Primary Action

**Continue**

## Secondary Actions

- Back.
- Save / Continue Later, if supported.

## Important States

### Empty

User has not entered information.

### In Progress

User is completing the form.

### Validation Error

Incorrect or missing information is identified.

### Saved

Progress is preserved if the feature is supported.

## Error / Edge Cases

- Required field missing.
- Invalid input.
- Incorrect format.
- Session interruption.
- Unsaved changes.

## UX Requirements

- Clear field labels.
- Helpful instructions.
- Inline validation.
- Visible progress.
- Logical grouping.
- Ability to correct information.

## Persona Relevance

Supports the need for guidance and reduced uncertainty during application completion.

---

# 9. Screen 07 — Document Checklist / Upload

## Purpose

Help users understand, submit, and track required documents.

## Primary User Goal

Know what is required and confirm that documents have been received.

## Required Information

For each document:

- Document name.
- Required / optional status.
- Upload status.
- Upload action.
- Review status where applicable.
- Additional action required, if any.

## Primary Action

**Upload Document**

## Secondary Actions

- Replace Document.
- View Document Status.
- Continue.

## Important States

### Required

Document has not yet been submitted.

### Uploading

Document is being processed.

### Submitted

Document was successfully received.

### Under Review

Document is being reviewed.

### Failed

Upload failed and requires retry.

### Additional Information Required

The user must provide another document or action.

### All Documents Complete

User can continue to application review.

## Example Structure

```text
Documents

✓ Identity Proof
  Submitted

✓ Address Proof
  Submitted

● Income Proof
  Upload Required

○ Bank Statement
  Upload Required

2 of 4 completed

[ Continue ]
```

## Error / Edge Cases

- Unsupported file.
- File too large.
- Upload failure.
- Duplicate document.
- Document rejected.
- Missing document.

## Persona Relevance

Directly addresses documentation friction and upload-status concerns identified in research.

---

# 10. Screen 08 — Application Review

## Purpose

Allow the user to verify their information before final submission.

## Primary User Goal

Confirm that the application is correct.

## Required Information

```text
Application Review
│
├── Personal Information
├── Employment Information
├── Financial Information
├── Loan Details
├── Documents
└── Important Terms
```

## Primary Action

**Submit Application**

## Secondary Actions

- Edit Personal Information.
- Edit Financial Information.
- Edit Loan Details.
- Review Documents.
- Go Back.

## Important States

### Ready for Submission

All required information is complete.

### Missing Information

User is shown what must be completed.

### Correction Required

User can return to the relevant section.

## Error / Edge Cases

- Required information missing.
- Document missing.
- Session expired.
- Submission conditions not met.

## Persona Relevance

Supports confidence and error prevention before commitment.

---

# 11. Screen 09 — Submission Confirmation

## Purpose

Confirm successful application submission and transition the user into the tracking experience.

## Primary User Goal

Know that the application was successfully submitted and understand what happens next.

## Required Information

- Confirmation message.
- Application/reference number.
- Current status.
- Next expected step.
- Timeline information where available.
- Tracking access.

## Primary Action

**Track Application**

## Secondary Actions

- View Application Details.
- Return Home.
- Contact Support.

## Important States

### Successful Submission

Application has been accepted into the next stage.

### Submission Failed

The user is clearly informed and given a safe next action.

## Key UX Principle

**Submission should never end with uncertainty about whether the application was received.**

## Persona Relevance

Strongly supports the Progress-Focused Applicant.

---

# 12. Screen 10 — Application Status / Tracker

## Purpose

Give users meaningful visibility into the application after submission.

## Primary User Goal

Understand where the application currently stands.

## Required Information

- Application number.
- Current status.
- Progress stages.
- Last update.
- Expected next step.
- Estimated timeline where available.
- Required action, if any.

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

The exact statuses remain a design hypothesis.

## Primary Action

**View Current Status**

## Secondary Actions

- View Documents.
- View Updates.
- View Required Actions.
- Contact Support.

## Important States

### Submitted

Application has been received.

### Documents Under Review

Submitted documents are being reviewed.

### Application Under Review

Application is being assessed.

### Additional Information Required

User must provide information or documents.

### Decision Pending

Review is nearing completion.

### Decision Available

Outcome is ready.

## Error / Edge Cases

- Status temporarily unavailable.
- Processing delay.
- User cannot access application.
- Additional action required.

## Persona Relevance

This is the highest-priority screen for the Progress-Focused Applicant.

---

# 13. Screen 11 — Application Updates / Required Actions

## Purpose

Provide communication and clearly separate information from tasks requiring user action.

## Primary User Goal

Understand what changed and whether anything needs to be done.

## Required Information

For each update:

- What changed.
- Date/time.
- Current status.
- Whether action is required.
- Relevant next step.

## Primary Action

**Complete Required Action**, when applicable.

## Secondary Actions

- View Application.
- View Documents.
- Contact Support.

## Important States

### Informational Update

No user action required.

### Action Required

The user must complete a task.

### Multiple Actions

Several outstanding actions are clearly prioritised.

## Example

```text
Application Update

Additional income documentation is required.

Action required:
Upload your latest income proof.

[ Upload Document ]
```

This is example content, not final UI copy.

## Persona Relevance

Directly addresses communication gaps and uncertainty after submission.

---

# 14. Screen 12 — Decision / Outcome

## Purpose

Clearly communicate the final application outcome.

## Primary User Goal

Understand the decision and what happens next.

## Required Information

The exact content depends on the outcome.

### Approved

Potential information:

- Approval confirmation.
- Approved amount.
- Interest information.
- EMI / repayment information.
- Fees.
- Important terms.
- Next steps.

### Not Approved

Potential information:

- Decision information.
- Appropriate explanation.
- Next-step guidance.
- Support access.

## Primary Action

### Approved

**Review Offer / Next Steps**

### Not Approved

**Review Next Steps**

## Important States

### Approved

User can understand and act on the approved outcome.

### Not Approved

User receives understandable information and a clear path forward where appropriate.

## Error / Edge Cases

The design should not invent reasons or explanations that the underlying system cannot legitimately provide.

## Persona Relevance

Supports both personas by making the final outcome understandable.

---

# 15. Screen 13 — Notifications

## Purpose

Provide a central place for important application-related notifications.

## Primary User Goal

Find recent updates without repeatedly checking the application.

## Required Information

- Notification type.
- Short summary.
- Date/time.
- Read/unread state.
- Link to relevant application context.

## Primary Action

**Open Notification**

## Secondary Actions

- Mark as Read.
- View Application.

## Important States

### Unread

Important new information.

### Read

Previously viewed notification.

### No Notifications

Clearly communicate that there are no new updates.

## Persona Relevance

Particularly relevant to the Progress-Focused Applicant.

---

# 16. Screen 14 — Support / Help

## Purpose

Provide assistance when users need clarification or cannot resolve a problem independently.

## Primary User Goal

Find an answer or contact appropriate support.

## Required Information

- FAQs.
- Help topics.
- Application-related help.
- Document-related help.
- Contact support option.

## Primary Action

**Get Help**

## Secondary Actions

- Search FAQs.
- View Application Help.
- View Document Help.

## Important States

### Search Results

Relevant help content is displayed.

### No Results

Offer alternative help or contact support.

### Contact Support

Provide the appropriate support route.

## Persona Relevance

Supports users who need reassurance or assistance during uncertainty.

---

# 17. Cross-Screen Requirements

Several requirements should remain consistent throughout the experience.

## 17.1 Progress Visibility

Multi-step processes should communicate:

- Current stage.
- Completed stages.
- Remaining stages.

## 17.2 Clear Primary Action

Each screen should have one visually dominant primary action.

## 17.3 Consistent Status Language

The same status should not be described using different terms across screens.

## 17.4 Clear Feedback

Important actions should produce visible confirmation.

## 17.5 Error Prevention

The experience should prevent avoidable errors before submission.

## 17.6 Recoverability

Where practical, users should be able to correct information rather than restarting the process.

---

# 18. Content Hierarchy

Each screen should generally follow:

```text
Screen Purpose
      ↓
Current State / Important Information
      ↓
Primary Task
      ↓
Supporting Information
      ↓
Secondary Actions
      ↓
Help / Additional Information
```

This hierarchy should prevent supporting content from overwhelming the user's primary task.

---

# 19. Critical States to Wireframe

The first wireframe pass should not only cover successful/default screens.

The following states should also be represented:

### Eligibility

- Initial.
- Processing.
- Eligible.
- Not eligible.

### Application

- Empty.
- In progress.
- Validation error.
- Complete.

### Documents

- Required.
- Uploading.
- Submitted.
- Failed.
- Under review.
- Additional information required.
- Complete.

### Submission

- Ready.
- Success.
- Failure.

### Application Tracking

- Submitted.
- Under review.
- Additional information required.
- Decision pending.
- Decision available.

### Decision

- Approved.
- Not approved.

These states will help prevent the wireframes from representing only an ideal happy path.

---

# 20. Mobile Considerations

The LoanEase experience should be designed with mobile use in mind.

This is especially important for:

- Application forms.
- Document uploads.
- Application tracking.
- Notifications.
- Status updates.

The wireframes should therefore consider:

- Small-screen readability.
- Touch-friendly controls.
- Clear scrolling structure.
- Simple form grouping.
- Easy document upload.
- Persistent access to important status information.

The final device-specific layout will be established during wireframing.

---

# 21. Research-to-Screen Traceability

| Research Finding | Screen Response |
|---|---|
| Eligibility difficulty | Eligibility Checker and Result |
| Difficulty understanding loan terms | Loan Details / Financial Information |
| EMI calculator requested by 26 participants | Loan Details / Financial Information |
| Eligibility checker requested by 25 participants | Eligibility Checker |
| Document collection difficulty | Document Checklist / Upload |
| Upload progress requested by 22 participants | Document status |
| Long approval process | Application Status / Tracker |
| Lack of application status updates | Application Status / Updates |
| Estimated approval timeline requested by 21 participants | Application Status / Progress |
| Customer support concerns | Support / Help |
| Need for clearer communication | Updates / Notifications |
| Uncertainty after submission | Submission Confirmation + Application Tracker |

---

# 22. Priority Wireframe Set

To keep the design process focused, the first wireframe set should concentrate on the core experience:

```text
1. Loan Details
       ↓
2. Eligibility Checker
       ↓
3. Eligibility Result
       ↓
4. Application Preparation
       ↓
5. Application Form
       ↓
6. Document Checklist / Upload
       ↓
7. Application Review
       ↓
8. Submission Confirmation
       ↓
9. Application Status / Tracker
       ↓
10. Required Action / Update
       ↓
11. Decision / Outcome
```

The Home, Notifications, and Support screens can then be added as supporting screens.

---

# 23. Portfolio Storyline

The screen requirements should support a clear portfolio narrative:

```text
Research Finding
      ↓
User Need
      ↓
Journey Problem
      ↓
User Flow
      ↓
Information Architecture
      ↓
Screen Requirement
      ↓
Wireframe
      ↓
Prototype
      ↓
Usability Testing
      ↓
Design Iteration
```

This traceability is important because the final portfolio should demonstrate **why the screens were designed**, not only what they look like.

---

# 24. Scope Boundary

This document defines UX screen requirements.

It does not define:

- Final visual design.
- Exact typography.
- Colour palette.
- Final component library.
- Backend logic.
- Actual banking eligibility calculations.
- Actual approval algorithms.
- Production API behaviour.

Those concerns belong to later design or technical stages.

---

# 25. Validation Plan

The screen requirements will be validated through:

1. Wireframe review.
2. Prototype testing.
3. Usability testing.
4. Observation of task completion.
5. Identification of navigation or comprehension problems.
6. Iteration based on findings.

The most important tasks to validate will be:

- Finding loan information.
- Checking eligibility.
- Understanding the application requirements.
- Uploading documents.
- Reviewing the application.
- Understanding submission confirmation.
- Finding application status.
- Understanding required actions.
- Understanding the final decision.

---

# 26. Next Step

The next stage is **Wireframing**.

At that stage, the requirements in this document will be translated into low-fidelity screen layouts.

The first wireframes should focus on the Priority Wireframe Set rather than attempting to design every possible screen immediately.

The wireframes will then be reviewed against:

- Research findings.
- Personas.
- User journey.
- User flow.
- Information Architecture.
- Screen requirements.

Only after the low-fidelity structure is validated should the project move into detailed Figma UI design.

---

## Related Documents

- [06 Research Synthesis](../02_Research/06_Research_Synthesis.md)
- [07 Personas](../02_Research/07_Personas.md)
- [01 User Journey](01_User_Journey.md)
- [02 User Flow](02_User_Flow.md)
- [03 Information Architecture](03_Information_Architecture.md)
- [02 Problem Statement](../00_Project_Documentation/02_Problem_Statement.md)
- [08 Decision Log](../00_Project_Documentation/08_Decision_Log.md)
- [10 Design Journal](../00_Project_Documentation/10_Design_Journal.md)
- [11 Retrospective](../00_Project_Documentation/11_Retrospective.md)

---

## Document History

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 2026-08-14 | Sri Krishna Prabhu Kasinadhuni | Created research-informed screen requirements and content structure as the bridge between Information Architecture and wireframing. |
