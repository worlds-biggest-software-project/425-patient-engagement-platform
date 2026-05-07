# Patient Engagement Platform — Feature & Functionality Survey

> Candidate #425 · Researched: 2026-05-07

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| DoctorConnect | Standalone engagement platform | Commercial SaaS | https://doctorconnect.net |
| Klara (ModMed) | Communication & collaboration platform | Commercial SaaS | https://www.klara.com |
| TeleVox | Omnichannel engagement platform | Commercial SaaS | https://televox.com |
| Relatient (Dash) | Scheduling & engagement platform | Commercial SaaS | https://www.relatient.com |
| Solutionreach | Patient relationship management | Commercial SaaS | https://www.solutionreach.com |
| Phreesia | Patient intake & activation platform | Commercial SaaS | https://www.phreesia.com |
| AdvancedMD | Integrated PM/EHR/engagement suite | Commercial SaaS | https://www.advancedmd.com |
| Actium Health (CENTARI) | AI-driven outreach & CRM intelligence | Commercial SaaS | https://actiumhealth.com |
| Epic MyChart | Patient portal (EHR-embedded) | Commercial (EHR vendor) | https://www.mychart.org |
| Salesforce Health Cloud | Enterprise CRM/engagement platform | Commercial SaaS | https://www.salesforce.com/healthcare |
| OhMD | Messaging-first engagement for practices | Commercial SaaS | https://www.ohmd.com |
| Medplum | Open-source FHIR healthcare platform | Open source (MIT) | https://www.medplum.com |

---

## Feature Analysis by Solution

### DoctorConnect

**Core features**
- Multi-channel appointment reminders (SMS, email, automated voice)
- Two-way HIPAA-compliant secure messaging
- Automated recall and no-show re-engagement messaging
- Digital intake forms and pre-visit document collection
- Online bill payment (RevPay)
- ARIA AI Receptionist: 24/7 inbound call triage, FAQ handling, and EHR-synced scheduling
- 150+ EHR and practice management system integrations
- Configurable reminder cadence (timing, channel, message content)

**Differentiating features**
- 30+ year market presence with a zero HIPAA violations track record
- ARIA Phase 1 AI agent reduces inbound call handling by up to 70%
- Breadth of EHR integrations (150+) is industry-leading for a standalone platform
- Serves over 500 active practices with documented 25–40% no-show reduction

**UX patterns**
- Staff-facing dashboard for managing patient communications
- Automated workflows with minimal required staff intervention
- Patient-facing confirmation and cancellation via reply-to-SMS flow

**Integration points**
- Bidirectional EHR integration (150+ systems)
- Practice management system sync for appointment data
- SMS gateway, email delivery, automated voice providers

**Known gaps**
- Limited AI-driven personalization beyond rule-based messaging
- No built-in patient portal for longitudinal record access
- Population health analytics are basic compared to enterprise platforms
- No native care gap identification; relies on EHR data feed

**Licence / IP notes**
- Proprietary commercial SaaS; no open-source components disclosed
- ARIA AI Receptionist is a proprietary AI component

---

### Klara (ModMed)

**Core features**
- Unified HIPAA-compliant conversation inbox (SMS, web chat, voicemail, phone all consolidated)
- Call-to-text deflection: automatically converts inbound calls to text threads
- Voicemail transcription
- Two-way patient messaging with intelligent staff routing
- Patient self-scheduling without portal login
- Automated pre-visit intake via digital eForms
- Broadcast messaging (closures, announcements, seasonal campaigns)
- Post-visit patient satisfaction surveys
- Video telemedicine with up to 4 participants
- Chrome extension for in-chart documentation during video visits

**Differentiating features**
- Consolidates all patient communication channels into a single thread without requiring portal activation
- "Call-to-text" deflection is a standout feature that reduces phone burden while preserving patient reachability
- Deep integration with ModMed EHR specialty workflows (dermatology, ophthalmology, plastic surgery)
- Video visit documentation via EHR Chrome extension is operationally differentiated

**UX patterns**
- Inbox-centric staff UI modeled on modern messaging apps
- No portal activation required from patients — engagement via SMS link
- Pre-visit automation reduces staff touchpoints before appointment day

