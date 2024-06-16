---
title: "Azure Notification Hub"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, notification]
---

[Azure Notification Hub](https://azure.microsoft.com/en-us/products/notification-hubs)
provide an easy-to-use and scaled-out push engine that enables you to send
notifications to any platform (iOS, Android, Windows, etc.) from any back-end
(cloud or on-premises). Notification Hubs works great for both enterprise and
consumer scenarios.

### Use cases

Here are a few example scenarios:

- Send breaking news notifications to millions with low latency.
- Send location-based coupons to interested user segments.
- Send event-related notifications to users or groups for
  media/sports/finance/gaming applications.
- Push promotional contents to applications to engage and market to customers.
- Notify users of enterprise events such as new messages and work items.
- Send codes for multi-factor authentication.

### Reference of usage in our organization

The Azure Notification Hub service is used within the IO infrastructure for
registering user devices and sending push notifications.

io-functions-pushnotifications is an example of an application that makes use of
Azure Notification Hub to send millions of push notifications to the devices of
App IO's users:

- [application repository](https://github.com/pagopa/io-functions-pushnotifications)
- [infrastructure definition](https://github.com/pagopa/io-infra/blob/52b624c44a5f00b434c86d999fa3bbdea91046d8/src/notification-hubs/prod/notification_hub_ntfns_common.tf#L1)
  to provision the Notification Hub namespace along with Notification Hubs and
  their authorization rules
