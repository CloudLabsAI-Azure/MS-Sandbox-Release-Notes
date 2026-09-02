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
  <summary>2026-08-13</summary>

## Release Date: 2026-08-13

### Summary of Changes

Completed a testing and validation cycle for the Guided Lab: *Migrate and Modernize .NET Apps & SQL DB to Azure*. Updates in this cycle focused on lab permissions, resource provider prerequisites, CI/CD pipeline reliability, and a full editorial pass across all exercises.

### Infrastructure Changes

1. Updated the custom **RBAC role** and **Azure Policy** applied to the lab user to include the permissions required for monitoring and observability resources, resolving authorization failures encountered while configuring **Application Insights** and its associated **Log Analytics workspace**.

2. Confirmed and documented the **Azure Migrate Owner** role requirement at the resource group scope for the lab user, along with the supporting RBAC and policy configuration needed for Azure Migrate project creation.

3. Documented the **resource provider registration** prerequisites that must be completed at the subscription level by the subscription owner, as these cannot be granted through a resource group–scoped role assignment.

4. Updated the **GitHub Actions workflow template** used by the CI/CD exercise so that the build runs on a compatible hosted runner, resolving a build agent failure during application deployment to the staging slot.

## Content Changes

1. Updated the Application Insights configuration guidance to align with the current Azure portal behavior and the resources provisioned in the lab environment.

2. Updated the CI/CD pipeline exercise, including the workflow file content and the accompanying deployment instructions.

3. Corrected step numbering and sequencing issues across multiple exercises, and aligned in-step callout references with the corresponding screenshots.

4. Refreshed tool and service references to match current versions and portal navigation, and updated screenshots where the UI had changed.

5. Performed an editorial pass across all exercises to improve clarity, consistency, and readability of the lab instructions, without changing the steps performed by the participant.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-08-13

### Testing Scope

Successfully completed end-to-end testing and validation of the lab. Verified permission and policy configurations, Azure Migrate and Load Testing resource creation, database assessment and migration workflows, CI/CD deployment through GitHub Actions, monitoring configuration, and network security exercises.

### Additional Notes

- Permission-related blockers identified during testing were resolved through updates to the custom RBAC role and policy, and through subscription-level prerequisites documented for the onboarding team.
- Lab testing completed successfully.

</details>


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
