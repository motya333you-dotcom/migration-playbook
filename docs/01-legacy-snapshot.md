# 01 - Legacy Snapshot

## Purpose

Before migrating, we need a **clear understanding of the existing VMware environment**.  
This chapter focuses on capturing the current state and identifying what will be migrated.

---

## Step 1 - Inventory

List all existing VMs and their roles:

- VM name
- CPU, RAM, and disk allocation
- Operating system
- Network configuration
- Critical services running

Create a simple table or spreadsheet to track this.

---

## Step 2 - Document Configurations

For each VM, note:

- Installed applications
- Dependencies (databases, services, files)
- Startup order and scripts
- Known issues or quirks

This documentation will **save time during migration**.

---

## Step 3 - Identify Data and Backup Needs

- Which data needs to be preserved?
- Are there snapshots or backups available?
- Can you afford downtime for each VM?

Document your backup strategy **before doing any migration**.

---

## Step 4 - Analyze Network

- Record IP addresses, VLANs, routing
- Note firewall rules or VPNs
- Identify critical connectivity between VMs

---

## Step 5 - Define Migration Candidates

- Decide which VMs **will be migrated first**
- Identify **non-essential VMs** to skip for Scope 1.0
- Flag **complex VMs** for later or logical-only migration

---

## Step 6 - Create a Baseline Repository

- Store all inventory, configuration notes, and diagrams in the `docs/` folder or version control
- This ensures **repeatability** and helps if rollback is needed
