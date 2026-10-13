DentalFlow V8.5.0 - Encounter Record Linking

Built on the V8.4.0 Encounter Workflow Launcher. Clinical Visit, Treatment Plan and Bill records created from an explicitly chosen in-progress Encounter now receive a safe encounter link. The Encounter stores the linked visit ID and de-duplicated plan/bill IDs. Opening forms elsewhere does not implicitly attach records to an encounter.

Safety boundaries: existing history is not batch-migrated or rewritten; treatment plan item statuses are not changed; bill line items, totals, payment transactions and due calculations are not changed by linking; follow-up dates do not create appointments. Linking is additive metadata only.

Before deployment: export a JSON backup and keep it outside the browser. Upload the ZIP contents to the repository root, preserving file names and relative paths. Do not clear browser/site storage.

Checks: JavaScript syntax checks, ZIP integrity, and focused static assertions passed. Android interactive testing and testing against real patient data have not been performed.
