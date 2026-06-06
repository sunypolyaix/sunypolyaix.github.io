---
id: r1-r2-link-map
type: facilitator-reference
title: Round 1 → Round 2 Data-to-Document Links
event: NYHIMA Workshop · June 7, 2026
purpose: >
  For each Round 1 data file, identifies the most productive Round 2 document
  pairing, the bridging question, and the judgment hook that points forward.
  Use to guide tables toward relevant documents after Round 1 debrief.
---

# Round 1 → Round 2 Link Map

Each entry follows the same structure:

> **Data file** — what it shows  
> **Bridge question** — what it can't answer alone  
> **→ Primary document** — what that document clarifies or complicates  
> **→ Secondary document** — alternate path  
> **Judgment hook** — what remains unresolved after both rounds

---

## Complications and Deaths

**What Round 1 shows:** Which NY hospitals have mortality and complication rates
worse, better, or no different than national benchmarks. Lower Estimate / Higher
Estimate columns bracket each score.

**Bridge question:** If this hospital's complication rate is worse than expected —
is that a clinical reality, or a documentation failure?

**→ Primary: 42 CFR § 482.24** — § 482.24(c)(4)(iv) explicitly requires
"documentation of complications" and "hospital acquired infections" as mandatory
record content. If a complication isn't documented, it can't be coded; if it isn't
coded, it won't appear in this data. The federal floor for what a record must contain
is three pages long. A hospital can be CoP-compliant and still have documentation
that makes complication coding unreliable.

**→ Secondary: VUMC Documentation Standards** — the institutional ceiling. Compare
what CMS requires (§ 482.24) to what VUMC requires (H.2: all diagnoses treated,
principal diagnosis identified, procedures, condition at discharge). The gap between
floor and ceiling is where documentation quality lives.

