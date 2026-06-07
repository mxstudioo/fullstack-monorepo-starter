# Full-Stack Monorepo Architecture Starter

Production-ready monorepo starter built with Turborepo, Next.js, Express, TypeScript, and Docker.

Designed to provide a scalable foundation for SaaS applications with multiple frontend apps, shared packages, type-safe development workflows, and containerized environments.

## Table of Contents

1. [Overview](#overview)
2. [Architecture](#architecture)
3. [Included Apps and Packages](#included-apps-and-packages)
4. [Technology Stack](#technology-stack)
5. [Key Features](#key-features)
6. [Development Workflow](#development-workflow)
7. [Getting Started](#getting-started)
8. [Docker Usage](#docker-usage)

---

## Overview

This project demonstrates a scalable full-stack monorepo architecture using Turborepo and PNPM workspaces.

The repository includes multiple applications, shared packages, centralized configuration, and Docker-based development environments. The goal is to reduce duplication, improve maintainability, and enable rapid development across multiple services.

---

## Architecture

The workspace follows a modular architecture:

- Multiple Next.js applications
- Dedicated Express API service
- Shared UI component library
- Shared TypeScript configurations
- Shared ESLint configurations
- Centralized dependency management
- Dockerized local and production environments

All packages are fully typed and integrated through workspace dependencies.

---

## Included Apps and Packages

### Applications

#### `@workspace/web`

Customer-facing Next.js application.

#### `@workspace/admin`

Administrative dashboard built with Next.js.

#### `@workspace/api`

Express-based backend service responsible for business logic and API endpoints.

---

### Shared Packages

#### `@workspace/ui`

Reusable UI component library shared between frontend applications.

#### `@workspace/typescript-config`

Centralized TypeScript configuration.

#### `@workspace/eslint-config`

Shared linting configuration used across all applications.

---

## Technology Stack

### Frontend

- Next.js
- React
- TypeScript

### Backend

- Node.js
- Express

### Infrastructure

- Docker
- Docker Compose

### Workspace Tooling

- Turborepo
- PNPM Workspaces

### Developer Experience

- ESLint
- Prettier
- TypeScript

---

## Key Features

- Monorepo architecture using Turborepo
- Shared UI package across multiple applications
- Shared TypeScript types and configurations
- Shared linting and code quality standards
- Containerized development and deployment workflow
- Automatic package rebuilding during development
- Workspace-based dependency management
- Consistent local and production environments

---

## Development Workflow

### Install Dependencies

```bash
pnpm install
```

I'd position it as an **architecture project**, not an application project.

The strongest thing here is not the features. It's the monorepo architecture, shared packages, Docker workflow, and type-safe full-stack setup.


### Start Development Environment

```bash
docker compose -f compose.dev.yaml up -d
```

### Run Applications

Web Application

```bash
http://localhost:3000
```

API Service

```bash
http://localhost:8000
```

Changes made to shared packages are automatically propagated to dependent applications during development.

---

## Getting Started

### Prerequisites

* Node.js 20+
* PNPM
* Docker
* Docker Compose

### Install

```bash
pnpm install
```

### Start

```bash
docker compose -f compose.dev.yaml up -d
```

---

## Docker Usage

Production Environment

```bash
docker compose up -d
```

Development Environment

```bash
docker compose -f compose.dev.yaml up -d
```

Docker is used to ensure consistent environments across development and deployment workflows.
