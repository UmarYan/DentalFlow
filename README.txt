DentalFlow V7.8.16 — Connected Appointment, Queue, Follow-up & Reminder Workflow

Base: DentalFlow V7.8.13 — Workflow Smart Suggestions.

Implemented:
- Appointment scheduling remains linked to the existing Patient record.
- Appointment check-in moves the appointment into Today’s Queue; queue has separate Waiting / In treatment / Completed actions and a dedicated queue view.
- Added a quick Walk-in action that creates a same-day queue entry for a selected patient.
- Follow-ups now have their own collection and UI tab, separate from reminders, with due date/time, reason, note, status and optional clinical-visit link.
- Clinical visits with a next-visit date automatically create a linked follow-up; existing visit next-visit dates are migrated on load without duplicating already-linked follow-ups.
- Follow-up → Schedule appointment carries patient, date, time, reason and note forward automatically. The appointment and follow-up remain linked; completing that appointment completes the linked follow-up.
- Reminders remain a separate feature and now support an optional due time.
- Backup/export/restore and data validation support the follow-up collection while remaining compatible with older backups that do not yet contain it.
- Service-worker cache version updated to avoid retaining the previous app shell.

Important behavior notes:
- Queue status is separate from whether the overall treatment plan is complete.
- Follow-up status is not completed merely because an appointment is created; it is completed when the linked appointment is completed or the user explicitly marks it complete.
- Reminder records are in-app records only. This build does not send SMS, WhatsApp or push notifications automatically; those require a separate delivery integration and permissions.
- Walk-in entries are represented as same-day appointment records with status Waiting so the existing appointment/visit links and data model remain compatible.

Safety & testing:
- Existing patient, clinical, treatment/service, fee, billing, smart-suggestion and localStorage flows were preserved by targeted edits.
- JavaScript syntax checks passed for all embedded scripts; ZIP integrity and HTML structure checks are run before packaging.
- Full Android/browser end-to-end testing has not been performed in this environment. Export a JSON backup and keep the prior ZIP for rollback before deployment. Test first with a fictional patient.
