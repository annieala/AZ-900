# Azure Policy

## Purpose

- **Key questions it answers:**
  - How do you make sure your resources stay compliant?
  - Can you be alerted when a resource's configuration changes?
- Lets you **create, assign, and manage policies** that **control or audit** your resources
- Enforces rules across resource configurations so they **stay compliant with your standards**

## How Azure Policy Works (Flow)

1. **Define an initiative** (a group of policies)
   - Example initiative: _Enable Monitoring in Security Center_
     - Policy: Monitor unencrypted SQL Database
     - Policy: Monitor OS vulnerabilities
     - Policy: Monitor missing Endpoint Protection
2. **Assign to a scope** (policies are inherited)
   - Management group → Subscription → Resource group
3. **Evaluate each resource**
   - VM → ✅ Compliant
   - SQL Database → ❌ Non-compliant
   - Storage → ✅ Compliant

## How Azure Policy Defines Policies

- **Two types of definitions:**
  - **Individual policies**
  - **Initiatives** = groups of related policies
- **Evaluates** resources and **highlights non-compliant** ones
- Can **prevent** non-compliant resources from being created

## Scope and Inheritance

- Policies can be set at **any level**: resource, resource group, subscription, management group, etc.
- Policies are **inherited** from parent to child
  - Set a policy high up → it automatically applies to everything below it
  - Example: a policy on a **resource group** applies to **all resources created in that group**

## Built-in Definitions

- Comes with **built-in policy and initiative definitions** for:
  - Storage
  - Networking
  - Compute
  - Security Center
  - Monitoring
- **Example:** a policy allowing only certain VM sizes
  - Triggers when you **create a new VM**
  - Triggers when you **resize an existing VM**
  - Also evaluates **existing VMs**, including ones **created before the policy existed**

## Automatic Remediation

- Can **automatically fix** some non-compliant resources and configurations
  - Example: require an **AppName tag** and have Azure Policy **add it if missing**
- You keep **full control**: resources can be marked as **exceptions**

## Integration with Azure DevOps

- Applies policies to **CI/CD pipelines**
- Covers both **pre-deployment** and **post-deployment** phases of your application

## Policy Guardrails for AI-Assisted Changes

- Azure Policy **still enforces your standards** even when teams use **Copilot**
- Can still require:
  - Allowed locations
  - Required tags
  - Approved resource SKUs
  - Security baseline controls
- Applies **no matter how the change was proposed**
- **Benefit:** teams move faster with AI while staying compliant with organizational and regulatory requirements

## Azure Policy Initiatives

- **Initiative** = a way of **grouping related policies** together
- Helps track your **compliance state for a larger goal**
- **Example initiative:** _Enable Monitoring in Azure Security Center_
  - **Goal:** monitor all available security recommendations for all Azure resource types in Security Center
  - **Includes policies such as:**
    - **Monitor unencrypted SQL Database** → finds unencrypted SQL databases and servers
    - **Monitor OS vulnerabilities** → finds servers that don't meet the configured OS vulnerability baseline
    - **Monitor missing Endpoint Protection** → finds servers without an endpoint protection agent installed
  - Contains **over 100 separate policy definitions** in total

## Quick Review

| Term            | Meaning                                                                               |
| --------------- | ------------------------------------------------------------------------------------- |
| **Policy**      | A single rule that controls or audits resources                                       |
| **Initiative**  | A group of related policies working toward one goal                                   |
| **Scope**       | Where a policy is assigned (management group, subscription, resource group, resource) |
| **Inheritance** | Policies at a higher level apply to everything below                                  |
| **Remediation** | Automatically fixing non-compliant resources                                          |
| **Exception**   | A resource excluded from a policy                                                     |
