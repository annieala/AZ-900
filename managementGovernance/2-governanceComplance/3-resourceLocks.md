# Azure Resource Locks

## Purpose

- A **resource lock** prevents resources from being **accidentally deleted or changed**
- **Why they're needed:**
  - Even with **Azure RBAC** in place, people with the right access could still delete critical resources
  - Locks add an **extra layer of protection** on top of RBAC
- Depending on the lock type, prevents resources from being **deleted** or **updated**

## Where Locks Can Be Applied

- Individual **resources**
- **Resource groups**
- Entire **subscriptions**

## Inheritance

- Locks are **inherited** from parent to child
- Lock a **resource group** → every resource inside it is also locked
  - Example: a lock on a resource group applies to its:
    - Virtual Machine
    - Storage Account
    - SQL Database

## Types of Resource Locks

There are **two** types:

### 1. Delete Lock

- Authorized users **can read and modify** the resource
- Authorized users **cannot delete** the resource

| Read       | Modify     | Delete     |
| ---------- | ---------- | ---------- |
| ✅ Allowed | ✅ Allowed | ❌ Blocked |

### 2. ReadOnly Lock

- Authorized users **can read** the resource
- Authorized users **cannot modify or delete** the resource
- Similar to restricting all authorized users to the **Reader role** permissions

| Read       | Modify     | Delete     |
| ---------- | ---------- | ---------- |
| ✅ Allowed | ❌ Blocked | ❌ Blocked |

## How to Manage Resource Locks

- **Azure portal** → **Locks** section in the resource's **Settings** pane
- **Azure PowerShell**
- **Azure CLI**
- **Azure Resource Manager (ARM) template**

## Modifying or Deleting a Locked Resource

1. **Remove the lock**
2. **Perform the action** (any action you have permission to do)

- Locks apply **regardless of RBAC permissions**
- Even an **Owner** must remove the lock before performing the blocked action

## Quick Review

| Term               | Meaning                                                     |
| ------------------ | ----------------------------------------------------------- |
| **Resource lock**  | Prevents accidental deletion or changes to resources        |
| **Delete lock**    | Can read and modify, but not delete                         |
| **ReadOnly lock**  | Can read only; no modify or delete                          |
| **Scope**          | Resource, resource group, or subscription                   |
| **Inheritance**    | Locks on a parent apply to everything inside it             |
| **Locks vs. RBAC** | Locks override RBAC; even Owners must remove the lock first |
