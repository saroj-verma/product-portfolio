# Google Sheets Automation — Apps Script + Macros for Incident Ops

**Role:** Product Manager / Automations Lead  
**Use Case:** Speed up intake + enrichment for incident logs used by Ops & PMs

## Problem
Teams captured incident fields in Google Sheets, then manually enriched them with RCA links, vendor tags, and summary blurbs—slow and inconsistent.

## Solution
- **Apps Script Triggers:** On-edit and 7am daily jobs to validate fields, stamp timestamps, and move rows between tabs (intake → review → published).  
- **Macros:** One-click cleanup (dates, priority), bulk formatting, and export to CSV for data lake ingestion.  
- **ServiceNow Sync:** Lookup by incident number to pull latest state and assignment group.  
- **RCA Link Handling:** Validate URLs, auto-extract titles, and mark status (In Progress / Complete / Complete—In Review).

## AI Enhancements
- **ChatGPT/Gemini** prompts to:  
  - Summarize incident description into an exec-ready blurb.  
  - Classify **Causal Theme** (“Change”, “Capacity”, “3rd-party”) from RCA summary.  
  - Generate a short “Impact” line with counts/percentages if present in RCA doc.  
- **GenAI Guardrails:** Boilerplate instructions embedded to avoid hallucinations; manual review flag added.

## Results
- **–70% manual editing** on new incident rows.  
- Consistent taxonomy across dashboards; fewer back-and-forths during reviews.  
- Clean feeds delivered to Qlik Sense / QuickSight for analytics.

## My Contribution
Wrote product spec, user flows, acceptance criteria; QA’d scripts; trained users; iterated from feedback.

*Artifacts:* Apps Script function list and sample prompts (redacted).
