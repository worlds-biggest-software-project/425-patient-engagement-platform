# Standards & API Reference

> Project: Patient Engagement Platform · Generated: 2026-05-07

---

## Industry Standards & Specifications

### HL7 / FHIR Standards

**HL7 FHIR R4 (Release 4)**
- URL: https://hl7.org/fhir/R4/
- The normative foundation for structured health data exchange. Defines RESTful APIs, resource types (Patient, Appointment, Communication, Observation, MedicationRequest, CarePlan, Questionnaire, QuestionnaireResponse), and the JSON/XML wire format. Required under ONC Cures Act certification rules. A patient engagement platform must expose and consume FHIR R4 APIs for EHR integration. FHIR R6 (in ballot as of 2026) will bring most clinical and administrative resources to normative status.

**HL7 FHIR R5**
- URL: https://hl7.org/fhir/R5/
- Adds 55+ new resources focused on patient engagement and care coordination, including topic-based subscriptions for real-time push notifications, improved Questionnaire and QuestionnaireResponse for PRO collection, and an enhanced Group resource for population health. Subscription model is foundational for event-driven engagement triggers.

**HL7 US Core Implementation Guide (STU 9.0.0)**
- URL: https://build.fhir.org/ig/HL7/US-Core/
- Defines the minimum constraints on FHIR R4 resources for US healthcare data exchange: US Core Patient Profile (demographics, preferred language, contact), US Core Appointment, US Core Condition, US Core Observation (labs, vitals), and US Core DocumentReference. Certification under ONC HTI-1 requires US Core conformance. Any engagement platform integrating with US EHRs must support these profiles.

**HL7 SMART App Launch Framework v2.2.0**
- URL: https://hl7.org/fhir/smart-app-launch/
- Defines the OAuth 2.0/OIDC-based authorization protocol for launching applications from within EHRs and patient portals. Specifies EHR launch, standalone launch, token scopes (clinical data access), and launch context (patient, encounter). Required for any app seeking distribution via Epic App Orchard or Cerner App Market. The standard mechanism for embedding patient-facing engagement apps inside EHR workflows.

**HL7 FHIR Bulk Data Access (Flat FHIR)**
- URL: https://hl7.org/fhir/uv/bulkdata/
- Defines asynchronous, large-scale FHIR data export for population health. Relevant for identifying care gaps across a patient population — the input data source for outreach campaign generation. Required under ONC Cures Act for certified EHR technology.

**HL7 Da Vinci Project — Patient Data Collection (PDC) and Coverage Requirements Discovery (CRD)**
- URL: https://www.hl7.org/fhir/us/davinci-pdex/
- FHIR-based implementation guides from the Da Vinci Project relevant to payer-provider data exchange, prior authorization workflows, and claims-driven patient outreach triggers.

---

### W3C & IETF Standards

**W3C Web Content Accessibility Guidelines (WCAG) 2.2**
- URL: https://www.w3.org/TR/WCAG22/
- The accessibility standard applicable to all patient-facing web interfaces and mobile apps. As of May 2026, healthcare organizations accepting Medicare/Medicaid/CHIP funding must meet WCAG 2.1 Level AA minimum; WCAG 2.2 AA satisfies and exceeds this requirement. Patient portals, intake forms, scheduling interfaces, and messaging UIs are all in scope. Key criteria: perceivable (color contrast, alt text), operable (keyboard navigation, no time limits), understandable (readable labels, error identification), and robust (assistive technology compatibility).

**RFC 7617 — HTTP Basic Authentication**
- URL: https://www.rfc-editor.org/rfc/rfc7617
- Baseline HTTP authentication scheme; relevant for internal API authentication between components.

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://www.rfc-editor.org/rfc/rfc6749
- The foundational authorization protocol used by SMART on FHIR and all FHIR API authentication flows. Patient engagement platforms must implement OAuth 2.0 authorization code flow for patient-facing app authentication and for EHR API access.

