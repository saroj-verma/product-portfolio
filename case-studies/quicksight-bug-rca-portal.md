# Amazon QuickSight — Bug & RCA Tracking Portal (ODL Athena via S3)

**Role:** Product Manager / Sr. IT BA  
**Goal:** Centralize defects & RCAs with drill-downs for Engineering and Leadership

## Problem
Defect and RCA information lived in scattered tools (Jira, Confluence, spreadsheets), slowing prioritization and masking recurrences.

## Approach
- **Data Model:** Unified schema for bug metadata, severity, component, owner, RCA theme, fix/restore timestamps.  
- **Data Source:** Curated tables in **Athena** (fed from S3 pipelines) joined with Jira exports.  
- **QuickSight Dashboards:**  
  - Drilldowns by service/vendor/asset.  
  - MTTR by theme, recurrence rate, “aging” defects.  
  - RCA library—searchable, filterable, exportable.

## AI Features
- **LLM Summaries (ChatGPT/Gemini):** One-click RCA executive summary; risk level and recommended next actions.  
- **GenAI Insight Cards:** Auto-generated “What changed this month?” and “Top 3 hotspots” cards.  
- **Natural-Language Q&A:** Prompt box for “Show RCAs for banking incidents last quarter with MTTR > 3h.”

## Outcome
- **–60% time** to prep RCA reviews.  
- **Faster prioritization:** weekly bug triage dropped from 90→45 minutes.  
- **Improved prevention:** clear recurrence tracking and owner follow-ups.

## My Contribution
Product spec, UX (wireframes), KPI design, security review, and adoption playbook for teams.

*Artifacts:* redacted dashboard views and PRD excerpt.
