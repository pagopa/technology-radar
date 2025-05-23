---
title: "Azure Function App"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, compute, dx]
---

[Azure Function App](https://azure.microsoft.com/en-us/products/functions) is a
serverless computing service on Microsoft Azure that allows developers to build
and deploy event-driven, scalable functions without managing the underlying
infrastructure. It enables the execution of code in response to triggers like
HTTP requests, timers, database changes, or messages from other Azure services.
Function Apps support multiple programming languages such as C#, JavaScript,
Python, and Java, facilitating rapid development and deployment of small,
focused pieces of code (functions) that can scale automatically based on demand.

## References of usage in our organization

We use Azure Function App to run code snippets written in different languages.

io-messages is an example of a Typescript function app:

- [application repository](https://github.com/pagopa/io-functions-app-messages)
- [infrastructure repository](https://github.com/pagopa/io-infra/blob/6d26bd3d90dc2103d4a0f1cb8212bddfc1af5340/src/core/app_messages.tf#L151)
  to provision Function App using internal Terraform modules
