# Guided Lab: .NET 11 Agentic Web - Building AI-Native ASP.NET Core & MAUI Apps

Welcome to the **Guided Lab: .NET 11 Agentic Web - Building AI-Native ASP.NET Core & MAUI Apps** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-09-02</summary>

## Release Date: 2026-09-02

### Summary of Changes

Authored the lab from scratch (6 modules, 6 hours) covering .NET 11/`dotnetup` setup, C# 15 union types with an agentic minimal API, Blazor agentic streaming components, .NET MAUI on-device AI with Phi-3-mini ONNX, `Microsoft.Extensions.AI` building blocks, and testing/Responsible AI checks — then performed live, hands-on end-to-end execution on real Azure lab VMs across every module, fixing each issue as it was actually hit rather than only reviewing the content on paper.

### Infrastructure Changes

- Adapted an ARM deployment template + VM provisioning/logon scripts for this lab's own resource requirements: a Microsoft Foundry (Cognitive Services `AIServices`) account with a single `gpt-5.4-mini` chat deployment, plus a Content Safety account for Module 6 — removing unrelated resources (Azure AI Search, Storage/blob datasets, Log Analytics, App Insights) that a sibling lab's template had included but this lab never uses.
- Corrected the automated role-assignment logic to grant **Cognitive Services OpenAI User** on the parent Cognitive Services account, not **Azure AI User**/**Foundry User** on a nested Foundry project — the exact RBAC scope-and-role-name mistake that caused a live `401 (Unauthorized)` during Module 3 testing.
- Added missing VM provisioning steps identified only through live testing: the actual .NET 11 preview 7 SDK (via `dotnet-install.ps1`, since Chocolatey only tracks stable channels), the `.NET MAUI` workload, Git LFS, and the Windows App Runtime redistributable (required for unpackaged WinUI3 MAUI apps in Module 4).

### Content Changes

- Fixed dozens of copy-paste and top-level-statement ordering bugs found only by actually running the code: `record` type declarations placed before `app.Run()` (`CS8803`), incorrectly qualified union case constructors (`AgentResult.ToolCall(...)` instead of `ToolCall(...)`, `CS0426`), a duplicate `AssistantRequest` record declaration (`CS0101`), and a missing `using AgenticWeb;`.
- Corrected the real `Microsoft.ML.OnnxRuntimeGenAI` v0.15.2 generation-loop API in Module 4 (`AppendTokenSequences`/`GenerateNextToken()`), replacing an earlier, since-removed API shape (`SetInputSequences`/`ComputeLogits`) that doesn't compile against the installed package.
- Root-caused and fixed a native WinUI3 crash (`0xc000027b`) in the MAUI on-device chat page down to two distinct causes: an empty/incomplete local model folder, and MAUI's DI-based page activation failing for a page with constructor dependencies — resolved by constructing the page directly instead of resolving it through the service provider.
- Documented the nested-project-folder trap that recurs across every module (`mkdir X; cd X; dotnet new ... -n X` scaffolds the real project one level deeper than expected), and converted every ambiguous relative `cd` sequence spanning separate terminal windows to explicit absolute paths.
- Added a `DefaultAzureCredential` fallback path for Module 5's `IChatClient` registration, for lab subscriptions where local (API key) authentication is disabled on the Cognitive Services account and every API key is rejected regardless of rotation.
- Added Windows PowerShell 5.1–specific guidance throughout (reading a failed request's real response body via `$_.Exception.Response.GetResponseStream()`, since `-SkipHttpErrorCheck` and `$_.ErrorDetails.Message` are both unreliable on this shell version).
- Removed the standard "Congratulations" validation-callout blocks from all six module files, and trimmed the overview page's stated duration from "6 Hours (Self-Paced)" to "6 Hours".

### Screenshot Update

- Screenshots are being captured and added directly by the lab author as each module is executed live; image numbering in the guide is managed by the author and is not altered by content edits.

## Validations

**Validations have not been added yet for this lab.** No formal validation/grading scripts (per-module or CloudLabs-wide) currently exist for `.NET 11 Agentic Web: Building AI-Native ASP.NET Core & MAUI Apps` — this is expected at this stage and is tracked as separate, future work.

### Testing Notes

- **Testing Date**: 2026-09-02

### Testing Scope

Performed live, hands-on end-to-end testing of every module in a real Azure lab VM environment (including a full VM re-provisioning mid-cycle), fixing real, reproduced build errors, runtime exceptions, and RBAC/authentication failures as they occurred, and updating the lab guide to reflect each confirmed root cause and fix. Formal validation scripts were intentionally not built as part of this cycle.

</details>
