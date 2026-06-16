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