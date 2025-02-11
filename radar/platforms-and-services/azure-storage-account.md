---
title: "Azure Storage Account"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, storage, dx]
---

[Azure Storage Account](https://azure.microsoft.com/en-us/products/category/storage)
provides highly available, secure, and massively scalable cloud storage for
storing any kind of data—blobs, files, queues, tables, and disks—accessible from
anywhere in the world via HTTP/HTTPS. It offers multiple storage types including
blob, file, table, and queue, suitable for various use cases from static website
hosting to backup and disaster recovery.

## Use cases

Here are a few example scenarios:

- Store unstructured data such as images, videos, and documents using Blob
  Storage.
- Host static websites directly from blob storage with scalable performance.
- Implement queues for asynchronous message processing between application
  components.
- Store and retrieve structured NoSQL data in a Table Storage.
- Manage large volumes of logs and backup data efficiently.
- Securely share files with managed access via Azure File Shares.

## Reference of usage in our organization

The Azure Storage Account service is widely used within the IO infrastructure
for multiple purposes, such as storing logs, handling notifications, and
providing durable storage for various workloads. All Function Apps deployed in
the infrastructure have an associated Azure Storage Account to manage state,
queues, and other necessary storage needs.

- [Storage definition](https://github.com/pagopa/dx/blob/main/infra/modules/azure_function_app/storage_account.tf)
  to provision Storage Accounts for different services, including log management
  and notification processing.
- [Used for notification Queue](https://github.com/pagopa/io-infra/blob/1d85e07b25c3c1c26dd36a25245abcfec87be56e/src/domains/messages-app/07_function_pushnotif.tf#L27)