**Integration points**
- Deep bidirectional integration with ModMed/EMA EHR
- HL7/FHIR API for third-party EHR connections
- SMS and email gateway integrations

**Known gaps**
- Deep integrations are primarily optimized for ModMed/specialty practices
- Limited population health or care gap outreach capabilities
- No native propensity modeling or AI-driven campaign prioritization
- Surveys are basic; no CAHPS-specific validated instrument library

**Licence / IP notes**
- Proprietary commercial SaaS; acquired by ModMed
- No open-source components

---

### TeleVox

**Core features**
- Omnichannel outreach: SMS, email, automated voice, chat
- Appointment reminders with procedure-specific instructions
- Patient self-scheduling, rescheduling, and cancellation via text/web
- Intelligent Virtual Agents (IVAs) for inbound and outbound conversation handling
- Pre-visit intake forms and insurance verification
- Post-visit follow-up and chronic care adherence messaging
- Care gap and wellness visit outreach campaigns
- AI-powered real-time language translation for patient messages
- Insights360 analytics: interaction-level visibility into communication outcomes
- Accessibility features: screen readers, adjustable text size

**Differentiating features**
- Insights360 analytics platform provides more granular communication performance metrics than most peers
- AI language translation at the conversation level (not just template translation) is a meaningful differentiator for diverse populations
- IVA-driven fully automated appointment management without staff intervention
- Accessibility-first design (WCAG compliance, screen reader support) is explicitly documented

**UX patterns**
- Text-based self-service keeps patients in their native messaging app
- IVAs handle multi-turn conversations without staff handoff for routine tasks
- Progressive disclosure: patients only see detail relevant to their specific appointment type

**Integration points**
- Direct EHR reads from Epic, Cerner, NextGen
- HL7 feeds for appointment and patient demographic data
- REST API for campaign triggering and data sync

**Known gaps**
- Enterprise pricing model makes it inaccessible to small independent practices
- Care gap logic relies on EHR data quality; limited ability to enrich with claims data
- No built-in patient portal; engagement is channel-based, not portal-based
- PRO (patient-reported outcome) collection is limited

**Licence / IP notes**
- Proprietary commercial SaaS
- IVA technology is proprietary; no open-source components

---

### Relatient (Dash)

**Core features**
- Patient self-scheduling via web, mobile, and text (24/7)
- AI-powered Voice AI Agents (Dash Voice) for inbound call handling
- Two-way secure messaging (Dash Chat)
- Automated appointment reminders and confirmations
- Digital registration and pre-visit intake forms
- Reputation management and post-visit survey collection
- Broadcast messaging to patient segments
- HITRUST and SOC 2 certified voice AI

**Differentiating features**
- Named athenahealth Preferred Solution Partner for intelligent scheduling (2026)
- Deep Epic EHR integration for scheduling workflows
- Dual AI approach: Voice AI (inbound calls) + Chat (asynchronous messaging) in one platform
- HITRUST and SOC 2 certification for Voice AI is a compliance differentiator

**UX patterns**
- Text-first patient interaction; scheduling and confirmation via conversational SMS
- Staff dashboard for managing chat threads and patient communications
- Online scheduling embeds directly in practice website

**Integration points**
- Epic EHR bidirectional integration
- athenahealth marketplace integration
- REST API for EHR data sync and webhook-based event triggers

**Known gaps**
- Analytics dashboard is less mature than enterprise platforms
- Limited care gap or population outreach beyond appointment-related messaging
- No built-in patient education content library
- Pricing reported as opaque; strict contract renewal windows and termination fees noted in user reviews

**Licence / IP notes**
- Proprietary commercial SaaS
- HITRUST and SOC 2 certified

---

### Solutionreach

**Core features**
- Two-way SMS, email, and voice appointment reminders and confirmations
- Branded automated post-appointment satisfaction surveys (CAHPS-aligned)
- Patient newsletter and health campaign messaging
- Online self-scheduling
- Patient portal with secure messaging, prescription requests, and bill pay
- Telehealth capabilities
- Reputation management (review solicitation and monitoring)
- Segmented messaging by appointment type, provider, or facility
- Insurance verification automation

