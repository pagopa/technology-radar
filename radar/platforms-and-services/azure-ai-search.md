---
title: "Azure AI Search"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, ai]
---

[Azure AI Search](https://learn.microsoft.com/en-us/azure/search/search-what-is-azure-search) (formerly known as "Azure Cognitive Search") provides secure information retrieval at scale over user-owned content in traditional and generative AI search applications.

Information retrieval is foundational to any app that surfaces text and vectors. Common scenarios include catalog or document search, data exploration, and increasingly feeding query results to prompts based on your proprietary grounding data for conversational and copilot search.

### Use cases

Here are a few example scenarios:

- A search engine for vector search and full text and hybrid search over a search index
- Rich indexing with integrated data chunking and vectorization, lexical analysis for text, and optional applied AI for content extraction and transformation
- Rich query syntax for vector queries, text search, hybrid queries, fuzzy search, autocomplete, geo-search and others
- Relevance and query performance tuning with semantic ranking, scoring profiles, quantization for vector queries, and parameters for controlling query behaviors at runtime

### Reference of usage in our organization

**Azure AI Search** powers the search engine behind the IO app, enabling users to swiftly search and navigate through hundreds of thousands of entities and services within milliseconds.

- The [Terraform configuration](https://github.com/pagopa/io-services-cms/tree/master/infra/_modules/ai_search) provisions a secured AI Search instance and the necessary resources, ensuring automatic data indexing and search operations.
- The [REST APIs](https://github.com/pagopa/io-services-cms/tree/master/apps/app-backend/src/functions) streamline integration between the IO app's backend and frontend, providing an efficient and seamless user experience.
