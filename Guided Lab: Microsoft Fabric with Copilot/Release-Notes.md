# Microsoft Fabric with Copilot

Welcome to the **Microsoft Fabric with Copilot** Release-Notes. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, and other relevant changes for the lab.

## Overview

This Page contains detailed notes about the latest updates and modifications made after each testing cycle. It includes:
`
- Testing dates
- Descriptions of changes to lab infrastructure
- Updates to content or documentation
- Changes to screenshots and visuals used in the lab

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`
`Email Support: cloudlabs-support@spektrasystems.com`

# Release Notes
<details>
  <summary>2026-10-29</summary>

## Release Date: 2026-10-29

### Summary of Changes

- Tested the lab end to end and updated all guides, screenshots and the architecture diagram to match the current Microsoft Fabric and Copilot UI. The lab now runs on a provided Fabric F2 capacity instead of the Fabric trial.

### Infrastructure Changes

- Updated the JumpVM size SKU to **Standard_D2s_v5**.

### Content Changes

- Removed the Fabric trial sign-up. Exercise 1 now creates the workspace on the lab's F2 capacity, which comes with a Power BI Pro licence and enables Copilot. Getting Started now covers Fabric sign-in with a Temporary Access Pass, and the Azure subscription prerequisite and the lab-extension section are removed.
- Exercise 2 now has learners create their own Direct Lake semantic model, because lakehouses no longer get a default one. It also adds the Copy job connection sign-in and the current lakehouse navigation.
- Exercise 3 adds a manual fallback for when Copilot splits the **Item** column only at the first space. The overview now makes clear the dataflow is not published.
- Exercise 4 runs the three create-dw script files in order, which prevents a broken SQL script. It also corrects the warehouse, data preview, relationship and Copilot report steps to match the current UI.
- Aligned UI labels and callout numbers with the current Fabric UI, and fixed spelling and wording across all exercises.

### Screenshot Update

- Refreshed outdated screenshots and the lab architecture diagram to match the latest UI and lakehouse naming, with deployment-specific values blurred.

### Testing Notes

- **Testing Date**: 2026-10-29

### Testing Scope

- Conducted end-to-end testing of all four exercises in a live lab environment. All validations succeeded, and every guide change was confirmed against the live UI.

</details>


<details>
  <summary>2026-04-16</summary>

## Release Date: 2026-04-16

### Summary of Changes 

-  Updated the lab guide for improved clarity and accuracy, enhancing the overall user experience.

### Infrastructure Changes

- NA

### Content Changes

- Refined a few instructions to improve clarity and enhance the overall user experience.

- All instructions have been verified to match the existing lab flow, and no new instructions were added.

### Screenshot Update

- All screenshots have been validated to align with the latest UI, with no additional screenshots introduced.
  
### Testing Notes

- **Testing Date**: 2026-04-16

### Testing Scope 

- Conducted end-to-end testing of the lab environment. The lab guide was updated with few screenshots and minor improvements to ensure better clarity and user experience

</details>
