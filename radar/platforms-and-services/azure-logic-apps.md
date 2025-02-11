---
title: "Azure Logic Apps"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, automation, integration]
---

[Azure Logic Apps](https://azure.microsoft.com/en-us/products/logic-apps/) is a
cloud-based integration and automation service that enables building scalable
workflows to orchestrate business processes and automate repetitive tasks. Logic
Apps supports connectors for various cloud services, like Office 365, Dynamics
365, and others, simplifying integration with on-premises applications and
third-party services.

## Use cases

Here are some typical scenarios:

- Business Process Automation: Create workflows to automate tasks like email
  sending, request approvals, or updating records in enterprise databases.
- System Integration: Connect and synchronize data across different systems,
  such as CRM, ERP, and document management systems.
- Monitoring and Management: Implement workflows to monitor events, send
  real-time notifications, and manage automatic corrective actions.
- Data Processing: Transform and transfer data between applications, performing
  extract, transform, and load (ETL) operations.
- Notification Management: Integrate with services like Microsoft Teams or Slack
  to notify teams of important events or updates.

## Reference of usage in our organization

Azure Logic Apps is used within the IO infrastructure to orchestrate automated
workflows and facilitate integration between internal systems and cloud
services. Most configurations for Logic Apps have historically been managed
directly through the Azure portal.

However, creating resources directly in the Azure portal **should be avoided**, all
Logic Apps should be provisioned and managed through code-based configuration in
Terraform to ensure consistency and maintainability. If a Logic App is created
in the portal or already exists, a backup of the configuration must be added to
the codebase to maintain a complete infrastructure record.

Code-based configuration, however, has only been implemented in this example:

- [Logic App example in Terraform](https://github.com/pagopa/terraform-azure-auditlogs/blob/2f3ab91b561f442d241dbb5524f7307113a80f1b/examples/simple/03-test.tf#L111)
  for a specific automation workflow
