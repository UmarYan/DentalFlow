DentalFlow V7.8.17 — Simplified Appointment, Queue & Follow-up

Base: DentalFlow V7.8.16 — Connected Workflow (based on V7.8.13 Workflow Smart Suggestions).

UX updates:
- Appointments and Queue remain one workspace; Queue is a compact subsection, not a separate module.
- Checking in an appointment adds it to the active queue; walk-in patients can be added without a prior booking.
- Queue states remain independent from whether the overall treatment plan is complete.
- Follow-ups and reminders are shown together on one page without separate tabs.
- Reminder is labelled as an optional clinic-task helper (e.g. call/payment/review) so it does not duplicate appointment and follow-up scheduling.
- Appointment dates/times and follow-up dates/times remain the source of truth for those visits; in-app reminders do not send SMS, WhatsApp or push notifications.
- Existing appointment, follow-up, reminder, patient, clinical visit, treatment/service, billing, smart-suggestion and backup data structures are retained.
- Existing records are preserved; this update changes presentation and navigation only.

Validation performed: JavaScript syntax checks, ZIP integrity, HTML structure and duplicate-ID checks. Full Android/browser end-to-end testing has not been performed here. Test using a fictional patient before deployment.
