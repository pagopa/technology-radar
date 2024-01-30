---
title: "Azure Application Gateway"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, networking]
---

[Azure Application Gateway](https://learn.microsoft.com/en-us/azure/application-gateway/overview) is a regional web traffic load balancer (OSI layer 7) service. It facilitates the optimization of performance, reliability, and security for web applications. Equipped with features such as SSL termination, URL-based routing, session affinity and Web Application Firewall (WAF) integration, Application Gateway ensures efficient traffic distribution, enhanced application scalability, and protection against common web vulnerabilities. It also can be used as ingress controller for [AKS](https://azure.microsoft.com/en-us/products/kubernetes-service).

### Use cases

Opt for Application Gateway when you need to load balance web applications (HTTP/HTTPS) that can be exposed on internet or not. Remember it is a regional service, so if your application runs in multiple regions you need to replicate the Application Gateway as well (opposed to the [Front Door](https://learn.microsoft.com/en-us/azure/frontdoor/front-door-overview)).
Application Gateway is often put in front of an [APIM](https://azure.microsoft.com/en-us/products/api-management) instance for its WAF capabilities, DDoS protection and SSL offloading.

A specific [implementation for containers](https://learn.microsoft.com/en-us/azure/application-gateway/for-containers/overview) is currently in preview.

`Standard` and `WAF V2` SKUs are generally used respectively for development and production environments.

### Reference of usage in our organization

Any public facing web application is protected by the Application Gateway, which has a single instance for each stream.

* [IO infrastructure definition](https://github.com/pagopa/io-infra/blob/bcc94656f1950299d67631335c7bfeefbc1e7cb6/src/core/appgateway.tf#L28)
* [SelfCare infrastructure definition](https://github.com/pagopa/selfcare-infra/blob/9fd412cd41d8109b879e96b8ebee69b502ace391/src/core/04_appgateway.tf#L106)
