# Tiered Escalation & Incident Workflow

> **Purpose:** Establish a structured cross-functional escalation framework for triaging critical customer issues, defining severity-based response targets, aligning Customer Success, Support, and Engineering, and protecting customer trust during high-stakes incidents.

---

## 1. Operating Principles

An escalation is not simply a support ticket that requires additional attention. It is an opportunity to demonstrate ownership, transparency, and coordinated problem-solving.

The following principles guide the escalation process:

- **Acknowledge before investigating:** Customers should know their issue has been received and is being addressed.
- **Prioritize business impact:** Severity should reflect the customer's operational impact, not simply the technical complexity of the issue.
- **Establish clear ownership:** Every escalation needs a directly responsible owner and documented next steps.
- **Communicate proactively:** Customers should never have to repeatedly chase the team for updates.
- **Separate investigation from communication:** Engineering investigates and resolves technical issues while Customer Success translates progress into customer-relevant information.
- **Avoid unsupported commitments:** Never promise a resolution time or product fix that the responsible technical team has not confirmed.
- **Close the loop:** Resolution includes customer confirmation, documentation, and follow-up where appropriate.

**Core principle:** The customer should not have to manage the escalation internally. The CSM coordinates the relationship and keeps the customer informed while the appropriate technical teams work toward resolution.

---

## 2. Severity Classification & SLA Matrix

Severity is determined by the scope of the issue, operational impact, affected users, available workarounds, and urgency of the customer's business requirements.

| Severity Level | Definition & Business Impact | Initial Response Target | Customer Update Cadence | Primary Owners |
| :--- | :--- | :--- | :--- | :--- |
| **SEV-1 (Critical)** | Complete production outage, data integrity risk, or severe security/compliance blocker with no workaround. | < 30 minutes | Every 60 minutes until mitigated | Incident Commander (Engineering) + Senior CSM + Support Lead |
| **SEV-2 (High)** | Major workflow degradation impacting core daily operations or blocking an active go-live or renewal milestone. | < 2 hours | Every 4 business hours | Tier-2 Support + Assigned CSM |
| **SEV-3 (Medium)** | Partial feature defect or non-blocking workflow friction with a verified temporary workaround. | < 1 business day | Every 48 business hours | Tier-1/2 Support + CSM |
| **SEV-4 (Low / Enhancement)** | Cosmetic UI issue, minor documentation gap, or net-new product feature request. | < 2 business days | Monthly / Quarterly roadmap sync, as appropriate | CSM + Product Feedback Owner |

*These are recommended operating targets for an example escalation framework. Actual response and resolution commitments must align with the organization's support policies, contractual SLAs, staffing model, and coverage hours.*

### Severity Assignment Guidelines

Before assigning severity, assess:

1. **Business impact:** What customer operation or business objective is affected?
2. **Scope:** Is the issue affecting one user, a department, multiple locations, or the entire customer environment?
3. **Criticality:** Is the affected workflow essential to daily operations?
4. **Workaround availability:** Can the customer continue operating through an alternative process?
5. **Time sensitivity:** Is the issue blocking a launch, financial process, contractual obligation, or critical business deadline?
6. **Risk exposure:** Does the issue involve potential data loss, security, privacy, or compliance concerns?

Severity should be reassessed as new information becomes available. An issue initially classified as SEV-3 may become SEV-2 or SEV-1 if its scope or business impact increases.

### Important Distinction: Response vs. Resolution

- **Initial response:** Confirmation that the issue has been received and an appropriate team has begun assessing it.
- **Mitigation:** An action that reduces the immediate customer impact, potentially through a workaround.
- **Resolution:** The underlying issue has been corrected or otherwise addressed.
- **Customer confirmation:** The customer has validated that the affected workflow is functioning as expected, where practical.

An initial response target is not a guarantee that the issue will be resolved within that timeframe.

---

## 3. Escalation Ownership & Accountability

Clear ownership prevents duplicated work, conflicting customer messages, and situations where an issue is passed between departments without accountability.

