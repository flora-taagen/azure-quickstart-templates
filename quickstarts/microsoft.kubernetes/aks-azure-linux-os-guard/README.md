---
description: Deploy a managed cluster with Azure Container Service (AKS) using Azure Linux container hosts with OS Guard security features
page_type: sample
products:
- azure
- azure-resource-manager
urlFragment: aks-azure-linux-os-guard
languages:
- bicep
- json
---
# Azure Container Service (AKS) with Azure Linux OS Guard

![Azure Public Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/PublicLastTestDate.svg)
![Azure Public Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/PublicDeployment.svg)

![Azure US Gov Last Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/FairfaxLastTestDate.svg)
![Azure US Gov Last Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/FairfaxDeployment.svg)

![Best Practice Check](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/BestPracticeResult.svg)
![Cred Scan Check](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/CredScanResult.svg)

![Bicep Version](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.kubernetes/aks-azure-linux-os-guard/BicepVersion.svg)

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fflora-taagen%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.kubernetes%2Faks-azure-linux-os-guard%2Fazuredeploy.json)
[![Deploy To Azure US Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.svg?sanitize=true)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fflora-taagen%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.kubernetes%2Faks-azure-linux-os-guard%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fflora-taagen%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.kubernetes%2Faks-azure-linux-os-guard%2Fazuredeploy.json)

## Deployment

This template deploys an **AKS cluster** with Azure Linux container hosts and enhanced security features through OS Guard capabilities. The template includes:

- **Azure Linux OS**: Container-optimized Linux distribution designed for Azure
- **Microsoft Defender for Containers**: Advanced threat protection for containerized environments
- **Security Monitoring**: Enhanced security posture with workload identity and security profiles
- **OS Guard Features**: Advanced security monitoring and protection for the operating system layer

## Security Features

### OS Guard Capabilities
This template enables several security features that collectively provide "OS Guard" functionality:

- **Microsoft Defender for Containers**: Provides runtime threat detection and vulnerability management
- **Workload Identity**: Enables secure authentication between workloads and Azure services
- **Security Monitoring**: Comprehensive logging and monitoring of security events
- **Azure Linux OS**: Hardened container-optimized operating system

### Parameters

- `clusterName`: Name of the AKS cluster
- `location`: Azure region for deployment
- `dnsPrefix`: DNS prefix for the cluster FQDN
- `agentCount`: Number of agent nodes (1-50)
- `agentVMSize`: VM size for agent nodes
- `linuxAdminUsername`: Administrator username for Linux VMs
- `sshRSAPublicKey`: SSH public key for authentication
- `enableDefender`: Enable Microsoft Defender for Containers (default: true)
- `logAnalyticsWorkspaceId`: Optional Log Analytics workspace for monitoring

## Prerequisites

1. **SSH Key Pair**: Generate an SSH key pair for secure access to the cluster nodes
2. **Log Analytics Workspace** (Optional): For enhanced monitoring and security logging
3. **Appropriate Permissions**: Ensure you have permissions to create AKS clusters and related resources

## Post-Deployment

After deployment, you can:

1. Connect to the cluster using `kubectl`
2. Review security recommendations in Microsoft Defender for Cloud
3. Monitor security events through Log Analytics (if configured)
4. Verify workload identity configuration

For information about managing AKS clusters, see the [AKS documentation](https://docs.microsoft.com/azure/aks/).

`Tags: Microsoft.ContainerService/managedClusters, SystemAssigned, AzureLinux, Defender, Security`