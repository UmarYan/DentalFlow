DentalFlow V7.8.43 — Shared Context Isolation & Record Guard

Based on V7.8.42 Shared Form Routing & Context Fix.

Changes:
- Validates that an edit record exists before opening the shared form.
- Derives patient context from the existing record when possible.
- Rejects mismatched patient/record contexts instead of opening an edit form against the wrong patient.
- Requires a valid bill for Payment form routing and checks patient/bill consistency.
- Clears stale form context dataset values before applying the current form context.
- Keeps existing forms, save handlers, record IDs, and financial calculations intact; no migration is performed.

Limitations:
- This is a defensive shared-routing step, not complete field-level unification of Patient Workflow and all six standalone forms.
- Static syntax/package checks do not replace browser end-to-end testing. Do not deploy over the current clinic version without a verified backup and separate test run.


V7.8.44 Shared Entry Adapters: existing public New/Edit form entry points route through the shared context controller; native form and save implementations are retained.


DentalFlow V7.8.45 — Shared Form Integration Guardrails
Based on V7.8.44.

Changes in this build:
- Shared form entry points retain one canonical existing form and save pathway per record type across FAB, patient profile, contextual details, and section entry points.
- Record lookup compares IDs as strings to avoid numeric/string identifier mismatches.
- Missing edit records fail closed instead of opening a new record form.
- Payment edit requires a valid bill and a payment that belongs to that bill.
- Patient/bill context mismatch is rejected before opening the form.
- No data migration; existing clinical and finance calculations are retained.

Verification performed: ZIP/package integrity, HTML parse, JavaScript syntax checks. Browser end-to-end testing was not completed in this build environment. Keep this as a separate test build; back up real clinic data before any deployment.
