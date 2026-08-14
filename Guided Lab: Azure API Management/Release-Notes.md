# Guided Lab: Azure API Management

Welcome to the **Guided Lab: Azure API Management** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-14</summary>

## Release Date: 2026-08-14

### Summary of Changes

Performed end-to-end lab testing and validation, including Echo API, Star Wars API, Self-hosted Gateway, and Colors API/Web exercises.

### Infrastructure Changes

- Fixed Echo API 401/403 error by enabling subscription requirement and adding the correct subscription key header.
- Identified and worked around an upstream outage of the public `swapi.dev` backend used by the Star Wars API by pointing the backend Web service URL to a static mirror (`swapi.info/api`).
- Resolved Azure Container Instance deployment failures for the Colors Web/API containers (`InvalidOsType`, `ResourceRequestsNotSpecified`) by explicitly specifying `--os-type Linux --cpu 1 --memory 1.5`.
- Resolved Azure Functions deploy failure caused by a `TargetFramework` mismatch (project targeted `net10.0`, installed SDK was 8.0.100) by retargeting the project to `net8.0` and rebuilding.
- Resolved Docker Desktop installation failure caused by a transient Chocolatey community feed outage (503/504 errors) by installing directly from Docker's CDN, after enabling the required `Microsoft-Windows-Subsystem-Linux` and `VirtualMachinePlatform` Windows features.
- Successfully deployed the Self-hosted Gateway (`OnPremiseGateway`) via Docker using the `env.conf` downloaded from the APIM Deployment blade.

## Content Changes

1. Verified that DevTools Network tab visibility issues in the developer portal walkthrough are a browser window/docking width limitation, not a lab content issue.
2. Verified that the APIM Test console's tracing UI has moved from separate Message/Trace tabs to an inline **Trace** button alongside **Send** in the current portal.

## Validations

All validations succeeded.

### Testing Notes

- **Testing Date**: 2026-08-14

### Testing Scope

Successfully completed end-to-end lab testing and validation across Echo API, Star Wars API, Self-hosted Gateway deployment, and Colors API/Web container instances. Thoroughly reviewed and validated all lab instructions, ensuring they are accurate, up to date, and aligned with the latest platform behavior.

---

</details>
