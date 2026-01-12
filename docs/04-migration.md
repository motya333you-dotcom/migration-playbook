# 04 - Migration

## Purpose

This chapter guides you through **migrating services from legacy VMware to the new Proxmox setup**.

Scope 1.0 focuses on **logical migration** — moving applications and data, not full VM disks.

---

## Step 1 - Prioritize VMs

- Identify **critical services** to migrate first
- Non-essential VMs can be skipped for Scope 1.0
- Flag any **complex dependencies** for later

---

## Step 2 - Prepare Proxmox VMs

- Ensure target VMs exist
- OS installed and updated
- Network and storage configured

---

## Step 3 - Install Docker

- On application VM: install Docker and Docker Compose
- Verify Docker runs correctly
- Document the installation process for repeatability

---

## Step 4 - Move Application Services

- Copy configuration files, scripts, and relevant data
- Recreate services in Docker containers using **docker-compose.yml**
- Test each service individually before moving to the next

---

## Step 5 - Validate

- Confirm services run correctly in the new environment
- Verify connectivity between VMs
- Test backups and snapshots
- Document any issues and solutions

---

## Step 6 - Optional: Database Migration

- If a database exists, create a container or VM for it
- Use logical export/import (SQL dump, data files)
- Test application connectivity
