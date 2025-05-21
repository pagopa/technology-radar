---
title: "PM2"
ring: adopt
quadrant: "tools"
tags: [nodejs, compute]
---

[PM2](https://pm2.keymetrics.io/) is a production process manager for Node.js applications with a built-in load balancer. It helps keep applications alive forever, reload them without downtime, and facilitate common system admin tasks.

## Use cases

- Managing Node.js applications in production
- Ensuring high availability and uptime

Use in Azure App Service to manage Node.js applications in production:

https://learn.microsoft.com/en-us/azure/app-service/configure-language-nodejs?pivots=platform-linux#configure-nodejs-server

## Reference of usage in our organization

- [IO Session Manager](https://github.com/pagopa/io-infra/blob/main/src/domains/citizen-auth-app/08_session_manager.tf#L250)