| Function | Primary Responsibility |
| :--- | :--- |
| **Customer Success Manager** | Owns customer communication, business impact assessment, stakeholder alignment, and relationship continuity. |
| **Support** | Owns ticket intake, initial troubleshooting, reproduction steps, documentation, and technical triage. |
| **Engineering** | Owns technical investigation, root-cause identification, remediation, and engineering deployment. |
| **Incident Commander** | Coordinates major incident response, establishes priorities, tracks workstreams, and maintains internal incident alignment. |
| **Product Management** | Evaluates product defects, feature limitations, enhancement requests, and longer-term product implications. |
| **CS Leadership** | Provides executive oversight, supports strategic account recovery, and helps prioritize customer risk. |
| **Sales / Account Management** | Provides commercial context and supports renewal or expansion considerations when the incident creates revenue exposure. |

### CSM Ownership During an Escalation

The CSM remains accountable for the customer experience even when the technical issue is outside their direct control.

The CSM should:

- Understand the customer's business impact.
- Confirm the appropriate severity classification with Support and Engineering.
- Establish a primary customer communication channel.
- Identify affected customer stakeholders.
- Maintain a record of updates and commitments.
- Coordinate internal resources when additional attention is needed.
- Communicate verified information without speculating.
- Track customer sentiment and account health throughout the incident.
- Confirm follow-up actions after resolution.

**The CSM does not independently diagnose production systems, authorize technical fixes, or commit Engineering to delivery dates.**

---

## 4. End-to-End Escalation Execution Loop

### Step 1: Intake, Triage & Reproduction

**Objective:** Understand the issue, validate its impact, and establish an initial severity classification.

**Primary Owner:** Support

Recommended actions:

1. Acknowledge receipt of the customer issue.
2. Capture the customer's description of the problem.
3. Identify affected users, teams, workflows, and locations.
4. Document the time the issue began and whether it is ongoing.
5. Gather screenshots, error messages, logs, and reproduction steps where available.
6. Determine whether the issue affects production functionality.
7. Identify any available workaround.
8. Review account context in Salesforce or HubSpot, including ARR, renewal date, and strategic importance.
9. Assign an initial severity level.
10. Notify the appropriate internal teams.

**Expected outcome:** A documented incident with a preliminary severity classification, known business impact, and assigned owner.

### Step 2: Severity Assignment & Internal Coordination

**Objective:** Ensure the appropriate teams are engaged and working from the same information.

**Primary Owners:** Support Lead + Incident Commander, where applicable

Recommended actions:

1. Confirm the assigned severity.
2. Create or update the support ticket in Zendesk or the designated support platform.
3. Link the ticket to the corresponding Jira engineering issue when applicable.
4. Notify the designated escalation channel, such as `#cs-escalations`.
5. Identify the technical owner responsible for investigation.
6. Establish the internal communication cadence.
7. Confirm the next customer update deadline.
8. Document any outstanding technical questions or dependencies.

For SEV-1 incidents, activate the organization's major incident response process and assign an Incident Commander.

**Expected outcome:** A coordinated response with defined technical ownership, communication responsibilities, and next steps.

### Step 3: Customer & Executive Communication

**Objective:** Maintain trust through timely, transparent communication.

**Primary Owner:** Assigned CSM

The CSM should communicate:

- What is currently known.
- Which customer workflows or users are affected.
- What the team is doing to investigate.
- Whether a workaround is available.
- What the customer should do in the meantime.
- When the next update will be provided.

Communication should focus on business impact rather than unnecessary technical terminology.

**Example:**

Instead of:

"Our engineering team is investigating a database synchronization issue."

Communicate:

"Our team is investigating an issue affecting the synchronization of customer records. This may delay updates appearing in your dashboard. Engineering is actively reviewing the issue, and we'll share another update by [time and timezone]."

**Expected outcome:** The customer understands the issue, its known impact, and what happens next.

### Step 4: Workaround & Mitigation Deployment

**Objective:** Reduce business disruption while the technical team works toward a permanent resolution.

**Primary Owners:** Engineering + Support

Recommended actions:

1. Determine whether an approved workaround exists.
2. Validate the workaround with the technical team.
3. Communicate instructions to the customer.
4. Confirm whether the workaround restores essential functionality.
5. Monitor the issue for recurring failures.
6. Document any limitations or additional customer responsibilities.
7. Continue customer updates according to the severity matrix.

