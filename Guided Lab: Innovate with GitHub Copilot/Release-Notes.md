# Guided Lab: Innovate with GitHub Copilot

Welcome to the **Guided Lab: Innovate with GitHub Copilot** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-03</summary>

## Release Date: 2026-08-03

### Summary of Changes

Removed the lab's remaining dependency on GitHub Codespaces and aligned all seven Getting Started pages with the local LabVM workflow the exercises now use. Replaced the architecture diagram, corrected outdated content, and completed a full wording, grammar, and consistency pass across all ten exercises.

### Infrastructure Changes

N/A

### Content Changes

- **Removed all GitHub Codespaces references from the lab.** The exercises had already been migrated to local Visual Studio Code on the LabVM, but all seven Getting Started pages still described Codespaces in their Overview, Architecture, and Explanation of Components sections. Every page now documents the local LabVM environment that the exercises actually use.
- **Replaced the architecture diagram** on all seven Getting Started pages. The previous diagram depicted the Codespaces-based, cloud-hosted development flow; the new diagrams show the local Visual Studio Code and LabVM architecture, with per-lab variants for the Azure portal (L4), JetBrains IntelliJ IDEA (L6), and Accessibility Insights and SQL Server Management Studio (L7).
- Rewrote each Getting Started page's Objective and Explanation of Components to match the exercise or exercises it actually fronts, removing components no longer used and adding those that were missing.
- Removed leftover Linux package-installation commands from **Exercise 2**, which no longer applied to the Windows LabVM; the step now runs the Node application directly.
- Corrected an incorrect step reference in **Exercise 7**, a reversed screenshot callout sequence, and a note in **Exercise 6** that referenced the wrong IDE.
- Fixed typos in Copilot prompts and comments across Exercises 2, 7, and 8.
- Consolidated duplicated notes and standardised terminology, task heading levels, and objective lead-ins across all ten exercises.
- Added a repository `README.md` covering the seven guided labs, all exercises, and their task breakdowns.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-08-03

### Testing Scope

Reviewed and validated all lab guides and Getting Started pages for accuracy and consistency against the current LabVM-based environment. Confirmed that no exercise references GitHub Codespaces, that every documented component is used by the exercises that list it, and that all image and cross-file references resolve.

---
</details>



<details>
  <summary>2026-04-04</summary>
  
## Release Date: 2026-04-04

### Summary of Changes

Performed end-to-end lab testing and validations. Updated the lab to reflect recent UI changes, with corresponding updates made to screenshots and instructions to ensure accuracy and consistency.

### Infrastructure Changes

N/A

### Content Changes

- Updated lab instructions to align with the latest UI changes.
- Refreshed screenshots to reflect the updated interface.
- Made minor content enhancements to improve clarity, consistency, and overall user experience.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-04

### Testing Scope 

Successfully completed end-to-end lab testing and validation. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest changes. 

---
</details>




