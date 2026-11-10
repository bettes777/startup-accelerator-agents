# RuralAI Triage — offline-first clinical triage assistant for nurse- & CHW-led rural primary care
*An explainable, offline-first AI + rules triage assistant that helps nurses and CHWs safely escalate urgent cases in low-connectivity rural clinics, designed for mixed paper/EHR workflows and procurement readiness.*

**Domain:** healthtech  
**Recommended funding stage:** Pre-seed → Pilot (prototype already underway or about to start)

## Pitch deck outline

### Slide 1: Cover / Hook
- Product: offline-first mobile triage assistant (hybrid rules + ML) for nurse- and CHW-led rural primary-care clinics.
- Primary value: reduce missed urgent cases, standardise escalation, and produce audit trails for procurement and ethics review.
- Why now: increasing attention to clinical AI validation, governance and practical offline tools in low-resource settings.
  - *Evidence:* M010 | Planner | plan (solution description and user flow); M049 | Research Agent | insight (offline-first app requirement); M052 | Research Agent | insight (need for clinical validation and governance)
  - *Contributed by:* Planner, Research Agent

### Slide 2: Problem — what rural clinics face
- Triage is often performed by lower-cadre staff (CHWs, nurses) who must identify and escalate urgent cases safely.
- Intermittent power/connectivity and mixed paper + EHR workflows make conventional cloud-first AI impractical.
- Poor manual-data quality and rising regulatory/ethics scrutiny undermine clinician trust and procurement decisions.
  - *Evidence:* M054 | Research Agent | insight (target customer: small rural primary-care clinics); M049 | Research Agent | insight (intermittent power/connectivity, offline-first requirement); M064 | Research Agent | insight (risk: poor data quality); M052 | Research Agent | insight (regulatory/ethical scrutiny)
  - *Contributed by:* Research Agent, Planner

### Slide 3: Solution — how the assistant works
- User flow: CHW/nurse opens offline app → guided form (complaint + vitals) → hybrid rules + on-device model → explainable recommendation (manage, urgent refer, emergency) → printed/SMS referral and audit log.
- Design choices: deterministic rules + ML for explainability, versioned decision logs, local encrypted storage, background sync.
- Interoperability: manual entry, CSV import, minimal API to fit mixed-paper/EHR environments.
  - *Evidence:* M010 | Planner | plan (user flow and decisions supported); M013 | Planner | plan (data & privacy approach); M050 | Research Agent | insight (flexible ingestion for mixed paper + EHR)
  - *Contributed by:* Planner, Research Agent

### Slide 4: Clinical scenarios & inputs
- Representative scenarios: acute febrile illness (red flags), suspected pneumonia (RR, SpO2, danger signs), maternal triage (antenatal danger signs).
- For each scenario the app lists required inputs, decision logic, action and an auditable explanation.
- Minimal sensor needs: optional pulse oximeter; core operation requires only basic Android device and manual inputs.
  - *Evidence:* M010 | Planner | plan (typical clinical scenarios); M051 | Research Agent | insight (task-shifting and CHW integration)
  - *Contributed by:* Planner, Research Agent

### Slide 5: Product architecture & security
- Offline-first mobile client with local encrypted store, background sync and a lightweight cloud backend for aggregate analytics and model updates.
- Auditability: versioned rules/models, time-stamped logs and consent capture at point-of-care to satisfy ethics/procurement reviewers.
- Security: local encryption, transport encryption on sync, configurable data residency (local-only or centralised) depending on district policy.
  - *Evidence:* M014 | Planner | plan (technical architecture & interoperability); M013 | Planner | plan (data & privacy approach); M052 | Research Agent | insight (validation, governance requirements)
  - *Contributed by:* Planner, Research Agent

### Slide 6: Deployment & operational model (devices, training, support)
- Minimum on-site tech: basic Android phones/tablet per clinic, battery backup (powerbanks/solar), optional pulse oximeter device per site.
- Support model: 1–2 day on-site training for clinicians/CHWs + job aids, district supervisor onboarding, remote support and scheduled on-site refreshers.
- Operations: local device management, periodic model/rule updates via background sync, supervisor dashboards for QA and feedback loops.
  - *Evidence:* M014 | Planner | plan (minimal device/IT requirements and on-site training/support); M049 | Research Agent | insight (offline-first necessity)
  - *Contributed by:* Planner, Research Agent

