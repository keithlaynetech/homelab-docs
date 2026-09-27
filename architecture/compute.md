# Compute Architecture

## Overview

The compute platform is a five-node Proxmox cluster.

### Primary Compute

- 3 × Minisforum MS-01

### Secondary Compute

- 2 × Beelink EQ14

## Why Proxmox

Proxmox provides a practical platform for virtual machines, LXC containers, cluster operations, workload placement, shared storage integration, network segmentation, snapshots, backups, and future high-availability testing.

## VM vs LXC

VMs are preferred when a workload requires stronger isolation, dedicated kernel behavior, specialized networking, or higher compatibility confidence.

LXC containers are useful for lightweight Linux services where shared-kernel operation is appropriate.

## Operational Model

The cluster is managed as one infrastructure platform rather than five unrelated servers.

Operational concerns include node health, cluster membership, storage availability, network connectivity, resource pressure, workload placement, and maintenance sequencing.

## Workload Lifecycle

Lifecycle management includes provisioning, configuration, patching, restart behavior, storage dependencies, network dependencies, backup considerations, and retirement.

## Templates and Standardization

A future direction is to standardize common deployments using:

- VM templates
- Container baselines
- Docker Compose
- Version-controlled configuration

## Cluster Quorum

The five-node cluster provides practical experience with quorum, node membership, cluster communication, and distributed decision making.

## High Availability

Proxmox High Availability is not currently enabled.

It is a future project and will be implemented only after the required storage, networking, workload placement, and recovery behavior are fully understood and tested.
