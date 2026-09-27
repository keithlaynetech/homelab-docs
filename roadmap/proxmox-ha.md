# Proxmox High Availability Roadmap

## Current State

The environment currently operates as a five-node Proxmox cluster.

Proxmox High Availability is not currently enabled.

## Goal

Introduce controlled workload failover after storage, network, and workload dependencies are understood and tested.

## Areas to Validate

- Cluster quorum
- Storage availability
- Workload placement
- Network dependencies
- Service startup behavior
- Stateful application behavior
- Recovery sequencing
- Failure-domain design

## Design Principle

HA should not be enabled only because the feature exists.