### Slide 7: Compact pilot protocol summary
- Design: 2–6 rural clinics (or one CHW program covering similar catchment) over 6 months to demonstrate safety, feasibility and procurement-readiness.
- Primary endpoint: reduction in missed urgent cases (operational definition to be finalised with clinical lead and ethics board). Secondary endpoints: change in referral rate, time-to-referral, data completeness, clinician adherence to recommendations, patient follow-up outcomes.
- Data collection: app encounter logs, paper register cross-checks, supervisor audit forms, and post-encounter follow-up phone calls. Field research officers collect and upload de-identified data. Outcomes adjudication: blinded clinical review panel reviewing de-identified encounter records and referral outcomes.
  - *Evidence:* M076 | Funding Advisor | funding (pilot framing: measurable clinical impact; 2–6 clinics); M010 | Planner | plan (pilot use and validation); M052 | Research Agent | insight (ethics/regulatory expectations and audit trails)
  - *Contributed by:* Funding Advisor, Planner, Research Agent

### Slide 8: 6–12 month timeline with milestones & go/no-go gates
- Month 0–1: finalise protocol, secure MOUs/LOIs with pilot sites, submit ethics/regulatory application.
- Month 2–3: device procurement & configuration, on-site training, baseline data collection.
- Month 4–9: pilot operations and iterative improvements; ongoing M&E and data collection.
- Decision gates: after 3 months operational data review — go/no-go if (a) data completeness >= target threshold, (b) no safety signal in blinded review, (c) minimum clinician uptake/adherence met. Final scale decision at pilot end based on pre-specified primary endpoint and procurement-readiness metrics.
- Time horizon: pilot 6 months typical; extended 9–12 months if ethics approvals or procurement trials require longer follow-up.
  - *Evidence:* Peer feedback (Funding Advisor) — requested timeline & gates; M076 | Funding Advisor | funding (pilot framing and procurement-readiness); M013 | Planner | plan (ethics & M&E needs)
  - *Contributed by:* Funding Advisor, Planner

### Slide 9: Funding asks — 3 realistic scenarios & itemised use-of-funds (model figures — verify)
- Scenario A – Small proof-of-concept grant (6 months): focused on 2 clinics to show basic safety and feasibility. (Suggested ask: model knowledge - verify: USD 40k–80k).
- Scenario B – Standard pilot grant (9 months): 4 clinics, full M&E, ethics submission and modest device procurement. (Suggested ask: model knowledge - verify: USD 120k–250k).
- Scenario C – Larger district pilot / scale-readiness (12 months): 6 clinics, stronger implementation support, procurement readiness work and district engagement. (Suggested ask: model knowledge - verify: USD 300k–600k).
- Itemised use-of-funds (major lines; unit costs are illustrative — model knowledge - verify): device procurement (Android tablet/phone @ USD 100–300 each; pulse oximeter @ USD 20–70 each); product dev & QA (feature dev, on-device model tuning) — person-months; field ops (local field officer salary or per-diem, travel & allowances); on-site training & refresher sessions (trainer days, materials); M&E/data collection & analysis (field data officers, statistician, monitoring tools); ethics/regulatory fees and translation; IT/data-security/compliance work (encryption, secure hosting, SOC-like checklist); overhead (institutional/admin) and 10–15% contingency.
- All dollar figures and unit costs are model knowledge - verify; founder must confirm local device/pricing, salary scales, ethics fees and procurement timelines before applying.
  - *Evidence:* Peer feedback (Funding Advisor) — requested funding scenarios, itemised use-of-funds and cost lines; M076 | Funding Advisor | funding (funding framing); M014 | Planner | plan (device & dev costs implied by deployment needs)
  - *Contributed by:* Funding Advisor, Planner

