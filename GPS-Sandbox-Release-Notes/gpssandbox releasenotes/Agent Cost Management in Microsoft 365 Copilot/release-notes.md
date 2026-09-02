# Agent Cost Management in Microsoft 365 Copilot

Welcome to the **Agent Cost Management in Microsoft 365 Copilot** Release Notes. This page records changes made during the latest testing cycle, including updates to lab content, screenshots, configuration guidance, and validation/test results.

- Testing dates
- Descriptions of changes to lab infrastructure or environment
- Updates to content or documentation
- Changes to screenshots and visuals used in the lab

For any further details or inquiries, reach out to the CloudLabs support team.

**Email Support:** cloudlabs-support@spektrasystems.com

## Release Notes

<details>
  <summary>2026-08-28</summary>

## Release Date: 2026-08-28

### Summary of Changes

- Updated lab content and screenshots for clarity and UI alignment.
- Improved step-by-step instructions in Lab 2 and Lab 3 to match the current Microsoft 365 Copilot UI.
- Added a troubleshooting note about per-user monthly spending limit validation in the estimator UI.

### Infrastructure / Environment Changes

N/A — no infrastructure code or provisioning changes were made. This release only updates lab content and assets.

### Content Changes

- Replaced or added updated screenshots throughout the lab (several new media assets were added and referenced).
- Corrected spacing, heading levels, and paragraph formatting for improved readability.
- Added explicit guidance and a troubleshooting note:
  - Note added to the budgeting step: if entering a smaller per-user monthly limit (e.g. 100) fails validation in the UI, use 2000 as the minimum allowed value for the per-user spending limit (the UI enforces a higher minimum in some environments).
- Clarified sequence steps for group and owner assignment in the Microsoft 365 admin center flows.
- Minor copy edits and typo fixes across Lab 2 and Lab 3 instructions.

## Validations

- End-to-end content validation performed against the current Microsoft 365 Copilot UI and the lab sandbox environment.
- Verified that all updated steps render correctly and the screenshots correspond to the written steps.

### Testing Notes

- **Testing Date:** 2026-08-28
- **Tester(s):** CloudLabs validation team
- **Scope:** Complete run-through of Lab 2 and Lab 3 exercises referenced in the Agent Cost Management lab, including:
  - UI flows for creating and assigning groups/owners in Microsoft 365 admin center.
  - Cost Management → Configuration flow: adding spending policies, selecting users/groups, and configuring per-user monthly limits.
  - Estimator behavior and saving agent estimates.
- **Results:** Pass — no functional issues found in the lab instructions. Documentation changes and screenshots verified for accuracy.

---

</details>
