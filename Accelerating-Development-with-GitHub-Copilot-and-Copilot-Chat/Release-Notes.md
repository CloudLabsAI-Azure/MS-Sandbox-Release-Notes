# Accelerating Development with GitHub Copilot & Copilot Chat

Welcome to the **Accelerating Development with GitHub Copilot & Copilot Chat** lab release notes. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, and other relevant changes for the lab.

## Overview

This Page contains detailed notes about the latest updates and modifications made after each testing cycle. It includes:

- Testing dates
- Descriptions of changes to lab infrastructure
- Updates to content or documentation
- Changes to screenshots and visuals used in the lab

`For any further details or inquiries, feel free to reach out to the CloudLabs support team. 
Email Support: cloudlabs-support@spektrasystems.com`

# Release Notes

<details>
  <summary>2026-05-27</summary>

## Release Date: 2026-05-27

### Summary of Changes

Resolved multiple learner-reported issues for the upcoming workshop. Fixed VPN-related access disruption guidance, GitHub identity-provider sign-in instructions, and rewrote the Git/SSO workflow in Exercise 5 for consistency. Corrected Markdown rendering issues in Exercises 3 and 4, standardized completion notes across all exercises, and added a support contact closing in Exercise 6.

### Infrastructure Changes

N/A

### Content Changes

- **Getting Started Page**: Added an Important callout at the top of "Accessing Your Lab Environment" advising learners to disconnect VPN before launching the lab to avoid disconnections and authentication failures.
- **Getting Started Page, Sign in to GitHub**: Added an Important callout instructing learners to click **Sign in with your identity provider** instead of entering a password, as CloudLabs GitHub accounts are provisioned via the organization's identity provider.
- **Exercise 1, Task 1**: Added a new step for "Continue without signing in" on the VS Code welcome screen.
- **Exercise 1, Task 1**: Merged the "Copilot icon" step with the new "Use AI Feature" button step into a single step with (1)/(2) annotations.
- **Exercise 1, Task 1**: Added the same identity-provider Important callout after the GitHub sign-in step.
- **Exercise 1, Task 1**: Consolidated the Command Palette + Split Editor + Chat-icon-drag steps into a single "Click on Toggle Chat" step to reduce confusion.
- **Exercise 1, Task 1**: Added a new step to click **Keep** to retain the AI-generated response.
- **Exercise 3, Task 3, Step 1**: Fixed the broken nested "Or" sub-bullet that escaped the numbered list. Inlined the alternate prompt inside Step 1 and corrected the hardcoded `2.` to `1.` to match the auto-numbering pattern.
- **Exercise 4 (title)**: Renamed from "Test" to **"Test and Validate"** for clarity and parallelism with other exercise titles.
- **Exercise 4, Task 2**: Fixed typo `resposnes` → `responses`. Normalized image indentation from 5 spaces to 4 spaces and removed an extra blank line that was breaking list flow.
- **Exercise 5, Task 1, Step 6**: Standardized the GitHub repository name to **`bookbuddy-mvp`** (hyphen) to match the local folder created in Exercise 1 and the remote URL. Set the **Add a README file** toggle to **Off** and added an Important callout explaining that initializing the remote with a README creates a separate commit history that conflicts with the local repository on push.
- **Exercise 5, Task 1**: Added a new step to create a `.gitignore` file (with `node_modules/` and `.env`) before staging any changes, preventing accidental commits of dependencies and secrets.
- **Exercise 5, Task 1**: Split the Git identity configuration into two clearly-labelled commands (`git config --global user.name "<Your GitHub username>"` and `git config --global user.email "<Your GitHub email>"`) with a Note showing example values from the Licenses tab. Removed the previous single, ambiguous placeholder that caused SSO learners to paste the wrong value.
- **Exercise 5, Task 1**: Reordered the terminal commands into logical groups: init → gitignore → identity → add/commit → remote → branch/push.
- **Exercise 6, Summary**: Added a support contact line (`cloudlabs-support@spektrasystems.com`) and a "Happy Learning!!" closing.
- **All Exercises (1–6)**: Standardized the completion note wording from "successfully completed the lab" to **"successfully completed the Hands-on Lab"**.

