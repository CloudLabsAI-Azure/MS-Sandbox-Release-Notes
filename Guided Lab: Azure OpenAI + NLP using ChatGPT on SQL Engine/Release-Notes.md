# Guided Lab: Azure OpenAI + NLP using ChatGPT on SQL Engine

Welcome to the **Guided Lab: Azure OpenAI + NLP using ChatGPT on SQL Engine** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-07-15</summary>

## Release Date: 2026-07-15

### Summary of Changes

Language and clarity pass across the lab guide, along with codebase updates to support the new Foundry portal, Foundry API endpoints, and GPT 5.4 model as well as the Build '26 updates including the codebase update.

### Infrastructure Changes

N/A

## Content Changes

* Expanded the overview, objectives, task intros, and summaries across the getting-started page and both exercises to more clearly describe what the reader builds and why.

* Updated Exercise 1 to reflect the resource-creation, project-setup, and model-deployment flow in the new Foundry portal, and corrected step numbering and callout inconsistencies.

* Updated Exercise 2 wording for the SQL Query Writing Assistant and Data Analysis Assistant walkthrough, including the token-per-minute rate-limit note.

### Codebase Changes

* Updated the application configuration to use the new Foundry API endpoint format (`.../openai/v1`) and the new GPT model deployment name.

* Aligned the guide's `secrets.env` and model-deployment instructions with the updated endpoint and GPT model.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-07-14

### Testing Scope

Reviewed and validated all lab instructions end to end, ensuring they are accurate, up to date, and aligned with the new Foundry portal, Foundry API endpoints, and GPT model.

</details>

<details>
  <summary>2026-06-25</summary>
  
## Release Date: 2026-06-25

### Summary of Changes

Performed end-to-end lab testing with minor content updates and fixes.

### Infrastructure Changes

N/A

## Content Changes

* Updated the RBAC and policy for the lab, as there were a few updates in resource creation.

* Updated the lab guide to reflect the new UI changes in the Foundry portal.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-25

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 
</details>

<details>
  <summary>2026-06-09</summary>
  
## Release Date: 2026-06-09

### Summary of Changes

Performed end-to-end lab testing.

### Infrastructure Changes

N/A

## Content Changes

No major changes identified, the lab flow is good and the content is well structured.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-09

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 
</details>


<details>
  <summary>2026-05-18</summary>
  
## Release Date: 2026-05-18

### Summary of Changes

Performed end-to-end lab testing using the latest updates from the Foundry portal.

### Infrastructure Changes

N/A

## Content Changes

1. Tested the lab end-to-end; based on the changes in the Microsoft Foundry portal, updates have been made accordingly, and the UI has also been updated.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-05-18

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 

---
</details>

<details>
  <summary>2026-04-07</summary>
  
## Release Date: 2026-04-07

### Summary of Changes

Performed end-to-end lab testing with minor updates and fixes.

### Infrastructure Changes

N/A

## Content Changes

1. Tested the lab end-to-end and identified an issue with the **App Service quota**.

2. The issue was caused by a hardcoded region in the **Bicep file**, which did not align with the deployment region.

3. Updated the Bicep configuration to dynamically use the region where the resources are deployed.

4. Minor updates were made to ensure smoother deployment and consistency with the current setup.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-07

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 

---
</details>