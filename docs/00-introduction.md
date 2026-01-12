# 00 - Introduction

## Purpose

This playbook is intended to guide solo engineers or very small teams through a **realistic migration path** from legacy VMware to a Linux-based Proxmox infrastructure with Docker.

The goal is **completion**, not perfection.  
We focus on making sure you can **finish the migration** and have a working environment you understand.

AI tools can assist you along the way, but they **do not replace judgment or structure**.  
This playbook provides the path.

---

## Scope

- Single Proxmox host with a few VMs
- Core services running in Docker
- Logical migration rather than full physical VM export
- Minimal networking and monitoring setup

**Out of scope for this playbook (initial chapters):**

- Multi-node clusters
- Kubernetes
- Full enterprise-grade HA
- Cloud-first architectures

---

## Who this playbook is for

- Solo engineers or very small teams (1–3 people)
- People maintaining a legacy VMware setup that “just exists”
- Those who want a **structured path** to modern Linux-based infrastructure
- Anyone with **limited time** (≈10 hours/week)

---

## How to use this playbook

1. Follow the chapters sequentially
2. Read each step carefully
3. Execute actions incrementally
4. Use AI tools to **assist with troubleshooting or understanding details**, not for decisions
5. Document your progress

Completion is defined in the **Definition of Done** in the main README.
