DentalFlow V7.8.40 — Treatment Plan Workflow

Changes:
- Adds a visible Save visit + plan remaining treatment action. It saves the clinical visit, then opens a treatment plan prefilled with the visit examination/diagnosis context and links the plan to the visit.
- Shows every treatment-plan item in the patient profile, with per-item status and scheduling actions.
- Supports Scheduled as a treatment-item status. Scheduling an appointment marks the linked plan item Scheduled.
- Starting a clinical visit from a linked appointment retains the plan/item link. Saving the visit marks the item Completed only when Treatment Done is documented; otherwise it becomes In progress.
- Preserves existing patient/visit/plan/appointment records and adds no bulk migration.

Validation performed: ZIP integrity, HTML parsing, and JavaScript syntax checks. Real Android end-to-end testing is not claimed. Back up the app's data before deployment.