### Slide 10: Which funder type for which instrument
- Foundation / public-health grant: proof-of-concept grant to cover pilot ops, M&E and ethics (short-term non-dilutive). Target ask: Scenario A or B depending on scope.
- Accelerator / implementation partners: non-dilutive support + mentorship and procurement introductions; useful for procurement-readiness and district introductions (Scenario B).
- District / Ministry procurement contract or innovation fund: scoped pilot procurement contract to embed the tool in routine workflows (Scenario C; aim to demonstrate procurement-readiness metrics required by buyer).
- Seed investors / angels (dilutive): pursue only after pilot demonstrates measurable impact and procurement interest — use for product scaling, commercialisation and hiring (next-stage ask estimated separately).
- Founder action: map each funder approach to a concrete ask and required deliverables (e.g., foundation grant to cover pilot ops & M&E for X months; accelerator cohort to cover implementation support & introductions).
  - *Evidence:* M076 | Funding Advisor | funding (recommended funder types and narrative); M015 | Planner | plan (procurement and pilot-to-scale routes)
  - *Contributed by:* Funding Advisor, Planner

### Slide 11: Procurement-readiness metrics, buyer economics & partner commitments
- Procurement-readiness metrics to demonstrate in pilot: per-facility and per-patient cost estimates (model knowledge - verify), clinician time-savings (minutes per encounter saved), escalation/referral accuracy targets, data completeness threshold (e.g., % of required fields captured), and safety (no increase in missed urgent cases).
- Buyer economics to articulate: expected per-patient cost vs current pathway, operational savings from faster referral, supervisor time-savings from digital audit trails and reduction in unnecessary referrals.
- Partner commitments: plan to secure MOUs/LOIs from pilot clinics and a district health office before applications; show signed LOIs in appendix. (Founder to obtain and insert MOUs/LOIs).
  - *Evidence:* Peer feedback (Funding Advisor) — requested procurement-readiness metrics and MOUs/LOIs; M015 | Planner | plan (buyer economics & procurement pathways)
  - *Contributed by:* Funding Advisor, Planner

### Slide 12: Team, next-stage funding triggers & verification note
- Team asks: clinical lead, product/tech lead, field ops/pilot lead, data security officer — list current bios and key hires required for pilot.
- Next-stage funding: after a successful pilot (meeting primary endpoint and procurement interest), consider seed/angel raise to scale product dev, expand to more districts and recruit commercial/business development staff. Estimated next-stage ask and runway should be prepared after pilot; figures here would be model knowledge - verify.
- Important: always verify funder eligibility, award sizes and deadlines with funders themselves before applying — funding programs change often.
  - *Evidence:* M075 | Funding Advisor | funding (recommended stage: pre-seed → pilot); Peer feedback (Funding Advisor) — requested next-stage funding paragraph and verification note; M013 | Planner | plan (ethics & regulatory preparedness)
  - *Contributed by:* Funding Advisor, Planner

## Funding options to explore (verify before applying)

