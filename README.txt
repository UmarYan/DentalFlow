DentalFlow V8.10.1 - Encounter Return Fix

Built as a focused fix on V8.10.0 Follow-up Status.

Fix:
- When a Clinical Visit is opened from an in-progress Encounter, saving it now returns to Encounter Workspace instead of sending the user to Patient Profile.
- The existing encounter visit link is preserved by the current save logic.
- Clinical visits opened outside an Encounter keep the previous behavior and return to Patient Profile.
- Service-worker cache name updated.

Important scope limitation:
- This is a navigation fix, not full workflow integration. Treatment plans, bills/payments and follow-ups still use existing screens and must be explicitly linked/verified. Do not assume all encounter workflow steps are fully connected.

Safety:
- ZIP contains app files only, no patient data.
- Before deployment, export a DentalFlow JSON backup and keep the previous ZIP. Do not clear browser/site storage.
- Test on device with a test patient/record first. Confirm that saving a visit opened from Encounter Workspace returns to Encounter Workspace and shows the linked visit. Also test a normal visit opened outside Encounter to confirm it still returns to Patient Profile.
- Syntax/archive checks do not replace full Android workflow testing.

Deploy: extract contents into the existing GitHub Pages repository, commit, wait for Pages to publish, then refresh/reopen the app.
