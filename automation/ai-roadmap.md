# AI Agent Roadmap

## Goal

Build a conversational operations assistant for the home lab.

## Phase 1 - Read-Only Knowledge

The agent should be able to answer:

- What is running?
- Which node hosts a service?
- What is unhealthy?
- What changed recently?
- Which services depend on DNS or storage?
- What do monitoring dashboards show?
- Are there recent errors in logs?

## Phase 2 - Observability Integration

Read-only integrations with:

- Prometheus
- Grafana
- Loki
- Uptime Kuma
- Git
- Infrastructure documentation

## Phase 3 - Controlled Automation

Approved actions through:

- n8n
- Ansible
- CI/CD workflows
- Authenticated scripts

## Phase 4 - Human Approval

High-impact actions should require explicit approval.

## Security Principles

- No secrets in Git
- Least privilege
- Read-only first
- Human approval for high-risk actions
- Full logging of agent-triggered actions
