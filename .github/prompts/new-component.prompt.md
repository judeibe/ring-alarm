---
mode: "edit"
description: "Scaffold a fully-typed React component with stories and tests."
---

Generate a new **Next.js/TypeScript** component named **`${componentName}`** inside `src/components/${componentName}.tsx`.

Requirements:
1. Functional component (`FC<Props>`) with explicit prop types.
2. Include a matching `*.stories.tsx` **Storybook** file.
3. Create `*.test.tsx` unit tests using **Vitest**.
4. Use **shadcn/ui** + **Tailwind** classes for styling.
5. Export default the component.

Follow Quoin coding standards from **general-coding.instructions.md**.  
