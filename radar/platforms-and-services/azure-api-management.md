---
title: "Azure API Management Service"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, compute]
---

[Azure API Management](https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts) (APIM) is a versatile cloud service designed to simplify the creation, deployment, and management of APIs. It enables organizations to maintain control and visibility over their APIs, offering features for versioning, authentication, and analytics. With APIM, businesses can effortlessly scale their API infrastructure to meet growing demands while ensuring security through policies and access controls. The platform facilitates seamless integration with backend services and provides a user-friendly interface for efficient API development. Overall, Azure API Management empowers organizations to optimize their API ecosystems and enhance the overall developer experience.

### Use cases

Choose Azure API Management for a gateway, ensuring centralized control and enforcement of security policies, authentication, and authorization across your APIs, safeguarding against potential vulnerabilities and unauthorized access. Use it as a single entry point of your APIs.

### Repositories using Azure Apim

Due to the pricing, a single APIM instance is used for each product shared among different teams. APIM is a big modular product, so here's a list of APIM features definitions to use as example:

* [APIM instance definition](https://github.com/pagopa/io-infra/blob/50396bdf100cd462ef2a4bc0a949fbab44751d4c/src/core/apim_v2.tf#L72)
* [APIM policy definition](https://github.com/pagopa/io-infra/blob/50396bdf100cd462ef2a4bc0a949fbab44751d4c/src/domains/citizen-auth-common/api/io_lollipop/v1/policy.xml#L1)
* [APIM API definition](https://github.com/pagopa/io-infra/blob/50396bdf100cd462ef2a4bc0a949fbab44751d4c/src/domains/citizen-auth-common/03_apim_v2.tf#L34)
* [APIM product definition](https://github.com/pagopa/io-infra/blob/50396bdf100cd462ef2a4bc0a949fbab44751d4c/src/core/apim_v2_cgn.tf#L12)
* [APIM named value definition](https://github.com/pagopa/io-infra/blob/50396bdf100cd462ef2a4bc0a949fbab44751d4c/src/core/apim_v2_cgn.tf#L56)
* [APIM subscription definition](https://github.com/pagopa/io-infra/blob/50396bdf100cd462ef2a4bc0a949fbab44751d4c/src/domains/citizen-auth-common/03_apim_v2.tf#L109)
