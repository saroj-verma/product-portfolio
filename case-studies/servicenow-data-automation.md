# ServiceNow → Data Lake Automation for Incident Analytics

**Role:** Product Manager / Sr. IT Business Analyst  
**Scope:** Incident data ingestion, quality, and self-serve analytics for Ops & Leadership  
**Timeline:** Multi-release; weekly increments

## Problem
Leaders lacked a trusted, timely view of incidents (P0–P3). Manual exports from ServiceNow were error-prone and delayed decisions.

## Objectives
- Reliable, near-real-time pipeline from ServiceNow.
- Standardized schema for QoQ/MoM reporting and RCA trending.
- Self-serve dashboards; reduce manual reporting work.

## Approach
1. **Source & Schema:** Defined canonical incident model (priority, service, caused CI, vendor, root cause, timestamps).  
2. **Pipelines:** Scheduled extracts (ServiceNow REST API) → landing in S3 → curated in **ODL Athena** with partitions for date/service.  
3. **Quality Gates:** DQ rules (nulls, enums, timestamp sanity, SLA fields), alerts via Slack/Jira when thresholds breached.  
4. **KPIs & Contracts:** MTTR, MTTD, repeat-incident %, vendor hot-spots, SEV heatmaps; published as a contract for downstream tools.

## AI & Analytics
- **ChatGPT / Gemini** APIs for: RCA summary drafts, “5-Whys” prompts, and exec one-pagers from incident text.  
- **NotebookLM** to synthesize historic RCAs and surface patterns during post-mortems.  
- **GenAI prompts** embedded in analyst playbooks to generate MoM/QoQ insights and anomaly callouts.

## Outcome
- **80% reduction** in manual reporting effort.  
- **<4h latency** from incident close to dashboard availability.  
- **–30% repeat incidents** (enabled by faster pattern detection and follow-through actions).

## Architecture (high level)
ServiceNow REST → S3 (landing) → Glue/Athena (curated) → BI (Qlik Sense / QuickSight) → Slack/Jira notifications.

## My Contribution
Product requirements, data contracts, acceptance tests, KPI definitions, DQ rules, and stakeholder alignment across Ops, Data, and Security.

*Artifacts:* sample data contract, DQ rule list, and dashboard screenshots (redacted).
