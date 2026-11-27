# Tiered Escalation & Incident Workflow

> **Purpose:** A structured cross-functional escalation framework designed to triage critical customer issues, establish clear severity SLAs, align Customer Success, Support, and Engineering, and protect account trust during high-stakes incidents.

---

## Severity Classification & SLA Matrix

| Severity Level | Definition & Business Impact | Initial Response SLA | Customer Update Cadence | Primary Owners |
| :--- | :--- | :--- | :--- | :--- |
| **SEV-1 (Critical)** | Complete production outage, data integrity risk, or severe security/compliance blocker with no workaround | **< 30 minutes** | Every **60 minutes** until mitigated | Incident Commander (Eng) + Senior CSM + Support Lead |
| **SEV-2 (High)** | Major workflow degradation impacting core daily operations or blocking an active go-live / renewal milestone | **< 2 hours** | Every **4 business hours** | Tier-2 Support + Assigned CSM |
| **SEV-3 (Medium)** | Partial feature defect or non-blocking workflow friction with a verified temporary workaround | **< 1 business day** | Every **48 business hours** | Tier-1/2 Support + CSM (async monitoring) |
| **SEV-4 (Low / Enhancement)** | Cosmetic UI issue, minor documentation gap, or net-new product feature request | **< 2 business days** | Monthly / Quarterly roadmap sync | CSM (logged in Product Feedback tracker) |

---

## End-to-End Escalation Execution Loop

1. **Triage & Reproduction (0–30 Mins):** Verify reproduction steps, affected user scope, error logs, and account ARR/renewal context in Zendesk and Salesforce/HubSpot before paging Engineering.
2. **Severity Assignment & Ticket Linking:** Tag the support ticket with the appropriate SEV level, link it to the Jira engineering issue, and alert the dedicated Slack escalation channel (`#cs-escalations`).
3. **Executive & Customer Framing:** CSM takes ownership of external stakeholder communication—translating technical root-cause updates into clear business impact and realistic timelines.
4. **Workaround & Mitigation Deployment:** Coordinate temporary operational workarounds with the customer's technical lead while Engineering deploys a permanent patch.
5. **Post-Incident Resolution & RCA:** Once resolved, deliver a formal Root Cause Analysis (RCA) summary for SEV-1/SEV-2 events and update the account's health score and QBR risk log.

---

## Executive Incident Update Template

> **Subject:** [SEV-1/SEV-2 Update] [Issue Summary] — [Customer Organization]
>
> Hi [Executive Sponsor / Champion Name],
>
> I am writing to share an update regarding **[Brief Issue Description]**, which our engineering and support teams are actively prioritizing.
>
> * **Current Status:** [Investigating / Root Cause Identified / Fix in QA]
> * **Business Impact & Scope:** [Specific workflow or user group affected]
> * **Active Mitigation / Workaround:** [Steps team can take right now, if applicable]
> * **Next Update:** You will hear from me directly by **[Time + Timezone]** with our next milestone update.
>
> Please reach out directly if you need to brief your internal leadership team in the meantime.
