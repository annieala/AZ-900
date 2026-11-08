# Azure Arc

## What Is It?

- Extends Azure **compliance and monitoring** to resources **outside Azure**
- Works through **Azure Resource Manager (ARM)**
- Delivers a **consistent management platform** for:
  - **Multicloud** environments
  - **On-premises** environments
- **Goal:** simplify **governance and management** across all your environments

---

## How It Works: Unified Management Across Environments

**Azure Arc (via Azure Resource Manager)** manages resources in three places:

| Environment      | What's Managed                                                                          |
| ---------------- | --------------------------------------------------------------------------------------- |
| **Azure**        | Native Azure resources, managed through ARM with **policy, monitoring, and compliance** |
| **On-premises**  | Servers, Kubernetes clusters, SQL Server, Azure data services, VMs                      |
| **Other clouds** | Servers, Kubernetes clusters, SQL Server, Azure data services, VMs                      |

---

## What Azure Arc Lets You Do

- **Manage everything together** by **projecting** existing non-Azure resources into **ARM**
- Manage **multicloud and hybrid** VMs, Kubernetes clusters, and databases **as if they were running in Azure**
- Use **familiar Azure services and management tools**, no matter where resources live
- Keep using **traditional IT operations (ITOps)** while adding **DevOps** practices for new cloud-native patterns
- Configure **custom locations** as an **abstraction layer** on top of Azure Arc-enabled Kubernetes clusters and cluster extensions

---

## Resource Types Azure Arc Can Manage Outside Azure

- **Servers**
- **Kubernetes clusters**
- **Azure data services**
- **SQL Server**
- **Virtual machines (VMs)**

---

## Quick Review

| Term                 | Meaning                                                     |
| -------------------- | ----------------------------------------------------------- |
| **Azure Arc**        | Manages non-Azure resources as if they were in Azure        |
| **ARM**              | Azure Resource Manager; the management layer Arc uses       |
| **Projecting**       | Making outside resources appear and be managed in ARM       |
| **Hybrid**           | A mix of on-premises and cloud                              |
| **Multicloud**       | Using more than one cloud provider                          |
| **Custom locations** | Abstraction layer on top of Arc-enabled Kubernetes clusters |

- **Key idea:** one place to manage **Azure + on-premises + other clouds**
