# Autonomous Stack

![Bun](https://img.shields.io/badge/Bun-%23000000.svg?style=for-the-badge&logo=bun&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-%23EF4444.svg?style=for-the-badge&logo=turborepo&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Expo](https://img.shields.io/badge/expo-1C1E24?style=for-the-badge&logo=expo&logoColor=#D04A37)

A modern monorepo template building towards an autonomous agent-ready stack using **Turborepo**, **Bun**, **Expo**, **TanStack Start**, and **Hono**.

## 🤖 Agent Rules

Before contributing or running any AI agent, please refer to the [AGENTS.md](./AGENTS.md) file which acts as the absolute rulebook for this repository.

## 🚀 Agent Skills

This repository uses [Agent Skills](https://agentskills.io) to automate workspace setup and management. These skills are located in the `.agents/skills/` directory and are designed to be executed by AI agents.

### Available Skills

| Skill | Path | Description |
| :--- | :--- | :--- |
| **setup-stack** | [SKILL.md](./.agents/skills/setup-stack/SKILL.md) | Initializes the monorepo with Expo (Mobile), TanStack Start (Web), and Hono (Backend). |

## 🛠 How to Use the Skills

To use these skills with an AI agent (like Antigravity), you can simply ask it to:

> "Please execute the **setup-stack** skill in `.agents/skills/setup-stack/SKILL.md`"

The agent will then follow the instructions in the markdown file to:
1. Initialize the Turborepo base.
2. Add a mobile app using Expo.
3. Add a web app using TanStack Start.
4. Add a backend service using Hono.
5. Install all dependencies using Bun.

## 📂 Folder Structure

```text
autonomous-stack/
├── apps/
│   ├── backend/    # Hono API
│   ├── mobile/     # Expo App
│   └── web/        # TanStack Start App
├── packages/       # Shared UI, config, etc.
├── .agents/        # AI Skills and configurations
├── AGENTS.md       # AI Rulebook
└── package.json
```

## 💻 Manual Development

Once the stack is initialized, you can start the development servers manually:

```bash
# Install dependencies
bun install

# Start all apps (Web, Mobile, Backend) simultaneously
bun run dev
```

## 📦 Stack Components

- **Monorepo Management**: [Turborepo](https://turbo.build/)
- **Package Manager**: [Bun](https://bun.sh/)
- **Mobile**: [Expo](https://expo.dev/)
- **Web**: [TanStack Start](https://tanstack.com/start)
- **Backend**: [Hono](https://hono.dev/)

---

*Note: This repository is initialized as an empty workspace with the agent skills ready to be triggered.*
