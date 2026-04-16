---
name: setup-stack
description: Initialize a Turborepo monorepo with Expo (mobile), TanStack Start (web), and Hono (backend).
category: initialization
---

# Setup Autonomous Stack

This skill automates the creation of a full-stack monorepo using Bun.

## Steps

### 1. Initialize Turborepo
Initialize the base Turborepo structure with Bun.
```bash
bunx create-turbo@latest . --package-manager bun --skip-install --yes
```

### 2. Add Mobile App (Expo)
Create an Expo mobile application in the `apps/mobile` directory.
```bash
bunx create-expo-app@latest apps/mobile --template blank --no-install
```

### 3. Add Web App (TanStack Start)
Create a TanStack Start web application in the `apps/web` directory.
```bash
bunx @tanstack/cli@latest create apps/web
```

### 4. Add Backend (Hono)
Create a Hono backend service in the `apps/backend` directory using Bun template.
```bash
bun create hono@latest apps/backend --template bun
```

### 5. Install Dependencies
Run a full installation at the root.
```bash
bun install
```
