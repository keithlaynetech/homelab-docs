# Network Architecture

## Overview

The home network is built around a UniFi-managed environment with redundant gateway infrastructure, managed switching, wired and wireless segmentation, and a 10GbE SFP+ backbone.

## Internet Edge

Internet connectivity is provided through AT&T Fiber using a BGW320 gateway.

Behind the ISP edge, a redundant pair of UDM Pro gateways provides the primary network and security control plane.

The UDM Pro pair is designed around an active/passive model.

## Switching

The UniFi switching environment includes:

- USW 16 PoE
- USW Aggregation
- USW Pro Max 24 PoE
- Smaller access switches supporting areas such as the family room and office

SFP+ is used between core networking components for higher-speed backbone connectivity.

## Structured Cabling

Cat6A cabling was personally installed and terminated throughout the house.

The guest-bedroom closet acts as the central Ethernet distribution point.

This replaced the limitations of the small builder-installed in-wall cabinet.

## Wireless

Wireless coverage is provided by multiple UniFi access points, including:

- 2 × U6-LR
- 2 × U6 Lite-class access points

## VLAN Design

| VLAN | Purpose |
|---|---|
| 10 | Infrastructure |
| 20 | Trusted |
| 30 | IoT |
| 40 | VPN |
| 50 | Security Cameras |
| 60 | Guest |
| 70 | Homelab |
| 80 | DMZ |
| 90 | Backup Homelab |

Inter-VLAN access is controlled through firewall policy.

## DNS Architecture

DNS is provided through AdGuard Home and Unbound.

AdGuard Home provides DNS filtering, client visibility, local naming, DNS rewrites, and policy control.

Unbound provides recursive DNS resolution.

Client devices are not allowed to bypass the internal DNS architecture. Network policy forces clients to use the approved DNS path rather than arbitrary external resolvers.

## VPN

WireGuard provides remote access.

Remote clients are assigned to VLAN 40 rather than being placed directly onto the Trusted VLAN.

Firewall policy determines which internal resources are reachable after the VPN tunnel is established.

WireGuard was initially tested in an unprivileged LXC container, but kernel and networking capability restrictions made that design less practical. It was moved to a dedicated Debian VM instead of weakening the container security model.

## Reverse Proxy and TLS

Traefik provides reverse-proxy and routing functions for internal applications.

TLS termination and certificate handling are centralized where practical.

Sensitive keys and secrets are not stored in public repositories.

## Cameras

Current environment:

- 4 × PoE cameras
- 2 × wireless cameras

Planned expansion:

- 2 additional wired cameras
- 2 additional wireless cameras