**RFC 8693 — OAuth 2.0 Token Exchange**
- URL: https://www.rfc-editor.org/rfc/rfc8693
- Relevant for federated identity scenarios where a patient engagement platform must exchange tokens between systems (e.g., between the engagement platform and an EHR).

**OpenID Connect Core 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- Builds on OAuth 2.0 to add identity layer for patient authentication. Standard mechanism for patient single sign-on (SSO) to engagement portals. Used in conjunction with SMART on FHIR for EHR-embedded app launch.

**RFC 7519 — JSON Web Token (JWT)**
- URL: https://www.rfc-editor.org/rfc/rfc7519
- JWT is the token format used by SMART on FHIR and OpenID Connect for access tokens, ID tokens, and patient identity assertions. All FHIR APIs exchange JWTs for authorization.

**RFC 8288 — Web Linking**
- URL: https://www.rfc-editor.org/rfc/rfc8288
- Defines the Link header and web linking syntax; used by FHIR pagination (Bundle.link) and SMART discovery.

**W3C Push API**
- URL: https://www.w3.org/TR/push-api/
- Enables server-sent push notifications to patient-facing progressive web apps (PWAs). Relevant for appointment reminder delivery via browser push without requiring a native mobile app.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1**
- URL: https://spec.openapis.org/oas/v3.1.0
- Standard for describing REST API contracts. Any patient engagement platform exposing webhooks, campaign trigger APIs, or integration APIs should publish an OpenAPI 3.1 spec to enable partner integrations and third-party developer access.

**FHIR R4 RESTful API**
- URL: https://hl7.org/fhir/R4/http.html
- The canonical RESTful interaction model for FHIR: read, search, create, update, patch, delete, and history operations on FHIR resources. Defines search parameters, Bundle responses, and CapabilityStatement declaration.

**HL7 v2.x Messaging**
- URL: https://www.hl7.org/implement/standards/product_brief.cfm?product_id=185
- Despite FHIR's growing adoption, HL7 v2 (specifically ADT, SIU, MDM, ORU message types) remains prevalent in hospital environments for appointment and ADT (admit/discharge/transfer) event feeds. A patient engagement platform must support v2 message parsing for legacy EHR integrations.

**DICOM SR (Structured Reporting)**
- URL: https://www.dicomstandard.org/
- Relevant for radiology-specific patient communication (results notification, imaging report delivery to patients via portal).

**USCDI (United States Core Data for Interoperability) v4/v5**
- URL: https://www.healthit.gov/isa/united-states-core-data-interoperability-uscdi
- Defines the minimum data elements that must be accessible via patient-facing APIs under ONC Cures Act. Relevant fields for engagement: patient demographics, preferred language, care team members, clinical notes, diagnostic results, medications, and immunizations.

**MCP (Model Context Protocol)**
- URL: https://modelcontextprotocol.io/
- An emerging open protocol for AI agent-to-system integration. DoctorConnect's AI Agent Gateway uses MCP alongside OAuth 2.1 and REST to expose patient engagement workflows to authorized AI agents (scheduling, messaging, recall). Relevant for building agentic AI capabilities into a next-generation engagement platform.

---

### Regulatory & Compliance Frameworks

**HIPAA Security Rule (45 CFR Parts 160 and 164)**
- URL: https://www.hhs.gov/hipaa/for-professionals/security/index.html
- Mandates administrative, physical, and technical safeguards for systems handling ePHI. For a patient engagement platform: access control (unique user IDs, role-based access, session timeouts, MFA), audit controls (immutable logs of all ePHI access), transmission security (TLS 1.2+ for all data in transit), and encryption at rest. HHS published a proposed NPRM in January 2025 to eliminate the "addressable vs. required" distinction, making all safeguards mandatory.

