# AI-Native Case Management: Copilot, Intent and Knowledge in Dynamics 365 Customer Service

Welcome to the **AI-Native Case Management: Copilot, Intent and Knowledge in Dynamics 365 Customer Service** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-27</summary>

## Release Date: 2026-08-27

### Summary of Changes

Onboarded this lab as a new 3–4 hour, L200 Hack in a Day on Dynamics 365 Customer Service. Learners act as the incoming **Customer Service Manager** at fictional **Northwind Traders**, a support desk where routing
lives in one coordinator's head and resolution knowledge is never written down, six weeks beme. Across a prerequisite and four challenges they build unified routing that anyone canread, use Copilot to find customers whose real intent contradicts how they were filed, publish knowledge articles out of already-solved cases, and prove the result on a dashboard against a stated baseline.

### Infrastructure Changes

- Authored the pre-event provisioning runbook (`provisioning/context.md`) and four PowerShell scripts, mirroring the existing environment automation — PAC CLI, results CSVs, exponential backoff, auto-resume on re-run:

| Step | Does |
|---|---|
| `0-preflight.ps1` | Read-only. Fails early if the `D365_CustomerService` template reports at the tenant holds no Customer Service licence and environments would be created without the service apps |
| `1-create-cs-envs.ps1` | One Sandbox environment per learner from `users.csv` |
| `2-grant-access-to-envs.ps1` | Grants the learner **System Administrator** on their own environment |
| `3-verify-envs.ps1` | Read-only verification using the existing PAC CLI auth profile; no c

- Provisioning seeds no data and holds no secrets. There is no app registration and no S2S in this lab.

### Content Changes

Onboarded the full guide set — overview, getting started, a prerequisite page and four challenges.

- **Prerequisite — Stand Up Northwind's Service Desk**: confirm Copilot and Dataverse searchane features and case summaries, approve the learner mailbox, surface the **Category** column on the account form the service apps actually render, then build the accounts, contacts and ten-case intake batch from the supplied brief.
- **Challenge 01 — Route the Work**: enable unified routing for the case channel, build five queues, author a work classification ruleset that derives priority from commercial tier and title urgency, author the route-to-queue ruleset, then route the intake batch and fix the case the rules put in the wrong queue — in the rules, not on the record.
- **Challenge 02 — Find the Real Intent**: build a six-value intent taxonomy on the Subject tree, use the Copilot pane to determine what each customer actually wants, identify the three cases whose intent
contradicts how they were filed, and add a cancellation-intent rule at the top of the routina retention specialist ahead of everything else.
- **Challenge 03 — Turn Resolved Cases into Knowledge**: configure knowledge management and Copilot case-to-knowledge drafting, enable the knowledge base as a Copilot source, resolve five cases from the engineers'
write-ups, publish the drafts worth publishing, and confirm Copilot cites a published article next similar case.
- **Challenge 04 — The Agent Desktop and Proving the Impact**: configure the agent experience profile so case summary, Copilot Q&A, knowledge search and email drafting are live together, instrument the Case table
with two custom columns, work three cases end to end through the desktop, and build a publisesult against the baseline.

Three learner assets were authored for a separate assets branch: the Northwind service desk handover brief (accounts, contacts, routing design, intent taxonomy and baseline metrics), the ten-message case intake
sheet with its expected routing table, and the five resolution write-ups.

### Screenshot Changes

- Reused the generic CloudLabs environment, sign-in and navigation screenshots from a sibling Dynamics 365 lab. Per Hack in a Day convention, screenshots appear in `getting-started.md` only.

### Licensing

Per learner:

| Licence | Covers |
|---|---|
| **Dynamics 365 Customer Service Enterprise** | Unified routing, queues, case management, kcase summary, *Ask a question*, *Write an email*, knowledge search, Copilot case-to-knowledge — all four challenges |
| **Microsoft 365 Business Standard** | Entra identity and the Exchange mailbox the learner |

Assessed and deliberately **not** required: Copilot Credits, a pay-as-you-go plan, Dynamics Service Premium, and Power BI Pro. Every licence claim was verified against current Microsoft documentation rather than inferred from the SKU name.

Dataverse capacity is the constraint to watch: roughly **1 GB per learner environment**.

## Validations

No validations have been authored for this lab yet.

### Testing Notes

- **Testing Date**: 27-08-2026

### Testing Scope

End-to-end feasibility testing for all four challenges, including the prerequisites, has been completed. All PowerSheWindows PowerShell 5.1 and PowerShell 7, both JSON files validated, and every image reference confirmed to resolve. Case identifiers, queue names, the intent taxonomy and the resolution-note set were cross-checked for consistency across the guide and the asset pack. Every product feature, UI path, app name
and licence requirement in the guide was verified against current Microsoft Learn documentation memory.

---
</details>

---