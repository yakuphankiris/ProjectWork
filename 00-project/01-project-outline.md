---
name: Yakuphan Kiris
neptun: JDCZNC
id: 2026_SD_4
github: https://github.com/yakuphankiris/ProjectWork.git
github_project: https://github.com/users/yakuphankiris/projects/1
---
# Receipt-based Shared Expense Allocation Application

Shared supermarket shopping can be difficult to divide fairly when some products are personal and others are shared. This project develops a mobile and web application that extracts an editable item list from receipt photographs, helps users allocate expenses, and tracks debts and repayments within a household group. AI assists receipt extraction, while application logic calculates amounts using verifiable rules.

The first version focuses on housemates sharing supermarket purchases in HUF. Users join a group through an invitation code, review expense allocations, and see their debts and receivables. One-off purchases with manually named participants are also supported for calculating shares and saving a personal receipt record, without requiring participant accounts.

## Objectives
- **Primary objective:** Make shared supermarket expenses easier to record, divide, verify, and track over time.
- **Target users / stakeholders:** Housemates sharing shopping expenses and individuals splitting one-off purchases with friends.
- **Measurable success criteria:** A user can upload and correct a receipt, allocate its total, and save the result. Approved group expenses and confirmed repayments produce the expected balances. Allocation tests preserve the receipt total, including discounts and rounding. OCR and structured AI processing are compared on manually checked receipts using recognition accuracy, correction effort, and entry time.
- **Constraints:** HUF only; readable printed supermarket receipts from Hungary; mobile camera entry and a web expense view; persistent storage; exact monetary calculations; service credentials kept server-side; no secrets or personal or production data in the repository.

## Scope
### In scope
- User accounts, household groups, and invitation codes.
- Receipt capture and editable AI-assisted extraction, with links to receipt-image regions and review of uncertain or missing fields.
- Equal splitting of the receipt total or manual product allocation, supporting equal, percentage-based, and fixed-amount shares. Remaining unassigned products can be shared in one action.
- Discount allocation, rounding, and checks against the receipt total.
- Shared receipt visibility, participant approvals, and correction proposals reviewed by the payer before balance updates.
- Group debts and receivables, recipient-confirmed repayments, refunds, and edit history.
- One-off purchases with manually named participants and saved share summaries, without participant approvals or account-linked debt tracking.
- Potential duplicate warnings, exportable summaries, and manual entry when AI processing is unavailable.

### Out of scope
- Bank integration, in-app money transfers, and tax or accounting compliance.
- Multiple currencies, offline entry, and QR invitations in the first version.
- Restaurant receipts, handwritten documents, and invoices in the initial version.

## Notes
Flutter/Dart is the proposed mobile direction; Flutter Web will be evaluated for the browser view. Backend, database, and AI services will be selected during technical planning. Development starts with manual entry and reliable allocation, followed by AI-assisted receipt processing. Detailed workflows and calculation rules will be documented in the specification. Restaurant support and QR invitations may be added after the core workflow is reliable.
