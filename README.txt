DentalFlow V8.4.0 — Encounter Workflow Launcher

This build adds patient-context quick actions from an in-progress Encounter to the existing Clinical Visit, Treatment Plan, and Bill forms. The patient is preselected to reduce repeated entry.

Important limitations: records are NOT automatically linked to the Encounter in this version. No legacy records are automatically migrated or rewritten. Bills and payment transactions continue to use the existing billing workflow.

Before deployment: export a JSON backup and keep it outside the browser. Upload the contents of this ZIP to the repository root, preserving file names and relative paths. Do not clear browser storage.

Checks performed: JavaScript syntax check, ZIP integrity check. Android interactive testing and testing against real patient data have not been performed.
