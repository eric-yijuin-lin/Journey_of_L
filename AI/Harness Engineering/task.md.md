#ai
### 目的
task.md 用來說明任務的細項規格，例如：
- 本次任務目標
- 實作的步驟跟要求
- 指令腳本
- 完成任務的認定規則
- 目前不允許做的事情

### task.md 範例
```
# Task 001: Bootstrap the Phaser project

## Goal

Initialize this repository as a minimal Phaser 3 and TypeScript application
using Vite.

The result should demonstrate that the development environment works.
It is not yet a tower-defense game.

## Required implementation

- Initialize Vite directly in the repository root.
- Use the Vite `vanilla-ts` template.
- Install Phaser 3 from npm.
- Remove the default Vite counter, logos, and demo content.
- Create a minimal Phaser game in `src/main.ts`.
- Use a canvas size of 960 by 540 pixels.
- Use a dark background.
- Display the text `TD Harness Lab` near the center of the canvas.
- Keep the implementation small.
- Do not add external image or audio assets.
- Do not add gameplay systems yet.

## Package scripts

Ensure that `package.json` provides these scripts:

- `dev`: start the Vite development server.
- `build`: create a production build.
- `typecheck`: run TypeScript checking without emitting files.
- `check`: run type checking followed by the production build.

## Acceptance criteria

The task is complete only when:

1. The project is created directly in the repository root.
2. Phaser is listed as a version 3 dependency.
3. TypeScript strict mode is enabled.
4. `npm run typecheck` passes.
5. `npm run build` passes.
6. `npm run check` passes.
7. `git diff --check` passes.
8. No tower-defense gameplay has been implemented.

## Out of scope

- Enemies
- Towers
- Projectiles
- Paths
- Waves
- Economy
- Automated tests
- External assets
- UI frameworks
- Git commits
```