# Describe the core architectural components of Azure

## What is Microsoft Azure

Azure is a comprehensive and continuously evolving cloud platform that helps address both current and future business needs. It provides the freedom to build, manage, and deploy applications on a global network using a wide range of tools and frameworks.

Key Offerings:

- Limitless innovation: Build intelligent applications with advanced AI, cloud services, and tools.
- Seamless unification: Manage infrastructure, data, analytics, and AI solutions efficiently on a unified platform.
- Trusted technology: Rely on secure, responsible, and industry-leading solutions for your business.

What you can do with azure: Azure offers over 100 services, enabling tasks like running applications on virtual machines (VMs), exploring AI and machine learning (ML), and leveraging storage solutions that grow dynamically. It empowers solutions that go beyond traditional computing, such as intelligent bots and mixed reality.

## Get started with Azure accounts

To use Azure services, you need an Azure subscription. When completing Learn modules, a temporary subscription is created in the Learn sandbox. For real applications, you must create an Azure account, which automatically includes a subscription. Additional subscriptions can be created for different departments like development, marketing, or sales.

New users can sign up for a free Azure account to explore services at no cost. This includes:

- 12 months of free access to popular Azure products.
- A 30-day credit to use on Azure services.
- Access to 25+ always-free products.

Azure Free Student Account:

- Includes 12 months of free Azure services.
- Provides $100 credit and free developer tools.
- No credit card required for signup.

Azure subscriptions can be purchased directly from Microsoft, through a Microsoft representative, or via a Microsoft partner.

## Describe Azure physical infrastructure

Azure's datacenters house computing resources with dedicated power, cooling, and networking. These datacenters are grouped into Regions and Availability Zones to enhance reliability and resiliency.

Regions:

- A region is a geographic area containing one or more low-latency, interconnected datacenters.
- When deploying resources in Azure, users must choose a region.

Availability Zones:

- Physically separate datacenters within a region, each with independent power, cooling, and networking.
- Designed for high availability—if one zone fails, others continue running.
- Used for VMs, managed disks, load balancers, and SQL databases.
- Types of services:
    - Zonal: Resources pinned to a specific zone (e.g., VMs, managed disks).
    - Zone-redundant: Automatically replicated across zones (e.g., zone-redundant storage).
    - Non-regional: Always available and resilient to regional outages.

Region Pairs:

- Most regions are paired with another region at least 300 miles away for disaster recovery.
- Benefits:
    - In case of major outages, one region is prioritized for recovery.
    - Planned updates are rolled out sequentially to minimize downtime.
    - Data remains within the same geography for compliance.
- Examples: West US ↔ East US, Southeast Asia ↔ East Asia.

Sovereign Regions:

- Isolated instances of Azure for legal or compliance reasons.
- US Government Regions: For U.S. agencies, operated by screened personnel (e.g., US DoD Central, US Gov Virginia).
- China Regions: Operated by 21Vianet under a Microsoft partnership (e.g., China East, China North).

## Describe Azure management infrastructure

Azure management is structured in a hierarchy: Resources → Resource Groups → Subscriptions → Management Groups.

Azure Resource Groups:

- Resource Group: A container for resources.
    - Each resource belongs to one group at a time.
    - Actions on a group (e.g., deletion, access control) apply to all resources inside.
    - Used to organize, manage, and provision resources efficiently.

Azure Subscriptions:

- A subscription is required to use Azure.
- Purpose:
    - Billing boundary: Separate invoices for different workloads.
    - Access control boundary: Different policies for departments or teams.
- Uses of multiple subscriptions:
    - Environments (e.g., separate development, testing, and production).
    - Organizational structures (e.g., different teams with different cost limits).
    - Billing separation (e.g., tracking production vs. testing costs).

Azure Management Groups:

- Used when managing multiple subscriptions to enforce policies at scale.
- Hierarchy:
    - Management Group → Subscriptions → Resource Groups → Resources.
- Benefits:
    - Unified policies: Apply compliance rules (e.g., restrict VMs to a specific region).
    - Access control: Assign roles at the management group level to cover multiple subscriptions.
- Limits:
    - 10,000 management groups per directory.
    - 6 levels of depth (excluding root and subscription levels).
    - Each subscription or management group has only one parent.

## Exercise - Create an Azure resource

### Task 1: Create a virtual machine

```bash
az vm create \
    --subscription "Azure subscription 1" \
    --resource-group "learn-microsoft" \
    --name vm-test \
    --authentication-type password \
    --admin-username azureuser \
    --admin-password "Password@123" \
    --nsg-rule NONE \
    --public-ip-sku Standard
```

### Task 2: Verify resources created

```bash
az resource list \
    --subscription "Azure subscription 1" \
    --resource-group "learn-microsoft" \
    --output table
```
