DentalFlow V8.0 — Encounter Workflow Foundation

Base: DentalFlow V7.8.0 (the build identified by the user as V7.8.0; source ZIP originally named V7.7.11).

Scope of this staged V8.0 step:
- Adds an encounters collection to the app data model without deleting or rewriting existing visit, plan, appointment, bill, reminder, or payment records.
- Normalizes encounter IDs, patient links, optional appointment links, status, and references to related records.
- Changes startup handling so malformed saved JSON / unexpected data roots are not silently replaced by empty data. The app shows its existing load-error screen with a more explicit data-preservation warning.
- Changes the service-worker cache name to prevent reuse of the prior version's cache.
- Keeps the existing app screens and current feature behavior in place for this foundation stage; the unified Encounter Workspace is NOT yet implemented.

Data safety:
- Before deploying any app update, export a DentalFlow JSON backup and keep a copy outside the browser.
- Do not clear browser/site storage during deployment.
- This ZIP contains app files only, not patient records.
- If saved data cannot be parsed, do not clear app storage or repeatedly save new data over it. Restore only from a known-good backup after checking the issue.

Validation performed:
- ZIP integrity check.
- All three inline JavaScript blocks passed Node syntax checks.
- Data-model smoke test: legacy-shaped data normalizes with an empty encounters array; malformed saved JSON throws rather than writing an empty dataset over it.
- Interactive Android/browser workflow, real clinic data migration, and payment/visit UI regression testing were NOT run in this environment. Treat this as a foundation build for further testing, not as a fully validated final V8.0 release.