A workaround should never be presented as a permanent resolution unless the responsible technical team confirms that the underlying issue has been addressed.

**Expected outcome:** Customer impact is reduced while permanent remediation continues.

### Step 5: Resolution, Validation & Root Cause Analysis

**Objective:** Confirm the issue has been addressed and establish whether additional preventive action is required.

**Primary Owners:** Engineering + Support

Recommended actions:

1. Confirm the technical fix or remediation has been deployed.
2. Validate the affected workflow internally.
3. Coordinate customer validation when appropriate.
4. Confirm whether the workaround can be discontinued.
5. Update the support ticket and linked engineering issue.
6. Communicate the resolution to the customer.
7. Complete a Root Cause Analysis for applicable incidents.
8. Identify preventive actions and assign owners.
9. Update account health and the customer risk log.
10. Schedule a follow-up conversation if the incident materially affected the relationship.

**Expected outcome:** The incident is documented, the customer understands the resolution, and remaining risks have assigned owners.

---

## 5. Executive Incident Update Template

**Subject:** [SEV-1/SEV-2 Update] [Issue Summary] — [Customer Organization]

Hi [Executive Sponsor / Champion Name],

I am writing to share an update regarding **[Brief Issue Description]**, which our Support and Engineering teams are actively prioritizing.

**Current Status:** [Investigating / Root Cause Identified / Fix in Progress / Monitoring]

**Business Impact & Scope:** [Specific workflow, department, or user group affected]

**Actions Underway:** [What Support and Engineering are currently doing]

**Active Mitigation / Workaround:** [Steps the team can take right now, if applicable]

**Next Update:** You will hear from me directly by **[Time + Timezone]** with our next milestone update.

We understand the importance of [affected business process] to your team. We're coordinating internally to address the issue and will continue to keep you informed as we make progress.

Please reach out directly if you need to brief your internal leadership team in the meantime.

Best,  
[CSM Name]

---

## 6. Internal Escalation Communication Template

**Subject:** [SEV Level] [Customer Name] — [Issue Summary]

**Account Information**
- Customer:
- Account Owner:
- ARR / ACV:
- Renewal Date:
- Support Ticket:
- Engineering Issue:
- Incident Start Time:

**Incident Details**
- Issue Description:
- Affected Workflows:
- Number of Users / Teams Affected:
- Business Impact:
- Current Workaround:
- Severity Level:
- Reason for Severity Classification:

**Ownership**
- Incident Commander:
- Support Owner:
- Engineering Owner:
- Customer Communication Owner:
- Executive Escalation Contact:

**Current Actions**
- Investigation:
- Mitigation:
- Customer Communication:
- Outstanding Dependencies:

**Next Steps**
- Next Internal Checkpoint:
- Next Customer Update:
- Action Owner:
- Expected Follow-Up:

---

## 7. Customer Communication Standards

Customer communication should remain consistent throughout the incident, even when technical progress is limited.

### Communication Expectations

| Severity | Communication Standard |
| :--- | :--- |
| **SEV-1** | Provide an initial acknowledgment within the response target and updates every 60 minutes until mitigated. |
| **SEV-2** | Provide an initial acknowledgment within the response target and updates every 4 business hours. |
| **SEV-3** | Provide an initial acknowledgment within the response target and updates every 48 business hours while actively monitored. |
| **SEV-4** | Communicate through the appropriate product feedback or roadmap process, with updates during relevant monthly or quarterly reviews. |

### Communication Best Practices

- Use one primary customer-facing communication owner.
- Keep updates concise and factual.
- Explain the business impact in language the customer understands.
- Separate confirmed information from ongoing investigation.
- Do not speculate about root cause.
- Avoid assigning blame to internal departments or individuals.
- Never promise an unconfirmed fix or delivery date.
- Communicate when the next update will occur, even if there is no major change.
- Escalate communication to executive stakeholders when business impact warrants it.

If an update deadline cannot be met, the CSM should communicate that proactively rather than allow the customer to discover the delay.

---

