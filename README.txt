DentalFlow V7.8.7 — Clinical Layout & Follow-up Time

Base: DentalFlow V7.8.6 Workflow Error Recovery.

Changes in this build:
- Patient Workflow now shows Chief complaint → Examination → Treatment done directly under Clinical, in that order.
- History, Diagnosis, Prescription and Advice remain inside the expandable “More clinical details” section.
- Follow-up includes Next visit date plus an optional time picker.
- The optional follow-up time is stored with the visit and associated reminder, included in draft recovery, and shown in reminder details/cards and timeline where supported.
- Existing visit/reminder records are normalized with empty time values when they predate this update; existing data and internal associations are preserved.
- Service-worker cache version updated.

Testing notes:
- JavaScript syntax and ZIP integrity checks should be run before deployment.
- Android end-to-end testing with a fictional patient and backup/restore acceptance testing are still required.
- Export a normal JSON backup before deployment. Do not clear Chrome site data.
