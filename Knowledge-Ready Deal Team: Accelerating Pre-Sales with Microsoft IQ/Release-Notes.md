# Knowledge-Ready Deal Team: Accelerating Pre-Sales with Microsoft IQ​

Welcome to the **Knowledge-Ready Deal Team: Accelerating Pre-Sales with Microsoft IQ​​** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-09-16</summary>

## Release Date: 2026-09-16

### Summary of Changes

Performed end-to-end lab testing and validation, uncovering and resolving several infrastructure and content issues encountered during the walkthrough.

### Infrastructure Changes

- Fixed a VM provisioning issue where the lab VM entered a continuous reboot loop every 2–3 minutes, caused by the startup script (`psscript-01.ps1`) lacking an idempotency check and unconditionally forcing a restart on every boot. Added a completion-flag guard and wrapped each provisioning step in error handling so the VM only restarts after a fully successful run.
- Updated the ARM template (`deploy-01.json`) to enable boot diagnostics on the VM for easier troubleshooting without RDP access, and to make the base image version pinnable via a parameter instead of always tracking `latest`.
- Corrected the lab content extraction path so `MultiIQ.zip` unpacks directly into `C:\LabFiles\MultiIQ` instead of creating a duplicated nested `MultiIQ\MultiIQ` folder structure.

### Content Changes

- Identified that the service principal (`ClientID`/`ClientSecret`) provided for the Foundry IQ API challenge did not exist in the target tenant, requiring a new app registration before the lab could proceed; flagged for the provisioning/SPN-creation pipeline to be checked for reliability.
- Found that the "Azure AI Developer" role referenced for granting Foundry file-upload permissions does not apply to Foundry projects (per Microsoft's own guidance) and documented that the correct role is **Foundry User**, assigned at both the Foundry account and project scope.
- Noted that the suggested Function App naming pattern (`func-multiiq-<ID>`) can collide across students since Function App names must be globally unique, and a uniquifying suffix is needed.
- The guide has been updated to high-level instructions for improved clarity and ease of following, without changing the underlying technical steps.

## Validations

N/A

### Testing Notes

- **Testing Date**: 2026-09-16

### Testing Scope

Completed end-to-end testing of the VM provisioning flow, the Foundry IQ API knowledge-base build/query steps, and the Azure Function App creation step. Root-caused and resolved the reboot loop, RBAC/permission gaps for Foundry file uploads, and folder-structure issues in the lab content, ensuring the lab instructions and underlying scripts/templates are accurate and reproducible.

---
</details>

<details>
  <summary>2026-08-31</summary>

## Release Date: 2026-08-31

### Summary of Changes

Onboarded this lab as a new 6 hour, Hack in a Day on which learners build a single Copilot Studio agent that combines governed knowledge grounding, live business-data retrieval, and expert escalation routing into one orchestrated, multi-hop conversation serving both pre-sales and customer service teams. Using Microsoft Entra ID, Microsoft Foundry, SharePoint, Power BI/Microsoft Fabric, Azure Functions, Microsoft Graph, Microsoft Copilot Studio, and Microsoft Teams, you design an end-to-end solution that answers product and policy questions with citations, grounds business facts in live customer data, and routes complex questions to the right internal expert.

### Infrastructure Changes

N/A

### Content Changes

Onboarded the content as per the shared agenda, with five challenges designed to progressively build on one another, and completed the feasibility check.

### Screenshot Changes

N/A

## Validations

No validations have been authored for this lab.

### Testing Notes

- **Testing Date**: 31-08-2026

### Testing Scope

End-to-end feasibility check for all for challenges have been completed, final round of testing has to be done before the delivery.

---
</details>

---