## 8. Root Cause Analysis (RCA) & Post-Incident Review

SEV-1 and SEV-2 incidents should receive a formal Root Cause Analysis. Other incidents may warrant one when they are recurring, customer-impacting, or strategically significant.

### Recommended RCA Structure

| Section | Required Information |
| :--- | :--- |
| Incident Summary | Brief description of what happened. |
| Timeline | When the issue began, was identified, escalated, mitigated, and resolved. |
| Customer Impact | Affected users, workflows, business operations, and duration. |
| Root Cause | Confirmed technical or operational reason for the incident. |
| Resolution | Fix, remediation, or workaround implemented. |
| Contributing Factors | Conditions that increased the likelihood or severity of the issue. |
| Preventive Actions | Changes intended to prevent recurrence. |
| Action Owners | Individuals or teams responsible for follow-up. |
| Target Dates | Agreed completion dates for corrective actions. |

### Post-Incident Review Questions

1. How was the issue first identified?
2. Was severity assigned appropriately?
3. Were the right teams engaged quickly?
4. Did the customer receive timely and accurate updates?
5. Was the workaround effective?
6. Were there delays caused by unclear ownership?
7. Did the issue reveal a product, process, or documentation gap?
8. What preventive action will reduce the likelihood of recurrence?

The objective is to improve systems and processes, not assign blame.

---

## 9. Customer Recovery & Account Health Management

Resolving the technical issue does not automatically restore customer confidence.

The CSM should assess the relationship impact and determine whether additional recovery activity is necessary.

### Customer Recovery Framework

| Phase | CSM Action | Desired Outcome |
| :--- | :--- | :--- |
| **Acknowledge** | Recognize the disruption and its impact on the customer's business. | Customer feels heard and taken seriously. |
| **Stabilize** | Confirm the issue is resolved or sufficiently mitigated. | Customer can resume essential workflows. |
| **Rebuild Confidence** | Share verified findings, corrective actions, and follow-up commitments. | Customer understands what changed and what happens next. |
| **Reinforce Value** | Revisit business objectives and confirm the path forward. | Customer regains confidence in the partnership. |
| **Monitor** | Track sentiment, adoption, and remaining risks. | Relationship recovery is sustained. |

### Account Health Review

After a material incident, the CSM should review:

- Customer sentiment and executive confidence.
- Product adoption and usage patterns.
- Outstanding support issues.
- Implementation or operational delays.
- Renewal timeline and commercial exposure.
- Executive sponsor engagement.
- Open recovery commitments.

If the incident has materially affected the account, update the customer health score and document the reason for any change.

A resolved ticket should not automatically result in a healthy account status.

### Recovery Follow-Up

For significant incidents, schedule a customer follow-up to:

- Confirm that critical workflows are functioning.
- Review any remaining customer concerns.
- Explain completed corrective actions.
- Confirm ownership of outstanding commitments.
- Reestablish alignment around business objectives.

---

## 10. Escalation Triggers & Decision Matrix

Certain situations require escalation beyond the standard support process, even when the original technical issue appears manageable.

| Trigger | Potential Risk | Recommended Action |
| :--- | :--- | :--- |
| Production outage | Complete interruption of customer operations | Activate SEV-1 response and major incident coordination. |
| Potential data loss or integrity issue | Financial, operational, or compliance exposure | Immediately involve Engineering and appropriate security or compliance owners. |
| Multiple customers affected | Broader product or infrastructure failure | Coordinate cross-account incident response. |
| Repeated unresolved issue | Declining confidence and potential churn | Involve Support leadership and the assigned CSM. |
| Issue blocks implementation or go-live | Delayed time-to-value | Coordinate a recovery plan with Implementation and Engineering. |
| Issue occurs near renewal | Commercial and retention exposure | Involve CS leadership and Account Management. |
| Executive dissatisfaction | Relationship and sponsorship risk | Establish an executive communication and recovery plan. |
| Customer threatens cancellation | Immediate retention risk | Involve CS leadership and commercial stakeholders. |
| No confirmed workaround | Extended operational disruption | Reassess severity and escalate technical ownership. |

### Escalation Levels

