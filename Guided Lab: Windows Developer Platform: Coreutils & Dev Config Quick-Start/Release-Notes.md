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

- Switched the VM to a public `MicrosoftWindowsDesktop / windows-11 / win11-24h2-pro` image, since the Spektra `cloudlabs-windows-jumpvm` offer has no Windows 11 SKU. This required TrustedLaunch with Secure Boot and vTPM, which Windows 11 mandates.
- Sized the VM at `Standard_D4s_v5` for nested virtualization and for a `dotnet build` running alongside the coding agent.
- Replaced the common library's `InstallModernVmValidator` with the reference labs' `RunModernVmValidator`, which installs .NET Core 3.1 explicitly. The library version left the CloudLabs VM Agent service created but unable to start on a Windows 11 client image.
- Added WinGet and NuGet prerequisite checks to `psscript-01.ps1`. The Windows 11 image ships whatever App Installer version it was built with, and clients below v1.26 cannot run `winget configure` at all; a fresh image can also have no NuGet source configured, which prevents the WinUI templates from installing.
- Added GitHub Enterprise Cloud provisioning through `Enable-GitHub -WithCopilot` from the common functions library, so no attendee personal GitHub accounts or paid Copilot seats are required.
- Removed the first-logon task that applied `dev-config.winget` in the background. In a self-paced lab the attendee is the first logon, so applying the configuration is now their task, which is also what the module title promises.

### Content Changes

- Authored all 4 exercises end-to-end, grounded in the real, published `microsoft/WindowsDeveloperConfig`, `microsoft/coreutils` and `microsoft/win-dev-skills` repositories (no fabricated commands).
- Exercise 01: added the `winget configure --enable` step, without which every configuration command fails. Restructured the idempotency task around `winget configure test`, since a second `winget configure` run produces identical output and does not demonstrate it. Corrected the authored configuration document to the DSC v3 schema.
- Exercise 02: reframed Task 1 from installing Coreutils to confirming it, since `dev-config.winget` already installs it. Rewrote Task 2 around the PowerShell profile hook Coreutils installs, which is why a command can work when typed and fail inside a script.
- Exercise 03: corrected the agent tooling. Two plugin entries are required and do different jobs, skills are namespaced, and the agent is selected when the session starts rather than by prefixing a prompt. Added guidance on redirecting the agent when it proposes an outdated project format.
- Replaced `winget list` with `dotnet --list-sdks` for .NET checks, as WinGet reports the SDK as not installed even when it is present and working.
- Removed the Azure portal sign-in, as the lab uses no Azure services, and rewrote the Getting Started page to the standard CloudLabs format.

### Screenshot Updates

- Captured and mapped 40 screenshots across Exercises 01 and 02, with 46 numbered UI references added across the guide.
- Rebuilt the architecture diagram from the verified deployment.

### Validation

- No validations are required for this lab.

### Testing Notes

- **Testing Date**: 2026-08-05

### Testing Scope

Performed live, hands-on end-to-end testing of every exercise on a real lab VM, including real package installs, real configuration application, real GitHub Copilot CLI sign-in, and real error reproduction/fixes (WinGet client version skew, missing NuGet source, configuration feature disabled by default, agent proposing an outdated project format). Confirmed the agent-built WinUI 3 application compiles, runs, and satisfies all documented success criteria. No validations are required for this lab.

</details>
