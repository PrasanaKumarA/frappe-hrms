# Frappe HRMS Development Workspace

This repository contains the development environment and workspace configuration for Frappe HRMS.

## Project Structure

```
├── .devcontainer/                  # VS Code Dev Container and Docker Compose configuration
├── deployment/                     # Deployment manifests and configurations
├── development/
│   └── frappe-bench/               # Bench environment configuration and sites
│       ├── apps/                   # Frappe, ERPNext, and HRMS apps
│       └── sites/                  # Local sites configuration
├── docs/                           # Documentation
├── frontend/                       # Frontend source files / customizations
└── tests/                          # Automated tests
```

## Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/) & [Docker Compose](https://docs.docker.com/compose/)
- [VS Code](https://code.visualstudio.com/) with the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Running with Dev Containers

1. Copy `.devcontainer/.env.example` to `.devcontainer/.env` and adjust passwords if needed:
   ```bash
   cp .devcontainer/.env.example .devcontainer/.env
   ```
2. Open the project in VS Code.
3. When prompted, click **Reopen in Container** (or run `Dev Containers: Reopen in Container` from the Command Palette).
4. The dev container starts MariaDB, Redis, and bench environment with ports mapped:
   - Web: `http://localhost:8000`
   - Realtime: `http://localhost:9000`

### Sites & Apps

The bench includes:
- **frappe** (`version-16`)
- **erpnext** (`version-16`)
- **hrms** (`version-16`)
- Site: `hrms.localhost`