- **Level 1 — Operational:** Routine product issues, incomplete information, and manageable workflow disruptions. Support and the CSM coordinate resolution.
- **Level 2 — Cross-Functional:** Major workflow issues, implementation blockers, or recurring defects. Support leadership, Engineering, and relevant functional owners become involved.
- **Level 3 — Strategic / Executive:** Critical outages, data integrity concerns, material contractual exposure, executive dissatisfaction, or significant churn risk. Activate incident leadership and executive oversight.

---

## 11. Escalation Performance Metrics

Escalation performance should measure both technical execution and the customer experience.

| KPI | Definition | Measurement |
| :--- | :--- | :--- |
| Initial Response Time | Time between incident submission and first meaningful response. | Average response time by severity. |
| Time to Mitigation | Time between incident identification and effective reduction of customer impact. | Average time by severity. |
| Time to Resolution | Time between incident identification and confirmed resolution. | Average resolution time by severity. |
| SLA Compliance | Percentage of incidents meeting applicable response targets. | Incidents meeting target / Total incidents × 100 |
| Escalation Volume | Number of escalated incidents over a reporting period. | Count by severity, product area, and customer segment. |
| Reopen Rate | Percentage of resolved tickets reopened due to incomplete or unsuccessful resolution. | Reopened tickets / Resolved tickets × 100 |
| Repeat Incident Rate | Frequency of recurring issues affecting the same customer or workflow. | Repeat incidents / Total incidents × 100 |
| RCA Completion Rate | Percentage of incidents requiring an RCA with completed documentation. | Completed RCAs / Required RCAs × 100 |
| Customer Incident Satisfaction | Customer feedback following incident resolution. | Post-resolution survey or direct feedback. |

### Review Cadence

- **Daily:** Review active SEV-1 and SEV-2 incidents.
- **Weekly:** Review open escalations, aging tickets, and recurring customer-impacting issues.
- **Monthly:** Analyze severity trends, response performance, and resolution patterns.
- **Quarterly:** Review systemic issues, customer impact, and opportunities for product or process improvement.

### Dashboard Recommendations

A centralized escalation dashboard should provide visibility into:

- Open incidents by severity.
- Incidents approaching response targets.
- Average response and resolution times.
- Accounts with multiple escalations.
- Recurring product defects.
- Incidents affecting strategic or renewal-sensitive accounts.
- Outstanding RCA actions.
- Customer recovery status.

---

## 12. Cross-Functional Governance

Escalation management requires clear working agreements between Customer Success, Support, Engineering, and Product.

### Customer Success

- Owns customer-facing communication.
- Tracks business impact and relationship risk.
- Coordinates executive stakeholder engagement.
- Maintains account health and recovery plans.

### Support

- Owns ticket intake and technical triage.
- Documents reproduction steps and troubleshooting.
- Maintains ticket accuracy and status.
- Coordinates technical escalation.

### Engineering

- Owns technical investigation and remediation.
- Provides verified technical updates.
- Identifies root cause.
- Implements and validates fixes.

### Product

- Reviews product defects and enhancement requests.
- Evaluates recurring product limitations.
- Provides context on product direction when appropriate.
- Helps prioritize systemic improvements.

### Leadership

- Supports prioritization when incidents create significant business exposure.
- Resolves cross-functional ownership conflicts.
- Engages executive stakeholders when necessary.
- Reviews incident trends and operational effectiveness.

---

## 13. Operating Philosophy

**Customers remember how an organization responds when something goes wrong.**

A strong escalation process is not measured solely by how quickly a ticket is closed. It is measured by how effectively the organization protects the customer's business, communicates throughout the disruption, and restores confidence in the partnership.

The operating framework is simple:

**Understand → Prioritize → Assign → Communicate → Resolve → Recover → Prevent**

- Understand the customer's business impact.
- Triage the issue based on severity.
- Prioritize the appropriate response.
- Assign clear technical and customer-facing ownership.
- Communicate proactively and transparently.
- Resolve the underlying issue.
- Recover customer confidence.
- Prevent recurring problems through documented improvements.

**Technical resolution closes the incident. Customer recovery protects the relationship.**