- **Foundations & Grand Challenge-style pilot grants (e.g., global health foundation proof-of-concept funds)** (Non-dilutive grant (foundation / challenge prize), Pre-seed → early pilot (prototype → small implementation)): Foundations commonly fund proof-of-concept and short operational pilots that de-risk clinical AI in low-resource primary care. Typical awards are pilot/proof-of-concept grants (6–18 months funding) or implementation grants that cover staff, local partnerships, and evaluation costs. Eligibility usually requires a clear health impact hypothesis, local partnerships (clinic/district/NGO), and an evaluation plan. Submission timelines vary by foundation but expect periodic calls (2–4 month application windows) and 3–6 month review cycles. *Source: model knowledge - verify. Foundations and challenge funds differ greatly by program; confirm each program's eligibility criteria, award sizes, budgets allowed for evaluation, and application deadlines on the funder's site before applying.*
- **District / ministry pilot procurement (local government pilot funding or digital health innovation units)** (Public procurement / pilot (government-run pilot funding), Pre-seed → Pilot → Implementation (proof-to-procurement pipeline)): Local health ministries or district health offices often run pilot procurement streams or innovation units that fund short pilots to test digital tools in a set of clinics. Typical awards are pilot contracts (3–12 month pilots) with in-kind commitments (clinic access, staff time) and sometimes small implementation budgets. Eligibility typically requires an MoU with the district/clinic leadership, alignment with national primary-care priorities, and data governance safeguards. RFPs and pilot calls align with budget cycles and can have long lead times (3–9+ months). *Source: model knowledge - verify. Procurement timelines and contracting requirements vary widely by country and district. Confirm procurement rules, pilot acceptance criteria and whether procurement includes purchase orders or just evaluation support.*
- **NGO and implementing-partner pilots (donor-funded program partnerships)** (Non-dilutive partnership + sub-award (NGO implementations), Pre-seed → Pilot → Scale via implementer networks): Large NGOs and implementers running donor-funded primary-care or CHW programs can run pilots or include tech partners as sub-grantees. Typical award types are subcontracts/sub-awards attached to existing donor programs (6–24 month pilots) and can lead to multi-district roll-outs if results are strong. Eligibility normally requires an operational partner with a history of implementing donor-funded programs and demonstrated capacity to manage human-subjects research if clinical validation is planned. *Source: model knowledge - verify. NGOs often require local staffing, M&E plans, and alignment with donor deliverables. Confirm partner interest, sub-award terms and whether the NGO's donor allows technology procurement or requires open-source solutions.*
- **Health innovation accelerators & intermediaries (accelerator cohorts, challenge-backed support)** (Accelerator / fellowship (hybrid: non-dilutive support + connections to procurement and investors), Pre-seed → Prototype → Pilot readiness): Accelerators focused on global health can provide small grants, mentorship, connections to pilot partners (ministries, NGOs), and investor introductions. Typical support: 3–6 month cohorts with seed grants, pilot introductions, and technical support. Eligibility is usually startup teams with a working prototype, clear pilot plan, and willingness to accept mentorship/cohort commitments. *Source: model knowledge - verify. Programs vary in what they offer (cash vs services) and in equity terms. Confirm whether support is non-dilutive, cohort dates, and pilot partnership facilitation specifics.*
- **Pre-seed angels, impact investors and early-stage healthtech VCs (convertible note/SAFE or small equity round)** (Dilutive funding (angel syndicates / seed VC), Pre-seed → Seed (to convert successful pilots into product development and regulatory readiness)): Investors with an interest in clinical AI or rural/LMIC health provide small pre-seed checks to cover expanded pilots, regulatory and validation work, and hiring. Common deal structures at pre-seed are convertible notes, SAFEs or small priced rounds. Investors expect milestones such as: working offline-capable prototype, pilot MoU or procurement agreement, preliminary clinical validation metrics, local partnerships, and a go-to-market pilot plan. Timelines to funding close vary but expect 2–4 months from first meetings to close for well-prepared teams. *Source: model knowledge - verify. Investor expectations and structure differ; confirm target investor thesis, typical check size, and expected milestones before outreach. Consider offering convertible instruments for speed and minimal dilution at pre-seed.*

## Gaps the founder should fill

- Local unit costs: exact device unit prices (tablets/phones/pulse oximeters) in target country(s) — needed to finalise budget.
- Local salary scales and per-diem/travel rates for field staff and trainers to finalise personnel lines.
- Baseline epidemiological metrics: current missed urgent-case rate, baseline referral rate and average clinic volumes to power sample size and set endpoint targets.
- Site-level commitments: signed MOUs/LOIs from 2–6 pilot clinics and a district health office to attach to funding applications.
- Country-specific ethics/regulatory submission fees and timelines to estimate lead time and costs.
- Precise next-stage funding target and runway needs post-pilot (founder inputs required).
- Any existing prototype metrics (usability, preliminary accuracy) and team bios to populate the Team/Ask slide.

## Open research questions

- Exact Ministry of Health procurement pilots, tender timelines and donor solicitations in chosen pilot districts — must be mapped locally.
- Device ownership and charging/infrastructure statistics for target facilities (percent of clinics with smartphones/tablets, charging availability).
- Local regulatory requirements and ethics review timelines for clinical AI in each proposed country.
- Data-sharing agreements, patient-consent norms, and legal constraints for reusing clinical data for model development in each country.
- Potential local implementation partners (NGOs, digital health implementers) and their capacity to support training and supervision.

## Final peer review

- Research Agent: not approved (3/5)
- Funding Advisor: not approved (2/5)