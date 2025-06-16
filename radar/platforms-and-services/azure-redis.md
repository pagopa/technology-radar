---
title: "Azure Cache for Redis"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, cache]
---

[Azure Cache for Redis](https://learn.microsoft.com/en-us/azure/azure-cache-for-redis/cache-overview) is a fully managed in-memory caching service that provides fast data access with low latency and high throughput. It is based on the open-source Redis engine and is designed to improve application performance by offloading database queries and enabling real-time analytics. The service supports multiple data structures, automatic scaling, and high availability with geo-replication options.

## Use cases

A common use case for Azure Cache for Redis is to improve application performance by caching frequently accessed database queries, reducing latency and load on the primary database. It is also used for real-time session storage in web applications, enabling fast and scalable user authentication and state management.

## Repositories using Azure Cache for Redis

- [infrastructure repository](https://github.com/pagopa/io-infra/blob/888081627bb9da110423d43c42def7dde5b839bf/src/common/_modules/redis/main.tf#L1) to provision Cache for Redis using Terraform
- [application code](https://github.com/pagopa/io-fims/blob/f1ddfffa0f1ebcfcc79d3035c6a1bbcd931f9f2b/apps/op-app/src/web.ts#L45)
