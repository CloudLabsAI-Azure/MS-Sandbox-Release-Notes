# Guided Lab: Microsoft Agent Framework: Build, Govern & Evaluate Production Agents

Welcome to the **Guided Lab: Microsoft Agent Framework: Build, Govern & Evaluate Production Agents** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-07-28</summary>

## Release Date: 2026-07-28

### Summary of Changes

New lab onboarded. Built and end-to-end tested the full Microsoft Agent Framework lifecycle across 6 modules: local development with the Agent Harness, sandboxed CodeAct/Hyperlight execution, deployment to Microsoft Foundry Agent Service, ASSERT/ACS governed evaluation, multi-agent handoff orchestration, and observability/cost measurement.

### Infrastructure Changes

- Removed unused resources from the ARM template (`deploy-01.json`): Azure AI Search, a separate Storage account, Application Insights, and Log Analytics workspace, none are referenced by any of the 6 modules.
- Fixed a mismatched blob path in `psscript-01.ps1` (`microsoft-agent-framework` vs `microsoft-agent-frameworks`) and a script bug where the autologon step referenced an undefined `$adminPassword` variable instead of the actual `$vmAdminPassword` parameter.
- Removed a Rust toolchain install (`rust-ms`) from the provisioning script, since Module 04 intentionally relies on the VM *not* having a Rust toolchain to teach the `litellm==1.91.4` pinning workaround.

### Content Changes

- Authored all 6 modules end-to-end, grounded in the real, published `microsoft/agent-framework` GitHub repository (no fabricated APIs).
- Module 02 (CodeAct & Hyperlight): documented the expected `No Hypervisor was found for Sandbox` failure on this VM size (no nested virtualization) and restructured the exercise to validate graceful failure handling instead of live sandbox execution.
- Module 04 (ASSERT & ACS Governance): resolved a real `litellm` Rust build failure by pinning `litellm==1.91.4`, and converged on an ACS policy schema (`allow`/`deny` only) that satisfies both `agt lint-policy` and `govern()`'s runtime schema.
- Renamed all "Azure AI Foundry" references to "Microsoft Foundry" per the current product naming.

### Screenshot Updates

- Corrected multiple mismatched/duplicated screenshot captions across all 6 modules (several captions had been copy-pasted from earlier steps and described the wrong screen).

### Validation

- Authored CloudLabs Custom Validation scripts for all 6 exercises. Confirmed the CloudLabs "Custom Validation" script type executes as an Azure Function (not on the lab VM), so each validation script uses `Invoke-AzVMRunCommand` to run the real check against the VM and returns the required `{Status, Message}` JSON contract.
- Exercise_01 validation confirmed **Succeeded** end-to-end after fixing an initial dot-sourcing dependency issue and a transient `Invoke-AzVMRunCommand` 409/Conflict (retry-with-backoff added).

### Testing Notes

- **Testing Date**: 2026-07-28

### Testing Scope

Performed live, hands-on end-to-end testing of every module on a real lab VM, including real Azure AI Foundry resource deployment, real package installs, and real error reproduction/fixes (BOM in `.env`, SDK version-skew ImportError, RBAC 403, ASSERT/litellm build failure, ACS policy schema mismatches). Confirmed CloudLabs Custom Validation works for Exercise_01; Exercises 2-6 use the same validated pattern and are pending a live Validate pass per exercise.

</details>

# Testing Checklist

- [ ] VM provisions successfully and the Custom Script Extension (`psscript-01.ps1`) completes without error
- [ ] **Module 01 - Agent Harness & Local Development**: SDK installs via `pip install --pre agent-framework-core agent-framework-foundry agent-framework-devui`; `az login` succeeds; `.env` created with real `FOUNDRY_PROJECT_ENDPOINT`/`FOUNDRY_MODEL` values; `basic_agent.py` returns a time response; `harness_agent.py` + DevUI launches and responds
- [ ] **Module 02 - CodeAct & Hyperlight Execution**: `agent-framework-hyperlight` installs; `codeact_agent.py` runs; DevUI Traces tab shows the expected graceful `No Hypervisor was found for Sandbox` failure (expected on this VM size)
- [ ] **Module 03 - Deploy to Foundry Hosted Agents**: `publish_agent.py` publishes `lab-time-agent`; the agent appears in the Microsoft Foundry portal's Agents list; `test_hosted_agent.py` reconnects and returns a valid response
- [ ] **Module 04 - ASSERT Evals & ACS Governance**: ASSERT installs cleanly with `litellm==1.91.4`; the evaluation suite runs and produces `scores.jsonl`/`metrics.json`; `agt lint-policy` passes; `governed_tool.py` blocks the `delete_database` action as expected; `agt verify` passes
- [ ] **Module 05 - Multi-Agent Handoff Orchestration**: `agent-framework-orchestrations` installs; `run_handoff.py` hands off from `triage_agent` to `order_agent` and returns the expected order-status response
- [ ] **Module 06 - Observability, Traces & ROI Measurement**: `ENABLE_INSTRUMENTATION`/`ENABLE_CONSOLE_EXPORTERS` produce local trace output; a matching trace appears under `lab-time-agent`'s Traces tab in the Foundry portal; Cost Analysis shows a real accumulated cost figure
- [ ] All 6 CloudLabs Custom Validation steps (Exercise_01 - Exercise_06) return **Succeeded** when run against a VM that has completed the corresponding module
- [ ] Re-run validations against a fresh, un-started VM to confirm they correctly report **Failed** (no false positives)

# Onboarding Checklist

- [ ] ODL ID assigned and linked to this lab
- [ ] Template ID assigned and linked to this lab
- [ ] ARM template (`deploy-01.json`) reviewed and deploys cleanly with no unused resources
- [ ] Provisioning scripts (`psscript-01.ps1`, `logontask-01.ps1`) reviewed and free of unrelated/unused steps
- [ ] Lab guide (overview + 6 modules) proofread for tone, formatting, and correct Microsoft Foundry naming
- [ ] CloudLabs Custom Validation configured for all 6 exercises with `subscriptionid` (`GET-SUBSCRIPTION`) and `deploymentid` (`GET-DEPLOYMENT-ID`) parameters, Replace By: System
- [ ] Cost & Efforts Estimation workbook reviewed and shared with stakeholders
- [ ] Support Handoff manual shared with the CloudLabs support team
- [ ] Known issues documented (Hyperlight sandbox limitation, `.env` encoding, `litellm` pin, ACS policy schema)
- [ ] Escalation matrix confirmed with support team contacts
