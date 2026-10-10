# DentalFlow V1 — Minimal Foundation

এটি DentalFlow-এর আলাদা, stable foundation build। এটি mobile-first এবং patient data browser-এর local IndexedDB-তে রাখে।

## V1-এ যা আছে
- Overview: মোট patient ও আজ যোগ করা patient count
- Patient add, search, details, edit ও delete
- Fields: name, phone, age, gender, general notes
- JSON backup download ও backup restore
- PWA manifest ও service-worker shell cache
- Responsive mobile layout
- Patient data source files বা GitHub repository-তে রাখা হয় না

## V1-এ যা ইচ্ছাকৃতভাবে নেই
Clinical visit, dental chart, diagnosis, treatment planning, prescription, appointments, billing, expenses, reports, login বা cloud sync—এগুলো এখন যোগ করা হয়নি। প্রথমে foundation স্থিতিশীল রাখা হচ্ছে।

## GitHub Pages-এ deploy
1. GitHub-এ নতুন repository তৈরি করো: `dentalflow-clinic`।
2. GitHub Free ব্যবহার করলে Pages-এর জন্য repository Public রাখো।
3. ZIP extract করে ভেতরের সব file repository root-এ upload করো। শুধু ZIP file upload করলে app চলবে না।
4. Repository → **Settings** → **Pages** → **Deploy from a branch** বেছে নাও।
5. Branch `main`, folder `/(root)` বেছে **Save** করো।
6. Pages URL খোলো। প্রথমবার online থাকাকালীন load করো, তারপর offline test করো।

## Privacy ও backup
- Patient records এই device/browser-এর local IndexedDB-তে থাকে।
- Browser storage clear বা device loss হলে records হারাতে পারে। নিয়মিত JSON backup রাখো।
- Backup file-এ confidential patient information থাকতে পারে। এটি public repository বা public link-এ upload/share করবে না।
- Restore করলে বর্তমান records replace হবে; confirmation দেখানো হয়।
- এটি local-first V1; login, cloud sync বা encryption-at-rest নেই। Device lock এবং private backup storage ব্যবহার করো।

## Phone থেকে deploy
ZIP extract করতে ফোনের file manager/ZIP app ব্যবহার করো। GitHub repository root-এ সব file upload করো এবং নিশ্চিত করো `index.html` root-এ আছে।

## Smoke test
- [ ] App opens without a blank screen
- [ ] Add and save a test patient
- [ ] Search by name and phone
- [ ] Open details, edit, delete a test patient
- [ ] Export JSON backup
- [ ] Restore a test backup (this replaces current records)
- [ ] Reload and confirm records remain
- [ ] Check offline shell after first successful load
- [ ] Check phone portrait layout

**Important:** Real patient data ব্যবহারের আগে backup/privacy workflow পরীক্ষা করো। V1-এ clinical visit বা treatment fields নেই।
