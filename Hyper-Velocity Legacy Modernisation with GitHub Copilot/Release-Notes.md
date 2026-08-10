# Hyper-Velocity Legacy Modernisation with GitHub Copilot
 
Welcome to the Hyper-Velocity Legacy Modernisation with GitHub Copilot Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.
 
## Overview
 
This page contains detailed notes about the latest updates and modifications made after each testing cycle. It includes:
 
* Testing dates
* Descriptions of changes to lab infrastructure
* Updates to content or documentation
* Changes to screenshots and visuals used in the lab

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`
`Email Support: cloudlabs-support@spektrasystems.com`

# Release Notes

<details>
  <summary>2026-08-10</summary>

## Release Date: 2026-08-10
 
### Summary of Changes
 
Performed end-to-end lab testing across all five challenges, with content updates and the addition of the lab code assets.
 
### Infrastructure Changes
 
N/A
 
### Content Changes
 
* Added the `codefiles` asset package containing the legacy `inventory.py` module, project dependencies, and the local MCP documentation server.
* Replaced the bundled MCP documentation server with a protocol-compliant implementation. The original was unable to complete the VS Code MCP handshake, which prevented Challenge 04 from being completed.
* Added `pbr` to `requirements.txt`. Bandit 1.7.5 imports this package at runtime but does not declare it as a dependency, causing `bandit --version` to fail on a clean environment.
* Updated Challenge 05 to use the correct Bandit suppression syntax (`# nosec` in place of `# noqa`), and revised severity references to align with the actual scan output following a successful migration.
* Added environment setup instructions to the Getting Started page covering repository clone, dependency installation, Git identity configuration, and working branch creation.
* Updated `@workspace` references to `@codebase` to align with the current Copilot Chat syntax in VS Code.
* Refined instructions across Challenges 01 to 04 for accuracy and consistency with the verified lab flow.
### Screenshot Update
 
* Added screenshots to the Getting Started page covering the GitHub account activation and sign-in flow.
### Validations
 
* No automated validations as the lab fully depends on GitHub Copilot.
### Testing Notes
 
* Testing Date: 2026-08-10
### Testing Scope
 
Successfully completed end-to-end testing of Challenges 01 through 05. All lab instructions were reviewed and validated against the observed lab flow, with content corrections applied where instructions did not match actual behaviour.
 