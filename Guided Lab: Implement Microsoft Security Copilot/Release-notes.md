# Guided Lab: Implement Microsoft Security Copilot

Welcome to the **Guided Lab: Implement Microsoft Security Copilot** Readme.md. In this page, we document the updates and testing status for each module based on the latest testing cycle.

## Overview
This page includes:

- Testing status of each module  
- Content updates and fixes  
- Known issues and pending tasks  

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`  

`Email Support: cloudlabs-support@spektrasystems.com`  

# Release Notes

<details>
  <summary>2026-05-22</summary>

## Release Date: 2026-05-22

### Summary of Changes

Successfully completed end-to-end testing and validation across all guided lab modules for Day 01, Day 02, and Day 03. Updated the lab guides with the latest UI enhancements, Environment tab changes, workflow corrections, updated screenshots, navigation improvements, and the latest Microsoft Defender portal UI updates to align with the current portal experience.

# Guided Lab: Day 1 - Implement Microsoft Security Copilot

## UI Changes

- Updated the lab guide based on the latest Microsoft Defender portal UI changes  
- Revised screenshots, navigation flow, and portal steps to align with the latest Defender portal experience  
- Updated the Getting Started page with the latest Environment tab UI changes  

## Content Changes

Completed end-to-end testing for Day 01 labs and all validations were validated successfully. Updated the lab guide content wherever required to align with the latest portal workflows and UI experience.

## Validations

All validations completed successfully.

### Testing Notes

- **Testing Date**: 2026-05-20

### Testing Scope

Completed end-to-end testing for Day 01 labs and all validations succeeded successfully. Updated the Getting Started page with the latest UI changes for the Environment tab and incorporated the latest Microsoft Defender portal UI updates across the lab guide.

# Guided Lab: Day 2 - Implement Microsoft Security Copilot

## UI Changes

- Updated the lab guide based on the latest Microsoft Defender portal UI changes  
- Revised screenshots, navigation flow, and portal steps to align with the latest Defender portal experience  
- Updated the Getting Started page with the latest Environment tab UI changes  

## Content Changes

Completed end-to-end testing for Day 02 labs and all validations were validated successfully. Updated the lab guide content wherever required to align with the latest portal workflows and UI experience.

## Validations

All validations completed successfully.

### Testing Notes

- **Testing Date**: 2026-05-21

### Testing Scope

Completed end-to-end testing for Day 02 labs and all validations succeeded successfully. Updated the Getting Started page with the latest UI changes for the Environment tab and incorporated the latest Microsoft Defender portal UI updates across the lab guide.

# Guided Lab: Day 3 - Implement Microsoft Security Copilot

## UI Changes

- Updated the lab guide based on the latest Microsoft Defender portal UI changes  
- Revised screenshots, navigation flow, and portal steps to align with the latest Defender portal experience  
- Updated the Getting Started page with the latest Environment tab UI changes  

## Content Changes

Completed end-to-end testing for Day 03 labs and all validations were validated successfully. Updated the lab guide content wherever required to align with the latest portal workflows and UI experience.

## Validations

All validations completed successfully.

### Testing Notes

- **Testing Date**: 2026-05-22

### Testing Scope

Completed end-to-end testing for Day 03 labs and all validations succeeded successfully. Updated the Getting Started page with the latest UI changes for the Environment tab and incorporated the latest Microsoft Defender portal UI updates across the lab guide.

</details>

<details>
  <summary>2026-08-19</summary>

## Release Date: 2026-08-19

### Summary of Changes

Added **Lab 12: Extending Microsoft Security Copilot with the Microsoft Sentinel MCP Server** to Day 03.

# Guided Lab: Day 3 - Implement Microsoft Security Copilot

## UI Changes

- Getting Started page updated: Lab 12 added to the Day 03 lab list, duration extended, MCP Server and Model Context Protocol concepts added to the objectives and component sections
- No changes made to Labs 07–11; Lab 12 references them read-only where relevant

## Content Changes

New lab added, structured as 4 tasks:

- **Task 1** – Build a custom Security Copilot agent and add Microsoft Sentinel's MCP tool collection from the agent Tools catalog
- **Task 2** – Publish the agent and connect its plugins
- **Task 3** – Review MCP extensibility and three investigation prompts *(read only — see Known Issues)*
- **Task 4** – Configure the agent to monitor a Microsoft Sentinel watchlist on a schedule *(enrichment step read only — see Known Issues)*

### Testing Scope

Completed for Tasks 1 and 2. Task 3 and Task 4's watchlist, KQL tool, trigger, publish, and run mechanics were exercised successfully; the agent's MCP-driven enrichment step was not.

### Known Issues

- **Microsoft Sentinel MCP tools return `404 (Not Found)` on invocation**, due to Sentinel data lake unavailability in the current region. Affects Task 3 and Task 4's enrichment step.

</details>
