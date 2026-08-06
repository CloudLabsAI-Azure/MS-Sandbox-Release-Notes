# Guided Lab: Windows Developer Platform: Coreutils & Dev Config Quick-Start

Welcome to the **Guided Lab: Windows Developer Platform: Coreutils & Dev Config Quick-Start** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-05</summary>

## Release Date: 2026-08-05

### Summary of Changes

New lab onboarded. Built and end-to-end tested the full lab across 2 modules and 4 exercises: declarative workstation configuration with Windows Developer Configurations, native command-line data analysis with Coreutils for Windows, agent-driven WinUI 3 application development with Windows Development Skills, and the review and validation of agent-generated code.

### Infrastructure Changes

- Provisioned the lab on a Windows 11 Pro 24H2 workstation with Trusted Launch enabled, sized at `Standard_D4s_v5` to support nested virtualization and a `dotnet build` running alongside the coding agent.
- Configured the CloudLabs VM Agent with the .NET Core 3.1 runtime it requires, so the agent service installs and starts cleanly on the Windows 11 client image.
- Added WinGet and NuGet prerequisite handling to `psscript-01.ps1`, so the WinGet client is brought to a version that supports `winget configure` and the default NuGet source is in place before the WinUI templates are installed.
- Added GitHub Enterprise Cloud provisioning through `Enable-GitHub -WithCopilot` from the CloudLabs common functions library, entitling each attendee's account to GitHub Copilot. No personal GitHub accounts or paid Copilot seats are required.
- Staged the sample log data, the Windows Developer Configuration document, and Developer Mode during provisioning, so the attendee applies the configuration themselves in Exercise 01 as the module intends.
- Included the CloudLabs standard components: credential file, embedded shadow support, VM Agent, Chocolatey, Edge with the Azure Portal shortcut, and the standard transcript logging.

### Content Changes

- Authored all 4 exercises end-to-end, grounded in the real, published `microsoft/WindowsDeveloperConfig`, `microsoft/coreutils` and `microsoft/win-dev-skills` repositories (no fabricated commands).
- Exercise 01: documented `winget configure --enable`, which turns on the opt-in configuration feature required by every subsequent configuration command, and built the idempotency task around `winget configure test`, which reports the machine state directly. The configuration document the attendee authors uses the DSC v3 schema, matching the published `dev-config.winget`.
- Exercise 02: framed Task 1 around confirming and exploring the 79 Coreutils utilities the configuration delivers, then built Task 2 around the PowerShell profile hook Coreutils installs, which explains why a command can behave differently when typed than inside a script.
- Exercise 03: documented the two plugin entries the agent tooling requires and what each provides, the namespaced form for invoking skills, and selecting the agent when the Copilot CLI session starts. Added guidance on reviewing and redirecting the agent's first proposal, which is the core skill the module teaches.
- Exercise 04: documented requesting a scoped enhancement with a constrained prompt, reviewing the change before applying it, and comparing the outcome against a deliberately vague request.
- Used `dotnet --list-sdks` for all .NET SDK checks, which reports the installed SDK reliably.
- Wrote the Getting Started page to the standard CloudLabs format, including the Windows out-of-box setup screens and the GitHub sign-in steps using the provisioned account and identity provider.

### Screenshot Updates

- Captured and mapped 40 screenshots across Exercises 01 and 02, with 46 numbered UI references across the guide.
- Built the architecture diagram from the verified deployment.

### Validation

- No validations are required for this lab.

### Testing Notes

- **Testing Date**: 2026-08-05

### Testing Scope

Performed live, hands-on end-to-end testing of every exercise on a real lab VM, including real package installs, real configuration application, real GitHub Copilot CLI sign-in, and real error reproduction/fixes (WinGet client version skew, missing NuGet source, configuration feature disabled by default, agent proposing an outdated project format). Confirmed the agent-built WinUI 3 application compiles, runs, and satisfies all documented success criteria. No validations are required for this lab.

</details>
