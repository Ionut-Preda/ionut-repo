# Agent team

For Mona's Project Pulse dashboard, I will use a four-agent custom team defined under the repository's agent folder:

- Planner — Target model: Claude Opus 5.5 (copilot). Responsibility: research the codebase, identify requirements and edge cases, and produce an ordered implementation plan with file ownership and validation expectations. Definition: `.github/agents/planner.agent.md`.
- Orchestrator — Target model: Claude Opus 5.5 (copilot). Responsibility: break the plan into phases, delegate work to specialist agents, coordinate parallel vs. sequential execution, and keep the overall build aligned. Definition: `.github/agents/orchestrator.agent.md`.
- Coder — Target model: GPT-5.5 (copilot). Responsibility: implement the app logic, fix bugs, and add any required runnable app support such as VS Code launch configuration for the dashboard. Definition: `.github/agents/coder.agent.md`.
- Designer — Target model: Gemini 3.7 Flash (copilot). Responsibility: shape the UI/UX, accessibility, information hierarchy, visual design, and responsive dashboard styling for Project Pulse. Definition: `.github/agents/designer.agent.md`.

This setup uses GitHub Copilot CLI in a Codespace to orchestrate the work, with the Orchestrator coordinating the Planner, Coder, and Designer across the project phases.
