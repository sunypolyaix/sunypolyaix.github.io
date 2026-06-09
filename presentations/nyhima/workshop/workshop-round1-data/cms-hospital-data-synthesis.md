---
title: CMS Hospital Quality Data — Synthesis for NYHIMA Workshop and Talk
date: 2026-06-06
type: data-synthesis
status: reference
project: nyhima-workshop
contributor: Steve
tags: [nyhima, cms, hospital-quality, data-synthesis, round1, directive-ai, workshop-materials]
source: claude-analysis
datasets:
  - Complications_and_Deaths-Hospital.csv
  - FY_2026_Hospital_Readmissions_Reduction_Program_Hospital.csv
  - CMS_PSI_6_decimal_file.csv
  - Healthcare_Associated_Infections-Hospital.csv
  - Maternal_Health-Hospital.csv
  - hospitals_file_inventory.csv
---

# CMS Hospital Quality Data — Synthesis for NYHIMA Workshop and Talk

Six CMS datasets uploaded June 6, 2026. This note synthesizes what is in them, what is usable for the workshop and talk, and what they surface about the challenge of reading data-driven outputs with professional judgment rather than deference.

---

## What the data is

The Centers for Medicare & Medicaid Services publishes hospital quality data through the Provider Data Catalog. The six files uploaded are a subset of that catalog, covering five quality domains and one inventory file that maps the full catalog. Together they represent the publicly available record of how American hospitals perform on safety, infection control, readmissions, patient safety incidents, and maternal outcomes — as measured, reported, and classified by CMS.

These are the same datasets participants work with in Round 1 of the workshop. They are real. They name real hospitals. The numbers carry real consequences: readmissions data determines Medicare payment penalties under the Hospital Readmissions Reduction Program; HAI data feeds the HAC Reduction Program; complications and deaths data feeds the Hospital Value-Based Purchasing program. A HIM professional working in quality reporting, compliance, or reimbursement touches this infrastructure daily, whether they know it or not.

---

## The five datasets

### 1. Complications and Deaths (95,840 rows / 161 NY hospitals / 20 measures)

The broadest of the five files. Covers 30-day mortality rates for AMI, heart failure, CABG, COPD, pneumonia, and stroke; complications rates for hip/knee replacement; pressure ulcer rates; perioperative pulmonary embolism; in-hospital fall fracture; postoperative sepsis; and the composite PSI-90 patient safety score.

**NY landscape.** Of 3,240 NY measure-hospital observations:

- 1,948 (60%) are rated "No Different Than the National Rate" — the modal outcome
- 658 (20%) are "Not Available" — data suppressed, usually small volume
- 321 (10%) are "Number of Cases Too Small" — below reporting threshold
- 122 (4%) are "Better Than the National Rate"
- 61 (2%) are "Worse Than the National Rate"
- 19 are "Worse Than the National Value" (composite measures use a different scale)

The distribution matters. Most hospitals cluster near the mean. The outliers — both better and worse — are the instructive cases, but they are a small fraction of the data. A model shown this file will pattern-match on the modal outcome and may underweight the tail.

**Selected NY hospitals rated worse than national:**

| Hospital | Measure | Score |
|---|---|---|
| Erie County Medical Center | Death rate among surgical inpatients with serious treatable complications | 240.42 |
| Canton-Potsdam Hospital | Death rate for pneumonia patients | 21.2 |
| Cayuga Medical Center at Ithaca | Death rate for pneumonia patients | 20.6 |
| Crouse Hospital | Death rate for pneumonia patients | 19.9 |
| Albany Medical Center Hospital | Death rate for stroke patients | 15.7 |
| CHSLI St Joseph Hospital | Hybrid all-cause risk standardized mortality rate | 5.1 |
| Cayuga Medical Center at Ithaca | Rate of complications for hip/knee replacement | 6.4 |
| Erie County Medical Center | Perioperative PE/DVT rate | 7.56 |
| Adirondack Medical Center | Pressure ulcer rate | 2.03 |

Several of these are rural or safety-net hospitals. The data does not explain why. That is the judgment gap — the number is not the story.

---

### 2. FY 2026 Hospital Readmissions Reduction Program (18,330 rows / 774 NY rows / 6 measures)

