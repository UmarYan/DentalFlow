DentalFlow V8.6.0 — Encounter Record Summary

Based on the supplied V8.5.0 Encounter Record Linking ZIP. This version adds a read-only summary of linked clinical visits, treatment plans and bills inside each Encounter card. It displays existing visit diagnosis/reason, plan title/status, bill title, and a recorded follow-up date where available. Missing linked records are flagged rather than silently removed.

Safety boundaries: this is a display-only change. It does not create, delete, migrate or relink records; does not change plan status; does not calculate or rewrite bill totals, payments or due; and does not turn follow-up dates into appointments. Existing patient history is not batch-modified.

Deployment: export a JSON backup and keep it outside the browser before replacing files. Upload all ZIP contents to the repository root, preserving relative paths. Do not clear browser/site storage.

Checks performed: source ZIP integrity, output ZIP integrity, expected patch presence, and JavaScript syntax checks for inline scripts. Interactive Android testing and validation with real patient data have not been performed. Treat as a test build until verified.
