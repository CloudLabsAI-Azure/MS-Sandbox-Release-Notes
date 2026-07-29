# Guided Lab: GitHub Copilot SDK & Agent Merge: Agentic Developer Workflows

Welcome to the **Guided Lab: GitHub Copilot SDK & Agent Merge: Agentic Developer Workflows** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-07-29</summary>

## Release Date: 2026-07-29

### Summary of Changes

New lab onboarded. Built and end-to-end tested a 4-hour, 4-exercise guided lab on agentic developer workflows with the **GitHub Copilot SDK (GA)** and the redesigned **Copilot CLI**. Learners act as a Platform Engineer at the fictional Contoso Traders and take one polyglot codebase from **"agents can read my code"** to **"agents ship my code under a governance policy I control."**

| # | Exercise | What the learner does |
|---|---|---|
| 1 | Copilot SDK Foundations - Python | Sets up the Copilot SDK in a Python virtual environment and builds a first agentic workflow — client, session, streaming, and a custom tool. |
| 2 | Multi-Language SDK & /security-review - Node.js | Ports the agent to Node.js, then runs the `/security-review` skill against a vulnerable module, fixes a finding, and re-scans. |
| 3 | Copilot CLI: TUI, Voice & /every Scheduling | Explores the redesigned TUI, drives the CLI by voice, and schedules recurring agent runs with `/every` backed by GitHub Actions. |
| 4 | Agent-Driven Delivery, Governance & Audit | Delegates an issue to a Copilot agent, authors a policy-as-code quality gate, has an agent repair a red build, and assembles the merge audit evidence. |

### Infrastructure Changes

- Moved the global Copilot CLI install (`npm install -g @github/copilot`) out of the provisioning script into the first-logon script — a global npm install can stall the non-interactive SYSTEM session and must never block deployment.
- Fixed `copilot` not being found in the terminal: the logon script now appends npm's global prefix to the machine PATH after install.
- Removed a hardcoded GitHub App client secret from the ARM template and provisioning script; it is now a `securestring` parameter (old value flagged for rotation).
- Added only the tooling this lab needs (Python 3.12, GitHub CLI) via non-interactive installs; automated the codebase clone to `C:\contoso-traders-api`; fixed script/blob path mismatches and a missing `ghsecret` parameter.

### Content Changes

- Authored the Getting Started page and all 4 exercises, with every install command and API verified against official documentation.
- Rebuilt the sample codebase as a true polyglot repo (added a Python `warehouse/` module with tests) so Exercise 1's "Python project" is literal; CI runs both suites.
- Fixed a real runtime blocker: SDK sessions deny agent tool calls unless a permission handler is supplied. Added it to every code block in Exercises 1–2.
- Exercise 2 delivers the vulnerable module as a paste-in snippet, since `/security-review` only scans uncommitted changes — a committed vulnerability would return an empty scan.
- Exercise 3 now has learners create their own repository, since the provisioned clone is read-only and Exercise 4 needs a repo they own.
- **Rewrote Exercise 4.** The original "Agent Merge Configuration & Audit" relied on Agent Merge, a technical-preview feature unavailable in the lab tenant. Replaced with "Agent-Driven Delivery, Governance & Audit" — same outcome using generally available features.
- Flattened task numbering to `Task 1/2/3` (max 3 per exercise) and standardised all exercises on the Spektra structure; added `masterdoc.json`.

### Screenshot Updates

- Restructured screenshots into per-page subfolders (`images/gettingstarted/`, `module1/`…`module4/`).
- Captured ~130 real screenshots across all pages, replacing every placeholder, with click-numbered annotations **(1)**, **(2)** matching the steps.
- Re-captured the full Exercise 4 set for the rewritten flow.

### Testing Notes

- **Testing Date**: 2026-07-22 to 2026-07-29

### Testing Scope

Live, hands-on testing on a real deployed instance:

- Verified the toolchain on the live VM (Git, Node.js, Python 3.12.10, Copilot CLI 1.0.73).
- Walked every exercise as a learner, running each command and code block as written and capturing screenshots.
- Reproduced and fixed real errors rather than working around them: the deployment hang, `copilot` missing from PATH, the SDK permission-denied failure, and `/security-review` needing experimental mode.
- Redeployed after the infrastructure fixes to confirm the environment reaches ready state unattended.

</details>