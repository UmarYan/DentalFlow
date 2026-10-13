DentalFlow V8.3.0 — Encounter Workspace Preview

Built from V8.2.0 Encounter Safety Check.

New in this staged preview:
- Adds an Encounter Workspace screen accessible from the hamburger menu.
- Allows starting one explicit encounter for a selected existing patient.
- Shows recent encounters and whether an appointment/clinical visit link exists.
- Offers a deliberate status change to mark an in-progress encounter complete.
- Avoids automatically linking old records or rewriting clinical, plan, bill, payment, appointment, or reminder data.

Important limitations:
- This is a first workspace preview, not the finished unified workflow. Starting an encounter does not yet auto-link subsequent clinical visits, plans, bills, payments or follow-ups.
- Existing forms remain separate.
- Android/browser interactive testing and real clinic-data migration have not been performed.

Before deployment: export a JSON backup and keep it outside the browser. Test using a separate copy/test data first. Do not clear site storage. Upload the ZIP contents to the repository root, preserving filenames.