### Screenshot Updates

- Added new screenshot `u2.png` for the VS Code "Continue without signing in" step in Exercise 1, Task 1.
- Added new screenshot `keep-response.png` for the Copilot Chat **Keep** step in Exercise 1, Task 1.
- Updated screenshot `new-pg10-1.png` to reflect the combined Copilot icon + Use AI Feature button view in Exercise 1, Task 1.
- Updated screenshot `2026-04-30_21-48-16.png` for the Copilot Chat prompt step in Exercise 1, Task 1.

### Testing Notes

- **Testing Date**: 2026-05-27

### Testing Scope

Performed end-to-end validation of the lab guide from Getting Started through Exercise 6. Verified the updated GitHub identity-provider sign-in flow, the rewritten Git/SSO workflow in Exercise 5 (repository creation, `.gitignore` setup, identity configuration, remote add, push, and PR compare banner), and the corrected Markdown rendering in Exercises 3 and 4. Confirmed all reported workshop ticket issues are resolved.

---
</details>
<details>
  <summary>2026-05-13</summary>

## Release Date: 2026-05-13

### Summary of Changes

Updated the UI screenshots, revised the login steps for the GitHub user account, updated the login method via SSO, and made the necessary changes to the lab guide steps as well.

### Infrastructure Changes

N/A

### Content Changes

- In the Getting Started Page, added Login to GitHub steps so that users can login to the GitHub before proceeding with the installation of GitHub Co-Pilot Extension.
- Exercise 1, Task 1, Step 13: Made few updates in the steps to reflect the latest changes. 
- Exercise 1, Task 1, Step 14: Changed the step to reflect the latest UI.
- Exercise 1, Task 1, Step 15: Removed the older step since Outlook option is no longer needed now, and replaced it with a new step to sign in to the GitHub.
- Exercise 1, Task 1, Step 16: Updated this step to follow the workflow in a structured flow.

### Screenshot Updates

- Added few additional screenshots in the Getting Started Page for GitHub Login.
- Exercise 1, Task 1, Step 12: Updated the screenshot since the older one was not clear.
- Exercise 1, Task 1, Step 13, 14, 15, 16 and 17: Updated the screenshot to follow the workflow.
  
### Testing Notes

- **Testing Date**: 2026-05-13

### Testing Scope 

Changed the login method of GitHub to SSO, and made necessary changes in the lab guide workflow as well.  

---
</details>

<details>
  <summary>2026-05-04</summary>

## Release Date: 2026-05-04

### Summary of Changes

Improved the overall lab experience by updating screenshots, improved the clarity of command instructions in the lab guide, and also added a few additional steps to improve user authentication to outlook mail.

### Infrastructure Changes

N/A

### Content Changes

- Exercise 1, Task 1, Step 15: Added an additional step to help users identify where the verification code appears in their Outlook email.
- Exercise 1, Task 1, Step 23: Modified the prompt to assist in creating the README.md file.
- Exercise 6, Task 2, Step 6: Removed the specific date and replaced it with the YYYY-MM-DD format.

### Screenshot Updates

- Exercise 1, Task 1, Steps 11 & 12: Updated the screenshots to reflect the latest UI.
- Exercise 1, Task 1, Step 24: Updated the screenshot to reflect the latest output.
- Exercise 1, Task 1, Step 23 & 24: Updated output screenshot.
- Exercise 5, Task 1, Step 6: Added an additional screenshot to guide users in creating a repository and updated the repository name to "bookbuddy_mvp."
      
### Testing Notes

- **Testing Date**: 2026-05-04

### Testing Scope 

 Performed end-to-end validation of the lab environment and documentation. Verified all instructions, commands, and portal navigation steps, and updated screenshots to match the current UI.

---
</details>

