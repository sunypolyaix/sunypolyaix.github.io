---
id: round1-exercise
type: participant
title: Round 1 — Working With Data
---

# Round 1 — Working With Data

In this round you take a real public dataset of New York hospitals, ask a model
to make sense of it, and turn what you find into a one-page memo you could send
to leadership. You will read the data, think about what it says, and write
something useful from it.

---

## Which model to use

**Use Gemini (free) — gemini.google.com**

For this round you want a model that can open a spreadsheet and actually do math
on it. Gemini's free version can run code on a file you upload, which means it
can count, sort, average, and chart real numbers instead of guessing at them.
That is what we need for data.

---

## Where to get the data

The Centers for Medicare & Medicaid Services (CMS) publishes hospital quality
data for free. You will download one file, filter it to New York, and upload it.

**Go to:** data.cms.gov/provider-data/dataset/xubh-q36u

That is the **Hospital General Information** dataset. Click the download button
to get the CSV file.

**A second option** (more focused, smaller): on the same CMS site, search for
**"Complications and Deaths — State"** and download `Complications_and_Deaths-State.csv`.
Either file works. Hospital General Information has star ratings and ownership
type, which makes for a richer story.

---

## How to filter to New York before uploading

The full file covers the whole country and may be large. Trim it to New York
first:

1. Open the CSV in Excel or Google Sheets.
2. Find the **State** column (it contains two-letter codes like NY, CA, TX).
3. Use **Data → Filter**, then filter that column to show only **NY**.
4. Copy the visible NY rows into a new sheet, or use **Save As** to export just
   the New York rows as a new CSV.
5. Name it something clear, like `ny-hospitals.csv`. Upload that file to Gemini.

Filtering first keeps the file small, keeps the model focused on New York, and
makes the free model faster and more reliable.

---

## The work — three moves

Do these in order, in the same Gemini conversation. Each builds on the last.

### 1. Read — understand what you have

> Here is a dataset of New York hospitals from CMS. Summarize the data
> structure. What patterns do you see?

Read the answer. Does it describe the columns correctly? Does anything surprise
you?

### 2. Think — find your story

Pick one angle, then ask:

> I want to tell a story about [New York's position / a regional comparison /
> star ratings by ownership type]. Help me think through what the data shows.

Choose the bracketed option that interests you, or write your own. Push back if
the model's first answer is thin — ask it to check the numbers.

### 3. Write — produce the artifact

> Generate a memo of no more than one page with a chart that tells this story to
> my hospital's leadership.

This is your artifact: a one-page memo with a chart, built from real data.

---

## End every round with the workbench prompt

When you have a memo you would actually use, paste this:

> Generate a markdown summary of what we did here, starting with my first
> prompt. Identify the questions I asked and how we arrived at the final
> product. Include the final artifact verbatim. I want to copy this into a
> Google Doc to share with colleagues.

Copy the result into a Google Doc. That is your record of this round.

---

## A note on file size and free limits

Free models have limits on how big a file they will accept and how much they
will process at once. If Gemini struggles, stalls, or says the file is too
large:

- Make sure you filtered to **New York only** before uploading.
- Drop columns you do not need before uploading — keep hospital name, city,
  ownership, star rating, and a few measures.
- Aim for a file under a few thousand rows. New York alone is well within that.

If the chart does not render, ask Gemini to describe the chart in words or give
you the numbers behind it — you can build the chart yourself in Excel.

*SUNY Poly AIX Center | sunypolyaix.github.io | tiny.cc/nyhima*
