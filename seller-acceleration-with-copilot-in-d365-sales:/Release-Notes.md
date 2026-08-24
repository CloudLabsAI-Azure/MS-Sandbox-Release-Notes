# Seller Acceleration with Copilot in Dynamics 365 Sales: From Prospect to Close with AI at Every Step

Welcome to the **Seller Acceleration with Copilot in Dynamics 365 Sales** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-21</summary>

## Release Date: 2026-08-21

### Summary of Changes

Onboarded this lab as a new 3.5-hour, L100/L200 Hack in a Day on Dynamics 365 Sales. Lenterprise Account Executive at fictional Contoso Cloud Solutions who has inherited the**Northwind Enterprises** CRM-upgrade deal — USD 480,000, closing in 75 days — from a predecessor who left no notes. They take that single deal from first research to post-meeting follow-up using the AI that ships inside Dynamics 365 Sales at every stage.

Key decisions taken during onboarding:

- **One Dynamics 365 Sales environment per learner, pre-created before the event.** Every configuration task in this lab — Copilot summary fields, the M365 Copilot app toggle, the predictive scoring model — is stored **per environment**, so learners in a shared environment would overwrite each other all day. Environments are **Sandbox** type with Dynamics 365 apps enabled; a Developer environment cannot host Dynamics 365 Sales at all.
- **Learners build their own data.** The environment arrives empty by design. The learner creates the Northwind account, three contacts, two competitors and the opportunity in the Prerequisite from a
supplied handover note. This removes any hard dependency on a seeding step and means Chven if nothing was pre-loaded.
- **Nothing in the lab is consumption-billed.** The design deliberately uses only features covered by the **Dynamics 365 Sales Enterprise** and **Microsoft 365 Copilot** licences. There are no Copilot
Credits to purchase or allocate, and no DLP connector allowances to arrange.
- **Provisioning seeds no data and holds no secrets.** The pre-event scripts create, grant and verify environments only.

### Infrastructure Changes

- Authored the ARM template, parameters file, deployment script and first-logon script for a single Windows JumpVM — the only Azure resource in the lab.
- `logon.ps1` re-checks all five assets on first sign-in and re-fetches any that are mif.
- Authored the pre-event provisioning runbook (`provisioning/context.md`) and four Powe existing developer-environment automation — PAC CLI, results CSVs, exponential backoff,auto-resume on re-run:

| Step | Does |
|---|---|
| `0-preflight.ps1` | Read-only. Fails early if the `D365_Sales` template reports *Is Disabled* — the signal that the tenant holds no Sales licence and environments would be created without Sales Hub |
| `1-create-sales-envs.ps1` | One Sandbox environment per learner from `users.csv` |
| `2-grant-access-to-envs.ps1` | Grants the learner **System Administrator** on their own environment. An S2S application user is opt-in and off by default |
| `3-verify-envs.ps1` | Read-only verification using only the existing PAC CLI auth proo client secret |

- Added an **optional** `4-load-pipeline-history.ps1`. Predictive opportunity scoring refuses to build a model without at least 40 won and 40 lost opportunities, and closed opportunities cannot be produced
any other way — a CSV import can neither close an opportunity nor backdate `createdon`.al accounts and 90 closed deals across all environments unattended, running severalenvironments concurrently on PowerShell 7 and falling back to serial on Windows PowerShell 5.1.
- All PowerShell verified to parse cleanly in **both** Windows PowerShell 5.1 (what the JumpVM runs) and PowerShell 7. Scripts containing box-drawing output are saved UTF-8 **with BOM**, without which 5.1 reads them as ANSI and fails with `The string is missing the terminator`.

### Content Changes

Onboarded the full guide set — overview, getting started, a prerequisite page and four challenges.

- **Prerequisite — Prepare Your Workspace**: turn on Copilot including audit history, athen build the Northwind deal in an empty CRM from `northwind-briefing.md`.
- **Challenge 01 — Teach Copilot the Deal**: read the weak default opportunity summary, then configure the fields Copilot grounds on, the recent-changes list and the competitor insight sections, and turn the regenerated summary into three evidence-backed talking points.
- **Challenge 02 — Open the Conversation**: enable **Contextual email drafting with AI**, draft and edit the CTO outreach and the meeting invitation with Copilot, manufacture the customer's reply so the
deal has a two-sided thread, and summarise it into the customer notes.
- **Challenge 03 — Score the Deal, Then Find What You Missed**: switch on **Microsoft 365 Copilot** in the Sales Hub app and use Dataverse-grounded **Chat** to reason across the pipeline, train and publish
a **predictive opportunity scoring** model on real won/lost history, then build a deal eholders, competitors and MEDDPICC gaps and turn it into two mitigation tasks.
- **Challenge 04 — Run the Meeting, Let AI Do the Admin**: generate a meeting preparation brief with Copilot, log the discovery call on the deal, build a reusable **Deal Debrief** prompt in prompt builder
that returns structured JSON, use its output to create tasks, notes and a follow-up emaback through AI-generated **Timeline highlights**.

Five learner assets were authored and published to a separate assets branch: the Northwind handover briefing, the discovery call script, three follow-up email templates plus the customer's reply, the
Contoso competitive battlecard, and the deal debrief prompt specification.

### Screenshot Changes

- Basic `getting-started.md` screenshot uploads for the landing page guidance.

### Licensing

Per learner:

| Licence | Covers |
|---|---|
| **Dynamics 365 Sales Enterprise** | Sales Hub, Copilot in D365 Sales, email assist, predictive scoring, timeline highlights, relationship analytics — Challenges 01–03 |
| **Microsoft 365 Business Basic + Microsoft 365 Copilot Business** | Exchange mailbox,osoft 365 Copilot in Sales Hub — Challenge 03 Task 1 |
| **Microsoft Copilot Studio User License** | Free. Satisfies the prompt-builder entitlement for Challenge 04 |

Sales **Premium**, Teams Premium, Teams Phone and Power Platform premium were all asses Every licence claim was verified against current Microsoft documentation rather thaninferred from the SKU name — including confirmation that **Copilot Business** grants the same agent access as the enterprise Copilot add-on, and that Copilot email assist inside Dynamics needs no Microsoft 365 Copilot licence at all.

Dataverse capacity is the constraint to watch: roughly **1 GB per learner environment**.

### Testing Notes

- **Testing Date**: 2026-08-21

### Testing Scope

Reviewed the ARM template, deployment and logon scripts, all five provisioning and testpage. All PowerShell was parse-checked in both Windows PowerShell 5.1 and PowerShell 7,and both JSON files validated. Asset delivery was proved end to end against the live assets branch, confirming all five files land in the desktop **Lab Assets** folder. The interactive history loader was
run successfully against a live Sandbox environment. Every product feature, UI path andguide was verified against current Microsoft Learn documentation rather than written from memory.

---
</details>