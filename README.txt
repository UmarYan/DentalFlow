DentalFlow V7.8.47 — Shared Form Integration Candidate

This package is based on the V7.8.46 PWA-assets-restored build. It fixes the visible version label and uses a distinct service-worker cache key, and includes all PWA files referenced by index.html.

IMPORTANT STATUS: DEVELOPMENT / TEST CANDIDATE, NOT A VERIFIED FINAL RELEASE.

The code contains a shared form-entry registry/controller that routes to existing Appointment, Clinical Visit, Treatment Plan, Follow-up, Bill, and Payment forms. This does NOT yet prove that Patient Workflow and standalone sections use one identical form field structure, validation path, and save implementation for all six record types. Do not assume that requirement is fully completed.

Before deployment:
1. Keep the currently deployed site unchanged.
2. Make and verify a separate backup of clinic data.
3. Test this package in a separate test deployment with dummy data.
4. Test New/Edit for all six types, patient/visit/plan/bill linkage, multiple payments/outstanding calculations, and backup/restore.
5. Only promote after those tests pass.

Upload the contents of this ZIP to the publishing root only for a separate test deployment. Do not clear browser storage or delete existing clinic data as a deployment step.
