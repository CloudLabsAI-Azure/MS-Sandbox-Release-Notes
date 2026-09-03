# Guided Lab: Threat Protection with XDR

Welcome to the **Guided Lab: Threat Protection with XDR** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-07-22</summary>

## Release Date: 2026-07-22

### Summary of Changes

Performed end-to-end lab testing and validation across Modules. Updated the Windows Security Events data connector setup to use the Azure Monitor Agent (AMA) and Data Collection Rules flow in place of the **deprecated** Legacy Agent flow, refreshed screenshots to match the current portal UI, and revised lab instructions and wording for clarity and accuracy. Included a custom policy to ensure the rule can be created, otherwise a possible work-around by creating a policy exemption.

### Infrastructure Changes

N/A

### Content Changes

- **Module 1 (Lab-01, Lab-02)**: Added guidance for creating/selecting a Sentinel Log Analytics workspace, updated Playbook creation/update steps with clearer screenshots, and migrated the Windows Security Events connector setup to the AMA + Data Collection Rule (DCR) wizard flow, including a new troubleshooting note for Azure Policy exemptions.
- **Module 3 (Lab-01, Lab-02, Lab-03)**: Migrated the Windows Security Events connector to the AMA/DCR flow (same as Module 1), added a caution note on avoiding duplicate Log Analytics workspaces in Defender for Cloud, and refreshed screenshots for analytics rule creation, entity mapping, and automation rules.
- **Module 4 (Lab-01)**: Migrated the Windows Security Events connector to the AMA/DCR flow, added the duplicate-workspace caution note, and renamed "Create a Search" to "Create a Search job" for accuracy.
- **Module 5 (Lab-01)**: Updated device onboarding and incident management steps with refreshed screenshots, removed a redundant validation callout, and improved instruction wording throughout.
- Updated the shared "Getting Started" pages (all modules) with grammar and phrasing fixes for consistency.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-07-22

### Testing Scope

Successfully completed end-to-end lab testing and validation for Modules 1, 3, 4, and 5. Thoroughly reviewed and validated all updated lab instructions, particularly the new AMA-based connector setup, ensuring they are accurate, up to date, and aligned with the latest portal UI.

---
</details>


<details>
  <summary>2026-04-24</summary>
  
## Release Date: 2026-05-01

### Summary of Changes

Performed end-to-end lab testing and validations. Updated the lab to reflect recent UI changes, with corresponding updates made to screenshots and instructions to ensure accuracy and consistency.

### Infrastructure Changes

N/A

### Content Changes

- Updated lab instructions to align with the latest UI changes.
- Refreshed screenshots to reflect the updated interface.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-05-01

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 

---
</details>
<details>
  <summary>2026-08-28</summary>

## Release Date: 2026-08-28

### Summary of Changes
Added **Lab 08: Multi-model incident analysis and AI-generated remediation playbooks** to the **Threat Protection with XDR** course. Cost estimates updated.

# Guided Lab: Threat Protection with XDR

## UI Changes
- Getting Started page updated: Lab 08 added to the lab list, duration extended, objectives and components updated

## Content Changes
New lab added, with 7 tasks:
- **Task 1** – Provision two model deployments
- **Task 2** – Build the incident evidence package
- **Task 3** – Analyse the incident with both models
- **Task 4** – Compare findings and document divergence
- **Task 5** – Create an integration profile
- **Task 6** – Auto-create a remediation playbook
- **Task 7** – Enable the playbook and create an Enhanced Alert Trigger

Cost estimates updated for the new lab.

### Testing Scope
Built New content, feasibility tested on the same. Content updated based on the test results and completed the onboarding end to end.

</details>
