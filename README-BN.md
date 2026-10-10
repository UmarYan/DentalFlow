# DentalFlow V2.1 — Add Visit dialog fix

V2.1 হলো V2-এর bug-fix release; V1-এর local-first foundation অপরিবর্তিত। এটি phone-first single-device app; patient ও visit data IndexedDB-তে থাকে।

## V2-এর features (অপরিবর্তিত)
- Patient profile থেকে Clinical Visit যোগ করা
- Visit date, chief complaint, history, examination, diagnosis, treatment done, advice, prescription notes, next visit ও follow-up status
- Patient-এর visit history একই profile-এ দেখা
- Visit edit ও delete
- Patient delete করলে তার linked clinical visits-ও delete হবে—confirmation দেওয়া হয়
- Backup V2-তে patients ও visits দুটোই থাকে; V1 backup-ও restore করা যায়
- IndexedDB schema version 2: existing V1 patient records preserve করার জন্য upgrade path

## V2.1-এর fix
- `Add visit` চাপলে patient details dialog আগে বন্ধ হয়, তারপর clinical visit form খোলে—mobile browser-এ nested modal dialog-এর সমস্যা এড়াতে।
- Visit save/cancel/close করলে patient details ও visit history আবার দেখা যায়।
- Service-worker cache version `dentalflow-v2.1-shell-1` করা হয়েছে, যাতে পুরোনো cached JavaScript আটকে না থাকে।
- Database name/schema অপরিবর্তিত; existing local patient ও visit data মুছে ফেলার কোনো migration নেই।

## এখনো নেই
Dental chart, tooth-wise status, treatment planning, payments/accounts, reports, appointment calendar, cloud sync/login—এগুলো এই build-এ নেই। এগুলো পরের ধাপে আলাদা করে যোগ করা হবে।

## Deploy
1. ZIP extract করো।
2. GitHub repository `dentalflow-clinic`-এর root-এ ZIP-এর ভেতরের files upload করো; পুরনো files overwrite করো।
3. GitHub → Settings → Pages → Deploy from a branch → `main` / `/(root)`।
4. Pages site reload করো। পুরনো cached version দেখা গেলে browser-এ refresh করো; service-worker cache version বদলানো হয়েছে; update load হতে একবার reload লাগতে পারে।

## Backup/privacy
- Patient ও visit data local IndexedDB-তে থাকে, public source files-এ নয়।
- Backup file-এ confidential data থাকতে পারে—public repo বা public link-এ কখনো upload/share করবে না।
- Restore current patient and visit data replace করে। Restore-এর আগে confirmation আসে।
- Browser storage clear/device loss হলে data হারাতে পারে। Regular JSON backup রাখো।
- No login, cloud sync or encryption-at-rest. Use device lock and private backup storage.

## Test checklist
- [ ] Existing V1 patient data remains after updating to V2
- [ ] Add/edit/search patient
- [ ] Open patient → Add visit; visit form opens
- [ ] Cancel/close visit form; patient details returns
- [ ] Open patient → Add visit → save
- [ ] Visit history appears under correct patient
- [ ] Edit and delete a visit
- [ ] Delete a test patient and confirm linked visits are removed
- [ ] Export backup and check it includes `patients` and `visits`
- [ ] Restore a test backup; verify it replaces current records
- [ ] Reload and verify records persist
- [ ] Test mobile layout and offline app shell

Real patient data ব্যবহার করার আগে test records দিয়ে সব workflow যাচাই করো।
