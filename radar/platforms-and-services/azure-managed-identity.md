---
title: "Azure Managed Identity"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, security]
---

[Azure Managed Identities](https://learn.microsoft.com/en-us/entra/identity/managed-identities-azure-resources/overview) simplify identity management for applications and services running in the cloud. They provide a secure and seamless way for applications to access Azure resources without the need for explicit credentials. Managed Identities are tightly integrated with [Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/whatis) and eliminate the need for developers to manage and rotate authentication keys manually. This helps enhance security by reducing the risk associated with managing and storing sensitive credentials. Azure Managed Identities come in two types: System-assigned, which is tied to an Azure resource, and User-assigned, which can be associated with multiple resources.

### Use cases

Managed Identities have a wide usage in our organization. They are the preferred way to authenticate services between each other due to the passwordless approach and the role assignment granularity. Creating a managed identity doesn't require any Entra ID role: RBAC built-in roles are sufficient. This is a strong point to prefer managed identities over service principals.

Managed identities are often preferred over connection strings. Connection strings are less granular in terms of role specification and make it difficult to identify who and what are using them. These strings should be treated as secrets, as they are at risk of being leaked if not securely stored. A key leak necessitates key rotation, creating a trickle-down effect where all related applications need to be updated accordingly.

Use system-assigned identities for any service that needs to communicate with others, such as an [App Service](https://azure.microsoft.com/en-us/products/app-service) that wants to read data from a [Storage Account](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview).

User-assigned identities are not bound to a specific resource in particular and they have their own lifecycle. For this reason, they are primarily used to federate a subscription with external services such as GitHub or Azure DevOps

### Repositories using Managed Identities

Any Azure resource can have a system-assigned identity. Here an example:

* [Grafana instance](https://github.com/pagopa/io-infra/blob/135a661b84b24e080856dda4248592a1c1a98320/src/core/grafana.tf#L17)

Often, PagoPA Terraform modules are in charge of creating the system assigned identity:

* [App Service](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/app_service/main.tf#L96)
* [Function App](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/function_app/main.tf#L312)
* [Storage Account](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/storage_account/main.tf#L78)

User-assigned identities are defined as standalone resources:

* [A user-assigned](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/github_federated_identity/main.tf#L5) managed identity [federated with GitHub](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/github_federated_identity/main.tf#L44)
* [Identity subscription roles](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/github_federated_identity/main.tf#L13)
