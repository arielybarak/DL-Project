# AGENTS.md — Copilot Coding Agent (CCA) Guide

This file is read by GitHub Copilot's Coding Agent (CCA) when it is assigned a GitHub Issue. It explains the repository layout, the available agent pipeline, and the conventions Copilot must follow when working here.

---

## Repository Purpose

This is a personal research and coding environment for **Python (PyTorch/ML)** projects. It is built around GitHub Copilot Agent Mode and is meant to be reused as a launchpad for future projects.

Key technologies used in projects spawned from this environment:
- **Python** (Google Python Style Guide, PEP 8, PyTorch)

---

## Directory Layout

```
.github/
  agents/           ← Custom Copilot agent definitions (one .agent.md per persona)
    coding/         ← Agents that write, fix, test, and clean code
    mentoring/      ← Agents that guide learning (never write code directly)
    planning/       ← Agents that produce plans, not code
    research/       ← Agents that research before coding
  instructions/     ← Auto-applied coding standards for specific file types
  prompts/          ← Prompt files for common workflows
  copilot-instructions.md  ← Global instructions applied to every Copilot session
.github/skills/             ← Reusable instruction snippets (load on demand)
src/                ← Practice / example source code
```

---

## Global Coding Rules (always apply)

1. **Industry standards** — write code the way a professional engineer at a real company would write it. Follow established conventions and explain the *why* behind them.
2. **Simplicity over cleverness** — prefer clear, readable code over clever one-liners.
3. **Python style** → [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)
4. **Consult `.github/skills/`** for domain-specific directives (e.g., `pytorch-best-practices.md`, `python-style-guidelines.md`).

---

## Agent Pipeline (recommended order for new features)

```
1. task-researcher  ──►  2. plan  ──►  3. tdd-red  ──►  4. implementer
                                                              │
                                                    (if bugs) ▼
                                                         5. debug
                                                              │
                                                  (when stable) ▼
                                                         6. janitor
```

For quick fixes or exploratory work: use **Software Engineer Agent** directly.

---

## Instruction Files (auto-applied by file type)

| File pattern | Instruction file | What it enforces |
|---|---|---|
| `**/*.py` | `python.instructions.md` | PEP 8, type hints, docstrings |
| `**/*.py` | `pytorch.instructions.md` | PyTorch training conventions, DataLoader, device placement, reproducibility |
| `**` | `code-review.instructions.md` | Code review priority levels and checklist |

---

## Skills Available

Load these when the task calls for it:

| Skill file                           | When to load                          |
|--------------------------------------|--- -----------------------------------|
| `.github/skills/add-educational-comments.md` | Any code generation that should teach |
| `.github/skills/python-style-guidelines.md`  | Python code generation or review      |
| `.github/skills/pytorch-best-practices.md`   | PyTorch / deep learning code          |

---

## CCA Workflow Notes

- **Always read `CONTEXT.md`** before starting — it lists the learning topics and intent of this repository.
- **Always read `.github/skills/` files** relevant to the language you are working in before generating code.
- **Do not create test frameworks** that don't already exist in the project.
- **Do not introduce new dependencies** without explaining the trade-off.
- **Prefer `pytest`** for Python test files.
- When the task involves ML code, follow the patterns in `.github/skills/pytorch-best-practices.md`.
