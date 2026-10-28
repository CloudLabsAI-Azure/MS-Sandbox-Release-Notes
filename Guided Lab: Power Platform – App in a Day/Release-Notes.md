# Guided Lab: Power Platform – App in a Day

Welcome to the **Guided Lab: Power Platform – App in a Day** Readme.md. In this page, we document the updates and testing status based on the latest testing cycle.

## Overview
This page includes:

- Testing status of the lab  
- Content updates and fixes  
- Known issues and resolutions  

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`  

`Email Support: cloudlabs-support@spektrasystems.com`  

# Release Notes
<details>
  <summary>2026-10-28</summary>

## Release Date: 2026-10-28

### Summary of Changes

Learners now create the Contoso Test environment themselves in the Pre-Requisites, instead of relying on the pre-created environment that failed to appear in the previous cycle. This release also covers the team's May–October content updates. The lab was tested end to end, steps that broke against the current UI were fixed, screenshots were refreshed, and all pages were polished for clarity and consistency.

## Lab: Power Platform – App in a Day

### Infrastructure Changes

Worked on changing the psscript to exclude logon script that comprised of creating an environment which caused failures. Now the user creates the environment themselves.

### Content Changes

- Pre-Requisites now includes creating the **Contoso Test** trial environment with Dataverse in the new Power Platform admin center, and the optional mobile-app install task is removed. Estimated duration changed from 10 to 20 minutes.
- Fixed steps that no longer matched the current UI: exact Properties pane position and size values for the drag-only canvas steps, the form field list, the people-picker **Use dynamic content** fields, the **fx** expression fallback, **My flows**, and the Approvals center **Sent** and **History** tabs. Approver is now auto-filled from the signed-in user.
- Added guidance for known stumbling points: browser pop-up blocking, the Calculated column deprecation banner, switching to the Device Procurement business process when it isn't shown, quoting text values in Power Fx, and using flow **Test > Manually** to pick up requests right away.
- Added a Lab Scenario to each module, and rewrote the Getting Started objectives, the architecture text and the module overviews to match what the lab actually builds.
- Added and refreshed about 120 screenshots to match the current UI, aligned callout numbers with the screenshots, fixed rendering issues, and standardized wording, headings and summaries across all pages.

### Validations

N/A

### Testing Notes

- **Testing Date**: 2026-10-28

### Testing Scope

Completed all four modules end to end in a live lab environment, from environment creation through the Power Automate approval and rejection paths. The lab flow and the step order are unchanged.

---

</details>

<details>
  <summary>2026-04-23</summary>

## Release Date: 2026-04-23

### Summary of Changes

Initially connected with Disha to understand the environment issue, as the pre-created Contoso Test environment was not visible under Dataverse. The issue was identified as caused by the CloudLabs manual agent not working properly, as mentioned by Disha. It was identified that a script needed to be executed. The script was run for the environment manually, after which the Contoso Test environment became available.

Successfully completed end-to-end lab testing with no issues identified. Disha is currently checking further on the issue related to the CloudLabs manual agent.

## Lab: Power Platform – App in a Day

### Content Changes

- Lab tested and verified successfully  

### Validations

NA

### Testing Notes

- **Testing Date**: 2026-04-23  

### Testing Scope

Successfully completed end-to-end testing of the lab environment and validated all lab guide steps. No issues were observed post environment fix, and the lab flow executed as expected.

</details>
