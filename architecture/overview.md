# Architecture Overview

## Purpose

This home lab is designed as a practical infrastructure platform for learning, experimentation, automation, and day-to-day self-hosted services.

The environment combines enterprise-style networking, virtualization, centralized storage, monitoring, observability, smart-home integrations, and automation while remaining small enough to operate as a personal lab.

## Design Goals

### Security and Segmentation
Separate trust zones and allow only the communication that is required.

### Reliability
Reduce single points of failure and build services around predictable operations.

### Local Control and Privacy
Keep core services and personal data under local control where practical.

### Automation
Replace repetitive manual work with repeatable workflows.

### Recoverability
Design systems so configuration and data can be restored rather than simply kept running.

### Continuous Learning
Use the lab to develop practical skills in infrastructure, networking, DevOps, observability, security, automation, and AI.

## Physical Infrastructure

The environment is centralized in a 24U floor rack located in an upstairs guest-bedroom closet.

The builder originally installed a small in-wall structured wiring cabinet, but it was not large enough for the infrastructure the lab eventually required.

To create a proper central distribution point, new fiber was run to the guest-bedroom closet and the space was converted into the primary home-lab and Ethernet aggregation location.

Cat6A cabling was personally installed, terminated, crimped, and distributed throughout the house.

SFP+ connectivity is used between core networking components to create a faster backbone between switching, compute, storage, and other infrastructure services.

## Core Components

- AT&T fiber connection
- AT&T BGW320
- Redundant UDM Pro gateways
- UniFi managed switching
- 10GbE SFP+ backbone
- 5-node Proxmox cluster
- Ubiquiti UNAS Pro
- UniFi wireless access points
- UniFi camera environment
- Home Assistant / Apple HomeKit
- Monitoring and observability stack
- Automation and AI roadmap

## Logical Architecture

The environment is segmented using multiple VLANs with inter-VLAN firewall controls.

Key workload domains include:

- Infrastructure
- Trusted devices
- IoT
- VPN
- Security cameras
- Guest
- Homelab
- DMZ
- Backup homelab

## Platform Strategy

Proxmox provides the primary virtualization layer.

Docker is used for many application workloads.

The UNAS Pro provides centralized storage.

Git is being introduced as the source-of-truth layer for documentation, application configuration, automation, and future Infrastructure as Code.

## Roadmap

The next major areas of development are:

- Infrastructure as Code
- CI/CD
- Kubernetes / K3s
- Proxmox High Availability
- AI-assisted operations
- Formal backup and disaster-recovery design
