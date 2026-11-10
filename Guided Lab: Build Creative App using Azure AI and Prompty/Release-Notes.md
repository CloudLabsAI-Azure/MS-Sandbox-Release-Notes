# Guided Lab: Build Creative Apps using Azure AI and Prompty

Welcome to the **Guided Lab: Build Creative Apps using Azure AI and Prompty** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-11-10</summary>

## Release Date: 2026-11-10

### Summary of Changes

Completed end-to-end testing of the Build Creative App using Azure AI and Prompty lab. Fixed the environment setup so the lab code reaches the VM, fixed the Exercise 3 backend error, and updated the lab guide with the testing feedback.

### Infrastructure Changes

- Fixed the setup script (`psscript.ps1`). It now creates `C:\LabFiles`, downloads the logon script there, and registers the logon task correctly.

- Fixed the logon task script (`logon.ps1`). The lab code is now downloaded as a zip file and extracted to `C:\creative-writer`, because the code repository is private and the previous `git clone` step failed.

- The logon task now installs the API packages, checks that the application dependencies load, and reports the deployment status as Succeeded or Failed.

### Code Changes

- Pinned the OpenTelemetry and Azure Monitor package versions in `src/api/requirements.txt`. This fixes the "Promptflow may not installed correctly" error when the backend starts in Exercise 3.

- Removed committed cache files and an old evaluation results file from the code package.

### Content Changes

- Updated step instructions to match the current Visual Studio Code and terminal flow.

- Updated code snippets in the lab guide to match the current application code.

- Corrected typos and wording across the lab guide.

## Validations

The deployment status check reports correctly after setup.

### Testing Notes

- **Testing Date**: 2026-11-09

### Testing Scope

Completed end-to-end testing on a fresh deployment.

</details>

---

<details>
  <summary>2026-06-02</summary>

## Release Date: 2026-06-02

### Summary of Changes

Successfully completed end-to-end testing and validation of the complete lab environment, including minor content updates.

### Infrastructure Changes

- N/A

### Content Changes

- Updated screenshots and step instructions based on the latest UI changes for a better user experience.

- Updated the lab 04 content because of depricated models.

- Corrected typo errors and improved overall wording consistency across the lab guide.


## Validations

The validations are good.

### Testing Notes

- **Testing Date**: 2026-06-02

### Testing Scope

Successfully completed end-to-end testing of the complete lab, including validation, exercise flow validation, screenshot verification, content review, model update verification, and validation testing.

</details>