---
title: "Azure Kubernetes Service (AKS)"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, azure, kubernetes, containers, orchestration]
---

[Azure Kubernetes Service](https://azure.microsoft.com/en-us/services/kubernetes-service/)
is a managed Kubernetes service in Azure that simplifies deploying, managing,
and scaling containerized applications. AKS provides fully managed Kubernetes
clusters with integrated tools, security, and monitoring, allowing for
streamlined orchestration of workloads across environments.

### Use cases

Here are some typical scenarios:

- Containerized Application Hosting: Run, manage, and scale containerized
  applications across distributed environments with high availability.
- CI/CD Integration: Enable automated deployments with integrated CI/CD
  pipelines, supporting quick and efficient application updates.
- Multi-region and Multi-environment Clusters: Provision clusters across
  different regions and environments to support global application requirements
  and disaster recovery.
- Batch Processing: Run batch jobs or intensive computational tasks in a
  scalable and cost-efficient environment.
- Hybrid and Edge Deployments: Extend AKS to on-premises or edge environments
  using AKS on Azure Stack for hybrid workload requirements.

### Reference of usage in our organization

Azure Kubernetes Service (AKS) is provisioned entirely through Terraform within
the IO infrastructure, providing consistency and scalability across
environments. The primary AKS configuration is located here, with a dedicated
Terraform module used for deployment.

- [AKS Configuration](https://github.com/pagopa/io-infra/tree/main/src/aks-platform)
  here a terraform code that create an AKS cluster.
- [AKS Module](https://github.com/pagopa/terraform-azurerm-v3/tree/main/kubernetes_cluster)
  a dedicated Terraform module used for deployment.
- [Prometheus module](https://github.com/pagopa/terraform-azurerm-v3/tree/main/kubernetes_prometheus_install)
  for monitoring services within the clusters.
- [to support backup and restore functionalities](https://github.com/pagopa/terraform-azurerm-v3/tree/main/kubernetes_cluster_velero)to
  support backup and restore functionalities.
- [Velero backup configuration](https://github.com/pagopa/terraform-azurerm-v3/tree/main/kubernetes_velero_backup)
  that work with previus module.
