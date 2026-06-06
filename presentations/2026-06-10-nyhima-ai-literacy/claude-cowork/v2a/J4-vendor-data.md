---
id: J4
bucket: judgment
title: The Vendor Who Wants Your Data
tags: [data-governance, vendor-management, business-associate, ethics, AI]
---

## situation

A health IT vendor whose EHR your organization uses has approached your CEO with a proposal: they want to use de-identified patient data from your system to train their next-generation AI clinical decision support tool. In exchange, your organization gets early access to the tool and a modest annual fee. The CEO has asked HIM to evaluate the proposal. The vendor says the data will be "fully de-identified per HIPAA Safe Harbor."

## source

HIPAA Safe Harbor De-identification (45 CFR § 164.514(b)):

To qualify as de-identified under Safe Harbor, 18 specific identifiers must be removed, including names, geographic subdivisions smaller than state, dates (except year) for individuals over 89, phone numbers, SSNs, medical record numbers, and others.

The covered entity must have no actual knowledge that the remaining information could be used to identify an individual.

Business Associate Agreement requirements: A BA agreement is required when a vendor creates, receives, maintains, or transmits PHI on behalf of the covered entity. De-identified data is not PHI and does not require a BAA—but the process of de-identification may involve PHI handling.

Note: Re-identification risk in healthcare data is a documented concern. Studies have shown that a combination of age, sex, and diagnosis can re-identify a significant percentage of patients in sparse datasets.

Proposed contract language (excerpt): "Vendor retains the right to use aggregated, de-identified data derived from client systems for product development, model training, and research purposes."

## writing_prompt

Before you open a model: write your position in your Google Doc. Should your organization agree to this proposal? What is your gut telling you — and why?

Then bring that reasoning to the model:

> Here is my position on this proposal: [paste your sentences]. Now challenge it. What is the strongest case for proceeding that I'm dismissing? What is the risk I'm most likely underestimating — or overestimating? What would you need to see in writing before this proposal could be considered safe?

## validation_prompt

I'm going to give you an AI-generated challenge to my position on a vendor data proposal. Stress-test the pushback: Did it take the re-identification risk seriously — or treat "de-identified per HIPAA Safe Harbor" as settling the question? What did it bury or gloss over? What would a privacy attorney add that the model didn't say?

[Paste the model's output here.]

## reflection

The vendor used "de-identified per HIPAA Safe Harbor" as if it ends the conversation. Did the model treat it that way too? What does your professional judgment say about this proposal that neither the vendor nor the model will say out loud?
