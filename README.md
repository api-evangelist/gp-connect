# GP Connect (gp-connect)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

GP Connect is a national NHS England interoperability programme that enables authorised clinical and patient-facing systems to securely access and update patient records held in GP principal clinical systems (EMIS Web, SystmOne, Vision). The programme exposes a suite of FHIR-based REST APIs spanning structured clinical record access (medications, allergies, immunisations, consultations, problems, investigations), unstructured document retrieval, appointment management, document sending, record updating, and patient-facing services for patients to view their own records, manage repeat prescriptions, and book appointments via the NHS App. Clinical system APIs are mediated through the Spine Security Proxy (SSP) over HSCN; patient-facing APIs use NHS login OpenID Connect at P9 identity verification. Access requires NHS England onboarding, an approved clinical use case, information governance compliance, and a clinical safety officer holding DCB0129 and DCB0160 certification. The service is funded by NHS England at no direct API cost to consuming organisations.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gp-connect/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gp-connect/refs/heads/main/apis.yml)

## Tags

- NHS
- FHIR
- Healthcare
- GP Records
- Appointments
- Prescriptions
- Interoperability
- UK
- Patient Records
- Electronic Health Records
- FHIR STU3
- FHIR R4

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### GP Connect Access Record - Structured FHIR API

Retrieve structured and coded clinical information from a patient's GP practice record via a FHIR STU3 interface. Supports retrieval of medications, allergies, immunisations, consultations, problems, investigations, and reviewed documents. Intended for clinical system consumers accessing data on behalf of healthcare professionals delivering direct care. Mediated through the Spine Security Proxy over HSCN. Current version is 1.5.0 and is in production.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-access-record-structured-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-access-record-structured-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect-access-record-structured-fhir`

#### Tags

- FHIR STU3
- Patient Records
- Medications
- Allergies
- Immunisations
- Consultations
- Problems
- Investigations
- Clinical Access

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-access-record-structured-fhir)
- [OpenAPI](https://raw.githubusercontent.com/NHSDigital/gp-connect-access-record-structured-fhir/master/specification/gp-connect-access-record-structured-fhir.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Sandbox](https://sandbox.api.service.nhs.uk/gp-connect-access-record-structured-fhir)
- [Git Hub](https://github.com/NHSDigital/gp-connect-access-record-structured-fhir)

### GP Connect Access Document FHIR API

Retrieve unstructured documents (e.g. scanned letters, attachments) from a patient's GP practice record. Complements the structured access API for cases where clinical information is held as binary document rather than coded FHIR resources. Mediated through the Spine Security Proxy over HSCN.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-access-document-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-access-document-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect-access-document-fhir`

#### Tags

- FHIR STU3
- Patient Records
- Documents
- Unstructured Records
- Clinical Access

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-access-document-fhir)

### GP Connect Appointment Management FHIR API

Manage GP practice appointments between different clinical systems. Enables consumers to search for free appointment slots, book appointments, retrieve appointment details, amend appointments, and cancel appointments at a patient's registered GP practice. Mediated through the Spine Security Proxy over HSCN. Version 1.2.7 in production; the appointment management capability has been available as a clinical system API since 2018.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-appointment-management-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-appointment-management-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect-appointment-management-fhir`

#### Tags

- FHIR STU3
- Appointments
- Slot Management
- Booking
- Clinical Access

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-appointment-management-fhir)
- [OpenAPI](https://raw.githubusercontent.com/NHSDigital/gp-connect-appointments-management-fhir/master/specification/gp-connect-appointments-management-fhir.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Sandbox](https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/appointments-management-fhir/FHIR/STU3)
- [Git Hub](https://github.com/NHSDigital/gp-connect-appointments-management-fhir)

### GP Connect Send Document FHIR API

Send a PDF consultation summary or clinical document to a patient's registered GP practice. Used when a patient is seen in a non-GP setting (out-of-hours, community pharmacy, urgent care centre) and the consulting clinician needs to update the patient's GP record. Messages use FHIR STU3 ITK3 composition payloads delivered via MESH messaging infrastructure. In production.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-send-document-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-send-document-fhir)
- **Base URL:** `https://digital.nhs.uk/developer/api-catalogue/gp-connect-send-document-fhir`

#### Tags

- FHIR STU3
- ITK3
- MESH
- Documents
- Messaging
- Clinical Access

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-send-document-fhir)

### GP Connect Update Record FHIR API

Send structured FHIR data to update a patient's GP record with medications, encounters, and observations. Currently approved for pharmacy use cases, including informing a GP that a patient has been prescribed antibiotics or had their blood pressure checked at a pharmacy. In development. Requires HSCN connectivity and Spine Directory Service (SDS) compliance.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-update-record-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-update-record-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect-update-record-fhir`

#### Tags

