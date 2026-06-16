# GP Connect (gp-connect)

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
