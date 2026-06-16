# 🤖 Agents Rulebook: Autonomous Stack

This document contains critical instructions and context for any AI Agent working in this repository. **You must read and follow these rules at all times.**

## 1. Project Architecture
This is a full-stack monorepo managed by **Turborepo** and **Bun**. 
The repository consists of:
- `apps/mobile`: React Native mobile application using Expo.
- `apps/web`: Frontend web application using TanStack Start.
- `apps/backend`: Backend API service using Hono.

## 2. Hard Rules (Never Break These)
- **Package Manager**: ALWAYS use `bun` (e.g., `bun install`, `bun run dev`, `bunx`). NEVER use `npm`, `yarn`, or `pnpm`.
- **Monorepo Awareness**: Before running commands, ensure you understand which app you are targeting. Use workspace-specific commands if needed.
- **Language**: Always use TypeScript (`.ts`, `.tsx`) with strict typing. Avoid using `any`.
- **Ask Before Deleting**: Do not delete core configuration files or large chunks of code without explicitly asking the user for permission.

## 3. Directory Context
- Global configs (ESLint, Prettier, Turbo) are at the root directory.
- AI Skills are scoped: specific skills are in `apps/<app_name>/.agents/skills` and global skills are at the root. Prioritize local skills when working inside a specific app.

## 4. Workflows
- When creating a new feature, start from the backend (`apps/backend`) to establish the API/schema, then move to the web/mobile implementation.
- Always check for existing Knowledge Items (KI) or `.agents/skills` before executing a complex setup task.
