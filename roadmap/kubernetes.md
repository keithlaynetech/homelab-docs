# Kubernetes / K3s Roadmap

## Goal

Build a lightweight Kubernetes environment on top of the existing Proxmox platform.

Kubernetes is a future learning and platform-engineering project rather than a current production dependency.

## Initial Scope

The first implementation will likely use K3s.

Areas of focus:

- Container orchestration
- Service discovery
- Cluster networking
- Ingress
- Persistent storage
- Application resiliency
- Helm
- Git-based deployment workflows
- Observability

## Design Principle

Existing Docker workloads will not be migrated simply for the sake of using Kubernetes.
