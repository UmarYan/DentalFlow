DentalFlow V7.10.0 — Billing & Treatment Plans Right-Rail Alignment

Base: DentalFlow_V7.9.59_Card_Readability.zip (the exact ZIP supplied for this update).

Change log:
- Billing cards: status moved to the top-right; action icons remain horizontally aligned directly below it.
- Treatment Plan cards: status moved to the top-right; existing Details, Edit, and applicable Schedule icons remain horizontally aligned directly below it.
- Left-side content remains Patient Name, Date, Service/Treatment Items, and Total/Paid/Due or Estimated Total.
- Billing and Treatment Plans date-wise grouping and search behavior retained.
- Only the two list-card renderers and their scoped styling were changed; underlying data and LocalStorage schema were not changed.
- Updated service-worker cache identifier for V7.10.0.

Validation performed:
- JavaScript syntax check for all 14 inline script blocks (Node.js): passed.
- HTML script/style tag balance: passed.
- ZIP integrity test: passed.
- Browser/UI testing: not performed.

Post-deployment checklist:
1. Open Billing and confirm status is at the far-right top, with horizontal action icons below.
2. Open Treatment Plans and confirm status is at the far-right top, with horizontal action icons below.
3. Check narrow mobile width for wrapping/overlap.
4. Test Payment (when applicable), Details/View, Edit, Receipt, and Schedule actions.
5. Confirm search, date-wise grouping, and existing records remain intact.

Rollback:
Redeploy the original V7.9.59 ZIP. Do not clear browser storage or LocalStorage.
