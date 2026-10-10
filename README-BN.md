# DentalFlow V3 — Payments & Clinic Accounts

V3 হলো V2.1-এর ওপর তৈরি additive update। Existing IndexedDB database name একই আছে এবং schema version 3-এ upgrade করে নতুন `transactions` store যোগ করে। Existing patients ও clinical visits মুছে ফেলার migration নেই।

## নতুন feature
- Collection / Income এবং Clinic Expense entry
- Date, amount, category, optional patient link, payment method ও note
- চলতি মাসের total collection, expense এবং net (collection − expense)
- Recent 50 transaction list; edit/delete
- Patient delete করলে linked transaction-এর financial entry রাখা হয়, শুধু patient link খুলে দেওয়া হয়
- Backup format V3: patients + visits + transactions
- V1/V2 backup restore supported; older backup-এ transactions না থাকলে restore current ledger-ও replace করে (0 transactions)

## Data & safety
- Data এই browser/device-এর IndexedDB-তে থাকে; cloud sync/login নেই।
- Deploy করার আগে JSON backup তৈরি করো। Backup-এ confidential patient/financial information থাকতে পারে—public GitHub repo-তে upload/share করবে না।
- প্রথমে dummy patient দিয়ে transaction add/edit/delete এবং backup/restore পরীক্ষা করো।
- Month summary হলো saved entries-এর simple total; এটি bank reconciliation বা tax/accounting advice নয়।

## Deploy
1. ZIP extract করো।
2. Folder-এর ভেতরের files তোমার existing GitHub Pages repository root-এ upload করে overwrite করো; ZIP ফাইল সরাসরি upload করবে না।
3. GitHub Pages deploy হওয়ার পর app reload করো। পুরোনো cached build থাকলে আরেকবার reload করো।
4. Existing patient/visit data থাকার কথা, তবে deploy-এর আগে backup অবশ্যই রাখো।
