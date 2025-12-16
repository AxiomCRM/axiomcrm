# AxiomCRM

## Vision

This project aims to build a **modular, backend-first CRM platform** designed for real operational businesses, not a single industry or use case.

Instead of hard-coding workflows for construction, sales, services, or any other sector, the system is built around a **pluggable module architecture**. Each client enables only the modules they need, defines their own data models, and runs workflows that match how their business actually operates.

The result is not just a CRM, but a **configurable business operating system**.

---

## Core Principles

### Sector-Agnostic by Design

No industry logic lives in the core.
All domain behavior is introduced through modules that can be enabled, disabled, or replaced without affecting other tenants.

### Backend-First Architecture

The backend is treated as the product.
APIs, data models, permissions, and workflows are designed first, with the frontend acting as a consumer, not a driver.

### Modular Everything

Modules define:

* Their own data models
* API routes
* Permissions
* Automations
* Configuration schemas

The core platform only provides shared infrastructure such as tenancy, auth, permissions, and orchestration.

### Cloudflare-Native

The platform is built entirely on **Cloudflare’s developer stack**:

* Workers for API and business logic
* D1 for relational data
* KV for configuration and fast lookups
* R2 for files and documents
* Queues and Cron for background work

This keeps the system globally distributed, low-ops, and cost-efficient.

### Multi-Tenant from Day One

Every request, record, and workflow is tenant-scoped by default.
There is no single-tenant shortcut or retrofit later.

---

## What This Is Not

* Not a construction CRM
* Not a sales CRM
* Not a generic CRUD app
* Not a frontend-driven experiment

This is a **production-grade backend foundation** intended to support many business models over time.

---

## Long-Term Goal

To create a stable, extensible backend core that can:

* Serve multiple clients safely
* Evolve without breaking existing tenants
* Support custom workflows without forks
* Scale from small teams to complex organizations

Frontends, integrations, and industry-specific behavior can evolve independently, without changing the core.

