---
mode: "agent"
tools: ['codebase', 'editFiles', 'terminalLastCommand', 'sequential-thinking']
description: "Scaffold a Feature-Slice (FSD) directory with typed code, stories, and tests."
---

Create a new **Feature-Slice** named **`${sliceName}`** under `src/features/${sliceName}`.

### 1 • Directory & files  
Use **#terminalLastCommand** to run:

```bash
mkdir -p src/features/${sliceName}/{ui,model,lib,api,__tests__}
touch src/features/${sliceName}/ui/${sliceName}View.tsx
touch src/features/${sliceName}/model/${sliceName}Store.ts
touch src/features/${sliceName}/lib/index.ts
touch src/features/${sliceName}/api/${sliceName}Api.ts
touch src/features/${sliceName}/index.ts
```

### 2 • UI component

Inside `${sliceName}View.tsx`:

* Functional React component (`FC<Props>`) with explicit props.
* Use **shadcn/ui** primitives and Tailwind utility classes.
* Export default component and a named `Skeleton`.

Generate a matching Storybook file `*.stories.tsx` beside it.

### 3 • State / model

`${sliceName}Store.ts` should expose a typed **Zustand** store or **Redux Toolkit** slice (if store already exists, integrate).
Add unioned selectors and action creators.

### 4 • Service layer

`${sliceName}Api.ts` exports typed async functions that hit existing service facades in `src/server/**`—no direct fetch calls.

### 5 • Barrel & public API

`index.ts` re-exports UI, model, api, and helpers so consumers import only from `features/${sliceName}`.

### 6 • Tests

Create Vitest unit tests in `__tests__/${sliceName}.test.tsx` covering:

* UI render snapshot.
* Store initial state & reducer logic.
* API happy/error paths (mock with msw).

### 7 • Code standards

Ensure generated code complies with all Quoin [general coding guidelines](../instructions/general-coding.instructions.md) rules.
After scaffolding, run **#codebase** lint and **#terminalLastCommand** `npm run test` to verify green.
