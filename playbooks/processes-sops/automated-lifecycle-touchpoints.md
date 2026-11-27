# Automated Lifecycle Touchpoints (HubSpot / Salesforce)

> **Purpose:** A scalable, trigger-based customer communication and internal alerting architecture designed to eliminate manual follow-up gaps across 300+ accounts, accelerate onboarding milestones, surface early churn signals, and protect renewal runway.

---

## Lifecycle Trigger & Automation Matrix

| Lifecycle Stage | Behavioral / CRM Trigger | Automated Action & Channel | Owner & Guardrails |
| :--- | :--- | :--- | :--- |
| **Onboarding Kickoff** | Deal status = `Closed-Won` + Kickoff not scheduled within 72 hours | Automated reminder email sent to Champion with CSM scheduling link + Slack alert to CSM | CSM reviews before send for Enterprise tier |
| **First Value Milestone** | Core workflow or integration active + < 50% licensed seats activated by Day 14 | Targeted role-based enablement guide triggered via HubSpot/Salesforce sequence | Auto-suppressed if open SEV-1/SEV-2 ticket exists |
| **Adoption Drop-Off** | Weekly active usage drops ≥ 25% over 14 days OR key admin inactive for 21 days | Internal CRM risk task created + automated check-in prompt queued for CSM | Health score automatically decremented by 15 pts |
| **Executive QBR Prep** | 75 days post-launch (and every 90 days thereafter) | Internal QBR prep task triggered 14 days prior + executive agenda preview sent | CSM customizes ROI metrics prior to send |
| **Renewal Runway** | Contract Renewal Date = `T-120 Days` and `T-90 Days` | Renewal forecast task created in Salesforce/HubSpot + value summary outreach triggered | Auto-escalates to CS Leadership if health score = Red |

---

## Governance & Suppression Rules

* **Support Ticket Suppression:** All marketing, NPS, and automated adoption sequences automatically pause whenever an account has an open `SEV-1` or `SEV-2` escalation in Zendesk.
* **Frequency Caps:** Customers receive no more than one automated lifecycle email every 10 business days to prevent alert fatigue.
* **Segment Routing:** SMB accounts receive fully automated digital touchpoints with self-serve resources, while Mid-Market and Enterprise triggers route through CSM task queues for personalized executive outreach.
* **Closed-Loop Attribution:** Reply rates, milestone completion, and post-touchpoint usage lifts are tracked in CRM dashboards to refine sequence timing quarterly.
