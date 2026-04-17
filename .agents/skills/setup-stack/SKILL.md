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
Create an Expo mobile application in the `apps/mobile` directory and add React-specific skills.
```bash
bunx create-expo-app@latest apps/mobile --template blank --no-install
bunx skills add PatternsDev/skills/react --path apps/mobile
```

### 3. Add Web App (TanStack Start)
Create a TanStack Start web application in the `apps/web` directory and add React-specific skills.
```bash
bunx @tanstack/cli@latest create apps/web
bunx skills add PatternsDev/skills/react --path apps/web
```

### 4. Add Backend (Hono)
Create a Hono backend service in the `apps/backend` directory using Bun template and add JavaScript-specific skills.
```bash
bun create hono@latest apps/backend --template bun
bunx skills add PatternsDev/skills/javascript --path apps/backend
```

### 5. Add General Project Skills
Install a collection of powerful agent skills for project management, debugging, and optimization.
```bash
bunx skills add addyosmani/agent-skills
```

### 6. Install Dependencies
Run a full installation at the root.
```bash
bun install
```
