---
title: "Azure App Service"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, compute]
---

[Azure App Service](https://azure.microsoft.com/en-us/products/app-service) is a fully managed platform offered by Microsoft Azure that enables developers to build, deploy, and scale web applications and APIs quickly and easily. It supports various programming languages, frameworks, and tools, including .NET, Java, Node.js, Python, and PHP, allowing for flexibility in application development.

### Repositories using Azure App Service

We use Azure App Service to run both frontend and backend applications written in different languages.

io-backend is an example of a Typescript backend application:

* [application repository](https://github.com/pagopa/io-backend)
* [infrastructure repository](https://github.com/pagopa/io-infra/blob/main/src/core/app_backend.tf#L642) to provision App Service using internal Terraform modules
