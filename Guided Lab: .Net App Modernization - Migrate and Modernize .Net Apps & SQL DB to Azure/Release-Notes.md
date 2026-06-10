# Guided Lab: .Net App Modernization - Migrate and Modernize .Net Apps & SQL DB to Azure

Welcome to the **Guided Lab: .Net App Modernization - Migrate and Modernize .Net Apps & SQL DB to Azure** Readme.md. On this page, we document the updates and testing status for each module from the latest testing cycle.

## Overview
This page includes:

- Testing the status of each module  
- Content updates and fixes  
- Known issues and pending tasks  

For any further details or inquiries, feel free to reach out to the CloudLabs support team.

Email Support: cloudlabs-support@spektrasystems.com

# Release Notes

<details>
  <summary>2026-05-29</summary>

## Release Date: 2026-05-29

### Summary of Changes

Completed end-to-end lab testing and validation for the Guided Lab: *Migrate and Modernize .NET Apps & SQL DB to Azure*. Major updates and fixes were implemented to address authentication, permissions, and validation-related issues impacting the lab experience.

### Infrastructure Changes

1. Updated the lab authentication flow by replacing **MFA-based access** with **Personal Access Token (PAT)** authentication for the lab user to ensure uninterrupted lab execution.

2. Addressed permission-related issues preventing users from creating the **Azure Migrate** service by coordinating on the creation and validation of custom **RBAC roles** and **Azure Policies** required for the lab environment.

## Content Changes

1. Updated lab guidance and supporting instructions related to authentication and Azure Migrate resource creation workflows.

2. Refined configuration and deployment steps to improve clarity and reduce potential permission-related blockers during lab execution.

3. Minor improvements were made across the lab instructions to align with the latest Azure portal behavior and deployment experience.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-05-18

### Testing Scope

Successfully completed end-to-end testing and validation of the lab. Verified authentication flow updates, Azure Migrate service creation permissions, RBAC and policy configurations, and migration workflows for .NET applications and SQL databases.

### Additional Notes

- Resolved a validation failure encountered in **Exercise 04 – Migrate On-Premises Database to Azure SQL Database** after investigation and fixes coordinated through the validation team.
- Lab testing completed successfully.

</details>
