# Automation

## Overview

Automation is a major design goal for the home lab.

The objective is to reduce repetitive manual work while maintaining visibility, control, and safety.

## Current Platform

n8n is the primary workflow orchestration platform.

GitHub is being introduced as the source-control and change-history layer.

## Automation Domains

- Infrastructure administration
- Application deployment
- Monitoring workflows
- Notification workflows
- Smart-home actions
- Configuration management
- Documentation
- Future AI-assisted operations

## Safety Boundaries

The long-term model separates read-only visibility, approved workflow execution, and privileged infrastructure actions.

Sensitive actions should require authentication and, where appropriate, explicit human approval.
