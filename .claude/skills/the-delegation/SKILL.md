---
name: the-delegation
description: Use The Delegation (github.com/arturitu/the-delegation), a no-code 3D multi-agent AI playground powered by Gemini, to brainstorm and develop new project ideas, or fork it as a starter codebase. Use when the user wants to explore a new idea with an AI agent team, design a custom agent team, or build an app on The Delegation.
---

# The Delegation – idea lab & starter kit

## Run it
```bash
git clone https://github.com/arturitu/the-delegation.git
cd the-delegation
npm install
npm run dev   # open http://localhost:3000/the-delegation (WebGPU browser: Chrome/Edge)
```
- Needs a Gemini API key (https://aistudio.google.com/app/apikey), entered in the app (BYOK, billed to the user).
- No-install option: https://arturitu.github.io/the-delegation/

## Use 1 – Develop an idea (no code)
1. Open the Team Editor; pick a preset or build a team (max 5 agents: 1 lead + subagents).
2. Turn on human-in-the-loop for the lead so you approve each step.
3. Choose output type: text (docs/pitch), image (logo/mockups), music, or video.
4. Give a brief, e.g. "App that helps X do Y: concept, features, name, landing copy, logo."

Example idea team: Product Lead (orchestrator, Pro model) -> Market Researcher, UX Designer, Tech Architect, Copywriter (Flash).

## Use 2 – Fork as a starter codebase
Stack: TypeScript, React, React Flow, Three.js WebGPU, Zustand, Gemini.
- `src/data/agents.ts` – team templates (`AGENTIC_SETS`, `AgenticSystem`/`AgentNode`, `MAX_AGENTS = 5`). Add a team by appending an entry.
- `src/core/agent`, `src/core/llm` – agent logic and LLM calls (swap here to use another provider, e.g. Claude).
- `src/interface/` – reusable UI: Kanban, review/approval modals, logs, inspector.
- `src/simulation/` – 3D characters, NavMesh pathfinding, state machine.

## License (check before commercial use)
- Code: MIT – free to use, modify, sell; keep the copyright notice.
- 3D models/textures/env maps: CC BY-NC 4.0 – NON-commercial only; replace them for paid products.

## Caveats
Agents are LLM-only: they can't run code or verify calculations. Treat outputs as drafts.
