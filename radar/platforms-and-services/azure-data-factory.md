---
title: "Azure Data Factory"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, data, etl, integration]
---

[Azure Data Factory (ADF)](https://azure.microsoft.com/en-us/products/data-factory) is a cloud-based ETL and data integration service provided by Microsoft Azure. It allows users to create, schedule, and orchestrate data workflows (pipelines) that can ingest data from various sources, transform it, and load it into destinations like data warehouses or data lakes. ADF supports a wide range of connectors and provides a visual interface for building and monitoring pipelines, as well as code-based options for more complex scenarios.

## Use cases

- **ETL/ELT Processes:** Extracting data from disparate sources (databases, SaaS apps, file shares), transforming it (cleaning, joining, aggregating), and loading it into analytical stores (Azure Synapse Analytics, Azure SQL Database, Azure Data Lake Storage).
- **Data Integration:** Combining data from multiple systems for a unified view.
- **Data Migration:** Moving data between on-premises and cloud environments or between different cloud services.
- **Orchestration:** Managing complex workflows involving data movement and processing tasks, potentially triggering other Azure services like Azure Databricks or Azure Functions.

## Reference of usage in our organization

Azure Data Factory has been adopted within our organization as a centralized solution for orchestrating data ingestion and transformation pipelines. We leverage its capabilities primarily for managing our data workflows through a single, centralized Data Factory instance.

An implementation includes our cross-region data migration initiative. We've successfully setup Azure Data Factory for data migration to the Italy North region. The infrastructure definition, is available in our [GitHub repository](https://github.com/pagopa/io-infra/blob/main/src/migration/prod/italynorth.tf).
