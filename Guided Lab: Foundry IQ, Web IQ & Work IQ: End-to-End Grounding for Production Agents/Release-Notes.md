# Guided Lab: Foundry IQ, Web IQ & Work IQ: End-to-End Grounding for Production Agents [NEW]

Welcome to the **Foundry IQ, Web IQ & Work IQ: End-to-End Grounding for Production Agents** Readme.md . In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, bug fixes, and other relevant changes for the lab.

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
  <summary>2026-08-19</summary>

## Release Date: 2026-08-19

### Summary of Changes

Onboarded the lab from scratch (8 exercises, 8 hours) covering the full grounding stack for a single "Contoso Support Copilot" agent: Foundry IQ corpus ingestion and retrieval tuning, Microsoft Web IQ real-time web grounding, Work IQ Microsoft 365 context grounding, a unified retrieval router across all three sources, re-ranking and faithfulness filtering, grounding evaluation and hallucination-rate measurement, and cost optimization for production readiness.

### Infrastructure Changes

- Provisioned Azure AI Search (Foundry IQ) for corpus ingestion and indexing, Azure OpenAI for chat and summarization, Azure Blob Storage as a knowledge source, and Microsoft Entra ID / Managed Identity / RBAC for authenticated access across exercises.
- Set up Grounding with Bing Custom Search as the underlying web engine for the Web IQ exercise, scoped by domain allow-lists and governed by the platform's First Party Consumption Service classification.
- Configured a Log Analytics workspace for diagnostic logging used in the final cost-attribution and production-readiness review.

### Content Changes

- Authored Exercise 1 (Foundry IQ: Corpus Ingestion and Knowledge Base Setup) and Exercise 2 (Advanced Retrieval Tuning and Measurement) covering index creation and relevance/latency/cost tuning.
- Authored Exercise 3 (Microsoft Web IQ: Real-Time Web Grounding), including the governance and compliance review step required before enabling live web results, and Exercise 4 (Work IQ: Microsoft 365 Context Grounding) for permission-trimmed SharePoint and M365 data access.
- Authored Exercise 5 (Unified Retrieval Router) to route mixed-intent queries across Foundry IQ, Web IQ, and Work IQ, and Exercise 6 (Re-ranking and Faithfulness Filtering) to improve answer quality on top of the merged retrieval set.
- Authored Exercise 7 (Grounding Evaluations and Hallucination Rate) and Exercise 8 (Cost Optimization and Production Readiness), the latter covering per-query cost attribution, tiered-routing cost reduction, Azure AI Search pricing tiers, and a production readiness checklist (identity, reliability, observability, compliance).

### Screenshot Updates

- N/A for this onboarding cycle; screenshots to be captured during the first live testing pass.

## Validations

**Validations have not been added yet for this lab.** No formal per-exercise validation or grading scripts currently exist for this lab, this is expected at the onboarding stage and is tracked as separate, future work.

### Testing Notes

- **Testing Date**: 2026-08-19

### Testing Scope

This cycle covers authoring and structural review of the lab guide against the masterdoc (all 8 exercises, overview, and objectives). Live, hands-on end-to-end execution on an Azure lab VM has not been performed as part of this entry, unlike the .NET 11 Agentic Web release note, this note does not claim reproduced build/runtime errors or RBAC fixes since no live testing pass has occurred yet.

---
</details>
