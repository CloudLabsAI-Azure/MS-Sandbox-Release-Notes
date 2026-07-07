# Guided Lab: Developing Cloud-Native Applications Using Microsoft Azure Cosmos DB

Welcome to the **Guided Lab: Developing Cloud-Native Applications Using Microsoft Azure Cosmos DB** Readme.md. In this page, we document the updates and testing status for each module based on the latest testing cycle.

## Overview
This page includes:

- Testing status of each module  
- Content updates and fixes  
- Known issues and pending tasks  

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`  

`Email Support: cloudlabs-support@spektrasystems.com`  

# Release Notes

<details>
  <summary>2026-03-24</summary>

## Release Date: 2026-03-24

### Summary of Changes

Performed testing across modules, resolved connectivity issue in Azure Functions, and updated lab content where required.

## Module 1: Explore Azure Cosmos DB

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-03-23

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 2: Migrate Existing Data using Azure Data Factory

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-03-23

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 3: Connect & Configure to Azure Cosmos DB for NoSQL with the SDK

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-03-23

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 4: Move Multiple Documents in Bulk with the Azure Cosmos DB for NoSQL SDK

### Content Changes

- Module tested and verified successfully  
- Updated content where required  

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-03-24

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 5: Process Azure Cosmos DB for NoSQL Data using Azure Functions

### Content Changes

- Resolved connection issue by using **Primary Connection String** instead of Endpoint and Key  
- Successfully connected and retrieved data from the database  

## Validations

Validations are successful after fix.

### Testing Notes

- **Testing Date**: 2026-03-24

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

</details>

<details>
  <summary>2026-06-26</summary>

## Release Date: 2026-06-26

### Summary of Changes

Performed end-to-end testing across all modules, resolved validation and environment issues identified during testing, and updated lab content where required.

## Module 1: Explore Azure Cosmos DB
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-18
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 2: Migrate Existing Data using Azure Data Factory
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-18
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 3: Connect & Configure to Azure Cosmos DB for NoSQL with the SDK
### Content Changes
- Investigated the reported connect & configure issue with the SDK — root cause identified: the Cosmos DB Emulator consumes 2.50 GB of RAM on a 4 GB VM, causing the environment to run out of memory
- Updated the VM size configuration to `"vmSize": "Standard_D4s_v3"` to resolve the memory constraint
- Updated the VM agent
- Module tested and verified successfully after the fix
## Validations
Validation check completed; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-26
### Testing Scope
Successfully completed end-to-end lab testing and validation, including a dedicated issue check for the SDK connection and configuration steps.

## Module 4: Create and Update Documents with the Azure Cosmos DB for NoSQL SDK
### Content Changes
- Identified validation stuck in "in-progress" state during testing
- Updated the VM agent to resolve the validation issue — connected with Riya, updated, and got it reviewed on the same
## Validations
Validation issue resolved after the VM agent update; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-22
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 5: Batch Multiple Point Operations Together with the Azure Cosmos DB for NoSQL SDK
### Content Changes
- Identified validation stuck in "in-progress" state during testing
- Updated the VM agent to resolve the validation issue — connected with Riya, updated, and got it reviewed on the same
## Validations
Validation issue resolved after the VM agent update; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-22
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 6: Move Multiple Documents in Bulk with the Azure Cosmos DB for NoSQL SDK
### Content Changes
- Identified validation stuck in "in-progress" state during testing
- Updated the VM agent to resolve the validation issue — connected with Riya, updated, and got it reviewed on the same
## Validations
Validation issue resolved after the VM agent update; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-22
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 7: Execute a Query with the Azure Cosmos DB for NoSQL SDK
### Content Changes
- Identified validation stuck in "in-progress" state during testing
- Updated the VM agent to resolve the validation issue — connected with Riya, updated, and got it reviewed on the same
## Validations
Validation issue resolved after the VM agent update; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-23
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 8: Review the Default Index Policy for an Azure Cosmos DB
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-23
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 9: Process Azure Cosmos DB for NoSQL Data using Azure Functions
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-23
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 10: Search Data using Azure Cognitive Search
### Content Changes
- Identified validation issue during testing — "Build indexer and index for Azure Cosmos DB NoSQL API data" validation was failing with no failure reason being displayed
- Connected with Arun and got the validation issue fixed on the same
## Validations
Validation issue resolved; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-24
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 11: Optimize an Azure Cosmos DB for NoSQL
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-24
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 12: Use Azure Monitor to Analyze an Azure Cosmos DB for NoSQL Account
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-25
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 13: Create a Stored Procedure with the Azure Portal
### Content Changes
- Module tested and verified successfully
- Updated content where required
## Validations
Validations are good.
### Testing Notes
- **Testing Date**: 2026-06-25
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

## Module 14: Implement and Use User-Defined Functions with the SDK
### Content Changes
- Identified validation stuck in "in-progress" state during testing
- Updated the VM agent to resolve the validation issue — connected with Riya, updated, and got it reviewed on the same
## Validations
Validation issue resolved after the VM agent update; validations are good.
### Testing Notes
- **Testing Date**: 2026-06-25
### Testing Scope
Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.
</details>
