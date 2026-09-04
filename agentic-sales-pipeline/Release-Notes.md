# Agentic Sales Pipeline: Sales Research Agent, Custom Copilot Studio Agent, and D365 Sales Automation​

Welcome to the **Agentic Sales Pipeline: Build a Lead Queue That Runs Itself** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

## Overview
This Page contains detailed notes about the latest updates and modifications made after each testing cycle. It includes:

- Testing dates
- Descriptions of changes to lab infrastructure
- Updates to content or documentation
- Changes to screenshots and visuals used in the lab

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`

`Email Support: cloudlabs-support@spektrasystems.com`

# Release Notes

<details>
  <summary>2026-09-04</summary>

## Release Date: 2026-09-04

### Summary of Changes

Onboarded this lab as a L300 Hack in a Day on Dynamics 365 Sales and Microsoft Copilot Studio. Learners act as the Sales Operations Architect at fictional **Contoso Cloud Solutions**, where 2,020 of last quarter's 2,400 inbound leads were never opened by a human. Across five challenges they take a 24-lead inbound queue and make it run itself — autonomous research, a custom scoring agent, self-enrolling cadences, agent-handled email replies, and the supervisor dashboard that proves what the agents produced.

Key decisions taken during onboarding:

- **One Dynamics 365 Sales environment per learner, created before the event.** Every configuration task in this lab — the agent instance, the custom Lead columns, the Copilot Studio agent, the sequences, the dashboard — is stored **per environment**. Learners sharing an environment would overwrite each other. Environments are **Sandbox** type with `D365_Sales` enabled; a Developer environment cannot host Dynamics 365 Sales at all.
- **Buy one agent, build the other.** The lab deliberately pairs Microsoft's Sales Qualification Agent (configured, not built) with a learner-built Copilot Studio agent. That boundary is the lab's central teaching point, not an implementation convenience.
- **The 24 leads are imported by the learner, not seeded.** They arrive as a CSV on the desktop and the learner imports them on the Prerequisites page. This removes any hard dependency on a data-loading step for Challenges 01–04.
- **Pipeline history *is* pre-seeded, and is required.** See the pre-seeding note below — Challenge 05's attribution reporting is meaningless without it.
- **The learner builds the agent's own identity.** Rather than pre-registering an Entra app and pushing an application user into every environment, the learner adds the CloudLabs-provisioned service principal (`odl_user_sp_<DeploymentID>`) as a Dataverse application user with the **AIsalesperson** role in Challenge 01. Nothing to register pre-event, and every learner gets a distinct identity.

### ⚠️ Pre-seeding is required

`provisioning/4-load-pipeline-history.ps1` must be run before the event. It seeds roughly **10 accounts, 90 closed opportunities and 15 open non-agent opportunities** into every learner environment.

The 15 open opportunities are the **denominator** for Challenge 05's attribution reporting. Without them, every Opportunity in the org came from the learner's agent, both dashboard tiles show the same number, and the attribution chart reads a meaningless 100%. Challenge 05 handles the missing-seed case gracefully rather than breaking, but the challenge's payoff is lost.

### ⚠️ Copilot capacity — pay-as-you-go fallback

Every agent in this lab consumes Copilot Credits. **If bundled or prepaid Copilot Credits are unavailable, assign a pay-as-you-go billing policy backed by an Azure subscription** so learners can work with the agents at all.

Two things caught us during testing, and both are easy to miss:

- **A pay-as-you-go billing policy covers *named* environments.** Learner environments are created fresh at provisioning time and are therefore not in any existing policy. Add them explicitly, or credits never reach them and the agents silently produce nothing, with no error shown.
- **Under pay-as-you-go, learners must also be in the Copilot Studio authors security group** (PPAC → Manage → Tenant settings), or publishing fails with a licence error even though billing is configured correctly.

### Infrastructure Changes

- Authored the ARM template, parameters file and deployment script for a Windows JumpVM — the only Azure resource in the lab.
- Authored the pre-event provisioning runbook (`provisioning/context.md`) and five PowerShell scripts following the existing environment automation pattern — PAC CLI, results CSVs, exponential backoff, idempotent auto-resume on re-run:

| Step | Does |
|---|---|
| `0-preflight.ps1` | Read-only. Fails early if the `D365_Sales` template reports *Is Disabled* — the signal that the tenant holds no Sales licence and environments would be created without Sales Hub |
| `1-create-sales-envs.ps1` | One Sandbox environment per learner from `users.csv` |
| `2-grant-access-to-envs.ps1` | Grants the learner **System Administrator** on their own environment |
| `3-verify-envs.ps1` | Read-only verification |
| `4-load-pipeline-history.ps1` | **Required.** Seeds accounts and closed/open opportunity history across all environments unattended |

- An Entra app registration/service principal and client secret are needed **only** for step 4's unattended seeding. Nothing in the learner-facing lab depends on it.

### Content Changes

Onboarded the full guide set — overview, getting started, a prerequisites page and five challenges. Each challenge consumes what the previous one produced.

- **Prerequisites — Environment Readiness and Lead Ingestion**: clear the three AI hub platform prerequisites, import the 24 inbound leads, and create the **Agent Score** and **Qualification Tier** columns the learner's own agent writes to. Learners record the *numeric* option values behind Hot/Warm/Cold here — those are generated per environment and needed in Challenges 02, 03 and 04.
- **Challenge 01 — Autonomous Lead Research and Qualification**: configure Microsoft's **Sales Qualification Agent** in Research-only mode, give it Contoso's identity, and scope it with selection criteria so it works 12 of the 24 leads and ignores the rest. The scoping decision, not the switch-on, is the exercise.
- **Challenge 02 — Custom Lead Scoring Agent in Copilot Studio**: build an agent with **generative orchestration** that reads a lead, applies Contoso's rubric, writes a score and tier back to Dataverse, then runs unattended from a Dataverse event trigger with a column filter that stops it triggering itself.
- **Challenge 03 — Automated Sequence Enrolment and Seller Handoff**: three sales-accelerator cadences, a flow that moves a lead between sequences on tier change via `msdyn_DisconnectSequence` / `msdyn_ConnectSequence`, and a Teams adaptive card that hands the lead to a seller with everything needed to act.
- **Challenge 04 — Agent-Driven Reply Handling and CRM Actions**: give the agent an Outlook trigger and three ways to act — create an Opportunity with attribution, draft a playbook-grounded rebuttal for human approval, or honour an unsubscribe and do nothing else. The compliance path is the one that matters and has the least code.
- **Challenge 05 — Pipeline Attribution and Supervisor Reporting**: qualify the Hot tier into real Opportunities, build Dataverse charts and an **Agent-sourced pipeline** view filtered on Originating Lead, assemble a published supervisor dashboard, generate a Power BI quick report on a Free licence, and build a scheduled flow that posts an AI-generated recommendation to Teams when Hot conversion falls.

Five learner assets were authored and published to a separate assets branch: the inbound lead CSV, the Contoso ICP and offerings briefing, the tiering rubric, the objection-handling playbook, and the three test reply emails.

### Fixes applied during feasibility testing

Running the lab live surfaced fixes in every challenge. The tier column's numeric option values replaced a misleading warning about label capitalisation, and the Sales Qualification Agent's knowledge-source step was dropped — it needs SharePoint-hosted documents and a licence-gated page, and one wrong click there stops the agent processing records at all. Learners now build the agent's identity from the existing CloudLabs service principal rather than registering anything. LinkedIn sequence steps were removed for lack of Sales Navigator, and Challenge 03's premise that a re-enrolment "fails cleanly" turned out to be wrong: Dataverse silently stacks a second live sequence connection, so the flow disconnects first and verification now checks membership rather than row counts. Challenge 04's four failures were all one bug — an autonomous run has nobody to answer a clarifying question, so any unpinned tool input stalls forever and silently; fixed by pinning the currency lookup, splitting the shared update tool into single-purpose ones, moving the Teams post to Flow-bot chat, and deactivating the built-in Escalate topic that was hijacking the unsubscribe path. Challenge 05 was trimmed to protect attention late in the day, with no objective dropped.


### Validations

No validation scripts have been authored for this lab.

### Testing Notes

- **Testing Date**: 2026-09-04

### Testing Scope

Ran the lab against a single live Sandbox environment with Dynamics 365 Sales, seeded via the interactive history loader. Prerequisites and Challenges 02, 03, 04 and 05 Task 1 were executed end to end in the live environment, and every fix listed above was reproduced and re-verified after the change. Every product feature, UI path and licensing claim was verified against current Microsoft Learn documentation rather than written from memory.

---
</details>
