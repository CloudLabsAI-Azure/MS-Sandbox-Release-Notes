# Guided Lab: Infrastructure Migration

Welcome to the **Guided Lab: Infrastructure Migration** Readme.md. In this page, we document the updates and testing status for each module based on the latest testing cycle.

## Overview
This page includes:

- Testing status of each module  
- Content updates and fixes  
- Known issues and pending tasks  

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`  

`Email Support: cloudlabs-support@spektrasystems.com`  

# Release Notes
<details>
  <summary>2026-06-26</summary>

## Release Date: 2026-06-26

### Summary of Changes

Wrapped up another full pass across all seven modules. Everything was tested end to end, the lab guides were cleaned up for clarity, and the steps now line up with the current Azure portal UI and workflow. The biggest catch this round was on the Windows migration lab, where replication was quietly failing until we added the missing managed identity role assignment on the cache storage account — that's documented below.

## Lab 01: Discovery, Assess, and Plan - Evaluate your current environment

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-22  

### Testing Scope 

Ran the lab from start to finish and walked through every step in the guide to make sure it still holds up. Refreshed the Getting Started page with current screenshots and tidied up a few steps, plus some small wording tweaks here and there to make the flow easier to follow.

## Lab 02: Migrate Windows Servers from Hyper-V to Azure

### Content Changes

- Module tested and verified successfully  
- Updated content where required  
- Added the steps to grant the **Storage Blob Data Contributor** role to the **Data replication vault** managed identity on the migration storage account, along with new screenshots (`st-iam1.png`, `st-iam2.png`, `st-iam3-03.png`)  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-22  

### Testing Scope 

Completed the full migration flow end to end. While testing, replication kept failing because the Recovery/Data replication vault had no write access to the cache storage account. To fix this, we added a role assignment on the storage account — under Access Control (IAM), the **Storage Blob Data Contributor** role is now assigned to the **Data replication vault** managed identity. Once that was in place, replication ran cleanly. Without this managed identity permission, replication simply isn't possible, so the step is now captured in the guide with screenshots. Also refreshed the Getting Started page and made minor clarity improvements throughout.

## Lab 03: Creating VM Scale sets from Azure VMs

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-24  

### Testing Scope 

Tested the lab end to end and validated each step in the guide. Updated the Getting Started page with the latest screenshots and revised steps, with minor improvements for clarity.

Worth noting: the portal UI didn't quite match the steps as written at first, so I reached out to the TO team to understand the current experience. After exploring a couple of alternative approaches, I was able to get the lab flow working as intended.

## Lab 04: Migrate Linux Workloads from Hyper-V to Azure

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-24  

### Testing Scope 

Ran through the lab end to end and confirmed every step works as documented. Updated the Getting Started page with fresh screenshots and revised steps, plus a few small clarity tweaks along the way.

## Lab 05: Run Workloads Anywhere and manage with Azure Arc

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-24  

### Testing Scope 

Completed end-to-end testing and validated all the lab guide steps. Refreshed the Getting Started page with current screenshots and revised steps, and made minor improvements for a smoother experience.

## Lab 06: Deploy Azure Site Recover and Failover to DR

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-26  

### Testing Scope 

Tested the lab end to end, including replication, test failover, and failback, and confirmed the guide steps line up with what actually happens in the portal. Updated the Getting Started page with the latest screenshots and revised steps, along with minor clarity improvements.

## Lab 07: Secure Infrastructure workloads with Defender for Cloud

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-26  

### Testing Scope 

Ran the full lab and validated each step against the current UI. Updated the Getting Started page with fresh screenshots and revised steps, with a few minor wording improvements for clarity.

</details>


<details>
  <summary>2026-04-14</summary>

## Release Date: 2026-04-14

### Summary of Changes

Successfully completed testing across all modules. Updated lab guides, improved clarity, and ensured alignment with the latest UI and workflow.

## Lab 01: Discovery, Assess, and Plan - Evaluate your current environment

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-09  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

## Lab 02: Migrate Windows Servers from Hyper-V to Azure

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-09  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

## Lab 03: Creating VM Scale sets from Azure VMs

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-13  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

Additionally, initially connected with the TO team to understand the UI. The steps outlined in the lab were not directly performable as expected; however, I explored alternative approaches and successfully executed the lab flow as intended.

## Lab 04: Migrate Linux Workloads from Hyper-V to Azure

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-13  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

## Lab 05: Run Workloads Anywhere and manage with Azure Arc

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-13  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

## Lab 06: Deploy Azure Site Recover and Failover to DR

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-14  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

## Lab 07: Secure Infrastructure workloads with Defender for Cloud

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-14  

### Testing Scope 

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. Updated the Getting Started page with the latest screenshots and revised steps. The lab guide was enhanced with minor improvements to ensure better clarity and user experience.

</details>
