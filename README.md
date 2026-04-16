# Autonomous Stack

A modern monorepo template building towards an autonomous agent-ready stack using **Turborepo**, **Bun**, **Expo**, **TanStack Start**, and **Hono**.

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

## 📦 Stack Components

- **Monorepo Management**: [Turborepo](https://turbo.build/)
- **Package Manager**: [Bun](https://bun.sh/)
- **Mobile**: [Expo](https://expo.dev/)
- **Web**: [TanStack Start](https://tanstack.com/start)
- **Backend**: [Hono](https://hono.dev/)

---

*Note: This repository is initialized as an empty workspace with the agent skills ready to be triggered.*
