# From Prompt to Production: Build an AI-Powered Expense App in a Day

Welcome to the **From Prompt to Production: Build an AI-Powered Expense App in a Day** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-10-01</summary>

## Release Date: 2026-10-01

### Summary of Changes

Tested and revised all four challenges against the current Power Platform UI, and added validations for Challenges 1, 2 and 4. The biggest content change: Copilot now builds the full schema from a detailed prompt, and the rules Copilot can't set (default status, amount limit) now sit on the Dataverse table instead of in app formulas. The lab was also cut down to match what works reliably in the time available.

### Infrastructure Changes

- Lab assets now download from CloudLabs storage as one zip, with three retries, and land in `C:\Users\Public\Desktop\Lab Assets`. Learners no longer get a manual download fallback; if the folder is missing, they contact support.
- Added three Validate-button scripts and a spare fallback script. They run as the CloudLabs S2S application and find each learner's own environment by Deployment ID (see Validations).

### Content Changes

- **Challenge 1**: The Copilot prompt now lists every column, including Policy Flag and Policy Reason. Learners check the draft against a schema table before saving, because a text column can't be converted to a choice column afterwards. The default status and the 0.01–9,999.99 amount limit are now set on the table, replacing the Power Fx `Notify` check.
- **Challenge 2**: Rejections now post a plain Teams message instead of an adaptive card, and the separate rejection email is gone. Added guidance on the two **Status** columns, picking the trigger's copy of duplicated dynamic content, the people-picker **To** field, and switching the Approvals app to the learner's environment.
- **Challenge 3**: Removed the **Spend Insights** grounded prompt. One AI Builder prompt is left (the policy check), running on Copilot Credits. The verdict columns now come from Challenge 1, and the receipt steps use a Field / Value / Action table.
- **Challenge 4**: Down to two visuals (spend by category, top 5 merchants); the approval-outcomes line chart is gone. Tiles now need both a title and a subtitle, or they show greyed out in Power Apps. The Add to Teams steps were rewritten for the current ribbon and web Teams prompts.
- **Getting Started / Prerequisites / Overview**: Getting Started now has learners add the CloudLabs S2S app user (System Administrator) in their environment, which the validations rely on. Teams, publisher and AI hub steps match the current UI, the overview reflects the smaller scope, and screenshots and wording were refreshed throughout.

## Validations

All validations succeeded.

- **Challenge 1 – Expenses table loaded**: Checks that the learner's environment has a custom **Expenses** table holding at least the 12 rows imported from the expense history file.
- **Challenge 2 – Approval flow activated**: Checks that a cloud flow named **Expense Claim Approval** exists and is turned on.
- **Challenge 4 – End-to-end claim approved**: Checks that the Expenses table has a USD 284.27 claim (from the electronics receipt) marked **Approved**. This proves the receipt scan, the claim submission and the approval write-back all worked. Only the amount and the status are checked, and any amount from 284.00 up to 285.00 passes, so a small scan difference can't fail anyone.
- A spare check that the **Contoso Expense Analytics** Power BI workspace exists for the learner is kept as a fallback. It isn't wired into the guide, because it needs Power BI admin API access in the tenant.

### Testing Notes

- **Testing Date**: 2026-10-01

### Testing Scope

Ran through all four challenges in a learner environment and updated the guide wherever the current UI or a real run didn't match it. Ran each Validate step against the completed work, and all of them passed.

---

</details>

<details>
  <summary>2026-08-12</summary>

## Release Date: 2026-08-12

### Summary of Changes

Onboarded this lab as a new 4-hour, intermediate Hack in a Day on the Power Platform. Learners act as the maker at fictional Contoso Retail and build a complete expense management application without writing traditional code — generating an app and data model with Copilot, adding a human approval workflow, layering on AI receipt reading and policy judgement, and publishing the result into Microsoft Teams with an embedded Power BI dashboard.

Key decisions taken during onboarding:

- **The lab is entirely browser-based.** Nothing is installed on the JumpVM and no PowerShell modules are required, so the VM exists only to give learners a clean, consistent browser and the sample files.
- **Environments are pre-created per learner, not by the lab.** Each learner works in a Developer environment created and assigned to their ODL user before the event. Learners never create an environment themselves, and neither does the deployment — this avoids provisioning failures mid-lab and keeps everyone out of the tenant's Default environment.
- **AI Builder capacity is pooled at the tenant level.** Pay-as-you-go billing policies cannot be applied to Developer environments, so capacity is shared from the tenant's unassigned credit pool rather than allocated per learner.
- **Minimal desktop footprint.** Only the sample files the challenges actually use are placed on the desktop; every portal is reached by URL from the lab guide instead of a shortcut.

### Infrastructure Changes

- Authored the ARM template, deployment script and first-logon script for a single Windows JumpVM — the only Azure resource in the lab.
- The deployment stages the challenge assets (two sample receipts and a seed expense history file) into a **Lab Assets** folder on the desktop, with a first-logon recovery step in case the download fails.
- Removed environment provisioning from the deployment entirely, in line with the pre-created environment model above.
- Documented the mandatory pre-event provisioning runbook: bulk-create one Developer environment per learner, and add the CloudLabs application as an S2S application user with System Administrator in each one.
- Authored the support handover document covering the pre-event steps, L1 troubleshooting and the escalation matrix.

### Content Changes

Onboarded the full guide set — overview, getting started, a prerequisite page and four challenges:

- **Prerequisite**: create the solution that holds everything, set up the Teams team used later, locate the sample files, and confirm AI Builder and Power BI are reachable before the work begins.
- **Challenge 1 — Build the Data Model and App with Copilot**: generate a Dataverse table and canvas app from a single sentence, then correct the generated data model, add validation, capture the submitter automatically, and import Contoso's expense history.
- **Challenge 2 — Automate Expense Approvals with Power Automate**: store the approver address as an environment variable, build an automated cloud flow triggered by new claims, route them through an approval, and write the decision and comment back onto the record.
- **Challenge 3 — Add Receipt Scanning and AI Policy Checks**: use the AI Builder receipt processor to populate a claim from a photographed receipt, and AI Builder prompts to judge claims against Contoso's expense policy.
- **Challenge 4 — Report in Power BI and Publish to Teams**: build a semantic model, report and dashboard in the browser, embed the dashboard in the app, and publish the app as a Teams tab.

A feasibility test document was also authored to cover the tenant and licensing setup required before the lab is delivered.

## Validations

Two validations were onboarded, covering the two challenges whose output can be confirmed reliably from the platform side:

| Challenge | Task | Asserts |
|---|---|---|
| Challenge 01 | Task 5 | The Expenses table exists and holds the imported expense history |
| Challenge 02 | Task 4 | The approval cloud flow exists and is turned on |

Both run as `System` and reuse the S2S application user granted during pre-event setup, so no secrets and no learner input are involved. Validation failures caused by setup gaps are reported as such and direct the learner to support rather than blaming their work.

### Testing Notes

- **Testing Date**: 2026-08-12

### Testing Scope

Reviewed the deployment and logon scripts, all guide pages and the validation scripts against the pre-created environment model. Licensing and capacity claims — including the pay-as-you-go environment-type restriction and AI Builder credit behaviour — were verified against current Microsoft documentation.

---
</details>
