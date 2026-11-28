# SOP: Async Enablement & Visual Workflow Documentation (Scribe & Loom)

**Owner:** Senior Customer Success Manager  
**Audience:** Customer Success, Onboarding Specialists, Implementation, Support  
**Purpose:** Replace dense text instructions and repetitive live walkthroughs with scannable step by step guides (Scribe) and concise video walkthroughs (Loom) to accelerate customer onboarding, prevent knowledge loss during team turnover, and standardize internal CS execution.

---

## 1. Tool Selection Matrix

Use the right medium based on the complexity of the workflow and how the customer or teammate will consume it:

| Use Case | Primary Tool | Target Length | Best For |
| :--- | :--- | :--- | :--- |
| **Click by click UI configuration** | **Scribe** | 8 to 15 steps | Workspace permissions, social profile connections, approval routing rules, billing updates |
| **Strategic workflow & context** | **Loom** | 2 to 4 minutes | Explaining *why* a workflow matters, walking through QBR dashboards, executive account handoffs |
| **High friction recovery & onboarding** | **Scribe + Loom** | 3 min Loom + 10 step Scribe | Embedding a Scribe guide directly inside a Loom summary so users can watch the overview and follow the clicks |

---

## 2. Standard Operating Procedure: Creating a Scribe Guide

1. **Scope a Single Outcome:** Limit each Scribe to one clear task (for example, *Setting Up Two Stage Client Approval Workflows* rather than *Complete Platform Setup*).
2. **Prep a Clean Environment:** Close unrelated browser tabs, hide bookmarks, and use a standardized demo workspace with realistic sample data.
3. **Capture with Deliberate Pacing:** Click slowly and pause briefly between actions so Scribe captures clean screenshots and accurate element labels.
4. **Edit & Redact Immediately:**
   * Remove accidental clicks, duplicate steps, or navigation detours.
   * Blur or redact any sensitive customer emails, API keys, or account IDs.
   * Rewrite auto generated step titles into clear action verbs (for example, change *"Click here"* to *"Select Require Executive Sign Off"*).
5. **Add Context Callouts:** Insert a brief tip or alert block at any step where users commonly make configuration mistakes.

---

## 3. Standard Operating Procedure: Recording a Loom Walkthrough

1. **Follow the 3 Part Script Structure:**
   * **Hook & Outcome (0:00 to 0:20):** State the exact problem being solved and what the viewer will be able to do by the end of the video.
   * **Live Demonstration (0:20 to 2:45):** Walk through the workflow on screen while narrating the business value behind each setting, not just where to click.
   * **Next Step & CTA (2:45 to 3:15):** Direct the viewer to the companion Scribe guide, template, or action item.
2. **Optimize Playback & Accessibility:**
   * Record at 1080p with clean audio and camera bubble enabled to maintain human connection.
   * Enable auto generated chapters and transcript review so busy stakeholders can jump directly to the section they need.
   * Title the video using a searchable naming convention: `[Category] Workflow Name (Duration)`.

---

## 4. Governance, Storage & Lifecycle Triggers

* **Central Repository:** Store all published Scribe links and Loom embeds inside the shared Notion Enablement Hub and link directly from relevant CS playbooks.
* **Trigger Based Creation:** Whenever a CSM explains the same workflow twice in one week, or resolves a recurring adoption blocker during a QBR, turn that resolution into a Scribe or Loom within 48 hours.
* **Quarterly Audit:** Review top shared guides alongside product release notes every quarter to archive outdated UI captures and refresh core onboarding links.