- FHIR STU3
- Patient Records
- Medications
- Encounters
- Observations
- Pharmacy
- Clinical Access

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-update-record-fhir)
- [OpenAPI](https://raw.githubusercontent.com/NHSDigital/gp-connect-update-record-fhir/master/specification/gp-connect-update-record-fhir.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Git Hub](https://github.com/NHSDigital/gp-connect-update-record-fhir)

### GP Connect Patient Facing Access Record FHIR API

Allow patients to access structured and coded information from their own GP practice record via a patient-facing application. Retrieves medications, allergies, immunisations, consultations, problems, investigations, and reviewed documents in accordance with the patient's permission level set at their GP practice. Requires NHS login at P9 identity verification level. Uses OpenID Connect and OAuth 2.0. Currently available to New Market Entrant GP system suppliers and the NHS App. In production.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-access-record-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-access-record-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/access-record-fhir/FHIR/STU3`

#### Tags

- FHIR STU3
- Patient Facing
- Patient Records
- Medications
- Allergies
- Immunisations
- NHS Login
- NHS App

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-access-record-fhir)
- [OpenAPI](https://raw.githubusercontent.com/NHSDigital/gp-connect-access-record-fhir/master/specification/gp-connect-access-record-fhir.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Sandbox](https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/access-record-fhir/FHIR/STU3)
- [Git Hub](https://github.com/NHSDigital/gp-connect-access-record-fhir)

### GP Connect Patient Facing Appointment Management FHIR API

Allow patients to book and manage their own appointments at their GP practice via a patient-facing application. Supports searching for free slots, booking appointments, retrieving existing appointments, and cancelling appointments. Patients cannot amend or reschedule; they must cancel and re-book. Requires NHS login at P9 identity verification level. Currently not available for new consumer onboarding; in development.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-appointment-management-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-appointment-management-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/appointments-management-fhir/FHIR/STU3`

#### Tags

- FHIR STU3
- Patient Facing
- Appointments
- Slot Management
- Booking
- NHS Login
- NHS App

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-appointment-management-fhir)
- [OpenAPI](https://raw.githubusercontent.com/NHSDigital/gp-connect-appointments-management-fhir/master/specification/gp-connect-appointments-management-fhir.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Sandbox](https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/appointments-management-fhir/FHIR/STU3)
- [Git Hub](https://github.com/NHSDigital/gp-connect-appointments-management-fhir)

### GP Connect Patient Facing Prescriptions Management FHIR API

Allow patients to manage repeat prescriptions held by their GP practice via a patient-facing application. Supports requesting a new instance of a repeat prescription, checking the status of a current prescription request, and requesting a new instance to a one-off nomination pharmacy. Conforms to FHIR R4 (v4.0.1) and UK Core STU2 1.1.3. Requires NHS login at P9 identity verification level. Silver service (24/7, business-hours support). In development; sandbox available.

- **Human URL:** [https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-prescriptions-fhir](https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-prescriptions-fhir)
- **Base URL:** `https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/prescriptions-management-fhir/FHIR/R4`

#### Tags

- FHIR R4
- Patient Facing
- Prescriptions
- Medications
- Repeat Prescriptions
- NHS Login
- NHS App
- UK Core

#### Properties

- [Documentation](https://digital.nhs.uk/developer/api-catalogue/gp-connect-patient-facing-prescriptions-fhir)
- [OpenAPI](https://raw.githubusercontent.com/NHSDigital/gp-connect-prescriptions-management-fhir/master/specification/gp-connect-prescriptions-management-fhir.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Sandbox](https://sandbox.api.service.nhs.uk/gp-connect/patient-facing/prescriptions-management-fhir/FHIR/R4)
- [Postman](https://god.gw.postman.com/run-collection/34036044-3c90d3e4-24ec-4a09-867e-26da1516ee61?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D34036044-3c90d3e4-24ec-4a09-867e-26da1516ee61%26entityType%3Dcollection%26workspaceId%3Dbad72f85-20d6-41c3-bd55-f30bf83f8c63) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Git Hub](https://github.com/NHSDigital/gp-connect-prescriptions-management-fhir)

## Common Properties

- [Portal](https://digital.nhs.uk/services/gp-connect)
- [Documentation](https://digital.nhs.uk/developer/api-catalogue)
- [Help And Support](https://digital.nhs.uk/developer/help-and-support)
- [Sign Up](https://digital.nhs.uk/services/gp-connect/develop-gp-connect-services/specifications-for-developers)
- [Authentication](https://digital.nhs.uk/developer/guides-and-documentation/security-and-authorisation/user-restricted-restful-apis-nhs-login-separate-authentication-and-authorisation)
- [Onboarding](https://digital.nhs.uk/services/gp-connect/develop-gp-connect-services/specifications-for-developers)
- [Git Hub](https://github.com/NHSDigital)
- [Standards](https://standards.nhs.uk/published-standards/gp-connect-access-record-structured-fhir-api)
- [Sandbox](https://orange.testlab.nhs.uk/)
- [Service Level](https://digital.nhs.uk/developer/guides-and-documentation/reference-guide#service-levels)
- [Network Access](https://digital.nhs.uk/developer/guides-and-documentation/network-access-for-apis)
- [Clinical Safety](https://digital.nhs.uk/services/clinical-safety)
- [Plans](plans/gp-connect-plans.yml)
- [Rate Limits](rate-limits/gp-connect-rate-limits.yml)
- [Fin Ops](finops/gp-connect-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
