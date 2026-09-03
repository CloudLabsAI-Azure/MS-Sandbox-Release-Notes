# Know Your Data: Discover, Classify, and Protect Sensitive Information with Microsoft Purview

Welcome to the **Know Your Data: Discover, Classify, and Protect Sensitive Information with Microsoft Purview** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-11</summary>

## Release Date: 2026-08-11

### Summary of Changes

Onboarded this lab as a 6 hour Hack in a Day on Microsoft Purview. Learners act as data security engineers at fictional Zava, discovering sensitive data, classifying it with sensitivity labels and auto-labeling, protecting it with DLP, and detecting insider risk across four challenges. Testing found all four challenges had been written for a pre-seeded tenant, so each was reworked to have learners generate their own evidence. The validation scripts were rebuilt after several were found to pass incorrect work or fail correct work.

### Infrastructure Changes

- Added the Entra directory commands to enable **sensitivity labels for Microsoft 365 groups and sites**, which has no portal equivalent. Without it the Groups & sites controls stay unavailable and Challenge 2 Task 1 cannot be completed.

- Completed the Purview tenant configuration the lab depends on: sensitivity labels created and published, auto-labeling policy in simulation across Exchange, SharePoint and OneDrive, both DLP policies, and the insider risk policy.

- Removed **endpoint DLP blocking** from scope. It needs an onboarded device, which this environment does not provide, so Challenge 3 is now scored on the policy configuration.

- Removed **Microsoft Security Copilot** references, as it is not provisioned in this environment.

- Raised the exhausted **VM runtime limit** with CloudLabs. The lab now needs the VM for one step only and could be made fully browser-based if container labelling is enabled during tenant preparation.

### Content Changes

- Rewrote all four challenge guides so learners create the data they later discover, classify, protect and investigate.

- Corrected the label name in Challenge 2, where the guide instructed learners to apply **Zava Confidential** while the validator grades **Zava Highly Confidential**.

- Stated explicitly how the DLP rule conditions combine in Challenge 3, which as written could never match the content created in Challenge 1.

- Rewrote Challenge 4 around the HR connector dependency, as the departing-user template only raises alerts once a connector supplies a departure date.

- Updated the Spec and Getting Started pages, which still advertised pre-seeded evidence and Security Copilot.

- Rewrote three graded questions that asked for counts from data that does not exist.

- Fixed the typos and grammatical errors identified during lab testing.

### Screenshot Changes

N/A

## Validations

Validations have been authored but are not enabled for this release. The lab is graded on the learner's recorded findings.

Eight grading defects were fixed in the validator scripts this cycle, including checks that passed policies with none of the required logic and one that could never pass a correct rule.

### Testing Notes

- **Testing Date**: 2026-08-10

### Testing Scope

Built all four challenges end to end in the live tenant as the lab account, covering sensitive information type discovery, label creation and publishing, the auto-labeling policy in simulation across all three workloads, both DLP policies with their full rule logic, and the insider risk policy on the correct template. 21 of 22 configuration checks passed. Reviewed all lab instructions against the current Purview portal. A final round of testing on a fresh deployment is required before delivery.

---
</details>

---
