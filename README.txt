DentalFlow V8.2.0 — Encounter Safety Check

Built from the V8.1.0 Encounter Link Safety foundation.

What this staged build contains:
- Keeps the existing single-file app entry point and existing clinical, appointment, plan, billing, payment, reminder, backup and restore screens.
- Extends the built-in Data Check to include encounter IDs, patient references, and explicit links from encounters to appointments, visits, treatment plans, bills and follow-up reminders.
- Does not auto-link historical records or alter clinical/billing/payment records.
- Uses a fresh service-worker cache version.
- Packages only the files needed by the current index.html entry point at repository root; the scripts/ folder from the development workspace is not referenced by index.html and is intentionally not included, making GitHub mobile upload simpler.

Important limitation:
This is an Encounter Safety Check step, NOT yet the completed unified Encounter Workspace. Existing workflow screens remain separate. Android/browser interactive testing and migration with real clinic data have not been performed.

Before deployment:
1. Export a JSON backup from the current app and keep it outside the browser.
2. Do not clear site storage.
3. Upload all files in this ZIP to the repository root, preserving filenames.
4. Test with a backup/test copy before using the app with live clinic records.

Checks performed for this package: JavaScript syntax checks and ZIP integrity.
