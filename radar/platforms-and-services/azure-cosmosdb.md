---
title: "Azure Cosmos DB"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, storage]
---

[Azure Cosmos DB](https://azure.microsoft.com/en-us/products/cosmos-db) is a
globally distributed, multi-model database service offered by Microsoft Azure.
It provides high-performance, low-latency access to data using various models
like document, graph, key-value, and wide-column stores. Cosmos DB ensures
global scalability with automatic and instant data replication across multiple
regions. Its multi-API support allows developers to use popular programming
models and languages to interact with the database. With its multi-region,
multi-master capabilities, Azure Cosmos DB ensures robust and resilient data
distribution, enabling seamless data access and availability across the globe.
Azure Cosmos DB stands out for its versatility by supporting SQL, MongoDB,
Cassandra, and other APIs, allowing developers to choose their preferred
programming models and seamlessly migrate existing applications to the platform.

## Use cases

Opt for Azure Cosmos DB for NoSQL simplicity with multi-model flexibility,
providing efficient and scalable data storage. More details can be found
[here](https://learn.microsoft.com/en-us/azure/cosmos-db/use-cases)

## Reference of usage in our organization

We utilize Azure Cosmos DB across multiple applications, predominantly employing
the SQL API, which receives excellent support directly from the vendor.

io-services-cms is an example of an application that reads and writes on a
Cosmos DB using SQL API:

- [application repository](https://github.com/pagopa/io-services-cms)
- [infrastructure definition](https://github.com/pagopa/io-services-cms/blob/10a0d758781e1e2ed7f3a4e5fc3e0d8044719724/infra/src/database_cms.tf#L2C28-L2C28)
  to provision Cosmos DB geo-replicated account and its databases and containers
