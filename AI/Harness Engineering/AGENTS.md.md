#AI 

(※ Claude 會有不同名字) 
### 目的
用來限定長期的通用規則，例如：
- 專案目標
- 技術限制（程式語言、框架等）
- 工作流程
- 驗收流程
- 工作報告

### AGENTS.md 範例
```
# TD Harness Lab

## Purpose

This repository is a learning lab for Harness Engineering.
The application being built is a small tower-defense game.

The main learning goal is reliable AI-agent orchestration.
Phaser and TypeScript are supporting technologies.

## Technology constraints

- Use Phaser 3.
- Use TypeScript with strict type checking.
- Use Vite as the development and build tool.
- Use npm as the package manager.
- Do not add React, Vue, a backend, or a database.
- Prefer simple Phaser graphics and text over external assets.
- Avoid CSS-heavy interfaces unless a task explicitly requires them.

## Working procedure

Before making changes:

1. Read this file.
2. Read `docs/current-task.md`.
3. Inspect the repository and run `git status --short`.
4. State a concise implementation plan.

While working:

- Work only on the current task.
- Keep changes small and reversible.
- Do not implement anticipated future features.
- Do not modify unrelated files.
- Do not add dependencies unless the current task requires them.
- Do not change this file or `docs/current-task.md` unless explicitly asked.
- Do not create Git commits unless explicitly asked.
- Avoid `any` unless its use is clearly justified.

## Verification

- Run all verification commands required by `docs/current-task.md`.
- Do not report success if a required check fails.
- If a check cannot be run, explain why.
- Run `git diff --check` before finishing.

## Final report

At the end of a task, report:

1. What changed.
2. Which files changed.
3. Which commands were run and whether they passed.
4. Any remaining risks, assumptions, or unverified behavior.
```