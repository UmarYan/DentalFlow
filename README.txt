DentalFlow V8.10.0 — Follow-up Status

Built from DentalFlow V8.9.0 Treatment Workflow.

Update:
- Adds an explicit Missed status to follow-up reminders.
- Adds a one-tap Missed action to active reminder cards.
- Preserves Pending, Done, and Snoozed behavior.
- Normalization accepts the new status while retaining existing reminder and clinical/financial records.
- Service-worker cache name bumped for update awareness.

Safety notes:
- This ZIP contains app files only; it does not contain patient data.
- Before replacing deployed files, download a DentalFlow JSON data backup and keep the previous source ZIP.
- Do not clear browser/site storage.
- Syntax and archive checks are not a substitute for real-device workflow testing. Verify a test reminder can be marked Missed, edited back to Pending, and that patient records, visits, plans, bills and payments remain present.

Deploy: extract ZIP contents into the existing GitHub Pages repository, commit, wait for Pages to publish, then refresh/reopen the app.