**21st Century Cures Act — ONC Cures Act Final Rule (HTI-1)**
- URL: https://www.healthit.gov/topic/oncs-cures-act-final-rule
- Requires ONC-certified health IT to support FHIR R4 Patient Access APIs, prohibits information blocking, and mandates that patients receive no-cost electronic access to all EHI. Engagement platforms that participate in clinical workflows must not implement information blocking practices. 2026 compliance: USCDI v3+ alignment, updated ONC certification under HTI-1.

**CMS Interoperability and Patient Access Final Rule (CMS-9115-F)**
- URL: https://www.cms.gov/priorities/burden-reduction/overview/interoperability/policies-regulations/cms-interoperability-patient-access-final-rule-cms-9115-f
- Requires CMS-regulated payers to implement FHIR-based Patient Access APIs and Provider Directory APIs. Relevant for engagement platforms serving payer-sponsored care management programs. The CMS Prior Authorization Rule mandates FHIR-based prior authorization APIs by January 2026.

**TCPA (Telephone Consumer Protection Act)**
- URL: https://www.fcc.gov/consumers/guides/stopping-unwanted-calls-and-texts
- Governs automated SMS and voice outreach. Healthcare exemption allows automated messages on patient-provided numbers without additional consent for healthcare-related communications (appointment reminders, test results, billing). Messages must be ≤160 characters (SMS) or ≤1 minute (voice), include an opt-out mechanism, and not include marketing or billing collection content. Violations: $500–$1,500 per message.

**CAN-SPAM Act**
- URL: https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business
- Governs commercial email. Requires accurate subject lines, functioning unsubscribe links, and sender physical address. Applies to marketing emails; transactional/appointment reminder emails are generally exempt from opt-in requirements but must still honor unsubscribe requests.

**ISO 27799:2025 — Health Informatics: Information Security Controls**
- URL: https://www.iso.org/standard/84647.html
- Healthcare-specific guidance layered on ISO/IEC 27002:2022 for information security management in health. The 2025 third edition defines controls for protecting personal health information in software systems, EHR systems, and medical devices. Applicable to the security design of a patient engagement platform.

**OWASP Application Security Verification Standard (ASVS) v4.0**
- URL: https://owasp.org/www-project-application-security-verification-standard/
- Defines security requirements for web applications: authentication (MFA, session management), access control, input validation, cryptography (TLS 1.2+, AES-256), and API security. OWASP ASVS Level 2 is the appropriate baseline for a HIPAA-scoped healthcare application.

**NIST Cybersecurity Framework (CSF) 2.0**
- URL: https://www.nist.gov/cyberframework
- Voluntary framework applicable to US healthcare organizations. CSF 2.0 functions: Govern, Identify, Protect, Detect, Respond, Recover. Provides the governance structure within which HIPAA Security Rule controls are implemented.

**SOC 2 Type II**
- URL: https://us.aicpa.org/interestandpreferences/soc2
- De facto compliance certification expected by health system procurement teams. Trust Service Criteria: Security (CC controls), Availability, Confidentiality, Processing Integrity, and Privacy. All major platforms (Relatient Dash, Medplum cloud) are SOC 2 Type II certified.

**HITRUST CSF**
- URL: https://hitrustalliance.net/
- Healthcare-specific security certification framework that incorporates HIPAA, NIST, ISO, and PCI requirements. Increasingly required by large health system vendors. Relatient Dash Voice AI holds HITRUST certification.

---

## Similar Products — Developer Documentation & APIs

### Epic (MyChart / open.epic)
- **Description:** Epic is the largest EHR vendor in the US. MyChart is the patient portal; open.epic is the developer program providing access to 750+ FHIR R4 APIs. Integration with Epic is essential for any engagement platform targeting large health systems.
- **API Documentation:** https://fhir.epic.com/Documentation
- **Developer Portal:** https://open.epic.com/
- **Developer Playbooks:** https://open.epic.com/Tutorial/Index (40+ use-case specific guides)
- **SDKs/Libraries:** No official SDK; FHIR R4 JSON/REST APIs with developer-provided client libraries
- **Standards:** FHIR R4, SMART on FHIR v2, US Core, USCDI v3+, OpenID Connect
- **Authentication:** OAuth 2.0 + SMART on FHIR (EHR Launch and Standalone Launch); backend services use client credentials with JWT

