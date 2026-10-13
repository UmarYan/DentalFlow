DentalFlow V8.7.0 — Encounter Link Check

Based on DentalFlow V8.6.0 Encounter Record Summary. Adds a read-only Encounter Link Check panel to review missing encounter-linked visits/plans/bills, patient-reference mismatches, and possible same-patient records that may need manual review.

Safety boundaries: the check never creates, deletes, or relinks records; never changes treatment status, appointments, follow-up dates, bills, payments, or dues. Same-patient matches are suggestions only because date similarity does not prove that records belong to the same encounter. Existing data schema and local-storage key are preserved.

Deployment: export a JSON backup and keep it outside the browser before replacing files. Upload all ZIP contents to the repository root, preserving file paths. Do not clear browser/site storage.

Checks performed: source/output ZIP integrity, expected UI/function/cache-version patch, and JavaScript syntax check for inline scripts. These are code-level checks only; interactive Android testing and validation with real patient data have not been performed. Treat as a test build until verified.