**Differentiating features**
- Survey and reputation management combination distinguishes it in the mid-market
- Dental-specific modules (DSO support) give it breadth across dental and medical practices
- Branded surveys sent from actual office phone number increases open rates
- Configurable multi-condition message rules (appointment type, provider, location)

**UX patterns**
- Newsletter-style bulk patient communication tools for non-appointment touchpoints
- Survey flows with response-branching logic for targeted follow-up
- Reputation monitoring dashboard aggregates review data across review platforms

**Integration points**
- EHR and practice management integrations across medical and dental platforms
- Patterson Dental marketplace partnership
- SMS gateway, email delivery, and voice call providers

**Known gaps**
- User interface described as disjointed in reviews (result of platform consolidations)
- Customer support response times frequently cited as slow
- Opaque pricing and aggressive contract terms
- AI capabilities trail newer entrants (Actium, TeleVox IVAs, DoctorConnect ARIA)

**Licence / IP notes**
- Proprietary commercial SaaS
- No open-source components

---

### Phreesia

**Core features**
- AI-powered digital intake (demographics, insurance, medical history, consent)
- Logic-driven intake interviews personalized to each patient's profile
- Real-time insurance eligibility verification during intake
- Appointment request forms (web-based, no portal login required)
- Mobile intake in 20 languages
- Consent form management with configurable presentation cadence
- Post-visit surveys and patient satisfaction measurement
- PhreesiaOnCall after-hours HIPAA-compliant answering solution
- Patient activation campaigns triggered from intake data

**Differentiating features**
- Logic-driven adaptive intake interviews (not static PDFs) dramatically improve data quality
- 20-language mobile intake is the widest multilingual coverage in the segment
- 180 million patient visits powered in 2026 — largest intake platform by volume
- Real-time insurance verification embedded in intake flow (not a separate step)
- AI-powered intake is the most mature in the market with longest deployment history

**UX patterns**
- Patient uses a tablet in the waiting room or completes on personal device before arrival
- Adaptive question branching based on prior answers reduces form fatigue
- Insurance verification results surfaced to front desk in real time during check-in

**Integration points**
- Deep EHR integrations across major platforms (Epic, Oracle Health, eClinicalWorks, eMDs, athenahealth, etc.)
- HL7 and FHIR-based data exchange
- Real-time insurance eligibility APIs (payer connections)

**Known gaps**
- Engagement capabilities beyond intake are weaker than pure-play engagement platforms
- No AI-driven outreach or propensity modeling for campaign prioritization
- Satisfaction surveys are competent but not analytics-rich
- Post-visit engagement and care gap outreach are not core competencies

**Licence / IP notes**
- Proprietary commercial SaaS
- Patented adaptive intake interview technology (logic-branching system)

---

### AdvancedMD

**Core features**
- Patient portal: medical records access, lab results, visit history, bill pay
- Online appointment scheduling with automated reminders (email, SMS, voice)
- Bilingual reminders (English and Spanish) with automatic language routing
- Secure patient-to-provider messaging via portal
- Health alerts and follow-up reminders (screening, chronic care)
- Pre-visit intake forms with EHR pre-population
- Patient-facing appointment confirmation links embedded in reminder messages

**Differentiating features**
- Fully integrated within AdvancedMD PM/EHR suite — no separate system for engagement
- Built-in bilingual support (English/Spanish) with preference-driven automatic routing
- All engagement data flows directly into the clinical record without manual import

**UX patterns**
- Portal-centric model: portal serves as the hub for all patient self-service
- Automated reminder confirmation links reduce front-desk confirmation calls
- Health alerts are linked to clinical workflows inside the EHR

**Integration points**
- Native integration within AdvancedMD EHR and practice management
- Third-party EHR integrations limited (best suited for AdvancedMD practices)

**Known gaps**
- Engagement features are subordinate to the EHR/PM suite; limited standalone value
- No AI-driven outreach or campaign personalization
- Two-channel reminders (English/Spanish); multilingual support does not extend further
- Analytics are practice-level; no population health or benchmark reporting

