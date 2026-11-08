# Azure Cost Management
source: https://learn.microsoft.com/en-us/training/modules/describe-cost-management-azure/2-describe-factors-affect-costs-azure
## Pricing Model
- **Pay as you go**
- Compute, storage, and networking: rent what you need and release it when you're done
- Costs scale with actual usage

## Factors That Affect Cost
| Factor | Description |
|---|---|
| **Resource type** | Type, settings, and region affect pricing |
| **Consumption** | Pay as you go, or commit for discounts |
| **Maintenance** | Unused resources still cost money |
| **Geography** | Region and data transfer zones |
| **Network traffic** | Outbound data transfer is priced by billing zone |
| **Subscription type** | Free trials and usage allowances vary |
| **Azure Marketplace** | Third-party vendor costs are added on top |

---

### Resource Type
With a VM, you may need to consider:
- Licensing for the operating system or other software
- The processor and number of cores
- The attached storage
- The network interface

> Just like with storage, provisioning the same virtual machine in different regions may result in different costs.

### Consumption
Discount options are available for predictable workloads:

- **Reservations**: Commit to specific resources for **1- or 3-year terms** to reduce cost. Reservations can apply to services such as:
  - Virtual machines
  - Databases
  - Storage
- **Azure Savings Plan for Compute**: Commit to an **hourly spend amount** on eligible compute services for 1 or 3 years. Azure applies the best available price as usage occurs.
- **Azure Spot Virtual Machines**: Use spare capacity at a discount, well suited to interruptible workloads such as batch data processing jobs.

### Maintenance
- Delete resources you're not using, since they still cost money.

### Geography
- Costs vary depending on the region where resources are deployed.

### Network Traffic
- **Bandwidth** refers to data moving in and out of Azure datacenters.
  - **Inbound** data transfers (data going into Azure datacenters) are generally free.
  - **Outbound** data transfers are priced based on billing zones.
- A **billing zone** is a geographical grouping of Azure regions used specifically for data transfer pricing.

### Subscription Type
- Some subscription types, such as free trials, include usage allowances that affect costs.

### Azure Marketplace
- Lets you purchase Azure-based solutions and services from third-party vendors.
- Vendor costs are added on top of your Azure costs.

