# Guided Lab: Microsoft Azure Infrastructure and Application Security

Welcome to the **Guided Lab: Microsoft Azure Infrastructure and Application Security** Readme.md. On this page, we document the updates and testing status for each module from the latest testing cycle.

## Overview
This page includes:

- Testing the status of each module  
- Content updates and fixes  
- Known issues and pending tasks  

`For any further details or inquiries, feel free to reach out to the CloudLabs support team.`  

`Email Support: cloudlabs-support@spektrasystems.com`  

# Release Notes

<details>
  <summary>2026-10-22</summary>

## Release Date: 2026-10-22

### Summary of Changes

All five modules were tested end to end and updated to match the latest Azure portal experience, including the new Virtual Network Flow Log wizard, the Network security hub that now includes Firewall Manager, and the updated WAF custom rule and condition panes.

Traffic Analytics on Virtual Network Flow Logs was failing because the lab's custom allowed-resources policy did not permit the data collection rule and data collection endpoint resources that Traffic Analytics creates. The policy has been updated to allow `Microsoft.Insights/dataCollectionRules` and `Microsoft.Insights/dataCollectionEndpoints`, and the storage SKU value was corrected from `StandardLRS` to `Standard_LRS`.

Rendering issues in the CloudLabs guide viewer, caused by indented lines directly after validation tags, have been fixed in Modules 2, 3, and 5. The Getting Started section of every module now uses a **Temporary Access Pass** for sign-in.

## Module 1: Secure administration and management

### Content Changes

- Updated the Virtual Network Flow Log steps for the new **Create a flow log** wizard (**Add virtual networks**, **Storage account**, **Configure**, and **Analytics** tabs, and **Create resource**).
- Added the **Log Analytics Workspace** and **Subscription** selections when enabling Traffic Analytics.
- Fixed grammar and wording throughout the module and updated screenshots.
- Updated the Getting Started section to use a **Temporary Access Pass**.

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-10-19

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content and screenshots were updated to match the current Azure portal.

## Module 2: Secure application

### Content Changes

- Updated the WAF custom rule steps for Application Gateway and Azure Front Door to the new **Add custom rule** and **Add condition** panes, including **Rule action**, **Operation**, and **Operator** fields.
- Updated the **Add security policy** steps and increased the Front Door propagation wait time to 15–30 minutes.
- Added a note to open **Front Door and CDN profiles** if the Azure Front Door page fails to load.
- Moved the validation step and removed the redundant prevention/detection mode toggle steps.
- Fixed grammar, rendering, and image paths, and updated screenshots.
- Updated the Getting Started section to use a **Temporary Access Pass**.

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-10-21

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content and screenshots were updated to match the current Azure portal.

## Module 3: Secure Infrastructure with Azure Firewall Premium

### Content Changes

- Updated navigation for **Firewall Manager**, which is now part of the **Network security** service, including **Azure Firewall Policies** and **Virtual Hubs**.
- Updated WAF policy association steps to **Settings > Associations**.
- Added troubleshooting notes for IDPS policy update timeouts, delayed IDPS enforcement, and the Key Vault access error for TLS inspection.
- Updated the IP Group step to use the **FirewallVMSubnet** address range instead of `*`.
- Updated log queries to **Firewall Logs (Resource Specific Tables)**.
- Added the missing validation step, fixed rendering issues, and updated screenshots.
- Updated the Getting Started section to use a **Temporary Access Pass**.

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-10-22

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content and screenshots were updated to match the current Azure portal.

## Module 4: Protecting Infrastructure with Azure DDoS Protection Plans

### Content Changes

- Clarified the public IP selection and **Add metric** steps for DDoS metrics.
- Updated the screenshot note and fixed grammar throughout the module.
- Updated the Getting Started section to use a **Temporary Access Pass**.

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-10-22

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content updates were applied to improve clarity and usability.

## Module 5: Network Management and Monitoring Revisited: Flow Logs and Traffic Analytics

### Content Changes

- Updated the Virtual Network Flow Log and Traffic Analytics steps for the new **Create a flow log** wizard.
- Updated Application Gateway and Azure Firewall navigation, and the **Network security** path for firewall policies.
- Corrected the Task 1 title, fixed the web server address placeholder, fixed rendering issues, and updated screenshots.
- Updated the Getting Started section to use a **Temporary Access Pass**.

### Validations

Validations are good. The previously failing Traffic Analytics validation has been resolved by updating the custom policy.

### Testing Notes

- **Testing Date**: 2026-10-22

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. The validation failure reported in the previous release has been resolved.

</details>

----

<details>
  <summary>2026-04-24</summary>

## Release Date: 2026-04-24

### Summary of Changes

Initial deployment failures were observed due to the service principal not being enabled and missing permissions. These issues have now been resolved, and deployments have succeeded.

Subsequently, policy-related issues were encountered. Upon cross-checking with the HOL combined lab, it was identified that custom ARM policies were not intended for guided labs. The policy has been disabled, and all lab modules are now functioning as expected.

All modules required content updates and improvements in the Getting Started section, which have been completed.

## Module 1: Secure administration and management

### Content Changes

- Module tested and verified successfully  
- Updated content and improved the Getting Started section  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-21  

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content updates were applied to improve clarity and usability.

## Module 2: Secure application

### Content Changes

- Module tested and verified successfully  
- Updated content and improved the Getting Started section  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-22  

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content updates were applied to improve clarity and usability.

## Module 3: Secure Infrastructure with Azure Firewall Premium

### Content Changes

- Module tested and verified successfully  
- Updated content and improved the Getting Started section  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-22  

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content updates were applied to improve clarity and usability.

## Module 4: Protecting Infrastructure with Azure DDoS Protection Plans

### Content Changes

- Module tested and verified successfully  
- Updated content and improved the Getting Started section  

### Validations

Validations are good.

### Testing Notes

- **Testing Date**: 2026-04-22  

### Testing Scope

Successfully completed end-to-end testing of the module and validated all lab guide steps. Content updates were applied to improve clarity and usability.

## Module 5: Network Management and Monitoring Revisited: Flow Logs and Traffic Analytics

### Content Changes

- Module tested; validation issues identified  
- Content updates and Getting Started improvements completed  

### Validations

Validation is currently failing and under review.

### Testing Notes

- **Testing Date**: 2026-04-22  

### Testing Scope

End-to-end testing was performed; however, validation failures were observed. I've shared this issue with Arun for further investigation and resolution.

</details>
