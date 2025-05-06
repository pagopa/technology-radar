---
title: "Azure Database for PostgreSQL - Flexible Server"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, database, postgresql, dx]
---

[Azure Database for PostgreSQL - Flexible Server](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/overview) is a fully managed database service designed to provide granular control and flexibility over database management functions and configuration settings. It offers robust cost optimization options, high availability within the same zone and across zones, and customer-managed maintenance windows.

## Use cases

Ideal for production workloads requiring a PostgreSQL database with high availability, granular control over server configuration, and cost optimization. Suitable for new applications or migrating from other PostgreSQL deployments or on-premises instances.

## Reference of usage in our organization

Azure Database for PostgreSQL - Flexible Server is our standard for PostgreSQL deployments and is utilized in various services, including:

-   Bonus & Payments - Carta Giovani Nazionale [infrastructure definition with DX module](https://github.com/pagopa/io-cgn/blob/main/infra-pe/resources/_modules/postgresql_db/postgresql_db.tf) | [application repository](https://github.com/pagopa/io-cgn)
-   IO Services CMS [infrastructure definition](https://github.com/pagopa/io-services-cms/blob/master/infra/src/database_review.tf) | [application repository](https://github.com/pagopa/io-services-cms)
