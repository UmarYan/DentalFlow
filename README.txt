DentalFlow V7.7.8 — Unified Patient View

Based on DentalFlow V7.7.5 Sky Blue Menu Header Update.

Focused update:
- Patient list now opens the full patient profile directly; no mandatory context-card step.
- Added a compact overview with recent visit, next appointment, due balance, next follow-up, active plans, visit count and medical alert when present.
- Added quick actions for New Visit, Appointment, Treatment/Visit History and Payment/Bill.
- Existing profile sections and their data links are retained: demographics, tooth status, treatment plans, billing, timeline, clinical visit history, editing and patient deletion.
- Updated service-worker cache version so the new interface can be picked up after deployment.

Deployment note: replace the existing app files with the contents of this ZIP in the same GitHub Pages repository. Do not delete the browser/local app data. Before updating a live clinic app, export a Safety Snapshot / JSON backup. This source ZIP contains app files only, not patient data.


V7.7.8 Unified Patient View layout update: patient details moved above overview; patient sections ordered Current Tooth Status, Treatment Plans, Visit History, Billing & Payments, Timeline. Existing patient data schema is unchanged.

V7.7.8: Patient profile cleaned; section order is Current Tooth Status, Treatment Plans, Billing & Payments, Visit History, Timeline. Create actions are on the profile FAB.
