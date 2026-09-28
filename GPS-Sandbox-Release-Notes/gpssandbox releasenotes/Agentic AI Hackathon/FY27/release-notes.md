# Agentic AI Hackathon

Welcome to the **Agentic AI Hackathon** lab release notes. On this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-09-18</summary>
  
## Release Date: 2026-09-18

### Summary of Changes

- Performed end-to-end lab testing and added validation.
- Updated the Challenge Guide and Solution Guide with screenshots and enhanced instructions to improve the overall learner experience.

### Project 1

### Infrastructure Changes

N/A

### Content Changes

N/A

## Validations

Validations are implemented and working as expected.

### Project 2

### Infrastructure Changes

N/A

### Content Changes

N/A

## Validations

Validations are implemented and working as expected.

### Project 3

### Infrastructure Changes

N/A

### Content Changes

N/A

## Validations

N/A

### Project 4

### Infrastructure Changes

N/A

### Content Changes

N/A

## Validations

N/A

### Testing Notes

- **Testing Date**: 2026-09-18

### Testing Scope 

Successfully completed end-to-end testing with successful validations across all four projects. Verified the updated lab documentation, including the revised screenshots and instructions, and confirmed that the overall lab workflows function as expected.

</details>

<details>
  <summary>2026-09-16</summary>

## Release Date: 2026-09-16

### Summary of Changes

- Completed end-to-end lab testing for Project 3 and Project 4, and updated the lab guides with all required screenshots and instructions.

## Project 1

### Infrastructure Changes

N/A

### Content Changes

N/A

### Validations

N/A

## Project 2

### Infrastructure Changes

N/A

### Content Changes

N/A

### Validations

N/A

## Project 3

### Infrastructure Changes

N/A

### Content Changes

- Corrected the notebook code in the guide, which was written against an older SDK version and did not match the working notebook.
- Resolved the weather tool failure caused by an expired SSL certificate on wttr.in by moving to an alternative service (Open-Meteo), confirmed with the Technofocus team.
- Added the Application Insights creation step required for the agent traces.

### Validations

Validations are implemented and working as expected.

## Project 4

### Infrastructure Changes

- Increased the model TPM capacity from the default of 50 to 150, as the indexing pipeline was hitting rate limits during image verbalization and embedding.

### Content Changes

- Corrected the object name prefix references, as the wizard appends an auto-generated number that did not match the names shown in the guide.

### Validations

Validations are implemented and working as expected.

## Testing Notes

- **Testing Date**: 2026-09-16

## Testing Scope

Successfully completed end-to-end testing for Project 3 and Project 4. Verified the updated lab documentation, including the revised screenshots and instructions, and confirmed that the overall lab workflows function as expected.

</details>

<details>
  <summary>2026-09-10</summary>

## Release Date: 2026-09-10

### Summary of Changes

- Completed end-to-end lab testing for Project 1 and updated the lab guide with all required screenshots and instructions.

## Project 1

### Infrastructure Changes

- Verified that both gpt-5.4 and gpt-image-1-mini are available only in a limited set of regions, and shared the list for the template mapping.

### Content Changes

- Restructured the notebook setup flow to use a virtual environment with a requirements.txt file, as the lab VM ships with older pre-installed packages that were conflicting with the required SDK versions.
- Identified that the Foundry SDK call requires data-plane RBAC permissions, which subscription Owner does not grant. Documented the required role assignment.

### Validations

Validations are implemented and working as expected.

## Project 2

### Infrastructure Changes

N/A

### Content Changes

N/A

### Validations

N/A

## Project 3

### Infrastructure Changes

N/A

### Content Changes

N/A

### Validations

N/A

## Project 4

### Infrastructure Changes

N/A

### Content Changes

N/A

### Validations

N/A

## Testing Notes

- **Testing Date**: 2026-09-10

## Testing Scope

Successfully completed end-to-end testing for Project 1. Verified the updated lab documentation, including the revised screenshots and instructions, and confirmed that the overall lab workflows function as expected.

</details>

<details>
  <summary>2026-09-09</summary>
  
## Release Date: 2026-09-09

### Summary of Changes

- Performed end-to-end lab testing.
- Updated the Solution Guide with screenshots and enhanced instructions to improve the overall learner experience.

### Project 4

### Infrastructure Changes

N/A

### Content Changes

- Picked up AAH FY27 Project 4: Building a Multimodal Retrieval-Augmented Generation Pipeline, completed end-to-end testing.
- Added the Getting Started page and completed the required minor updates to the lab.
- Connected with Anand, worked on generating RBAC and policy configurations.

## Validations

N/A

### Testing Notes

- **Testing Date**: 2026-09-09

### Testing Scope 

Successfully completed end-to-end testing

</details>


</details>

