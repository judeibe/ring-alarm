---
applyTo: "**/*.ts,**/*.tsx"
---
# Quoin • TypeScript & React Rules

- Use **functional components** (`FC<Props>`)—avoid class components.  
- Always type props & return values explicitly; never use `any`.  
- Derive **React component display names** from file names for better traces.  
- Prefer **React Server Components** in `app/`; mark client components with `"use client"`.  
- Keep hooks at the top; obey the **Rules of Hooks**.  
- Use **Zod** for runtime validation of external data.  
