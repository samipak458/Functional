# User Story: Prescription Transcription — Scan-to-Delivery Workflow

Context
- Source: “MazikCare Workshop PP01 - Prescription Transcription & SLAs-20250212_093422-Meeting Recording”
- Repository file: [MazikCare Workshop PP01 - Prescription Transcription & SLAs.md](https://github.com/samipak458/Functional/blob/10e047f9b88b6ff3b99c02b3e9adc692d35c6e61/MazikCare%20Workshop%20PP01%20-%20Prescription%20Transcription%20%26%20SLAs.md)
- This story covers the workflow once a scanned prescription (and associated scanning activity) exists in the system and AI has attempted to populate a prescription. The upstream scanning hardware/process and AI ingestion details are out of scope here as they will be covered separately.

## Primary User Story
As a user managing prescriptions, I want to review AI-populated prescription records, verify the transcription, and have the system generate delivery orders, so that patients receive medication in line with the contract and prescribed regimen.

## Scope
- In scope:
  - Viewing scanning activities and their processing outcomes (success/failure).
  - Reviewing and editing the Prescription form (General, Patient Details, Prescriptions, Delivery Orders, Stock Check tabs where relevant).
  - Verifying transcription to trigger delivery order generation.
  - Viewing/using “Next Projected Delivery Date” and delivery visit calculations.
  - Managing “Failed Scanning Activities” via system views with failure reasons.
- Out of scope:
  - The physical/bulk scanning process and the AI pipeline that converts documents to records (noted for a later session).
  - Detailed transcription rules logic beyond what is explicitly stated.

## Key Functional Requirements (derived from transcript)
1. Scanning activities and AI outcomes
   - The system creates a Scanning Activity record per scanned document.
   - A scheduled background job attempts to process open scanning activities; on success it creates/updates the Prescription and closes the activity.
   - On failure, the Scanning Activity remains open with a populated failure reason.
   - System views must exist to list:
     - Open Scanning Activities
     - Failed Scanning Activities (including a visible Failure Reason column)

2. Prescription creation and required fields
   - AI populates the Prescription with relevant fields: hospital/provider, patient, referral, therapy code, diagnosis, and medication lines when possible.
   - Prescription types (exact values): New Patient, Renewal, Dose Change.
   - Mandatory fields on the Prescription form: Patient, Referral, Start Date.
   - Users can manually associate missing details and convert a Scanning Activity into a Prescription if AI fails.

3. General tab behavior
   - Delivery visit calculation:
     - Formula uses Duration in days and Delivery Frequency in days.
     - If no End Date is provided, the user can provide Duration directly (with unit).
     - Example provided: Duration = 100 days, Frequency = 4 weeks (28 days) → calculated deliveries = 3.
   - Next Projected Delivery Date:
     - If a prior prescription exists, take the date of the last delivery from the previous prescription and add the new prescription’s delivery frequency to display the Next Projected Delivery Date.
     - If no prior prescription exists, this field is not calculated by default.
   - The scanned prescription document should be visible/linked on the Prescription General tab (when created via scanning).
   - Delivery details on the form include Purchase Order Number and confirmation.
   - Flags on the General tab include: Clinical Screened, Loading Dose Required, Controlled Prescription.
   - Duplicate prescription handling:
     - If a prescription is expired with a reason of “Duplicate,” the system flags it as duplicate.
   - Activation/deactivation:
     - Deactivated prescriptions are excluded from views/calculations (treated as recoverable “delete”).
     - Expired/fulfilled prescriptions can still be Active for the purposes of calculating Next Projected Delivery Date.

4. Tabs and views
   - Patient Details tab: shows patient snapshot and allows recording weight/height.
   - Prescriptions tab: shows prescriptions associated with the same context (active ones; deactivated are excluded).
   - Delivery Orders tab: lists deliveries generated for the prescription, with scanned document/work order product details visible.
   - Stock Check tab: becomes relevant during later stages (e.g., awaiting ACD) and supports recording stock on subsequent deliveries.

5. Transcription rules (coverage level per transcript)
   - Rules conceptually check:
     - Required product information is present.
     - Prescription complies with contract specifications.
     - The patient order/medication line has required information.
   - Detailed rule definitions/field-level validations to be clarified.

6. Manual prescription creation (configuration option)
   - It is possible to manually create a prescription from Referral/Episode of Care.
   - If prescriptions must only be created via scanning, the manual creation option can be hidden.

## Acceptance Criteria

- Scanning activities
  - Given a scanned document, when the background job runs, then successful activities are closed and corresponding Prescription records are created/updated.
  - Given a scanned document the AI could not process, when the background job runs, then the Scanning Activity remains open with a Failure Reason populated and appears in the “Failed Scanning Activities” system view.
  - The “Failed Scanning Activities” view includes a visible Failure Reason column.

- Prescription creation and required fields
  - Given an AI-processed scanned document, when a Prescription is created, then the Prescription includes population (where available) for: hospital/provider, patient, referral, therapy code, diagnosis, and medication lines.
  - Given a user is creating or editing a Prescription, when saving, then Patient, Referral, and Start Date are required.
  - Given a failed scanning activity, when the user manually associates the item to patient/referral/provider, then the user can convert it into a Prescription.

- General tab calculations and fields
  - Delivery visit calculation:
    - Given Start Date and End Date (or user-entered Duration and unit) and a Delivery Frequency, when the calculation runs, then the number of deliveries is computed from Duration (days) / Delivery Frequency (days).
    - Given Duration = 100 days and Delivery Frequency = 28 days, when calculated, then the number of deliveries equals 3 (as per example in session).
  - Next Projected Delivery Date:
    - Given a previous prescription exists with a last delivery date and a new prescription with Delivery Frequency, when the new prescription is created, then Next Projected Delivery Date = last delivery date (previous Rx) + delivery frequency.
    - Given no previous prescription exists, when viewing the new prescription, then Next Projected Delivery Date is not populated by default.
  - The General tab shows:
    - Link/reference to the scanned prescription document (for prescriptions created via scanning).
    - Delivery details: Purchase Order Number and confirmation.
    - Flags: Clinical Screened, Loading Dose Required, Controlled Prescription.
    - Duplicate prescription flag behavior aligns with expiring a prescription for reason “Duplicate.”

- Activation/deactivation
  - Given a prescription is deactivated, when viewing lists and running calculations, then the deactivated prescription is excluded.
  - Given a prescription is expired/fulfilled but still active (not deactivated), when computing Next Projected Delivery Date for a new prescription, then the active prior prescription can be used as the source.

- Tabs and visibility
  - Patient Details tab allows viewing patient info and recording weight/height.
  - Prescriptions tab lists associated prescriptions (excluding deactivated).
  - Delivery Orders tab shows all deliveries for the prescription, including scanned document and work order product details.

- Transcription verification to delivery generation
  - Given a Prescription is ready for transcription, when the user selects “Verify Transcription,” then the system generates the Delivery Orders associated with the prescription.
  - After delivery orders are generated, users can review labels and quantities.

- Manual creation configuration
  - If configuration to restrict manual prescription creation is enabled, then the “Create Prescription” option from Referral/Episode is hidden.

## Non-Functional/Operational Notes
- Background/batch job schedules process Scanning Activities and create Prescription records; exact cadence/SLAs to be defined.
- Views are configurable; columns (e.g., Failure Reason) must be present in the “Failed Scanning Activities” view by default.
- Columns in the Prescriptions tab view are configurable if additional information is required.

## Open Items (to be clarified)
- Detailed transcription rule definitions and any blocking vs. warning behavior prior to “Verify Transcription.”
- Exact rounding/round-up behavior for delivery visit calculation beyond the provided example.
- Units supported for Delivery Frequency and Duration (e.g., weeks → 7 days; how mappings are maintained).
- Whether manual prescription creation should be disabled in production.
- Which user roles are allowed to “Verify Transcription,” deactivate prescriptions, and manage failed scanning activities.
- Any SLAs for:
  - Processing scanning activities.
  - Resolving failed scanning activities.
  - Completing transcription verification to delivery order generation.
- Required columns for the “Failed Scanning Activities” view beyond Failure Reason.
- Handling specifics for “Controlled Prescription” and “Loading Dose Required” (any additional steps/approvals).
- Expected behavior of “Duplicate” flag across reporting and validation.
- Whether “Stock Check” workflows are in scope for this phase or deferred to a later story.
- Any additional mandatory fields on the Prescription form beyond Patient, Referral, and Start Date that must be enforced?