# 03 - Proxmox Setup

## Purpose

This chapter guides you through **installing and configuring Proxmox** for the target architecture.

Scope 1.0 setup: single Proxmox host with 3 VMs.

---

## Step 1 - Install Proxmox

1. Download Proxmox VE ISO
2. Boot the host and install Proxmox
3. Set hostname, network, and root password
4. Update Proxmox to the latest version

---

## Step 2 - Configure Storage

- Local storage for VMs
- Optional: additional disks for Docker volumes
- Configure backup storage (can be local or NFS)

---

## Step 3 - Create VMs

- **Management VM**
  - OS: minimal Linux (Debian/Ubuntu)
  - Install monitoring tools (Zabbix, Netdata, or simple scripts)
- **Application VM**
  - OS: minimal Linux
  - Prepare for Docker installation
- **Database VM** (optional)
  - OS: minimal Linux
  - Prepare for DB container or local database

---

## Step 4 - Networking

- Ensure VMs can communicate internally
- Optional: configure NAT or VPN for remote access
- Document IP addresses and network topology

---

## Step 5 - Proxmox Settings

- Enable snapshots
- Configure backups
- Document all configurations
- Test VM creation and deletion to ensure rollback works

---

## Step 6 - Verification

- Log in to Proxmox web UI
- Verify all 3 VMs exist and can start/stop
- Take a snapshot of the base state (this is your **baseline for migration**)
