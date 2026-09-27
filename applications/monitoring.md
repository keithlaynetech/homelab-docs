# Monitoring

Monitoring answers:

> Is the environment healthy right now?

## Core Tools

- Prometheus
- VictoriaMetrics
- Grafana
- Uptime Kuma
- Node Exporter
- SNMP Exporter
- Blackbox Exporter
- Alertmanager

## Monitoring Domains

### Compute
CPU, memory, disk, node health, and resource pressure.

### Storage
Capacity, availability, mount state, and storage health.

### Network
Device availability, interface status, traffic, latency, and link state.

### Applications
Service uptime, endpoint reachability, application availability, and supporting dependencies.

## Design Philosophy

Monitoring should provide actionable signals rather than simply collecting large amounts of data.
