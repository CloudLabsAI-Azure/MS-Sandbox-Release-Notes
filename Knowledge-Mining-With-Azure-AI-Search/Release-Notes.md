# Knowledge Mining With Azure AI Search

Welcome to the **Knowledge Mining With Azure AI Search** Readme.md. In this page, we will document the changes made during the last testing cycle, including updates related to the infrastructure, content, screenshots, and other relevant changes for the lab.

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
  <summary>2025-05-27 - Onboarding</summary>

### Summary

- Successfully onboarded the Explore Knowledge Mining lab. The lab environment, Azure AI Search workflow, AI enrichment pipeline, and end-to-end indexing and querying scenarios have been validated.
 
### Infrastructure

- Provisioned and configured the required lab environment, including:
  - Lab VM pre-configured with all required files and resources for the hands-on lab experience.

- Provisioned and configured the required lab environment, including:

  - Microsoft Azure AI Search resource for indexing and querying customer review data.
  - Azure AI Services resource for AI-powered enrichment and cognitive skills processing.
  - Azure Storage Account with Blob Containers for storing raw documents and knowledge store outputs.
  - Knowledge Store containers for storing enriched projections, images, entities, and extracted metadata.
  - Pre-configured datasets containing customer review documents for indexing scenarios.

### Content 

- Integrated the lab guide aligned with the TOC, which includes:

  - Step-by-step instructions for creating Azure AI Search, AI Services, and Storage Account resources.
  - Hands-on exercises for uploading customer review documents to Azure Blob Storage.
  - AI enrichment scenarios using OCR, sentiment analysis, key phrase extraction, location extraction, image tagging, and caption generation.
  - End-to-end indexing workflow using Azure AI Search Import Data Wizard.
  - Querying and filtering scenarios using Search Explorer with JSON-based search queries.
  - Knowledge Store exploration scenarios covering projections, entities, image outputs, and table storage validation.

### Validation

- Successfully validated the following in the lab:

  - Azure AI Search resource deployment and configuration.
  - AI Services integration with Azure AI Search enrichment pipeline.
  - Storage Account and Blob container setup with uploaded review documents.
  - Successful execution of indexer, skillset, and search index creation workflows.
  - AI enrichment outputs including OCR, sentiment detection, key phrase extraction, image captions, and location extraction.
  - Search Explorer queries and filtering scenarios for sentiment and location-based searches.
  - Knowledge Store outputs including projections, JSON objects, images, and table entities.

### Testing Scope

- Performed end-to-end testing of all lab tasks to ensure alignment with instructions, successful AI enrichment processing, indexing workflow execution, and query validation scenarios.
---
</details>