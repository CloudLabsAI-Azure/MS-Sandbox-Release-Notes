# Guided Lab: Enterprise Agentic AI with Microsoft Agent Framework

Welcome to the **Guided Lab: Enterprise Agentic AI with Microsoft Agent Framework** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-07-20</summary>

## Release Date: 2026-07-20

### Summary of Changes

Updated the lab for Microsoft Build 2026, and performed live, hands-on end-to-end testing and validation in a sandbox environment.

### Infrastructure Changes

N/A

### Content Changes

- Added Foundry User role/IAM steps required by the new Foundry portal before agent creation, and refreshed content for the new portal experience (Foundry IQ knowledge bases, Traces/Monitor tabs).
- Replaced manual runtime content-filter configuration with a real Agent Control Specification (ACS) governance manifest and Rego policy, validated via OPA and wired into the live agent.
- Added a new exercise authoring and running a Microsoft ASSERT eval spec to automatically validate A2A handoff routing and Freshdesk ticket creation.
- Redesigned the deployment exercise around the two real Foundry agent models — portal-managed agents vs. code-first agents connected via `FoundryChatClient`.
- Updated all agent-creation code to the current Microsoft Agent Framework SDK after `ChatAgent`/`AzureAIAgentClient` were renamed and removed upstream.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-07-20

### Testing Scope

Performed live, hands-on end-to-end testing of the full multi-agent system across every exercise in a real Azure/Foundry sandbox environment, including runtime governance and automated behavior validation with ASSERT. Identified and fixed real upstream Microsoft Agent Framework SDK breaking changes encountered during testing, and confirmed all lab instructions are accurate and reproducible end-to-end.

</details>

<details>
<summary>2026-10-05</summary>

## Release Date: 2026-10-05

### Summary of Changes
Moved lab files to blob storage, updated agent code to the latest package versions, and replaced Freshdesk ticketing with SharePoint.

### Infrastructure Changes
1. Moved lab files (datasets, code, telemetry) from the broken GitHub link to blob storage and updated the deployment script.
2. Updated the agent code for the latest package versions and fixed the MCP package conflict.

## Content Changes
1. Added notes and fixes to the lab guide in Exercises 2, 3, 5, and 6.
2. Replaced the Freshdesk ticket creation task with SharePoint, because Freshdesk sign-up does not accept the lab user email.

## Validations
Validations are good.

### Testing Notes
- **Testing Date**: 2026-10-05

### Testing Scope
End-to-end testing was completed. Routing, search grounding, monitoring, and ticket creation all work as expected.

---
</details>