Covers 30-day readmission rates for pneumonia, heart failure, heart attack (AMI), CABG, hip/knee replacement, and COPD. The key derived metric is the **Excess Readmission Ratio (ERR)**: predicted rate divided by expected rate. ERR > 1.0 means more readmissions than expected given the hospital's patient mix; ERR < 1.0 means fewer. Hospitals with ERR > threshold face Medicare payment reductions.

**NY statistics (520 hospitals with reportable data):**

- Mean ERR: 1.00 (essentially at benchmark)
- Median ERR: 1.01
- Range: 0.58 to 1.33

NY hospitals perform close to the national expectation on average, but the range is substantial. An ERR of 1.33 means 33% more readmissions than expected — a meaningful quality and cost signal.

**NY hospitals with ERR > 1.1 (at-risk for penalty):**

| Hospital | Measure | ERR | Readmissions |
|---|---|---|---|
| St. John's Episcopal Hospital at South Shore | Pneumonia | 1.327 | 81 |
| Maimonides Medical Center | Pneumonia | 1.301 | 250 |
| Mount Sinai West | Hip/Knee | 1.260 | 27 |
| Mount Sinai South Nassau | Hip/Knee | 1.258 | Too few to report |
| NY Community Hospital of Brooklyn | Heart failure | 1.242 | 120 |
| Nyack Hospital | Hip/Knee | 1.225 | 11 |
| Richmond University Medical Center | Pneumonia | 1.213 | 78 |
| St. Joseph's Hospital Health Center | Heart failure | 1.207 | 142 |
| Staten Island University Hospital | Hip/Knee | 1.207 | Too few to report |
| South Brooklyn Health | Pneumonia | 1.198 | 139 |

Note "Too few to report" appearing alongside high ERRs. This is a known tension in the dataset: the ERR can be statistically volatile when volume is low. A model told "this hospital has an ERR of 1.26" without knowing volume may overread the number's precision.

---

### 3. CMS PSI-6 Decimal File (52,360 rows / 1,771 NY rows / 11 PSI measures)

Patient Safety Indicators are AHRQ-derived measures of in-hospital adverse events: pressure ulcers, iatrogenic pneumothorax (PSI-06), in-hospital fall fractures, postoperative hemorrhage, postoperative acute kidney injury, respiratory failure, PE/DVT, sepsis, wound dehiscence, abdominal puncture or laceration, and the composite PSI-90.

This file provides six-decimal precision rates — useful for actuarial and statistical work, visually overwhelming for most professional use.

**PSI-06 specifically: iatrogenic pneumothorax (collapsed lung caused by a medical procedure).** This is the measure that gave the file its name.

NY PSI-06 statistics (133 hospitals with reportable data):

- Mean: 0.210 per 1,000 at-risk discharges
- National mean: 0.211 — NY is essentially at benchmark
- Range: 0.085 to 0.397
- The national max is 0.636 — some outliers elsewhere are far above NY's range

**NY hospitals with highest PSI-06 rates:**

| Hospital | PSI-06 Rate |
|---|---|
| St. Mary's Healthcare | 0.397 |
| Elmhurst Hospital Center | 0.371 |
| Rochester General Hospital | 0.347 |
| Bellevue Hospital Center | 0.341 |
| Strong Memorial Hospital | 0.339 |
| Wynn Hospital | 0.335 |
| St. Joseph's Medical Center | 0.333 |

Several of these are high-volume academic or safety-net hospitals. Higher procedural volume — especially central line insertions, thoracentesis, and lung biopsies — directly increases PSI-06 exposure. The rate does not adjust for case mix in the same way mortality rates do. This is a data literacy point: what the number measures is not always what it appears to measure.

---

### 4. Healthcare-Associated Infections (172,512 rows / 5,832 NY rows / 36 measures)

The largest file. Covers six HAI categories: central line-associated bloodstream infection (CLABSI), catheter-associated urinary tract infection (CAUTI), surgical site infection following colon surgery (SSI-Colon) and abdominal hysterectomy (SSI-Hysterectomy), MRSA bacteremia, and Clostridioides difficile infection (CDI). For each, CMS reports a Standardized Infection Ratio (SIR) — observed cases divided by predicted cases — plus upper and lower confidence limits, device days or procedure counts, and a "compared to national benchmark" classification.

**NY benchmark distribution:**