**Licence / IP notes**
- Proprietary commercial SaaS
- Engagement features are part of the integrated AdvancedMD suite licensing

---

### Actium Health (CENTARI)

**Core features**
- Dual propensity modeling: clinical (medical needs) + behavioral (engagement likelihood) models
- Intelligent Audience Generator (IAG): AI-driven, continuously updated patient list building
- CRM intelligence platform (CENTARI) for health system outreach campaign management
- Outbound AI-driven voice call agents for patient activation
- Machine learning on EMR + claims + third-party datasets
- Bias-mitigation controls to prevent demographic/socioeconomic skew in outreach prioritization
- Predictive analytics dashboards for service line growth and care gap closure

**Differentiating features**
- Dual propensity modeling (clinical + behavioral) is unique in the market
- IAG eliminates manual list-building — audiences update in real time based on clinical events
- Acquired by Syllable Corporation, adding voice AI depth to the propensity modeling platform
- Demonstrated 4–8x better outreach outcomes versus conventional rule-based approaches
- Case study: academic medical center generated $39M additional revenue via AI-driven outreach

**UX patterns**
- Health system marketing and care management team-facing platform
- Campaign builder UI with AI-generated audience segments
- Reporting dashboards oriented around service line revenue and quality measure performance

**Integration points**
- EMR data ingestion (Epic, Cerner, and others)
- Claims data feeds from payers and clearinghouses
- Third-party social determinants and consumer data enrichment

**Known gaps**
- Enterprise health system focus; not suited to small/mid-size independent practices
- No patient-facing portal or direct patient UI
- Messaging execution requires integration with separate communication platform
- Less emphasis on portal activation or two-way patient communication

**Licence / IP notes**
- Proprietary commercial SaaS
- Acquired by Syllable Corporation (2025)
- Propensity modeling and IAG technology is proprietary

---

### Epic MyChart

**Core features**
- Comprehensive patient portal: lab results, imaging, medication list, visit summaries, care plans
- Online appointment scheduling, cancellation, and rescheduling
- Secure patient-provider messaging (inbox)
- E-check-in (pre-visit digital verification from home)
- MyChart Central: single Epic ID across multiple organizational portals
- In-app wayfinding (blue-dot navigation in care facilities, November 2025 release)
- Emmie AI assistant for scheduling, billing inquiries, and navigation
- Prior authorization status tracking via patient-facing API
- Video visit integration
- Prescription refill requests

**Differentiating features**
- MyChart Central federated identity system is the only cross-organization portal unification solution at scale
- Installed base: deployed at the majority of large US health systems, creating network effects
- Emmie AI assistant is EHR-native with access to full longitudinal clinical record
- In-app wayfinding (blue-dot) addresses a long-standing patient friction point at scale

**UX patterns**
- Portal-centric model with heavy emphasis on longitudinal record transparency
- Push notifications via MyChart app drive return engagement without staff action
- E-check-in flow parallels airline check-in UX (familiar mental model for patients)

**Integration points**
- Native integration with Epic EHR (full bidirectional)
- Open@Epic FHIR APIs for third-party developer access
- Apple Health, Google Health integrations for wearable/device data
- Prior authorization APIs (payer-facing)

**Known gaps**
- Requires Epic EHR deployment; not available as a standalone product
- Portal activation rates remain in the 40–60% range across Epic deployments
- Messaging inbox creates staff inbox management burden at scale
- Non-Epic providers cannot participate without Epic relationship

**Licence / IP notes**
- Proprietary; bundled with Epic EHR licensing
- Open@Epic provides FHIR-compliant APIs under developer program terms
- No open-source components

---

### Salesforce Health Cloud (Agentforce Health)

**Core features**
- Unified Patient 360: clinical + claims + social determinants + behavioral data in one profile
- Omnichannel outreach orchestration (email, SMS, voice, web, app push)
- Care gap closure campaigns with data-driven patient targeting
- Longitudinal journey management and lifecycle messaging
- Real-time care team collaboration and task delegation
- Agentic AI (Agentforce): AI agents for scheduling, triage, adherence, and member services
- Integration with EHRs, payers, and third-party data sources
- Configurable rule and workflow engine for complex care management programs
- Payer-provider hybrid organization support

