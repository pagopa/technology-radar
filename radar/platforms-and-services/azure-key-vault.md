---
title: "Azure Key Vault"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, security]
---

[Azure Key Vault](https://azure.microsoft.com/en-us/products/key-vault) is a cloud service offered by Microsoft that allows users to securely store and manage sensitive information such as keys, passwords, certificates, and other secrets. It provides a centralized platform for managing cryptographic keys and secrets used by cloud applications and services. Key Vault helps to safeguard data with industry-standard encryption and access control mechanisms, ensuring confidentiality and integrity. It offers features like key management, secret rotation, and integration with other Azure services, enhancing security and compliance for organizations. With Azure Key Vault, users can efficiently manage and protect their sensitive information in a scalable and highly available environment. It also provides mechanism for soft delete, key rotation, granular access control using either RBAC or Entra ID integrated access policies.

### Use cases

Azure Key Vault is essential for our organization's security, particularly when it comes to storing sensitive data such as connection strings and TLS certificates. It guarantees secure storage and management of these crucial assets, boosting data protection and ensuring compliance. Its integration with various Azure services streamlines workflows while maintaining strong security protocols, showcasing our dedication to safeguarding confidential information. Additionally, Key Vault's seamless integration with Azure services allows for easy access to secrets without compromising security.

### Repositories using Azure Key Vault

Every project running on Azure has its own Key Vault to store sensitive information.

* [Key Vault module](https://github.com/pagopa/terraform-azurerm-v3/blob/92627ccc9629c51acbfbc5800377b496ba65b036/key_vault/main.tf#L2)
* [Key Vault definition](https://github.com/pagopa/io-infra/blob/900acb9f3b9307d831725367280469bb9a171aee/src/core/keyvault.tf#L9)
* [Key Vault Access Policy definition](https://github.com/pagopa/io-infra/blob/900acb9f3b9307d831725367280469bb9a171aee/src/core/keyvault_access_policy.tf#L7)
* [Key Vault secret definition](https://github.com/pagopa/io-infra/blob/900acb9f3b9307d831725367280469bb9a171aee/src/core/keyvault.tf#L34)
* [Key Vault secret usage](https://github.com/pagopa/io-infra/blob/900acb9f3b9307d831725367280469bb9a171aee/src/core/assets_cdn.tf#L67)