- Not Available: 2,514 rows (43%) — suppressed or unreportable
- No Different than National Benchmark: 2,082 (36%)
- Better than the National Benchmark: 1,200 (21%)
- Worse than the National Benchmark: 36 (0.6%)

**NY hospitals worse than benchmark:**

| Hospital | Measure | SIR |
|---|---|---|
| Mount Sinai West | SSI - Abdominal Hysterectomy | 3.441 |
| Long Island Community Hospital | SSI - Colon Surgery | 3.085 |
| Maimonides Medical Center | CLABSI (ICU + select wards) | 1.609 |
| Kings County Hospital Center | SSI - Colon Surgery | (CI spans 1.024–4.633) |

A SIR of 3.4 means 3.4 times as many infections as predicted. That is not a rounding difference. For a hospital's infection control leadership, this is an operational emergency. For a HIM professional processing the quality reports that feed this data, understanding what goes into the SIR — numerator definitions, denominator eligibility criteria, risk-adjustment methodology — is not optional.

The 43% "Not Available" rate also matters. It does not mean those hospitals had no infections. It means their data did not meet reporting thresholds, was excluded for methodological reasons, or was not submitted. Absence of a number is itself information — and a model shown this data will not tell you that unprompted.

---

### 5. Maternal Health (17,959 rows / 591 NY rows / 4 measures)

Four measures:

- **PC-02**: Cesarean birth rate
- **PC-07a**: Risk-adjusted severe obstetric complications (all)
- **PC-07b**: Risk-adjusted severe obstetric complications (excluding blood transfusion)
- **SM-7**: Whether the hospital screens for maternal depression and other mental health conditions

**SM-7 is a binary yes/no measure.** For NY (153 facilities in the file):

- Yes: 101 hospitals
- Not Applicable (no inpatient labor/delivery): 37
- Not Available: 14
- No: 1

One NY hospital reported that it does not screen for maternal depression in a delivery setting. That is not a data anomaly — it is a policy position. The one hospital that answered "No" matters more than the 101 that answered "Yes."

**PC-02 and PC-07a/b are largely "Not Available" for NY** — most facilities either lacked sufficient volume, did not submit, or had their data suppressed. This is a common condition in maternal health data; obstetric volume is concentrated in a relatively small number of high-volume facilities, and the denominator requirements for risk-adjusted measures exclude many hospitals from reportable status.

This is the dataset with the highest proportion of missing data and the highest human stakes. The measures are about what happens to pregnant people during and after hospitalization. The gaps in the data are not neutral.

---

## The inventory file

The `hospitals_file_inventory.csv` is a map of the full CMS Provider Data Catalog as of this download — 75 files listed, covering every domain from HCAHPS patient experience surveys to value-based purchasing program scores to ASC (ambulatory surgical center) quality measures. It was generated to support efficient navigation of the catalog without downloading everything.

Key files not uploaded but available in the catalog that are relevant to this project:

- **Hospital General Information** (5,432 rows) — star ratings, ownership type, emergency services, bed count. This is the primary Round 1 dataset.
- **Timely and Effective Care** (138,173 rows) — ER wait times, sepsis bundle compliance, stroke care. Highly relevant to HIM workflow analysis.
- **HCAHPS** (325,856 rows) — patient experience. Connects to the human stakes dimension.
- **HVBP Clinical Outcomes, Safety, and Efficiency** — the value-based purchasing framework that ties many of these measures to payment.
- **FY 2026 HAC Reduction Program** (3,055 rows) — payment penalties linked directly to HAI performance.

---

## What this data surfaces for the workshop and talk

### For Round 1 (Data)

Participants are asked to take a CMS dataset, ask a model to make sense of it, and turn what they find into a one-page leadership memo. The datasets above give that exercise real texture:

The **Complications and Deaths** file is the richest for storytelling — it has a "Compared to National" column that lets a model quickly classify hospitals, it covers familiar outcome categories (mortality, pressure ulcers, complications), and the NY data includes enough variation to support multiple analytical angles. The Erie County Medical Center surgical mortality number (240.42 on in-hospital death among surgical inpatients with serious treatable complications) is the kind of outlier that stops a reader cold — and that invites the question of what the denominator is.

The **HRRP Readmissions** file is better for memo writing because the ERR is a single derived metric with a clear policy implication (ERR > 1 = penalty exposure). A participant can upload NY data, ask Gemini to sort by ERR descending, and produce a memo about readmissions penalty risk in fifteen minutes. The exercise works. The question is whether they push back on what the ERR actually measures.

