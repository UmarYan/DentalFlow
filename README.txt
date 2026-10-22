DentalFlow V7.8.67 — Journal Accuracy & Export

Changes (based on V7.8.66):
- Improved the generated double-entry journal to represent patient bills as Accounts Receivable / Dental Service Income and patient payments as Cash/UPI/Bank / Accounts Receivable. This supports a clearer accrual-style view without extra manual entry.
- Excludes cancelled bills and their payments from the generated patient journal.
- Added a monthly Journal CSV export with date, source ID, description, account, debit and credit columns.
- Removed a redundant second call to render the patient receivables panel.
- Preserves existing Finance Budgets & Funds, transaction receipts, supplier payables, reconciliation records, existing billing and other clinic workflows.
- Updated service-worker cache version.

Important limitations:
- This is an operational bookkeeping aid, not certified accounting software or a tax-compliance engine. Review opening balances, historical bills, cancellations, supplier payable records and payments before using reports for formal accounts.
- The journal is generated from current source records; it is not an immutable, locked accounting ledger. Bill edits or cancellations may change the generated view.
- Supplier payables are journalled from payable records and their linked payments; historical supplier-payment records should be checked for consistency.
- Reconciliation records compare a book balance with a stated actual balance but do not post adjustment entries.
- Receipt attachments are stored locally with transaction data and can increase storage use. Make a fresh JSON backup and verify restore before relying on it.

Compatibility & safety:
- No existing patient, clinical, appointment, bill/payment, finance transaction, budget or fund data is intentionally deleted or renamed. Changes are additive and limited to journal presentation/logic and export.
- Do not clear LocalStorage during deployment. Export a fresh JSON backup first.
- Validation: ZIP integrity, required-file presence, HTML parsing, manifest JSON, service-worker syntax and inline JavaScript syntax checked. Automated logic smoke tests performed for patient bill/payment debit-credit balance and cancelled-bill exclusion. Browser end-to-end testing was not performed.
- Rollback: redeploy DentalFlow_V7.8.66_Double_Entry_Finance_Receipts.zip. Do not clear LocalStorage.