**Differentiating features**
- Salesforce CRM foundation provides the most mature campaign management and journey orchestration of any platform
- Agentforce rebranding signals a full commitment to agentic AI embedded in the engagement layer
- Patient 360 with social determinants integration enables the most contextually rich engagement
- Suited to payer-provider hybrid organizations and large multi-site health systems where no other platform competes

**UX patterns**
- Enterprise CRM-style UI: dashboards, campaign builder, journey maps
- Clinician and care coordinator collaboration via shared task and note feeds
- Patient communication is orchestrated rather than message-centric

**Integration points**
- Salesforce ecosystem: MuleSoft for EHR/payer data integration
- FHIR R4 data model support
- Third-party data enrichment (social determinants, consumer data)
- EHR integrations via MuleSoft connectors (Epic, Oracle Health, etc.)

**Known gaps**
- Enterprise-only pricing; not accessible to practices below large health system scale
- Implementation complexity and customization burden is very high
- Not optimized for clinical workflow-embedded engagement (vs. CRM-layer campaigns)
- No native intake or scheduling product; depends on EHR integrations for clinical triggers

**Licence / IP notes**
- Proprietary commercial SaaS (enterprise licensing)
- Agentforce AI capabilities are proprietary to Salesforce

---

### Medplum

**Core features**
- Open-source FHIR R4/R4B server and developer platform
- HIPAA-compliant and SOC 2 Type II certified infrastructure
- FHIR-native data model for patient, clinical, and administrative resources
- OWASP-compliant security with penetration testing
- REST and GraphQL APIs for all FHIR resource types
- Subscription-based event triggers for workflow automation
- Access control via SMART on FHIR and role-based permissions
- TypeScript/React UI component library for rapid portal development
- 150+ open source contributors

**Differentiating features**
- Only HIPAA-compliant open-source FHIR platform in the market
- Full FHIR R4 compliance enables interoperability with any FHIR-native system
- SMART on FHIR auth enables standard EHR app launch integration
- Provides the infrastructure layer on which a custom patient engagement platform can be built
- Developer-first: API-complete, no vendor lock-in, self-hostable

**UX patterns**
- Developer and builder-focused: provides primitives, not a finished product
- React component library accelerates UI development but requires engineering investment
- No opinionated engagement workflows; all workflows are custom-built on the platform

**Integration points**
- SMART on FHIR for EHR app launch (Epic App Orchard, Cerner App Market)
- US Core FHIR profiles for standardized data exchange
- Subscription webhooks for real-time event-driven integrations

**Known gaps**
- Not a finished patient engagement product; requires substantial engineering to build engagement features on top
- No out-of-the-box appointment reminders, campaigns, or patient communication modules
- Community support only for open-source tier; enterprise support requires paid plan

**Licence / IP notes**
- Open source under MIT licence
- Cloud-hosted managed service available under commercial terms
- No known patent encumbrances

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Multi-channel appointment reminders (SMS, email, voice) with configurable timing
- Two-way HIPAA-compliant secure messaging between patients and care team
- Patient self-scheduling (web or mobile, 24/7, no login required)
- Automated recall messaging for no-shows and lapsed patients
- Digital pre-visit intake forms with EHR data pre-population
- Post-visit patient satisfaction surveys
- Basic EHR integration for appointment and demographic sync
- Broadcast/bulk messaging for announcements and campaigns

### Differentiating Features
- AI-driven propensity modeling to prioritize outreach (Actium CENTARI, Salesforce Agentforce)
- Adaptive logic-branching intake interviews (Phreesia)
- Agentic AI for inbound call handling and scheduling (DoctorConnect ARIA, Relatient Dash Voice, TeleVox IVA)
- Federated patient identity across multiple organizations (Epic MyChart Central)
- Real-time multilingual conversation translation (TeleVox)
- Unified omnichannel conversation thread without portal activation requirement (Klara)
- Social determinants + clinical + claims unified patient profile (Salesforce Health Cloud)