### athenahealth (athenaOne)
- **Description:** Cloud-based EHR and practice management platform widely deployed in ambulatory practices. Offers both proprietary REST APIs and FHIR R4 APIs; over 400 partner apps are built on the athenahealth API.
- **API Documentation:** https://docs.athenahealth.com/api/
- **FHIR R4 Documentation:** https://mydata.athenahealth.com/fhirapidoc/r4
- **Core Implementation Guide:** https://fhir.athena.io/athenacoreext/index.html
- **GitHub:** https://github.com/athenahealth
- **Standards:** FHIR R4, SMART on FHIR, US Core, USCDI, Bulk Data Export (Cures Act compliance)
- **Authentication:** OAuth 2.0 with SMART on FHIR scopes; developer registration required

### DoctorConnect (AI Agent Gateway)
- **Description:** Patient engagement and appointment reminder platform with 150+ EHR integrations. The AI Agent Gateway is a REST API enabling authorized AI agents to trigger scheduling, messaging, recall, and intake workflows.
- **API Documentation:** https://doctorconnect.net/healthcare-ai-apis-integration-compliance-and-practical/
- **AI Gateway FAQ:** https://doctorconnect.net/healthcare-ai-api-faq/
- **Standards:** REST/JSON, OAuth 2.1, MCP (Model Context Protocol)
- **Authentication:** OAuth 2.1 (private pilot availability)
- **Note:** API is in private pilot as of 2026; full public availability not yet announced

### Medplum (Open Source FHIR Platform)
- **Description:** Open-source FHIR R4 server and developer platform with HIPAA compliance and SOC 2 Type II certification. Serves as both a backend health data store and an application development platform with TypeScript SDK, React component library, and subscription event engine.
- **API Documentation:** https://www.medplum.com/docs/api
- **FHIR API:** https://www.medplum.com/docs/api/fhir
- **GitHub:** https://github.com/medplum/medplum
- **SDKs/Libraries:** TypeScript/JavaScript SDK (npm: @medplum/core, @medplum/react), Python client (community)
- **Developer Guide:** https://www.medplum.com/docs
- **AI Build Guide:** https://www.medplum.com/docs/ai
- **Standards:** FHIR R4 (v4.0.1), SMART on FHIR, US Core, USCDI, OWASP security guidelines
- **Authentication:** OAuth 2.0 / SMART on FHIR; client credentials for backend services
- **Licence:** Apache 2.0 (open source core); managed cloud under commercial terms

### Twilio (Programmable Messaging + SendGrid + Healthcare Solutions)
- **Description:** Cloud communications platform providing SMS, voice, email, and WhatsApp APIs. Used as the underlying channel delivery layer by many patient engagement platforms. Provides HIPAA-eligible services under BAA for customers handling ePHI.
- **API Documentation:** https://www.twilio.com/docs/messaging/api
- **SendGrid Email API:** https://www.twilio.com/docs/sendgrid/api-reference
- **Healthcare Solutions:** https://www.twilio.com/en-us/solutions/healthcare
- **SDKs/Libraries:** Official SDKs for Node.js, Python, Java, PHP, Ruby, Go, C#
- **Standards:** REST/JSON, WebSockets (real-time messaging), TCPA compliance tooling, HIPAA-eligible under BAA
- **Authentication:** API Key (HTTP Basic Auth over HTTPS); Account SID + Auth Token

