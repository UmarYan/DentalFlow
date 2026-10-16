DentalFlow V7.8.19 — Chairside Workflow Revamp

Base: DentalFlow V7.8.18 — Reminder Modal & Icon Actions.

Chairside UX updates:
- Appointments / Queue and Follow-up / Reminders now use paired tabs within the same workspace.
- Tap a tab or swipe horizontally to switch within that pair; vertical scrolling remains available.
- Tabs remain sticky while the workspace scrolls.
- Active appointments and follow-ups/reminders are grouped by date (Overdue, Today, Tomorrow, then later dates) and sorted by time within each group.
- Completed appointments, queue visits, follow-ups and reminders are separated from active lists in expandable Completed sections.
- Queue is limited to today's checked-in active patients; completed queue visits are shown separately. Walk-ins remain supported.
- Key chairside actions use compact icon buttons with accessible labels and tooltips.
- Appointment completion does not automatically mark a linked follow-up complete; these statuses remain independent.
- Existing patient, clinical visit, treatment/service, billing, smart suggestion, backup and record data structures are retained.

Reminder notes:
- In-app reminders do not send SMS, WhatsApp or push notifications.
- This release focuses on presentation/navigation and chairside list handling; validate on a test dataset before deployment.

Validation performed for this package: JavaScript syntax check and ZIP integrity check. Full Android/browser end-to-end interaction testing has not been performed here.
