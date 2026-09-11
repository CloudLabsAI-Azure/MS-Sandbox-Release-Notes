# Call Center data analysis using Azure AI services and Azure OpenAI

Welcome to the **Call Center data analysis using Azure AI services and Azure OpenAI** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

## Overview
This page contains detailed notes about the latest updates and modifications made after each testing cycle. It includes:

- Testing dates
- Descriptions of changes to lab infrastructure
- Updates to content or documentation
- Changes to screenshots and visuals used in the lab

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`

`Email Support: cloudlabs-support@spektrasystems.com`

# Release Notes

<details>
  <summary>2026-09-10</summary>

## Release Date: 2026-09-10

### Summary of Changes

Corrected the lab guide to match the current deployment assets and Azure portal experience: fixed the ARM template file name and parameter label used in Challenge 1, switched the sample audio file referenced across Challenges 4 and 5. Replaced the Getting Started screenshots affected by the Environment tab UI changes.

### Infrastructure Changes

No infrastructure changes. The lab now references the renamed deployment template `azuredeploy-01.json` (previously `azuredeploy-logicapp.json`).

### Content Changes

- **Getting Started:** Sign-in step now instructs learners to enter a **Temporary Access Pass** instead of a password; refreshed the `gs-leave-2.png` and `gs-leave-3.png` screenshots for the updated Environment tab UI.
- **Challenge 1:** Updated the custom template file name and deployment parameter label; added a note pointing learners to the Environment tab for any additional values; model verification now routes through the **Microsoft Foundry portal > Model deployments**, with a note on turning off the new Foundry experience toggle when the portal opens on the project creation screen instead of the existing resource.
- **Challenge 3:** Minor formatting fix in the Logic App run history steps.
- **Challenge 4:** Replaced references to `bad_review.wav` with `Call_apply_loan.wav` in the transcript review step and the SQL comparison query.
- **Challenge 5:** Replaced `bad_review` with `Call_apply_loan` in the row-validation steps and the `SELECT Summary` query.
- **Challenge 6:** Power BI report save step now uses **File > Save As** instead of **File > Save**.

### Validations

Challenge 5 validation is not working, will look into that in next cycle, except all validations are working fine.

### Testing Notes

- **Testing Date**: 2026-09-10

### Testing Scope

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes.

</details>