### Klara / ModMed (Patient Communication API)
- **Description:** Patient communication and collaboration platform acquired by ModMed. Provides HIPAA-compliant two-way messaging, digital intake, telemedicine, and appointment workflows. API access available to ModMed EHR partners.
- **API Documentation:** https://www.klara.com/patient-communication (public docs limited; partner integration via ModMed)
- **Developer Info:** https://www.modmed.com/what-we-do/patient-engagement/
- **Standards:** REST/JSON, HL7 FHIR (ModMed integration), HIPAA-compliant messaging
- **Authentication:** OAuth 2.0 for partner integrations

### Relatient / Dash (Patient Engagement API)
- **Description:** Scheduling, voice AI, and patient communication platform with deep Epic and athenahealth integrations. Dash provides REST APIs for appointment scheduling, messaging, and patient engagement workflow triggers.
- **API Documentation:** https://www.relatient.com/ (partner integration via EHR marketplace)
- **Epic Integration:** https://www.relatient.com/dash-epic-ehr-software-integration/
- **Standards:** REST/JSON, HL7 FHIR, HITRUST and SOC 2 Type II certified
- **Authentication:** OAuth 2.0; EHR marketplace credentials (Epic App Orchard, athenahealth marketplace)

### Salesforce Health Cloud (Agentforce Health)
- **Description:** Enterprise CRM-based patient engagement platform. Provides REST and SOAP APIs via Salesforce platform, FHIR R4 data model support via MuleSoft, and agentic AI (Agentforce) capabilities for orchestrating complex patient engagement journeys.
- **API Documentation:** https://developer.salesforce.com/docs/health/health-cloud/overview
- **MuleSoft FHIR Connectors:** https://www.mulesoft.com/exchange/com.mulesoft.connectors/mule-hl7-connector/
- **SDKs/Libraries:** Salesforce Platform SDKs (Java, JavaScript, Python, Apex); REST and SOAP
- **Standards:** FHIR R4 (via MuleSoft), REST/SOAP, OpenAPI, OAuth 2.0 / OpenID Connect
- **Authentication:** OAuth 2.0 with Salesforce Connected App; JWT Bearer for server-to-server

### Phreesia (Patient Intake API)
- **Description:** Patient intake and activation platform powering 180 million visits in 2026. Provides APIs for EHR-connected digital intake, real-time insurance verification, consent management, and post-visit survey collection.
- **API Documentation:** https://www.phreesia.com/solutions/health-systems/ (partner integration; public API docs are limited)
- **Standards:** HL7 FHIR R4, HL7 v2, REST/JSON; real-time insurance eligibility (270/271 X12 transactions)
- **Authentication:** OAuth 2.0 for EHR integrations; credentials provisioned via partner onboarding

---

## Notes

**FHIR Maturity and Adoption:** FHIR R4 is the current regulatory baseline and the version to build against. R5 subscriptions are an important future target for real-time event-driven engagement triggers (appointment created, lab resulted, care gap identified). R6 is in ballot as of 2026 and is not a production target for new projects yet.

**HL7 v2 Persistence:** Despite FHIR's growth, HL7 v2.x (particularly ADT A04, SIU S12/S15, ORU R01 message types) remains in widespread use for appointment and admission event notifications in hospital systems. A complete engagement platform integration layer must handle v2 messages in addition to FHIR.

**MCP Emergence:** The Model Context Protocol (MCP) is gaining traction as the standard interface for AI agent tool use. DoctorConnect's AI Agent Gateway already uses MCP. New engagement platforms with agentic AI capabilities should consider publishing MCP server specifications to enable interoperability with LLM-based agents.

**TCPA 2026 Update:** The FCC issued updated TCPA rules effective January 2025 with stricter one-to-one consent requirements for marketing messages. Healthcare appointment reminder exemptions remain intact but platforms must implement robust consent management, opt-out tracking, and auditable preference records to mitigate TCPA exposure.

**WCAG May 2026 Deadline:** US healthcare organizations receiving federal funding must meet WCAG 2.1 AA for all patient-facing digital touchpoints as of May 2026. Patient portals, intake forms, and scheduling interfaces built for the US market must be accessibility-tested against this standard.
