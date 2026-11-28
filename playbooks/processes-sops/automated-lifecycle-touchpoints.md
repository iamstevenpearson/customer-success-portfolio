# Automated Lifecycle Touchpoints (HubSpot / Salesforce)

> **Purpose:** Build a scalable, trigger-based customer communication and internal alerting process that reduces manual follow-up gaps across large account portfolios, keeps onboarding milestones on track, identifies early signs of disengagement, and gives CSMs better visibility into upcoming renewals.

The goal is not to automate every customer interaction. It is to automate the reminders, signals, and routine touchpoints that help CSMs focus their time on conversations that require judgment and relationship management.

---

## 1. Lifecycle Trigger & Automation Matrix

| Lifecycle Stage | Trigger / Condition | Automated Action | Owner & Guardrails |
| :--- | :--- | :--- | :--- |
| **Onboarding Kickoff** | Deal marked `Closed-Won` and kickoff has not been scheduled within 72 hours | Create a CSM follow-up task and queue a kickoff scheduling email with the appropriate booking link | CSM owns follow-up. Enterprise communications are reviewed before sending |
| **First Value Milestone** | Core workflow or integration is active, but fewer than 50% of licensed seats are activated by Day 14 | Trigger a role-based enablement email or create a personalized outreach task with relevant training resources | CSM reviews account context before outreach. Suppress automated messaging during major support escalations |
| **Adoption Drop-Off** | Weekly active usage declines by 25% or more over a 14-day period, or a key administrator has been inactive for 21 days | Create an account risk task, flag the account for health-score review, and queue a CSM check-in | CSM validates the signal before changing account health status or contacting the customer |
| **Executive QBR Preparation** | 75 days after launch and every 90 days thereafter | Create an internal QBR preparation task 14 days before the target review date and remind the CSM to prepare an updated value summary | CSM validates adoption, business outcomes, open risks, and ROI metrics before sharing anything externally |
| **Renewal Runway** | Contract reaches 120 days and 90 days before its renewal date | Create renewal planning and forecast tasks, review account health, and prompt the CSM to prepare a value summary | CSM owns the renewal plan. Red accounts are escalated to CS leadership for additional review |

*Note: The timeframes and thresholds above are proposed operating guidelines. They should be adjusted based on product usage patterns, customer segments, contract terms, and actual team capacity.*

---

## 2. Governance & Suppression Rules

Automation should improve the customer experience, not create more noise. These rules help ensure that messages are relevant, appropriately timed, and consistent with the account's current situation.

- **Support Ticket Suppression:** Pause marketing, NPS, and automated adoption campaigns when an account has an unresolved SEV-1 or SEV-2 escalation in Zendesk. Route the account to its CSM for appropriate communication instead.

- **Communication Frequency:** Limit automated lifecycle emails to one per account every 10 business days. Allow critical service notifications and manually approved CSM communications to follow their own communication requirements.

- **Segment-Based Routing:** Use digital-first touchpoints and self-service resources for SMB accounts. Route Mid-Market and Enterprise triggers into CSM task queues so outreach can reflect account complexity, stakeholder relationships, and business priorities.

- **Enterprise Review:** Require CSM review before sending sensitive communications involving executive relationships, renewal risk, adoption concerns, or significant changes in customer engagement.

- **Data Quality:** Confirm that renewal dates, account ownership, lifecycle stages, user activity, and escalation status are accurate before triggering workflows. Missing or outdated CRM data should create a review task rather than generate an unreliable customer message.

- **Closed-Loop Attribution:** Track email engagement, replies, milestone completion, task completion, and subsequent product usage. Review performance quarterly to identify which touchpoints are helping customers progress and which need adjustment.

---

## 3. Workflow Ownership & Execution

| Function | Responsibility |
| :--- | :--- |
| **Marketing Operations / RevOps** | Configure workflows, maintain trigger logic, manage suppression rules, and monitor automation performance |
| **Customer Success** | Review account-specific alerts, personalize outreach, validate risk signals, and document customer follow-up |
| **Support** | Maintain accurate ticket severity and escalation status so suppression rules work correctly |
| **CS Leadership** | Review escalated accounts, monitor renewal exposure, and evaluate portfolio-level trends |

### CSM Follow-Through

An automated alert is a signal to take action, not proof that a customer is at risk.

When a workflow creates a task, the CSM should:

1. Review the account's recent activity and communication history.
2. Confirm that the trigger reflects a meaningful change.
3. Check for open support issues, stakeholder changes, or other context.
4. Decide whether the next step should be an email, call, enablement session, or internal escalation.
5. Record the action taken and update the account's health or lifecycle status when appropriate.

---

## 4. Automation Performance Metrics

Measure whether the workflows are improving execution and customer outcomes, not simply how many emails they send.

| Metric | What It Measures |
| :--- | :--- |
| **Onboarding Follow-Up Time** | Time between Closed-Won and the first meaningful CSM follow-up |
| **Milestone Completion Rate** | Percentage of accounts completing defined onboarding milestones on schedule |
| **Adoption Recovery Rate** | Percentage of flagged accounts that return to their previous or target usage levels |
| **CSM Task Completion** | Percentage of triggered tasks completed within the expected timeframe |
| **Renewal Preparation Coverage** | Percentage of upcoming renewals with a documented plan and current account assessment |
| **Engagement Rate** | Customer replies, meeting acceptance, and meaningful engagement following automated or CSM-assisted outreach |

The quarterly review should answer three questions:

- Are the right accounts being flagged?
- Are CSMs taking meaningful action after an alert?
- Are the workflows improving onboarding progress, adoption, engagement, and renewal readiness?

---

## 5. Operating Principle

**Automate the signal. Personalize the response.**

Use HubSpot and Salesforce to identify important customer milestones, surface changes in behavior, and keep follow-up from falling through the cracks. Keep the CSM responsible for interpreting the context, deciding what action makes sense, and maintaining the customer relationship.
