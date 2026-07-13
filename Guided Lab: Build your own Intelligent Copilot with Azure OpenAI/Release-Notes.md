# Guided Lab: Build your own Intelligent Copilot with Azure OpenAI

Welcome to the **Guided Lab: Build your own Intelligent Copilot with Azure OpenAI** Readme.md. In this page, we document the updates and testing status for each module based on the latest testing cycle.

## Overview
This page includes:

- Testing status of each module  
- Content updates and fixes  
- Known issues and pending tasks  

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`  

`Email Support: cloudlabs-support@spektrasystems.com`  

# Release Notes

<details>
  <summary>2026-07-13</summary>

## Release Date: 2026-07-13

### Summary of Changes

Successfully completed comprehensive migration from Azure OpenAI portal to Microsoft Foundry portal, updated all model deployments from GPT-4.1 to GPT-5 series, and refreshed user interface documentation to align with the latest Azure portal experience.

### Infrastructure Changes

**Portal Migration**
- Migrated all lab resources from "Azure OpenAI" to "Microsoft Foundry" portal interface
- Updated navigation flows across Labs 1-3 and getting-started guides
- Transitioned from classic portal UI to **new Foundry experience**
- Removed deprecated "New Foundry toggle" instructions as the new interface is now standard

**Model Updates**
- Upgraded deployment model versions from GPT-4.1/GPT-4.1-mini to **GPT-5.4** (Lab 1)
- Updated GPT-5 series references across Labs 2-3 (GPT-5.2 specifications)
- Updated embedding models from **ada-002** to **text-embedding-3-small** in configuration files
- Modified deployment names and capacity configurations to reflect new Foundry standards

### Content Changes

**Lab 1 (Chat Application Setup)**
Switched portal nav/UI from Azure OpenAI to Foundry (resource creation, deployment flow, Home tab endpoint/key retrieval); updated model to gpt-5.4 (Global Standard) and fixed deployment name/secrets config.

**Lab 2 (Function Calling Setup)**
Updated portal nav to Foundry, model verification path to Build > Models, and API config (`OPENAI_API_BASE`→`OPENAI_API_ENDPOINT`, config.json params); fixed "Runnning" typo and summary wording.

**Lab 3 (HR/Payroll Copilot)**
Updated portal nav to Foundry workflow, model to GPT-5, embedding to text-embedding-3-small (incl. Cognitive Search vector config, removed API key auth); updated Bicep params and fixed step numbering/formatting.


### Minor Fixes

- Fixed formatting inconsistencies and improved visual spacing
- Corrected typos: "Micosoft" → "Microsoft", "example question ." → "example question."
- Improved step numbering and sequence consistency
- Enhanced code block formatting for environment variable instructions
- Updated placeholder text for consistency across all labs
- Removed obsolete navigation toggles and deprecated UI references
- Fixed line-ending issues and removed trailing spaces

### Code Compatibility Updates

- **API Configuration**: Updated all code references to use new Foundry API endpoints and authentication methods
- **Model Deployment**: Updated Python configuration files to reference GPT-5.4 deployment names
- **Embedding Models**: Updated all embedding model references from ada-002 to text-embedding-3-small in code samples
- **Environment Variables**: Updated all `.env` configuration examples to match new Foundry standards
- **Bicep Infrastructure**: Updated IaC templates to deploy with new Foundry resource configurations

## Validations

Validations are good for all labs.

### Testing Notes

- **Testing Date**: 2026-07-13
- **Portal Tested**: Microsoft Foundry (new portal interface)
- **Models Tested**: GPT-5.4 deployment and verification
- **End-to-End Validated**: All three labs with updated portal workflow

### Key Improvements

- **Unified Portal Experience**: All labs now use consistent Microsoft Foundry navigation
- **Modern Model Support**: Upgraded to lifecycle-supported GPT-5 series models
- **Clearer Documentation**: Simplified step-by-step instructions with new portal workflows
- **Better API Integration**: Updated to match latest Azure OpenAI Foundry API specifications
- **Enhanced User Experience**: Removed deprecated UI elements and streamlined configuration process

</details>


<details>
  <summary>2026-06-09</summary>

## Release Date: 2026-06-09

### Summary of Changes

Successfully completed end-to-end testing and validation of the complete lab environment, including minor content updates.

### Infrastructure Changes

- N/A

### Content Changes

- Updated screenshots and step instructions based on the latest UI changes for a better user experience.

- Corrected typo errors and improved overall wording consistency across the lab guide.


## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-06-09

### Testing Scope

Successfully completed end-to-end testing of the complete lab, including validation, exercise flow validation, screenshot verification, content review, model update verification, and validation testing.

</details>

<details>
  <summary>2026-02-23</summary>

## Release Date: 2026-02-23

### Summary of Changes

Performed testing across modules and updated lab content where required to align with the latest UI and workflow.

## Lab 1: Getting Started with Building a Chat Application

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-02-23

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Lab 2: Understand function calling in OpenAI GPT

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-02-23

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Lab 3: Deploy and Run the HR/Payroll Copilot Application

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-02-23

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

</details>

<details>
  <summary>2026-05-19</summary>

## Release Date: 2026-05-19

### Summary of Changes

Performed end-to-end testing across all modules and validated the overall lab functionality. Major UI changes were identified in Lab 3 and the corresponding content and screenshots were updated to align with the latest Azure experience.

## Lab 1: Getting Started with Building a Chat Application

### Content Changes

- Module tested and verified successfully.
- Reviewed lab content, screenshots, and functionality.
- No content changes were required.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-05-19

### Testing Scope

Successfully completed end-to-end testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and functioning as expected.

## Lab 2: Understand Function Calling in OpenAI GPT

### Content Changes

- Module tested and verified successfully.
- Reviewed lab content, screenshots, and functionality.
- No content changes were required.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-05-19

### Testing Scope

Successfully completed end-to-end testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and functioning as expected.

## Lab 3: Deploy and Run the HR/Payroll Copilot Application

### Content Changes

- Module tested and verified successfully.
- Identified major UI changes in **Task 2: Integrate Azure Cognitive Search with your Application**.
- Cross-checked the latest workflow and updated the lab guide instructions accordingly.
- Refreshed screenshots to align with the current Azure portal experience.
- Updated navigation steps impacted by the UI changes.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-05-19

### Testing Scope

Successfully completed end-to-end testing and validation. Reviewed the updated workflow, validated all module functionality, and confirmed that the revised instructions and screenshots accurately reflect the current experience.

</details>
