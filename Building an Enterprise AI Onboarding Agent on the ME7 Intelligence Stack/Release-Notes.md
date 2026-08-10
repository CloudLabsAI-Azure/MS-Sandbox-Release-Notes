# Building an Enterprise AI Onboarding Agent on the ME7 Intelligence Stack

Welcome to the **Building an Enterprise AI Onboarding Agent on the ME7 Intelligence Stack** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-10</summary>

## Release Date: 2026-08-10

### Summary of Changes

Performed end-to-end lab testing and validations across all 6 challenges, with major content updates to every challenge guide and a full deployment template fix.

### Infrastructure Changes

- Fixed `deploy-01.json`: a stray extra closing brace was prematurely closing the `parameters` object, causing `InvalidTemplate` ("Required property 'resources' not found") on every deployment attempt.
- Fixed `deploy-01.json`: the `arg6` variable (carrying `AppId`/`AppSecret`/`azuserobjectid`) was defined but never included in the final `arg` concatenation, so those values were silently never passed to the VM setup script.
- Removed the `AppId`/`AppSecret`/policy-assignment block and the `GitHubPat`/private-repo-clone approach from `psscript-01.ps1` — neither is needed for this lab; the 3 sample onboarding documents are downloaded via plain HTTP from the same blob container as the script instead.
- Removed dead weight from `psscript-01.ps1`: the unused `$InstallCloudLabsShadow` parameter, a Python 3.11 downgrade block (this lab has no Python anywhere), and a `Setup-MyDevEnv` download step not referenced by any challenge.
- Corrected `deploy-01.parameters.json`: parameter names did not match the template (`vmAdminUsername`/`vmAdminPassword` vs. the template's actual `adminUsername`/`adminPassword`), which would have failed deployment outright.
- Added a Cost Estimation workbook with real Azure resource pricing sourced from the Azure Retail Prices API.
- Authored CloudLabs custom validation scripts for all 6 challenges.

### Content Changes

- **Challenge 1**: Corrected the Foundry project creation flow to the current unified Foundry resource + Project model (the Hub-based flow referenced in older guidance is not supported in the current Foundry portal).
- **Challenge 2**: Documented the full root-cause chain behind the Foundry IQ → Azure AI Search MCP `401 Unauthorized` error: managed identity must be enabled at the account level, the `Search Index Data Reader` role must target the project's managed identity (not the signed-in user), and the search resource's API access control must allow **Both** (RBAC + keys), not RBAC-only.
- **Challenge 3**: Documented that `az login`/`az account get-access-token` cannot obtain `People.Read` (Azure CLI's own first-party app cannot be preauthorized for it) — the working path is `DeviceCodeCredential` against the lab's own dev app registration, with `403`/`404` from `/me/manager` and `/me/people` handled as graceful `null`/`[]`, not failures.
- **Challenge 4**: Documented that Copilot Studio has no manual HTTP-action form — custom tools are registered by uploading an OpenAPI 3.0.1 spec through the REST API plugin wizard. Documented a real trap: requesting `People.Read` in the tool's OAuth connection scope blocks the connection on admin approval before the server's own graceful-degradation code ever runs; the fix is requesting only `User.Read`. Documented the redirect-URI mismatch between `token.botframework.com` and Power Platform's actual `global.consent.azure-apim.net` consent redirect. Documented that the built-in **Greeting** system topic intercepts the same trigger phrases as a custom welcome topic and must be disabled, and that the built-in **Fallback** topic already auto-routes to **Escalate** — no manual per-topic routing needed.
- **Challenge 5**: Documented that `a365 setup all` requires the signed-in account to hold **Global Administrator** — no lesser role works, confirmed via direct testing. Documented a one-time manual follow-up (`New-MgServicePrincipalAppRoleAssignment`) needed when the Observability API's service principal doesn't yet exist in a fresh tenant. Documented a real discrepancy: `setup all` grants a broader default permission template rather than the intended least-privilege set when run against a folder with no detected coded project (expected for a Copilot Studio–based agent).
- **Challenge 6**: Documented that tracing is configured in Copilot Studio's own agent Settings (Advanced → Application Insights), not the Microsoft 365 admin center, which has no monitoring controls for agents at all. Documented that generative-orchestration agents do not expose a raw confidence-score telemetry field — the alert rule's real signal is `TopicAction` events landing on **Escalate**/**Fallback**, confirmed via direct Log Analytics queries.

## Validations

Validations are good. All 6 challenges completed end-to-end against a live CloudLabs sandbox, including the full 10-turn Challenge 4 test conversation (0 generic fallbacks) and confirmed telemetry/alerting in Challenge 6.

### Testing Notes

- **Testing Date**: 2026-08-10

### Testing Scope

Successfully completed end-to-end lab testing and validation across all 6 challenges. Thoroughly reviewed and validated all lab instructions, the ARM deployment template, and the setup script, ensuring they are accurate, up to date, and aligned with the actual behavior of Foundry, Foundry IQ, Copilot Studio, and Agent 365 as confirmed live.

---
</details>
