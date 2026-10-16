# Guided Lab: Hands-on with Microsoft Foundry and Agent frameworks

Welcome to the **Hands-on with Microsoft Foundry and Agent frameworks** release notes page. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-10-15</summary>

## Release Date: 2026-10-15

### Summary of Changes

Completed a testing and update cycle that moved the lab and its notebooks repository to the current Microsoft Foundry SDK (v2) and keyless authentication. The biggest change is Exercise 6, which now uses Foundry agents and the Microsoft Agent Framework in place of Semantic Kernel and AutoGen.

### Infrastructure Changes

1. Upgraded the lab VM to Python 3.14.0. The notebooks now run on a pre-built `ai-foundry-workshop (Python 3.14.0)` kernel.

2. The workshop codebase is now downloaded as a zip from the lab dataset, with automatic retries. The `.env` file is pre-created with the model, index and API-version values.

3. Pinned every notebook dependency to tested versions, including `azure-ai-projects` 2.3.0, the OpenAI SDK, the Agent Framework and OpenTelemetry. The logon script checks the SDK imports so a broken install is caught at deployment.

4. Updated the deployment template, the deployment and logon scripts, and the RBAC and policy files to match these changes, and pushed them to Azure DevOps.

5. Cleaned up the notebooks repository. The Semantic Kernel, AutoGen, Bing Grounding, Azure Functions and evaluation notebooks and the unused `docs` folder were removed or replaced, and the requirements files and `.env.example` were rewritten to match.

### Content Changes

1. Moved authentication to keyless Microsoft Entra ID. Learners no longer copy model API keys, the project connection string or an inference endpoint, and DeepSeek-V3.2 is now called through the same project endpoint.

2. Replaced Bing Grounding with the built-in **Web Search** tool. Learners no longer create a Bing connection.

3. Rebuilt Exercise 6. Task 1 attaches Azure AI Search to a Foundry agent as a tool. Task 2 builds a three-agent RAG team (TipsResearcher → FitnessCoach → SafetyReviewer) with the Microsoft Agent Framework. The GitHub sign-in and PAT steps are gone.

4. Trimmed the lab to steps that run inside the learner's sandbox:
   - Removed the Hosted Agent deployment from Exercise 4 and the Evaluation task from Exercise 5. Both now appear as short concept notes.
   - Removed the event-driven objective from Getting Started.
   - Exercise 5 tracing now connects to the project's Application Insights.
   - Changed the models to DeepSeek-V3.2 and Phi-4-reasoning.

5. Added steps to confirm each agent under **Build > Agents** in the Foundry portal before it is deleted. Getting Started's architecture and component sections were rewritten to match the lab. A clarity, wording and consistency pass was made across all exercises, and screenshots were refreshed to match the current Foundry portal and notebook output.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-10-15

### Testing Scope

Reviewed and updated all exercises, the notebooks repository and the VM deployment and logon scripts for the Foundry SDK v2 and keyless authentication. Ran each exercise's notebooks against the current Foundry portal and refreshed the screenshots to match.

---

</details>

<details>
  <summary>2026-07-08</summary>

## Release Date: 2026-07-08

### Summary of Changes

Completed a testing and validation cycle for the lab, focused on realigning the guide with the latest Microsoft Foundry experience. Updates in this cycle covered the recommended model version, the migration of exercises to the new Foundry portal, and a refresh of the underlying sample codebase.

### Infrastructure Changes

1. Updated the lab's default model deployment guidance to reference the current recommended model version, replacing references to the prior, now-superseded model.

2. Migrated all portal-based exercises from the legacy Azure AI Foundry experience to the new Foundry portal, updating navigation steps, screenshots, and terminology to match current portal behavior.

3. Refreshed the sample codebase used across the exercises to align with current SDK versions and current portal/API behavior.

### Content Changes

1. Updated exercise steps and screenshots to reflect the new Foundry portal's navigation, layout, and terminology.

2. Updated model deployment and configuration steps to reference the current recommended model.

3. Revised code samples and setup instructions to match the refreshed codebase.

4. Performed a clarity and consistency pass across the exercises, tightening instructions without changing the steps performed by the participant.

## Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-07-08

### Testing Scope

Reviewed and updated the lab guide, screenshots, and sample codebase for alignment with the new Foundry portal and current model recommendations. Verified exercise steps against current portal behavior.

### Additional Notes

- Lab testing completed successfully.

</details>
