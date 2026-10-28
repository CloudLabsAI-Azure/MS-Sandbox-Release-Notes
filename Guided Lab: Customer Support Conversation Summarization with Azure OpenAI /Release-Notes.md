# Guided Lab: Customer Support Conversation Summarization with Azure OpenAI

Welcome to the **Guided Lab: Customer Support Conversation Summarization with Azure OpenAI** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-10-27</summary>
  
## Release Date: 2026-10-27

### Summary of Changes

Performed end-to-end lab testing and updated the lab guides for the latest Azure portal and Microsoft Foundry changes.

### Infrastructure Changes

N/A

### Content Changes

- Added a new **Task 1 - Create a storage account** to **Lab 01**. The Language service creation wizard's **New storage account** option creates a general-purpose v1 storage account, which Azure no longer supports. The deployment failed with a `Conflict` error on `deployStorage` (`AccountKindNotSupported`). Learners now create the `openaistorage<DeploymentID>` storage account (Standard, LRS) first.

- Updated **Task 2 of Lab 01** to select **Existing storage account** and choose `openaistorage<DeploymentID>`, instead of creating a new storage account. Removed the **Storage account type** field and renumbered the callouts.

- Updated the **Language service** (Lab 01) and **Speech service** (Lab 02) steps, as both services are now listed under **Single-capability** in the Microsoft Foundry left pane.

- Updated the **Foundry resource** creation steps in **Lab 01** and **Lab 02**, as the portal menu changed from **Use with Foundry > Foundry** to **All models, agents & tools > Microsoft Foundry**.

- Added steps in **Lab 01** and **Lab 02** to turn off the **New Foundry** toggle and dismiss the feedback pop-up. The new Foundry portal does not include the **Summarize for call center** (Language) or **Video translation** (Speech) playgrounds, so these tasks use the classic Foundry portal.

- Corrected the inject key `DeploymentID` to `Deployment-ID` in the Foundry resource steps of **Lab 01** and **Lab 02**, so the resource group and resource names display correctly.

- Renumbered the summarization task in **Lab 01** to **Task 3**, corrected the Language Studio note, fixed typos, and replaced outdated screenshots.

## Validations

Validations are passing.

### Testing Notes

- **Testing Date**: 2026-10-27

### Testing Scope 

Completed end-to-end testing of **Lab 01** with the lab policy applied. Reviewed and updated the **Lab 02** instructions for the latest portal changes.

</details>

----

<details>
  <summary>2026-05-28</summary>
  
## Release Date: 2026-05-28

### Summary of Changes

Performed end-to-end lab testing and validations, with major content updates.

### Infrastructure Changes

N/A

### Content Changes

- The content has been updated for **Lab 01**, as the Language Studio "Try it out" feature returned **Error 410 Gone** due to the retirement of API version `2023-11-15-preview`. The lab steps have been revised to use the **Microsoft Foundry Language Playground** with API version `2025-05-15-preview` for summarizing customer-agent conversations.

- Updated **Task 2 of Lab 01** to use the **"Summarize for call center"** tile in Microsoft Foundry Language Playground instead of the retired Language Studio summarization feature. The conversation input format has also been updated from plain `Agent:/Customer:` text to the required **JSON format with participant IDs**, as the Foundry playground requires structured input.

- Updated the **Lab 01 Summary** to reflect the use of Microsoft Foundry Language Playground and the latest API version instead of the retired Language Studio interface.

- The content has been updated for **Lab 02**, as the **Post Call Transcription and Analytics** feature in Speech Studio (`speech.microsoft.com/portal/callcenter`) is no longer accessible (page permanently unavailable). The lab steps have been revised to use the **Microsoft Foundry Speech Playground** with **Real-time/Fast Transcription** for audio analysis, combined with the **Language Playground "Summarize for call center"** tile for generating issue and resolution summaries.

## Validations

Validations are failing.

### Testing Notes

- **Testing Date**: 2026-05-28

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 

---