DentalFlow V7.8.44 — Smart Workflow Finalization

Base: V7.8.42 Finance Layout Unified, carrying forward the V7.8.43 smart-workflow implementation.

Changes in this build:
- Keeps the existing Sky Blue theme, PWA assets, clinical workflow, treatment plans, billing, payments and backup/restore files.
- Adds contextual optional Left and Delay reason fields to the appointment/queue form and stores the selected values on the appointment record.
- Makes Follow-up Purpose optional; patient and due date remain required.
- Keeps Cancellation Reason visible only for Cancelled status and No-show Reason visible only for No-show status.
- Keeps reminder records linked to their originating appointment/follow-up and explicitly does not imply delivery; existing delivery status is preserved and defaults to Not sent.
- Includes Left queue items in the completed/left queue history.
- Updates service-worker cache version to avoid reusing the previous app cache.

Validation performed for this build: ZIP integrity, JavaScript syntax checks for extracted inline script blocks (the main legacy script contains embedded HTML/script text and is not safely testable with a naive script-tag regex), HTML structure spot checks and required-feature string checks. Browser E2E was not performed, so this is an implementation build and not a fully browser-verified stable release. Back up existing clinic data before deployment.
