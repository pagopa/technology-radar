---
title: "Azure Application Insights"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, monitoring, observability]
---

[Azure Application Insights](https://azure.microsoft.com/en-us/products/monitor)
is a powerful application performance management (APM) service that enables
real-time monitoring and analysis of live applications. It helps in detecting
issues, diagnosing performance bottlenecks, and understanding how users interact
with applications. Application Insights supports a wide range of platforms,
including .NET, Java, Node.js, and more, allowing for comprehensive
observability of your application’s performance and availability.

## Use cases

Here are a few example scenarios:

- Monitor the performance and response times of API endpoints.
- Detect and diagnose performance bottlenecks or exceptions in real-time.
- Track user interactions and flows within the application.
- Analyze the overall health and performance of distributed microservices.
- Collect custom telemetry data for deeper insights into specific application
  components.
- Correlate logs, traces, and metrics to detect potential application issues
  early.

## Reference of usage in our organization

Azure Application Insights is deeply integrated into the IO infrastructure for
monitoring and observing the performance and availability of all deployed
applications. It is used to track the health of services, collect custom
telemetry, and monitor application dependencies to ensure smooth operation.

- [Resource definition](https://github.com/pagopa/io-infra/blob/main/src/common/_modules/monitoring/appi.tf)
  to provision Application Insights resources for real-time performance
  monitoring and diagnostics for various services in our platform.
- [Data retrieve](https://github.com/pagopa/io-infra/blob/1d85e07b25c3c1c26dd36a25245abcfec87be56e/src/core/monitor.tf#L4)
