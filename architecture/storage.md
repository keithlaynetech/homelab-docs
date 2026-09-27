# Storage Architecture

## Platform

Centralized storage is provided by a Ubiquiti UNAS Pro.

## Capacity

- 6 drives
- Approximately 40 TB usable capacity
- RAID 5

The 40 TB figure represents usable capacity after RAID 5 rather than raw drive capacity.

## RAID

RAID 5 provides single-drive fault tolerance.

RAID is not treated as a backup strategy.

## Protocols

- NFS
- SMB

## Uses

Centralized storage is used for application data, media libraries, shared VM storage, file shares, and supporting backup workflows.

## Network Connectivity

Storage participates in the higher-speed SFP+ backbone so compute and application workloads can access centralized storage efficiently.

## Persistent Mounts

Persistent mounts are treated as an operational dependency.

A VM or container may be running successfully while the application itself is unhealthy if required storage mounts are unavailable.

## Backup Strategy

A formal backup and disaster-recovery architecture is still being developed.

Planned work includes retention policy, restore testing, off-site protection, recovery objectives, and backup monitoring.
