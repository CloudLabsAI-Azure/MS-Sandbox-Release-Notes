# Building Intelligent AI Agents with Microsoft Foundry

Welcome to the **Building Intelligent AI Agents with Microsoft Foundry** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-19</summary>
  
## Release Date: 2026-08-19

### Summary of Changes

Updated the lab to align with the current Microsoft Foundry experience. The retired AI Hub + Project architecture has been replaced with the unified Foundry resource, all model deployments have been refreshed to the latest models, and the environment configuration and tracing setup have been reworked accordingly.

### Infrastructure Changes

- Replaced the **Azure AI Hub + separate Foundry Project** creation flow with a single **Foundry resource** that provisions a default project, as the Hub-based path is no longer available.

- Updated the GPT model from **GPT-4.1** to **GPT-5.5**.

- Updated the DeepSeek model from **DeepSeek-R1** to **DeepSeek-V4-Flash**.

- Updated the Phi model from **Phi-4** to **Phi-4-reasoning**, and applied the 50K TPM rate limit to this deployment.

- Added steps to enable the **system-assigned managed identity** on the Azure AI Search resource, and to assign the **Cognitive Services OpenAI User** role on the Foundry resource to both the ODL user and the Search service identity.

- Added **Application Insights** provisioning from the Azure portal for tracing, replacing the retired *Tracing > Create new* option in the Foundry portal.

### Content Changes

- Updated the lab guide content based on the infrastructure change and testing feedback.

- Fixed the typos and grammatical errors identified during lab testing.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-08-19

### Testing Scope 

Successfully completed end-to-end lab testing and validation across all five challenges. Verified the unified Foundry resource creation, all four model deployments (GPT-5.5, text-embedding-3-large, DeepSeek-V4-Flash, and Phi-4-reasoning), the AI Search and Bing grounding connections, role assignments, the updated `.env` configuration, the Foundry Agent RAG flow, and Application Insights tracing. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

</details>