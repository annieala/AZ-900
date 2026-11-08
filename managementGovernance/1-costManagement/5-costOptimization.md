# Azure Cost Optimization Options (AZ-900 Notes)

Source: [Describe cost optimization options in Azure – Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-cost-management-azure/7a-describe-cost-optimization-options)

---

## Reservations

- Best for **stable, predictable** workloads.
- You commit to **specific resource capacity** for a **one-year or three-year** term, and Azure applies discounted pricing to matching usage.

## Azure Savings Plan for Compute

- Another **commitment-based** option for compute services.
- Instead of committing to a specific VM family or instance type, you commit to an **hourly spend amount** for **one or three years**.
- Savings are applied to eligible compute usage.

## Spot Pricing

- Spot Virtual Machines use **unused Azure capacity** at reduced prices.
- Best for **interruptible** workloads, because Azure can reclaim that capacity when it needs it.

---

## Decision Guide

| Choose... | When... |
|---|---|
| **Reservations** | Workloads are predictable and long-running, with stable resource needs |
| **Azure savings plan for compute** | Usage is steady, but you need flexibility across compute services |
| **Spot pricing** | Workloads are fault-tolerant or interruptible, and lowest cost is the top priority |

### Examples

- **Reservations:** A production SQL workload that runs 24/7.
- **Savings plan for compute:** A mixed web/API workload that shifts among compute services.
- **Spot pricing:** Batch rendering or test jobs that can restart.

---

## Review Choices Regularly

Usage patterns change over time, so revisit your pricing choices:

- A workload that starts as interruptible might become **business-critical** later and need to move from Spot to a more predictable pricing model.
- A workload that becomes **more stable** over time may save money long term by moving from on-demand (pay-as-you-go) pricing to a commitment model.

---

## Quick Review

| Option | Commitment | Flexibility | Risk of interruption |
|---|---|---|---|
| Reservations | 1 or 3 years, specific resource | Low | None |
| Savings plan for compute | 1 or 3 years, hourly spend | Medium (across compute services) | None |
| Spot pricing | None | High | Yes, Azure can reclaim capacity |