### Underserved Areas / Opportunities
- **Digital equity tools**: No platform provides robust outreach optimization for low-connectivity or low-digital-literacy patient populations (elderly, rural, low-income). Voice and print fallback channels are rudimentary across all platforms.
- **Patient-controlled preference learning**: Most platforms use rule-based channel assignment; none learn individual channel and timing preferences from behavioral signals.
- **Longitudinal engagement analytics**: No platform provides cross-encounter engagement analytics tying engagement touchpoints to clinical outcomes (adherence, HbA1c, readmission rates).
- **Explainable AI outreach**: Actium's propensity models are the most mature, but transparency and patient-facing explanations of why they received outreach are absent across the market.
- **Open interoperability**: Most platforms are proprietary with bilateral EHR integrations. A FHIR-native open platform (Medplum-style) with built-in engagement tooling does not yet exist in the market.
- **Patient-reported outcomes (PRO) collection**: Validated PRO instruments (PROMIS, HOOS, KOOS, PHQ-9, GAD-7) are available in some platforms but rarely integrated into care workflow feedback loops.
- **Care plan adherence support**: Beyond reminders, no platform provides AI-driven coaching or behavioral nudging for complex chronic disease self-management.

### AI-Augmentation Candidates
- **Channel and timing optimization**: Replace rule-based reminder delivery with reinforcement learning that adapts to individual patient response history
- **Propensity-scored outreach prioritization**: Extend AI-driven list generation (currently enterprise-only) to small/mid-size practice scale
- **Intelligent intake pre-population**: Use LLM-assisted inference to pre-complete intake fields from available clinical data, reducing patient data-entry burden
- **Conversational AI for triage**: Replace IVR and basic chatbot flows with LLM-powered conversational agents that handle multi-turn clinical queries
- **Engagement analytics narrative generation**: Auto-generate plain-language summaries of engagement performance for practice administrators who lack analytics expertise
- **AI-assisted content personalization**: Personalize health education content and post-visit instructions to patient literacy level, language, and condition profile

---

## Legal & IP Summary

No open-source-licensed components are present in the major commercial platforms (DoctorConnect, Klara, TeleVox, Relatient, Solutionreach, Phreesia, AdvancedMD, Actium Health, Epic MyChart, Salesforce Health Cloud). All are proprietary commercial SaaS products. Phreesia holds patents on its adaptive logic-branching intake interview technology, which would need to be designed around in any competing implementation. Epic's Open@Epic developer program provides FHIR API access but does not confer any rights to replicate MyChart functionality. Medplum is the only MIT-licensed open-source platform in the space and provides a legally clean foundation for building on top of. No specific patent conflicts were identified for building a new engagement platform that avoids replicating Phreesia's specific intake interview branching approach. FHIR, SMART on FHIR, HL7 standards, and HIPAA compliance frameworks are open standards. Use of standard OAuth 2.0, OpenID Connect, and FHIR R4 is unrestricted.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Multi-channel appointment reminders (SMS, email) with configurable timing and two-way confirmation/cancellation
- HIPAA-compliant two-way secure messaging between patient and care team
- Digital pre-visit intake forms with logic branching and EHR pre-population
- Patient self-scheduling (web-based, 24/7, no portal account required)
- EHR bidirectional integration via FHIR R4 APIs (appointment, patient, observation resources)
- Post-visit satisfaction survey with automated delivery and basic response reporting

**Should-have (v1.1)**
- AI-driven channel and timing personalization based on patient engagement history
- Broadcast messaging with audience segmentation (by condition, provider, location, demographics)
- Automated recall and no-show re-engagement messaging
- Patient portal with lab results, visit summary, medication list, and care team contact
- Patient-reported outcome (PRO) collection using validated instruments (PHQ-9, GAD-7, PROMIS)
- Engagement analytics dashboard with no-show rate, portal activation, message response, and campaign conversion metrics

**Nice-to-have (backlog)**
- AI propensity scoring to prioritize care gap outreach across a patient population
- Real-time multilingual translation for patient messages
- Agentic AI receptionist for inbound scheduling and FAQ handling
- Patient care plan adherence coaching with behavioral nudging
- Social determinants of health data integration for equity-aware outreach
- Cross-organization patient identity federation (for multi-site deployments)
