# Azure Cost Management (AZ-900 Notes)
source: https://learn.microsoft.com/en-us/training/modules/describe-cost-management-azure/6-describe-azure-tool

## Why Cost Management Matters

Microsoft Azure is a global cloud provider, meaning you can provision resources anywhere in the world.

You can provision resources rapidly to meet a sudden demand, to test out a new feature, or even by accident. You may not be aware of these resources until it's time for the invoice.

**Cost Management** is a set of tools that helps organizations analyze, monitor, and manage costs to avoid those situations. It lets you:

- Quickly check Azure resource costs
- Create alerts based on resource spend
- Create budgets that can be used to automate management of resources

---

## Cost Analysis

Cost analysis is a feature within Cost Management that provides a quick visual of your Azure costs. You can view the total cost in a variety of ways, including by:

- Billing cycle
- Region
- Resource
- Service

Use cost analysis to explore and analyze your cloud costs:

- View **aggregated costs** by subscription, resource group, or service to understand where costs accrue and identify spending trends.
- View **accumulated costs over time** to estimate monthly, quarterly, or yearly cost trends against a budget.

---

## Cost Alerts

There are three types of cost alerts. All of them can be viewed in the Azure portal under **Cost alerts**.

### 1. Budget Alerts

- Notify you when spending reaches or exceeds a threshold you define.
- Budgets can be created in the **Azure portal** or with the **Azure Consumption API**.
- Alerts are generated automatically whenever the budget alert conditions are met.
- When an alert is generated, it appears in Cost alerts, and an email is sent to the people on the budget's alert recipient list.

> **Example:** An alert is set at 80% of a monthly dev/test budget, so the team can investigate and right-size resources before costs exceed the target.

### 2. Credit Alerts

- Notify you when your **Azure prepayment** is consumed.
- Azure prepayment applies to organizations with **Enterprise Agreements (EA)**.
- Generated automatically at **90%** and **100%** of your Azure credit balance.
- When an alert is generated, it appears in Cost alerts and in an email sent to the account owners.

### 3. Department Spending Quota Alerts

- For **Enterprise Agreement** customers.
- Notify you when department spending reaches a fixed threshold of the quota (for example, 50% or 75% of the quota).
- Spending quotas are configured in the Azure portal.
- When a threshold is met, an email is sent to department owners and the alert appears in Cost alerts.

---

## Budgets

- Set spending limits by **subscription**, **resource group**, or **service type**.
- Configure **automation** to suspend or modify resources when a threshold is reached.

---

## Common Cost Management Tasks

- Spotting a **sudden spend increase** after a deployment
- Identifying **idle resources** in non-production subscriptions
- Validating whether **tagging and budgets** are working as expected

---

## Quick Review

| Feature | What it does |
|---|---|
| Cost analysis | Visualize and explore costs by billing cycle, region, resource, or service |
| Budget alerts | Notify when spend hits a threshold you define |
| Credit alerts | Notify at 90% and 100% of EA prepayment consumed |
| Department spending quota alerts | Notify EA department owners when spending hits a quota threshold |
| Budgets | Set spending limits and trigger automation at thresholds |

