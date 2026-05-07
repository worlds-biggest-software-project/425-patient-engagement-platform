# Patient Engagement Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source patient engagement layer that unifies appointment management, secure messaging, digital intake, and personalized outreach across every communication channel patients actually use.

Patient engagement is the strongest predictor of health outcomes, yet most practices still rely on fragmented, single-channel tools or enterprise systems priced far beyond the reach of independent and mid-size organizations. This project delivers a FHIR-native, HIPAA-compliant engagement platform that integrates bidirectionally with EHR systems to automate outreach, close care gaps, and reduce no-show rates -- without requiring patients to activate a portal or staff to manage a separate system.

---

## Why Patient Engagement Platform?

- **No-show rates remain at 20-30% nationally.** Digital reminder systems consistently demonstrate a 40% reduction in no-shows, but existing solutions lock this capability behind enterprise contracts or EHR-specific bundles (Epic MyChart, AdvancedMD) that exclude practices on other platforms.

- **Enterprise pricing excludes the majority of practices.** Salesforce Health Cloud, Actium Health CENTARI, and TeleVox target large health systems with enterprise pricing models. Independent practices, FQHCs, and behavioral health organizations -- the segments with the highest clinical need -- are underserved.

- **Incumbents are channel-limited, not truly omnichannel.** Most platforms specialize in one or two channels. DoctorConnect focuses on reminders; Klara on messaging; Phreesia on intake. No single open platform unifies reminders, messaging, intake, outreach campaigns, education, and surveys in one coherent layer.

- **AI capabilities are siloed at the enterprise tier.** Actium Health's propensity modeling and DoctorConnect's ARIA AI Receptionist are proprietary and available only to their respective customers. AI-driven personalization of channel, timing, and content should be accessible at every practice scale.

- **No FHIR-native open-source engagement platform exists.** Medplum provides a FHIR-compliant infrastructure layer but requires substantial engineering to build engagement features on top. Every other competitor is proprietary commercial SaaS with no open-source components.

---

## Key Features

### Appointment Management
- Multi-channel reminders (SMS, email, voice) with configurable cadence and two-way confirmation/cancellation
- Patient self-scheduling via web, 24/7, without portal account requirement
- Automated recall and no-show re-engagement messaging
- Procedure-specific pre-appointment instructions

### Secure Messaging and Communication
- HIPAA-compliant two-way asynchronous messaging between patients and care teams
- Staff inbox management with intelligent routing and SLA tracking
- Broadcast messaging with audience segmentation by condition, provider, location, or demographics
- Audit logging for all patient-staff communication

### Digital Intake and Forms
- Pre-visit digital intake (demographics, insurance, medical history, consent) with logic-branching question flows
- Intelligent pre-population from existing EHR record data
- Multi-language support for intake forms
- Real-time insurance eligibility verification during intake

### Outreach and Campaigns
- Configurable care gap closure campaigns (overdue screenings, wellness visits, chronic care follow-up)
- Post-visit follow-up and medication adherence messaging
- Health education content delivery personalized to patient literacy level and language
- Patient-reported outcome (PRO) collection using validated instruments (PHQ-9, GAD-7, PROMIS)

### Surveys and Analytics
- Post-visit CAHPS-aligned patient satisfaction surveys with automated delivery
- Engagement analytics dashboard: no-show rates, portal activation, message response rates, campaign conversion
- NPS collection with closed-loop follow-up workflows

---

## AI-Native Advantage

This platform replaces rule-based reminder scheduling with reinforcement learning that adapts channel, timing, and message content to each patient's demonstrated response patterns. AI-driven propensity scoring -- currently available only in enterprise platforms like Actium Health CENTARI -- is brought to practices of every size to prioritize care gap outreach by both clinical need and engagement likelihood. LLM-powered conversational agents handle inbound scheduling, FAQ resolution, and multi-turn clinical triage, reducing staff phone burden without the limitations of traditional IVR. Health education content and post-visit instructions are automatically personalized to the patient's literacy level, language, and condition profile.

---

## Tech Stack and Deployment

The platform is built on a FHIR R4-native data model, enabling bidirectional integration with any FHIR-compliant EHR (Epic, Oracle Health, athenahealth, eClinicalWorks, and others) via SMART on FHIR and standard OAuth 2.0/OpenID Connect authentication. Deployment supports self-hosted, cloud-managed, and hybrid configurations. SMS, email, and voice delivery integrate through standard gateway providers. The architecture follows the Medplum precedent of an MIT-licensed open-source core with optional managed cloud services, ensuring no vendor lock-in while providing a production-ready hosted option. All messaging and data handling is designed for HIPAA compliance with SOC 2-aligned security controls.

---

## Market Context

The global patient engagement solutions market was valued at approximately $23 billion in 2025 and is forecast to grow at a 17-20% CAGR through 2030, driven by value-based care incentives, consumerization of healthcare, and regulatory emphasis on patient-centered quality metrics (CAHPS, MIPS). The primary buyers span independent practices seeking no-show reduction and scheduling efficiency, value-based care organizations targeting care gap closure and chronic care adherence, and payers focused on reducing avoidable utilization. Incumbent pricing ranges from mid-market SaaS (DoctorConnect, Solutionreach) with opaque per-provider fees to enterprise platforms (Salesforce Health Cloud, Actium Health) requiring six-figure annual commitments.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
