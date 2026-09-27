# Infrastructure as Code

## Goal

Move infrastructure configuration from manual, one-off changes toward repeatable and version-controlled definitions.

## Planned Tooling

- GitHub
- Ansible
- Terraform / OpenTofu
- Docker Compose
- GitHub Actions

## Target Operating Model

1. Define the desired change in Git.
2. Review the change.
3. Validate syntax and configuration.
4. Apply the change through controlled automation.
5. Record the result.
6. Monitor the environment after deployment.

## Public vs Private Repositories

Public repositories contain sanitized documentation and portfolio examples.

Private repositories contain internal addressing, hostnames, port mappings, sensitive topology, and operational configuration.

Passwords, private keys, API tokens, and similar secrets remain outside source control.
