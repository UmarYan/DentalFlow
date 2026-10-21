DentalFlow V7.8.64 — Clinic Finance Management

What changed:
- Added a dedicated Clinic Finance view under More, with a monthly overview and account balances for Cash, UPI and Bank.
- Added manual Other Income, Expense and inter-account Transfer entries.
- Added Supplier Payables with partial payments, outstanding balance tracking and payment reversal through transaction voiding.
- Patient collection is calculated from existing bill payment records, avoiding duplicate patient-payment entries.
- Added monthly transaction filtering, voided transaction history, CSV export and opening-balance settings.
- Extended backup snapshots and health checks to include the new finance data.

Compatibility and safety:
- Existing patient, clinical, appointment, billing, payment, settings and template data structures remain intact; finance fields are additive.
- Do not clear LocalStorage during deployment.
- Rollback: redeploy the exact previous V7.8.63 ZIP. Older versions ignore the new finance fields; restoring an older backup can remove finance records created after that backup.

DentalFlow V7.8.50 — Vertical Workflow Inline Expansion

Changes in this version (based on the current V7.8.49 build):
- Today's Workflow cards are stacked vertically in this order: Appointments, Queue, Follow-ups, Reminders.
- Tapping a card header expands/collapses its list inline on the Home screen; it no longer navigates away.
- Preserves the existing card title, count, summary, list rendering, search/header controls, and underlying data structures.
- Updated service-worker cache name for the new release.

Deployment: Extract this ZIP and publish the DentalFlow folder contents to the existing GitHub Pages deployment.
Rollback: Redeploy the previous ZIP. Do not clear LocalStorage; this update does not intentionally change stored data.

Validation performed: JavaScript syntax, HTML parsing/IDs, service-worker syntax, ZIP integrity, and required-file checks. Browser end-to-end testing was not performed.


V7.8.59 — App-wide helper-text cleanup: removed static explanatory helper copy across section headings, forms, Settings and More cards. Labels, placeholders, dynamic record details, validation and empty states are retained.


V7.8.60 — Finance New Bill Fix
Fixed openBillForm referencing the removed billPaymentHint helper-text element. The hint is now optional, so New Bill/Edit Bill can open without a null-element exception. No data keys or bill/payment data structures changed.


V7.8.61 — Appointments tab count fix
Added a count badge to the Appointments tab in Appointments & Queue. It displays today's active appointments (excluding Completed and Cancelled), matching the existing Today metric, and updates whenever renderAppointments runs. Queue count behavior is unchanged.
Validation: JavaScript syntax, HTML parsing/IDs, manifest JSON, service-worker syntax, ZIP integrity and required-file checks. Browser end-to-end testing was not performed.


V7.8.63 — Settings template section removal
- Completely removed the “Clinical & Prescription Templates” management card from Settings.
- Kept the existing clinical/prescription template data and chairside template insertion workflow intact; no stored data is deleted or migrated.
- Updated the About version label and service-worker cache name.
Validation: JavaScript syntax, HTML parsing/structure, manifest JSON, service-worker syntax, ZIP integrity and required-file checks. Browser end-to-end testing was not performed.
Rollback: Redeploy DentalFlow_V7.8.62_More_Tiles_Compact_Design.zip. Do not clear LocalStorage.


V7.8.64 — Clinic Finance Management
- Added a Clinic Finance section accessible from More.
- Added manual Other Income, Expense, and inter-account Transfer transactions.
- Added month-based financial summary, Cash/UPI/Bank balances, configurable opening balances, transaction filtering, voiding (retained history), and CSV export.
- Patient collection is derived from existing bill payment records; no duplicate patient-payment ledger is created.
- Added finance transaction/settings fields through backward-compatible normalization; existing patient, clinical, appointment, bill, payment, settings and template data are retained.
- Transfers affect account balances but are excluded from income and expense totals.
- The income-less-expenses tile is an operational summary and is not a tax-ready accounting profit calculation.
Validation performed:
- JavaScript syntax: all 11 inline scripts and service worker passed Node.js syntax checks.
- HTML structure: parsed with Python HTML parser; 336 IDs checked, no duplicate IDs.
- Required project files and manifest JSON: checked.
- Finance logic smoke test: collection derivation, expense save, balance update and void behavior passed.
- Supplier payable smoke test: payable creation, partial payment, expense recording and payment void/reversal passed.
- Legacy data compatibility smoke test: existing patient and bill/payment data preserved while new finance fields initialize safely.
- ZIP integrity: verified after packaging.
- Browser end-to-end testing was not performed because a browser executable was not available in the environment.
Rollback: Redeploy the exact previous V7.8.63 ZIP. Do not clear LocalStorage. New finance fields are additive; the previous version should ignore them, but restoring an older backup can remove finance records created after that backup.

Known limitations for V7.8.64:
- Budget limits, formal reserve/growth-fund allocation tracking, receipt attachments and a full accrual/tax-ready accounting ledger are not included in this incremental release.
- Supplier payable payments are recorded as cash-basis expenses when paid; unpaid payable amounts are tracked separately and are not included in the paid-expense total.
- “Income less expenses” is a simple operating cash summary, not a certified profit/loss or tax report.
