# CLAUDE.md

## Project overview
- Project name: ScoreFrenzy
- A 2-minute arena game: 1 player vs multiple AI enemies.
- Tech stack: C++ (Rider) + Unreal Engine 5.
- Focus: AI behavior system design and implementation.

---

## Architecture expectation
- AI logic is expected to be implemented using a combination of:
  - C++ (core logic, performance-critical systems)
  - Blueprint (high-level behavior, tuning, visualization)
- Behavior Tree, Blackboard, and AIController are expected core components.

---

## General rules
- Before making any major change:
  - First inspect the current code
  - Explain the problem
  - Propose minimal safe fixes
- DO NOT directly implement new features unless explicitly asked
- DO NOT refactor unrelated parts of the project
- Prefer minimal, incremental, and safe modifications

---

## C++ vs Blueprint rule
- If a feature can be implemented in both C++ and Blueprint:
  1. Explain trade-offs
  2. Suggest a preferred approach
  3. Ask for confirmation before implementation

---

## Unreal-specific rules
When diagnosing or modifying code, always check:

- Module names consistency
- Build.cs / Target.cs correctness
- API export macros (e.g., XXX_API)
- Include paths and generated headers
- UObject / Actor lifecycle correctness
- Compatibility with Unreal reflection system (UCLASS, UFUNCTION, UPROPERTY)

---

## Code style
- DO NOT modify existing comments
- Add comments in Chinese for:
  - Every new function
  - Important logic steps
- Keep naming consistent with existing project
- Prefer clear and explicit naming

---

## Safety constraints
- Do not touch assets (Blueprints, maps, etc.) unless explicitly required
- Do not assume missing files — ask first
- If unsure about Unreal-specific behavior, explain uncertainty before acting

---

## Workflow rules
Always follow this order:

1. Read repository structure
2. Understand current system
3. Identify problems
4. Propose fixes
5. Wait for confirmation (if needed)
6. Implement changes
7. Explain what was changed and why

---

## Task control
- Always read `CLAUDE_TASK.md` before starting work
- Treat `CLAUDE_TASK.md` as the source of truth for current objectives

---

## Interaction style
- Be precise and structured
- Prefer bullet points and step-by-step reasoning
- When debugging:
  - Identify root cause
  - Avoid guessing