**Judgment hook:** The data can't tell you whether a high complication rate reflects
real patient harm or a coding shop that documents aggressively. Which would you
rather have your hospital accused of? J1 (physician who won't document) sits exactly
here.

---

## FY 2026 Hospital Readmissions Reduction Program

**What Round 1 shows:** Which NY hospitals are in excess readmission territory
(ratio > 1.0) for which of six conditions (AMI, COPD, CABG, HF, hip/knee,
pneumonia), and what the payment penalty exposure is.

**Bridge question:** A readmission reduction vendor has access to your discharge
data and claims to be helping. What can they actually do with that data?

**→ Primary: Model Business Associate Agreement** — Section 2 permits use "as
reasonably necessary to provide services." Section 14 states data stewardship does
not confer ownership rights. But Section 2.B also permits use for "proper management
and administration" with "reasonable assurances" from third parties. A vendor
analyzing discharge summaries to train a readmission prediction model may argue that
falls under healthcare operations. The BAA as written may not stop them.

**→ Secondary: HIPAA Policy Manual** — Section 5.1 (permitted uses for payment and
health care operations). The insurance companies requesting "complete medical records"
to adjudicate readmission determinations are making a payment-purpose request. The
minimum necessary standard applies. Does "complete records" satisfy minimum necessary
for a readmission determination? The Policy Manual says you may reasonably rely on
the requestor's representation — but you are not required to.

**Judgment hook:** The payment penalty is public. The discharge summary that explains
why the patient came back is PHI. A plaintiff's attorney, a journalist, and a payer
all want the same document for different reasons and under different rules. J4 (vendor
who wants your data) is the forward look.

---

## FY 2026 HAC Reduction Program

**What Round 1 shows:** Which NY hospitals have high rates of hospital-acquired
conditions (CLABSI, CAUTI, SSI, CDI, MRSA), their Total HAC Score, and whether
CMS is reducing their payment.

**Bridge question:** HAI data flows from the hospital to NHSN (the CDC's infection
surveillance system). NHSN is a business associate. If something goes wrong with
that transmission, who is responsible — and to whom?

**→ Primary: Breach Notification Rule** — The four-factor risk assessment governs
whether an impermissible disclosure constitutes a reportable breach. Factor 3
("whether PHI was actually acquired or viewed") and Factor 4 ("extent to which
risk has been mitigated") are the operative questions when HAI data is involved
in an incident. The Rule's 60-day notification timeline runs from discovery.

**→ Secondary: Model Business Associate Agreement** — Section 5 requires the
business associate to notify the covered entity no later than 30 days after
discovery of a breach. The BAA is stricter than the Rule. If NHSN discovers an
unauthorized access on day 1 and notifies the hospital on day 45, the hospital
has met the Rule but the BAA has been violated. Those are different problems.

**Judgment hook:** The patient-level data feeding into the HAC score is PHI.
The published HAC score is not. At what point does a determined researcher
re-identify a patient from a combination of public quality data? P4 (breach
notification clock) runs the four-factor test on a simpler scenario. This one
is harder.

---

## HVBP Total Performance Score

**What Round 1 shows:** Each NY hospital's Total Performance Score and the
four domain breakdown: Clinical Outcomes, Safety, Patient/Community Engagement,
Efficiency. Which domain is dragging each hospital's score.

**Bridge question:** The Patient/Community Engagement domain is built from
HCAHPS survey data. HCAHPS data flows between hospitals, survey vendors, and CMS.
What rules govern whether that flow is compliant?

**→ Primary: Information Blocking Exceptions Fact Sheet** — The Manner Exception
and Fees Exception govern how actors must fulfill data exchange requests. A hospital
that delays sharing HCAHPS results with its regional HIE may be technically meeting
its CMS reporting obligation while simultaneously blocking information that would
improve care coordination — and its score. The IB Exceptions fact sheet is where
the distinction between legitimate non-disclosure and information blocking lives.
The model will list the nine exceptions correctly. It will struggle to apply them.

**→ Secondary: E/M Coding Guide** — The Clinical Outcomes domain includes mortality
and readmission measures that depend on E/M coding accuracy. CareOregon's policy:
if the E/M code submitted exceeds the level supported by documentation, they will
recover payment. If that recovery happens at scale across a hospital's patient
population, it affects the spending data that feeds the Efficiency domain.

**Judgment hook:** A hospital with a low VBP score has a financial incentive to
improve quality metrics. The data is public. What they do with the patient-level
data to improve those metrics — contracting vendors, sharing records, implementing
AI tools — is governed by BAAs and the information blocking rule. J4 is the
judgment scenario here.

---

## CMS PSI 6 Decimal

**What Round 1 shows:** Patient Safety Indicator rates at six decimal precision
for NY hospitals: pressure ulcers (PSI-03), iatrogenic pneumothorax (PSI-06),
postoperative PE/DVT (PSI-12), postoperative sepsis (PSI-13), and others.

**Bridge question:** PSI-12 (postoperative PE/DVT) fires when a PE is coded as a
complication — which depends on whether the Present on Admission (POA) indicator is
"N." If the physician documents "PE" without specifying onset, who makes the call?

**→ Primary: ICD-10-CM Guidelines** — The POA indicator rules are explicit: POA "N"
means the condition was not present at admission. The ICD-10 guidelines govern
how coders assign POA when documentation is ambiguous. If the clinical documentation
doesn't clearly establish onset, the coder must query the physician. If no query
is sent, a default may be assigned. That default determines whether PSI-12 fires.
The model will explain the POA rules correctly. It will not explain what happens
when documentation quality prevents the rules from being applied.

**→ Secondary: VUMC Documentation Standards** — Section H.2 (Discharge Summary)
requires identification of "all diagnoses treated" and a "principal diagnosis."
Section H.6 (Operative Report) requires documentation of "complications, if any,
including notating 'none' if no complications occurred." That documentation is the
evidence base for the PSI coding decision.

**Judgment hook:** A hospital's high PSI-12 rate could mean patients are developing
postoperative clots, or it could mean coders are properly capturing complications
that other hospitals are missing, or it could mean documentation is so ambiguous
that POA defaults are landing on "N" incorrectly. The data alone cannot tell you
which. That distinction requires expertise the model will not spontaneously produce.
D2 (coding accuracy audit) is the data scenario that parallels this.

---

## Unplanned Hospital Visits

**What Round 1 shows:** Which NY hospitals have more or fewer return visits than
expected, and the raw count of patients who returned within 30 days by condition.

**Bridge question:** Preventing those returns requires contacting patients after
discharge. Who is calling, what PHI are they using, and under what authority?

**→ Primary: HIPAA Policy Manual** — Section 5.1 distinguishes treatment, payment,
and health care operations uses of PHI. A follow-up call to a heart failure patient
3 days post-discharge is a care coordination activity. Whether it's a treatment
use (generally permitted, minimal restriction) or a healthcare operations use
(minimum necessary standard applies) determines what information the coordinator
can access and discuss. The Policy Manual's Section 5.5 covers this distinction.

**→ Secondary: Breach Notification Rule** — The coordinator uses a list generated
from discharge records. If that list is emailed to the wrong address — the exact
scenario in P4 — the four-factor breach analysis applies. How many patients are
on that list? What PHI is included? Was it encrypted? Those are the operative
questions before the 60-day clock starts.

**Judgment hook:** J2 (record request that worries you) puts this in sharp relief:
the same patient whose return visit is counted in this data may be the patient
requesting their psychiatric notes post-discharge. The right to access PHI and
the care coordination use of PHI exist simultaneously, with different rules.

---

## Healthcare Associated Infections

**What Round 1 shows:** CLABSI, CAUTI, CDI, SSI, and MRSA Standardized Infection
Ratios (SIR) for NY hospitals. Below 1.0 = better than expected. Above 1.0 = worse.

**Bridge question:** This data was generated by patient-level PHI transmitted to
NHSN. The SIR is public. The underlying data is not. What obligations come with
holding and transmitting that data?

**→ Primary: Model Business Associate Agreement** — NHSN operates as a business
associate of the covered entity for HAI reporting. Section 7 (subcontractor
requirements) requires NHSN to have BA agreements with any subcontractors who
handle that PHI. Section 3 (safeguards) requires appropriate administrative,
physical, and technical safeguards. Section 12 (books and records) gives HHS
the right to inspect. A hospital that signed an NHSN data use agreement signed
something that functions as a BAA. Most did not read it as carefully as this
template requires.

**→ Secondary: Breach Notification Rule** — The HAI data involves highly sensitive
clinical information (MRSA, C. diff infections) about identifiable patients at
the record level. Any impermissible disclosure is presumed to be a reportable
breach unless the four-factor risk assessment demonstrates low probability of
compromise. The published SIR alone cannot be used for re-identification. But
combined with admission dates, demographics, and unit assignments, it might be.
That's Factor 1 of the risk assessment.

**Judgment hook:** A plaintiff's attorney in a hospital-acquired infection
malpractice case wants the NHSN data your hospital submitted. It's PHI. The
published SIR they already have. What do you produce under subpoena, and does
the BAA with NHSN say anything about that?

---

## Timely and Effective Care

**What Round 1 shows:** ED throughput times, sepsis bundle compliance (SEP-1),
vaccination rates, and process-of-care measures for NY hospitals.

**Bridge question:** The physician seeing a septic patient in the ED has 30 minutes
to initiate the bundle. The documentation supporting the E/M code for that visit
must reflect the complexity of MDM. How does documentation time interact with
clinical time when both are measured?

**→ Primary: E/M Coding Guide** — CPT codes 99281–99285 for ED visits use MDM only
(no time-based coding). The guide states that to determine MDM level, two of three
elements must be met: number/complexity of problems, amount/complexity of data
reviewed, and risk of complications. A septic patient in the ED satisfies all
three at the highest level. But if the physician's documentation doesn't explicitly
capture the data reviewed or the risk assessment — the code may not be supported,
and CareOregon (or any payer) may recover payment. Documenting for quality measures
and documenting for billing are the same act performed under different pressures.

**→ Secondary: VUMC Documentation Standards** — Section H.15 governs ED
documentation: pertinent history, diagnostic orders, clinical observations,
diagnostic impression, disposition. Timeliness: within 24 hours. A hospital with
poor SEP-1 compliance may have excellent documentation after the fact; the bundle
measure cares about what happened within the time window, not what was charted
the next morning.

**Judgment hook:** J3 (AI note in the chart) lives here. An ambient AI
documentation tool generating a sepsis note that includes a clinical inference
the physician didn't make is a documentation error inside a time-sensitive billing
and quality reporting context. The False Claims Act exposure is not hypothetical.

---

## Hospital General Information

**What Round 1 shows:** NY hospital star ratings (1–5), hospital type and ownership,
and counts of measures where each hospital is performing better, no different, or
worse across five domains.

**Bridge question:** A hospital with three stars and multiple "worse" measures has
a record behind every one of those measures. What is the federal minimum that record
must contain?

**→ Primary: 42 CFR § 482.24** — The CoP for medical records is the floor below
every quality measure. § 482.24(c)(4) lists minimum content: H&P, admitting
diagnosis, consultations, complications, HAIs, informed consent, all orders, and
discharge summary with final diagnosis within 30 days. That last requirement is
the one most often breached. D1 (discharge completion data) quantifies exactly
how often. The star rating may be measuring documentation quality as much as
clinical quality.

**→ Secondary: VUMC Documentation Standards** — This is the ceiling. Comparing
the federal floor (§ 482.24) to an institutional high-standard policy (VUMC)
shows what "compliant" means vs. what "good" means. A hospital can satisfy
§ 482.24 and still have records that don't support accurate quality measurement.

**Judgment hook:** Hospital ownership type is in this file. A government-owned
hospital, a for-profit chain, and a nonprofit academic center all hold the same
CMS minimum documentation requirements. But their governance, their resources,
and their incentives differ enormously. Star ratings don't account for those
differences. Should they? That's the broader argument of the workshop — and
of the June 9 talk.

---

## Maternal Health

**What Round 1 shows:** Cesarean birth rates (PC-02), severe maternal morbidity
(PC-07), and episiotomy rates for NY hospitals, with a sample size column.

**Bridge question:** A patient who experienced severe maternal morbidity during
delivery wants her complete medical record. What does she have an absolute right
to — and what can be withheld?

**→ Primary: HIPAA Policy Manual** — Section 8.2 (right of access): individuals
have the right to access PHI in the designated record set, generally within 30 days.
Grounds for denial are narrow. The physician's delivery notes, operative reports
for a C-section, anesthesia records, and postpartum documentation are all in the
designated record set. If a patient at a hospital with a high SMM rate is requesting
that record, she almost certainly gets it. The Policy Manual also covers what must
be in the written denial if access is refused — and what that patient's rights are.

**→ Secondary: 42 CFR § 482.24** — § 482.24(c)(4)(v) requires "properly executed
informed consent forms for procedures and treatments." A C-section is a surgical
procedure. The informed consent form is part of the medical record. If it's missing
or inadequate, that's a CoP deficiency — and potentially evidence in a malpractice
case.

**Judgment hook:** J2 (the record request that worries you) is explicitly about
psychiatric records post-suicide attempt. The maternal health scenario is the
parallel: a patient requesting records after a traumatic delivery. The same
HIPAA framework governs both. The physician's request to withhold psychiatric
notes "because releasing them poses a risk of harm" does not apply here —
the maternal records don't qualify for the endangerment denial. J2 is the hard
case. This one isn't.

---

## Medicare Hospital Spending Per Patient

**What Round 1 shows:** MSPB ratio for NY hospitals: the ratio of actual spending
per episode (3 days pre-admission through 30 days post-discharge) to expected
spending. Above 1.0 = more expensive than expected.

**Bridge question:** A payer that processes your MSPB claims sees a pattern of
higher-than-expected E/M coding levels. They want to audit. What documentation
standard do they apply?

**→ Primary: E/M Coding Guide** — CareOregon's policy is explicit: if the E/M
code submitted is higher than the level the documentation supports, they will
adjust reimbursement, deny the claim, or recover prior payments. The MSPB ratio
is an aggregate of thousands of E/M coding decisions. A hospital above 1.0 may
have higher-complexity patients — or may have a coding culture that systematically
up-codes. The documentation is the only way to tell. CareOregon is an Oregon payer;
NY payers have the same authority.

**→ Secondary: Model BAA** — CMS aggregates spending data across all episodes to
calculate the MSPB ratio. Section 1.D of the BAA defines "Data Aggregation" as
combining PHI from multiple covered entities for analyses that relate to Health
Care Operations. CMS performing MSPB calculations is a form of data aggregation.
The Model BAA permits this — but the scope of what CMS can do with that aggregated
data, including publishing it, is a question the BAA doesn't fully resolve.

**Judgment hook:** The MSPB ratio is publicly available. The claim-level data that
produced it is not. A hospital's compliance team knows their MSPB is high and
suspects E/M upcoding. Investigating requires accessing PHI to audit coding
accuracy. That investigation is a health care operations use — permitted. But who
conducts it, and what happens to what they find?

---

## Outpatient Imaging Efficiency

**What Round 1 shows:** Which NY hospitals overuse contrast CT for abdominal
imaging (OP-10), order MRI for low-back pain without prior conservative treatment
(OP-8), and order cardiac stress imaging after low-risk procedures (OP-32).

**Bridge question:** When is imaging medically necessary, and where in the record
does that justification have to appear?

**→ Primary: E/M Coding Guide** — Ordering or interpreting a diagnostic test cannot
be included in the E/M MDM calculation when the interpretation is billed separately.
This creates a structural question: a physician who orders a CT and interprets it
bills twice. The E/M coding guide governs one half of that transaction. Whether
the imaging was necessary at all depends on the diagnosis documented in the office
visit that generated the order. A vague ICD-10 diagnosis code ("abdominal pain,
unspecified") may not justify the contrast CT that was ordered.

**→ Secondary: ICD-10-CM Guidelines** — The diagnosis code documented must support
the medical necessity of the imaging. Outpatient coding guidelines require the
highest level of certainty documented. If the physician documents "rule out
malignancy" as the indication, the coder cannot code malignancy — they code the
symptom. If the symptom code doesn't meet the payer's criteria for contrast CT,
the claim is denied. The imaging efficiency data is the aggregate outcome of
thousands of those documentation-to-coding-to-billing chains.

**Judgment hook:** A hospital with high contrast CT overuse has a radiology
department ordering imaging that a quality measure flags as potentially unnecessary.
Who has responsibility for that pattern — the ordering physician, the radiologist,
the coder, the CDI team, or HIM? The E/M guide says the documentation must support
the service. The ICD-10 guidelines say the code must reflect the documentation.
Neither says who is responsible when both are technically compliant but the
aggregate pattern is wrong.

---

## Employee Handbook (JHM Intrastaff)

**What Round 1 shows:** This document doesn't pair directly with a single data file —
it's the document that connects to any finding that raises a question about who
was working when the quality metric was generated.

**Bridge question:** A temporary nurse employed through a staffing agency had access
to 200 patients' records during her assignment. She's gone. What obligations followed
her out the door — and who enforces them?

**→ Primary: HIPAA Policy Manual** — Section 9.1 (HIPAA Officials) and Section 9.3
(Sanctions) govern workforce members, including contractors and temps. The Policy
Manual applies to "all workforce members within the City designated health care
component." Workforce includes volunteers and trainees, not just employees. A temp
placed through JHM Intrastaff is a workforce member for HIPAA purposes. The
handbook is how the agency extends those obligations — it is a compliance instrument
in HR clothing.

**→ Secondary: Model BAA** — JHM Intrastaff is itself a business associate of the
hospitals where it places workers. The BAA governs the relationship between
the agency and the covered entity. Section 7 requires the BA to ensure subcontractors
agree in writing to the same restrictions. A temp worker receiving PHI access is
a form of subcontractor arrangement.

**Judgment hook:** hvbp_tps Patient/Community Engagement scores reflect patient
experience, which is shaped partly by frontline staff behavior. If a hospital's
patient experience scores dropped after a merger that increased temp staffing,
is that a quality problem, a HR problem, or a compliance problem? The handbook
says: all three, simultaneously, in different sections.

---

## DME Guide

**What Round 1 shows:** NY Medicaid DME coverage criteria and HCPCS codes for
durable medical equipment, prosthetics, and orthotics.

**Bridge question:** A patient discharged after hip/knee replacement needs specific
DME to recover safely. If the discharge summary doesn't document the medical
necessity — or documents it wrong — who bears the consequence?

**→ Primary: 42 CFR § 482.24** — § 482.24(c)(4)(vii) requires a "discharge summary
with outcome of hospitalization, disposition of case, and provisions for follow-up
care." The DME order is part of the disposition. If the discharge summary doesn't
support the medical necessity of the prescribed DME, the DME supplier cannot
bill Medicaid — and the patient may not receive the equipment.

**→ Secondary: Complications and Deaths data** — COMP_HIP_KNEE in this file shows
surgical complication rates for hip/knee replacement. Patients in this cohort are
the primary recipients of the orthotic, prosthetic, and mobility equipment in the
DME guide. The connection: inadequate DME coverage post-discharge increases
complication and readmission risk, which feeds directly into COMP_HIP_KNEE and
HRRP scores. The documentation that supports the DME order and the documentation
that prevents a readmission are, in many cases, the same note.

**Judgment hook:** The DME guide lists specific documentation requirements for
each code — detailed limb measurements, clinical notes, plan of care. A hospital
HIM professional reviewing a discharge summary for DME support may find the
physician documented "needs walker" with nothing else. That's a Medicaid denial
waiting to happen. Who should have caught it — the coder, the CDI specialist,
the discharging physician, or the case manager? J1 (physician who won't document)
ends here.
