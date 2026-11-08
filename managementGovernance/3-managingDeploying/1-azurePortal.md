# Azure Management Tools

## Overview

| Category         | Tool                  | What It Is                                                                    |
| ---------------- | --------------------- | ----------------------------------------------------------------------------- |
| **Graphical**    | **Azure Portal**      | Web-based console to **build, manage, and monitor** cloud resources           |
| **Environment**  | **Azure Cloud Shell** | Browser-based shell with **built-in authentication**; no local install needed |
| **Command line** | **Azure PowerShell**  | **Cmdlet**-based scripting for repeatable automation tasks                    |
| **Command line** | **Azure CLI**         | **Bash**-based commands with the **same capabilities** as PowerShell          |
| **AI-assisted**  | **Copilot in Azure**  | AI assistant giving **contextual guidance in natural language**               |

---

## Azure Portal

- Manage your Azure subscription using a **graphical user interface (GUI)**
- **What you can do:**
  - **Build, manage, and monitor** everything from simple web apps to complex cloud deployments
  - Create **custom dashboards** for an organized view of resources
  - Configure **accessibility options** for an optimal experience
- **Resiliency and availability:**
  - Has a presence in **every Azure datacenter**
  - **Resilient** to individual datacenter failures
  - Avoids network slowdowns by being **close to users**
  - **Updates continuously** with **no downtime** for maintenance

---

## Azure Cloud Shell

- A **browser-based shell** to create, configure, and manage Azure resources
- **No local installation or configuration** required
- **Already authenticated** with your Azure credentials
  - Knows **who you are** and **what permissions you have** when you sign in
- **Choose your shell:**
  - **Azure PowerShell**
  - **Azure CLI**

---

## Azure PowerShell

- A shell where **developers, DevOps, and IT** run commands called **cmdlets**
- Cmdlets call the **Azure REST API** to perform management tasks
- **Ways to use cmdlets:**
  - Run **independently** for one-off changes
  - **Combine** them to orchestrate complex actions, such as:
    - Routine **setup, teardown, and maintenance** of one or many connected resources
    - **Deploying an entire infrastructure** (dozens or hundreds of resources) from imperative code
- **Scripts** make the process **repeatable and automatable**
- **Where it runs:**
  - Azure Cloud Shell
  - Installed locally on **Windows, Linux, and macOS**

---

## Azure CLI

- Same capabilities as Azure PowerShell
- **Only difference = command syntax**
  - Azure CLI uses **Bash** commands
  - Azure PowerShell uses **PowerShell cmdlets**

---

## Copilot in Azure (AI-Assisted Operations)

- An **AI assistant** that helps administrators **work faster**
- Gives **contextual guidance in natural language**
- Some workflows can be **agent-like**, helping coordinate **multistep tasks**
- Treat Copilot as an **operational assistant**; you should still:
  - **Validate** its recommendations
  - **Confirm permissions**
  - **Review deployment changes** before applying them in **production**

---

## Quick Review

- **Portal** = GUI, dashboards, always available, no maintenance downtime
- **Cloud Shell** = browser shell, pre-authenticated, supports **both** PowerShell and CLI
- **PowerShell** = cmdlets, scripts for automation, runs on Windows/Linux/macOS
- **CLI** = same as PowerShell, but **Bash syntax**
- **Copilot** = natural-language AI helper; **always review** before production changes