The **HAI** file is harder — 172,000 rows, 36 measures, suppression everywhere. Better for demonstrating what "Not Available" means and why it matters than for producing a clean analytical artifact in 25 minutes.

### The data literacy points these datasets teach

Every file contains something a model will get wrong or misread if the participant doesn't push back:

**The ERR volatility problem.** Mount Sinai West has an ERR of 1.26 for hip/knee readmissions on 27 cases. That's a small-N ratio. A model will report it as a high-readmission hospital. A professional with population health literacy will ask: is this statistically meaningful? The confidence interval on 27 cases is wide.

**The missing data problem.** In HAI, 43% of NY rows are "Not Available." In Maternal Health, most PC-02 and PC-07 entries are suppressed. A model will analyze the available data and give you a finding. It will not tell you that the finding describes only the 57% of hospitals that met reporting thresholds, and that the missing 43% are not randomly distributed — smaller, rural, and safety-net hospitals are disproportionately missing.

**The denominator problem.** PSI-06 does not adjust for procedural volume the way mortality measures adjust for case mix. A high PSI-06 rate at a major academic medical center that performs thousands of central line insertions annually is not the same as a high PSI-06 rate at a community hospital. The rate is real. Its interpretation requires knowing what it measures.

**The composite problem.** PSI-90 is a composite of 11 individual PSIs. It is used in value-based purchasing calculations. A hospital can have a PSI-90 score "Worse Than the National Value" (composite) while having individually unremarkable scores on most components — because one PSI is driving the composite. A model told the PSI-90 score will not decompose it unless asked.

**The scale problem.** The Maternal Health SM-7 measure — are you screening for maternal depression? — is binary. The one hospital that answered "No" is the finding. A model summarizing the SM-7 distribution will report that 66% of NY hospitals said yes and 1 said no. The 1 is the story.

### For the Talk

The talk argument is that directive AI is already operating across HIM workflows before professionals engage with it. These datasets are the upstream of that argument. Before a coding suggestion appears in an EHR, before a quality alert fires in a dashboard, before a readmissions risk score surfaces in a care management tool — this data has been processed, modeled, and embedded in the system. The HIM professional who cannot read these numbers is not just less analytically capable. They are less able to evaluate what the directive AI is doing with them.

The HRRP Readmissions data is the clearest example. CMS publishes the ERR. Hospitals receive payment adjustments based on it. Health systems build readmissions-reduction programs around it. Clinical documentation improvement (CDI) programs — a core HIM function — target the diagnoses and comorbidities that affect expected readmission rates, which is the denominator of the ERR. The chain from raw claim data to ICD-10 coding to risk-adjustment to ERR to payment penalty runs directly through HIM. A directive AI tool that flags records for CDI review is using logic built on this data. The professional who cannot read the data cannot evaluate the tool.

---

## Notes on data currency and provenance

All five datasets carry CMS measure dates. Key date ranges:

- Complications and Deaths: April 2021 – March 2024 (most measures)
- HRRP: July 2021 – June 2024
- PSI-6: July 2022 – June 2024
- HAI: July 2024 – June 2025 (most recent)
- Maternal Health: January 2024 – December 2024

The HAI data is the most current. The others reflect a lag of one to two years, which is typical for risk-adjusted quality measures — the denominator calculations require complete claims data, which arrives after a delay.

For workshop use: participants should understand that what they're looking at is a historical record, not a live dashboard. The hospital they're analyzing in the exercise may have already addressed — or worsened — whatever the data shows. That is not a limitation of the exercise. It is a feature: data is always historical, and professional judgment always operates on a lag.

---

## Files not included in this analysis

The inventory file lists 74 additional CMS files not uploaded. Notable absences for future workshop iterations:

- **Hospital General Information** — star ratings and ownership type, the richest storytelling dataset
- **HCAHPS** — patient experience, connects quality data to human experience
- **HAC Reduction Program FY 2026** — the payment consequence of HAI performance
- **Timely and Effective Care** — ER wait times and process measures, highly concrete for HIM audiences

These could extend the workshop's Round 1 data library, particularly if future iterations add a track focused on reimbursement or patient experience.

---

*SUNY Poly AIX Center · Steve Schneider · sunypolyaix.github.io*
