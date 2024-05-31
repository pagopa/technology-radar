---
title: "Azure Notification Hub"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, notification]
---

[Azure Notification Hub](https://azure.microsoft.com/en-us/products/notification-hubs) provide an easy-to-use and scaled-out push engine that enables you to send notifications to any platform (iOS, Android, Windows, etc.) from any back-end (cloud or on-premises). Notification Hubs works great for both enterprise and consumer scenarios.

### Use cases

Here are a few example scenarios:

- Send breaking news notifications to millions with low latency.
- Send location-based coupons to interested user segments.
- Send event-related notifications to users or groups for media/sports/finance/gaming applications.
- Push promotional contents to applications to engage and market to customers.
- Notify users of enterprise events such as new messages and work items.
- Send codes for multi-factor authentication.

### Reference of usage in our organization

The Azure Notification Hub service is used within the IO infrastructure for registering user devices and sending push notifications.

io-services-cms is an example of an application that reads and writes on a Cosmos DB using SQL API:

* [application repository](https://github.com/pagopa/io-functions-pushnotifications)
