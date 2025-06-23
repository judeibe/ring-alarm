---
mode: "agent"
tools: ['codebase', 'editFiles', 'search']
description: "Convert stateful component logic into a reusable hook."
---

Locate the file `${componentPath}` via **#codebase**. Extract its internal state & side-effects into a new hook `use${ComponentName}Logic.ts` placed in `src/hooks/`.

Perform in-file modifications with **#editInPlace**:
1. Remove state logic from the component.  
2. Import and call the new hook.  
3. Ensure hooks order compliance.

Generate the hook file with full JSDoc and unit tests.
