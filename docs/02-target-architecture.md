# 02 - Target Architecture

## Purpose

This chapter defines the **goal state** for Scope 1.0: the minimal Proxmox + Docker setup.

The objective is to create a **working, simple infrastructure** that is manageable by a single engineer or a very small team.

---

## Architecture Overview

- **Proxmox Host**
  - 1 physical or virtual host
  - Runs multiple VMs
- **VMs**
  - Management VM (Proxmox web UI, backups, monitoring)
  - Application VM (services running in Docker)
  - Database VM (optional, small-scale database)
- **Networking**
  - Basic internal network between VMs
  - VPN or NAT if needed for remote access
- **Storage**
  - Local storage for Scope 1.0
  - Snapshots and backups configured

---

## Principles

- **Keep it simple**: avoid multi-node clusters
- **Logical migration first**: move services, not entire disks
- **Document everything**: inventory, network, services
- **Checkpoints**: use snapshots before major changes

---

## Diagram

Create a simple diagram (ASCII or image) showing:

